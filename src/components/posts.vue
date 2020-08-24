<template>
<div class="PostZone">
    <h1>{{title}}</h1>
    <input type="text" v-model="searchTerm" placeholder="search">
    <div v-for="post in filterSearch" :key="post.id">

        <h3>{{post.title}}</h3><hr>
        <p>{{post.body | snippet}}</p>


    </div>

    
    </div>    
</template>

<script>
import axios from 'axios'
export default {
    name:'PostZone',
    data(){

        return{

            title:'This is Post Zone',
            posts:[],
            searchTerm:''
        }
    },

    computed:{
     filterSearch(){

        return  this.posts.filter(post=>{

             return post.title.match(this.searchTerm)
         })
     }

    },

    created(){

        axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response=>{
     this.posts = response.data
     
        })
        .catch(error=>{

            console.log(error)
        })
    }

    
}
</script>

<style scoped>
h1{

    color: blueviolet;
    text-align: center;
}

</style>