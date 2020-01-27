<template>    
        <!-- Sidebar -->
        <div class="bg-light border-right" id="sidebar-wrapper">
            <div class="sidebar-heading">Start Bootstrap </div>
            <div class="list-group list-group-flush">
                <a href="#" class="list-group-item list-group-item-action bg-light" v-bind:key="menu.id" v-for="menu in menus">{{ menu.name }}</a>
            </div>
        </div>
    <!-- /#sidebar-wrapper -->
   
</template>


<script>
export default {
    name: "Sidebar",
    props: [
        'menus'
    ]
}
</script>