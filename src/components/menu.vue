<template>
    <div id="Navbar">
      <nav>
          <ul>
  <li><a class="active" href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>
      </nav>
    </div>
</template>

<script>
export default {
    name:'Navbar',
    data(){

        return{

        }
    }
    
}
</script>

<style scoped>

nav ul{

    list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

nav li{

     float: left;
}

nav li a{

    display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

nav li a:hover:not(.active){

    background-color: #111;
}

.active {
  background-color: #4CAF50;
}

</style>