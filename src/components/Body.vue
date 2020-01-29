<template>    
        <!-- Page Content -->
        <div id="page-content-wrapper">            
            <TopNav/>
            <div class="container-fluid">
                <Todos/>
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
            
        }
    }

}
</script>