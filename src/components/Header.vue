<template>
    <header>
        <h1>{{title}}</h1>
        <Button v-show="homePage" @click="$emit('show-task-form')" :text="toggleAddButton ? 'Close' : 'Add Task'" :color="toggleAddButton ? 'red' : 'green'"/>
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
     },
     computed: {
        homePage() {
            if(this.$route.path == '/'){
                return true 
            } else return false
        }
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
