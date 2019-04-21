<template>
    <div class='ui centered card'>
        <div class='content'>
            <div class='header'>
                {{ task.title }}
            </div>
            <div class='meta'>
                {{ task.project }}
            </div>
            <div class='extra-content'>
                <span class='right floated edit icon'>
                    <i class='edit-icon'></i>
                </span>
            </div>
        </div>
        <div class='ui bottom attached green basic button' v-show="task.done">
            Completed
        </div>
        <div class='ui bottom attached red basic button' v-show="!task.done">
            Complete
        </div>
    </div>
</template>

<script>
export default {
    props: ['task']
}
</script>

<style scoped>

</style>


