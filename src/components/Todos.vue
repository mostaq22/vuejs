<template>
    <div>
        <h1>Todo List</h1>
        <hr>
        <ul class="list-group">
            <li v-bind:key="post.id" v-for="post in posts" class="list-group-item">
                <h3>{{ post.title  }}</h3>
                <hr>
                <button class="btn btn-primary btn-sm">Comments</button>
                <br/>                
                <!-- Comments Component-->
                <Comments v-bind:post="post" v-bind:style="{'margin-left':`100px`}"/>
            </li>           
        </ul>
    </div>    
</template>

<script>
import Comments from './Comments'
export default {
    name: "Todos",
    components: {
        Comments
    },
    props: [],
    data(){
         return {
            posts: null,
            posts_condition: {

            }
        }
    },
    created: function(){
       setTimeout(()=> {
            this.load_todo();
       },1000)
       
    },
    methods: {
        load_todo: function()
        {
            fetch('https://jsonplaceholder.typicode.com/posts/')
            .then(response => response.json())
            .then(data => {
                this.posts = data;
                data.map(function(d){
                    // console.log(d)
                    this.posts_condition['s_'+d.id] = d.id;
                });
            })
        },
    }
     
}
</script>

<style scoped>

</style>