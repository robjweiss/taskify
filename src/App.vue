<template>
  <div id="app">
    <task-list v-bind:tasks="tasks"></task-list>
    <create-task v-on:add-task="addTask"></create-task>
  </div>
</template>

<script>
const uuidv4 = require('uuid/v4');

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
          id: uuidv4(),
          title: 'Todo A',
          project: 'Project A',
          done: false
        },
        {
          id: uuidv4(),
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
