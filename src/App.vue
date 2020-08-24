<template>
<div id="app">
<h2>{{title}}</h2>
<MenuBar></MenuBar>
<Pricecheck></Pricecheck>





</div>
</template>
<script>

import MenuBar from './components/menu.vue'

import Pricecheck from './components/PriceCheck.vue'




export default {   
  name: 'App',
  data(){

    return{

      title:'This is a Vue Project',
       
    }
  },
  components:{
  MenuBar,Pricecheck

  },

 
}

 
  
</script>

<style>
h2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:rgb(99, 95, 160);
  margin-top: 60px;

}
</style>
