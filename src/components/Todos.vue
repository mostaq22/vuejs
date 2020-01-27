<template>
    <div>
        <h1>Todo List</h1>
        <ul class="list-group">
            <li v-bind:key="todo.id" v-for="todo in todo_items" class="list-group-item" v-bind:class="todo.completed=='completed' ? 'list-group-item-success' : 'list-group-item-warning'">
                {{ todo.title  }}
            </li>
        </ul>
    </div>    
</template>

<script>
export default {
    name: "Todos",
    props: ["todo_items",]
}
</script>

<style scoped>

</style>