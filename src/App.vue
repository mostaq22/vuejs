<template>
  <div id="app" class="d-flex">
   <Sidebar v-bind:menus="menu_list"/>
   <Body/>  

  </div>
</template>
<script>

import Sidebar from './components/Sidebar';
import Body from './components/Body';

export default {
  name: 'app',
  components: 
    {
      Body,
      Sidebar
    }
    
    
  ,
  data(){
    return {
      menu_list: [
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
  }
  
}
</script>

<style>

</style>
