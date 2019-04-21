<template>
  <div id="app">
    <task-list v-bind:tasks="tasks"></task-list>
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'

export default {
  name: 'app',
  components: {
    TaskList
  },

  data() {
    return {
      tasks: [
        {
          id: 1,
          title: 'Todo A',
          project: 'Project A',
          done: false
        },
        {
          id: 2,
          title: 'Todo B',
          project: 'Project B',
          done: true
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
