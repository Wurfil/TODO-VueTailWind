<template>
  <div>
    <header class="py-20">

      <button
          class="bg-fuchsia-700 hover:bg-fuchsia-900 transition-all text-cyan-50 rounded-lg align-middle text-3xl w-14 h-14 mr-10"
          @click="addTask"
      >+
      </button>
      <input type="text" placeholder="Введите вашу задачу" v-model="newTodo"
             class="text-cyan-50 bg-black pl-5 w-80 h-14 rounded-lg">
    </header>
    <main class="text-cyan-50 text-2xl">
      <div v-if="!todos.length">Список задач пуст</div>
      <template v-else>
        <ul v-for="(todo,index) in todos" :key="todo" class="justify-center flex justify-center">
            <li class="mb-6 pl-5 hover:bg-fuchsia-700 transition-all rounded-lg hover:shadow-lg hover:shadow-amber-50 place-items-center flex justify-between w-auto h-14">
              {{ todo }}
              <button class="ml-5 hover:bg-red-500 w-14 h-14 rounded transition-all" @click="deleteTask(index)">
                ×
              </button>
            </li>
        </ul>
      </template>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [],
      newTodo: ""
    }
  },
  methods: {
    addTask() {
      if (this.newTodo) {
        this.todos.unshift(this.newTodo)
        this.newTodo = ''
      }
    },
    deleteTask(index) {
      this.todos.splice(index, 1)
    }
  }
}
</script>

