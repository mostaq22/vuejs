<template>
  <div id="app" class="d-flex">
   <Sidebar/>
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
      
    }
  },
  
}
</script>

<style>

</style>
