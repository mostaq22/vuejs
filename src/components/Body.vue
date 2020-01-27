<template>
    
        <!-- Page Content -->
        <div id="page-content-wrapper">            
            <TopNav  v-bind:top_menus="top_menu_list" />        

            <div class="container-fluid">
                <Todos v-bind:todo_items="todo_list"/>
            </div>
        </div>
    <!-- /#page-content-wrapper -->
</template>

<script>
import Todos from './Todos'
import TopNav from './TopNav'

export default {
    name: 'Body',
    // props: ['top_menus'],
    components: {
        Todos, TopNav
    },
    data(){
        return {
            todo_list: 
            [
                {
                    id: 1,
                    title: "Install VueJs Framework",
                    completed: 'completed'
                },
                {
                    id: 2,
                    title: "Follow a tuts",
                    completed: 'completed'
                },
                {
                    id: 3,
                    title: "Understand eco-system of VueJs",
                    completed: 'pending'
                },
            ],            
            top_menu_list: [
                {
                id: 1,
                name: 'Home',
                child: false
                },
                
                {
                id: 2,
                name: 'Link',
                child: false
                },
                {
                id: 3,
                name: 'Dropdown',
                child: [
                    {
                    id: 1,
                    name: 'Edit'
                    },
                    {
                    id: 2,
                    name: 'Delete'
                    },

                ]
                },

            ]
        }
    }

}
</script>