<template>
  <div id="app">
    <task-list v-bind:tasks="tasks"></task-list>
    <create-task v-on:add-task="addTask"></create-task>
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'
import CreateTask from './components/CreateTask.vue'

export default {
  name: 'app',
  components: {
    TaskList,
    CreateTask
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
  },
  methods: {
    addTask(task) {
      this.tasks.push(task);
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
