<template>    
        <!-- Sidebar -->
        <div class="bg-light border-right" id="sidebar-wrapper">
            <div class="sidebar-heading">Start Bootstrap </div>
            <div class="list-group list-group-flush">
                <a href="#" class="list-group-item list-group-item-action bg-light" v-bind:key="menu.id" v-for="menu in menu_list" @click="load_page(menu.name)">{{ menu.name }} </a>
            </div>
        </div>
    <!-- /#sidebar-wrapper -->
   
</template>


<script>
export default {
    name: "Sidebar",
    props: [
        
    ],
    data(){
        return {
            menu_list: 
            [
                {
                    id: 1,
                    name: 'Dashboard',
                    path: '#'
                },
                {
                    id: 3,
                    name: 'Shortcuts',
                    path: '#'
                },
                {
                    id: 4,
                    name: 'Overview',
                    path: '#'
                },
                {
                    id: 5,
                    name: 'Events',
                    path: '#'
                }

        ],
        }
    },
    methods: {
       
    }
}
</script>