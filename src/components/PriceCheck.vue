<template>
<div id="priceCheck">
    <h2>{{title}}</h2>
<select v-model="selected">
    <option v-for="product in products" :key="product.id" :value="{price:product.price,name:product.name}"  >{{product.name}}</option>
    
</select>
price: <input type="text" :value="selected.price">
Quantity:<input type="number" min="0" v-model="quantity"  @click="Cal">
Total:<input type="text" :value="total">
Paid:<input type="text" v-model="paid" @keyup="DueCal">

<p>{{status}}</p>

</div>
    
</template>

<script>
export default {
    name:'priceCheck',
    data(){

        return{

            title:'Product Price Check',
              selected: '',
              total:0,
              quantity:0,
              paid:0,
              due:0,
              status:'',


            products:[
                {id:1,name:'Mango',price:100},
                {id:2,name:'Apple',price:200},
                {id:3,name:'Banna',price:400},
                {id:4,name:'Orange',price:500}
            ],
          
        }
    },
    methods:{

        Cal(){

            this.total = this.quantity * this.selected.price
        },

        DueCal(){
             this.due = this.total - this.paid
          if(this.due == 0)

          this.status = 'Paid'
          

          else 
         
          this.status = `Due:${this.due}`
         


        }
    }

  

  
    
}
</script>

<style scoped>
h2{

    text-align: center;
    color: blueviolet;
}

</style>