<template>
    <header>
        <h1>{{title}}</h1>
        <Button @click="$emit('show-task-form')" :text="toggleAddButton ? 'Close' : 'Add Task'" :color="toggleAddButton ? 'red' : 'green'"/>
    </header>
</template>

<script>
import Button from './Button'
export default {
     name: 'Header',
     props: {
        title: String,
        toggleAddButton: Boolean,

     },
     components: {
        Button
     }
}
</script>


<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>
