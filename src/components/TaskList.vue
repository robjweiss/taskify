<template>
  <div>
    <p>Completed Tasks: {{tasks.filter(task => {return task.done === true}).length}}</p>
    <p>Pending Tasks: {{tasks.filter(task => {return task.done === false}).length}}</p>
    <task v-for="task in tasks" :key="task.id" v-bind:task="task"></task>
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
    }
};
</script>

<style scoped>
</style>