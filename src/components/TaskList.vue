<template>
  <div>
    <p>Completed Tasks: {{tasks.filter(task => {return task.done === true}).length}}</p>
    <p>Pending Tasks: {{tasks.filter(task => {return task.done === false}).length}}</p>
    <task v-on:delete-task="deleteTask" v-for="task in tasks" :key="task.id" v-bind:task="task"></task>
  </div>
</template>

<script>
import Task from './Task';

export default {
    props: {
        tasks: Array
    },
    components: {
        Task
    },
    methods: {
      deleteTask(task) {
        const taskIndex = this.tasks.indexOf(task);
        this.tasks.splice(taskIndex, 1);
      }
    }
};
</script>

<style scoped>
</style>