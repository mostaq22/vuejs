<template>
    <div>
        <h1>Todo List</h1>
        <hr>
        <ul class="list-group">
            <li v-bind:key="todo.id" v-for="todo in todo_list" class="list-group-item" v-bind:class="todo.completed ? 'list-group-item-success' : 'list-group-item-warning'">
                {{ todo.title  }}
            </li>
        </ul>
    </div>    
</template>

<script>
export default {
    name: "Todos",
    props: [],
    data(){
         return {
             todo_list: null,
         }
    },
    created: function(){
       setTimeout(()=> {
           console.log('Fired...')
           this.load_todo();
       },5000)
       
    },
    methods: {
        load_todo: function()
        {
            fetch('https://jsonplaceholder.typicode.com/todos/')
            .then(response => response.json())
            .then(todo_data => {
                // console.log(json)
                this.todo_list = todo_data
            })

            
            // this.todo_list = [
            //     {
            //         id: 1,
            //         title: "Install VueJs Framework",
            //         completed: 'completed'
            //     },
            //     {
            //         id: 2,
            //         title: "Follow a tuts",
            //         completed: 'completed'
            //     },
            //     {
            //         id: 3,
            //         title: "Understand eco-system of VueJs",
            //         completed: 'pending'
            //     },
            // ]
        },
    }
     
}
</script>

<style scoped>

</style>