<template>
    <ul class="list-group">
        <li class="list-group-item" v-bind:key="comment.id" v-for="comment in post_comments">
            <h3>{{ comment.name }}</h3>
            <p>{{comment.body}}</p>
        </li>
    </ul> 
</template>


<script>
export default {
    name: 'Comments',
    props: ['post'],
    data() {
         return {
            post_comments: null,
            example: null,           
         }
    },
    methods: {
        load_comments: function() {
            
                fetch('https://jsonplaceholder.typicode.com/comments?postId='+this.post.id)
                .then(response => response.json())
                .then(posts => {
                    this.post_comments = posts
                })
        }
    },
    created: function(){
        this.load_comments();
        
    }
}
</script>