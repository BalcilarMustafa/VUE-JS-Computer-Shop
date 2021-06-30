<template>
 <div class="container">
   <div class="cart">
      <h3>CART</h3>
    <ul>
      <li v-for="item in cartItems" :key="item.id">{{ item.title}}</li>  
   </ul>
    <p v-if="cartItems.length==0"> Your Cart is Empty. You can start shopping...</p>
   </div>
<Product @addToCart="cartItems.push($event)" :product="product" v-for="product in productList" :key="product.id" />
 </div>
</template>

<script>
import Product from "@/components/Product.vue"
export default {
  components: {
   Product
  },
  data: () => ({
  productList: [
       {
         id: 1,
         img: "../assets/logo.png",
         title:'MacBook Pro', 
         price: 100, 
         count: 0,
         description: "DESC1"
         },
         {
         id: 2,
         img: "../assets/logo.png",
         title:'Iphone', 
         price: 500, 
         count: 100,
         description: "DESC2"
         },
         {
         id: 3,
         img: "../assets/logo.png",
         title:'Keyboard', 
         price: 10, 
         count: 1000,
         description: "DESC3"
         },
          {
         id: 4,
         img: "../assets/logo.png",
         title:'Mouse', 
         price: 20, 
         count: 500,
         description: "DESC4"
         },
          {
         id: 5,
         img: "../assets/logo.png",
         title:'Speaker', 
         price: 30, 
         count: 600,
         description: "DESC5"
         },
          {
         id: 6,
         img: "../assets/logo.png",
         title:'Screen', 
         price: 300, 
         count: 100,
         description: "DESC6"
         }
    ],
    cartItems: []
  })
}

</script>

<style scoped>
.container{
display: flex;
justify-content: center;
align-items: center;
flex-direction: column;
}

.cart{
  margin-bottom: 50px;
}
</style>