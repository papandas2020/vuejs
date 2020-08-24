<template>
    <div class="Hook">
        <h1>{{title}}</h1>
        <button @click="titleChnage">Click Me</button>
    </div>
</template>

<script>
export default {
    name:'Hook',
    data(){
        return {

            title:'HOOK ZONE'
        }
    },
    methods:{

        titleChnage(){

            this.title = 'HOOK ZONE UPDATE'
        }
    },
    beforeCreate(){

        alert('load before')
    },
    created(){
alert('load after')

    },

    beforeUpdate(){

        alert('Update Before')
    },
    updated(){
 alert('Update After')

    }

    
}
</script>


<style scoped>

h1{

    text-align: center;
}

</style>