<template>
  <div class="product">
  
  <Strong>{{ product.title }}</Strong>
   <img id= "still"  src="../assets/mac.png">
  <p>{{ product.description }}</p>
  <Strong>Price:{{ product.price }} | Count:{{ product.count }}  </Strong>
   <br><br>
  <button @click="addToCart(product)">Add to Cart</button>
  </div>
</template>


<script>

export default {
  props: ["product"],
  methods: {
    addToCart() {
      this.$emit("addToCart", this.product)
    }
  }
}
</script>


<style>
.product {
  border: 2px dashed #666 ;
  padding: 5px 20px;
  width: 40%;
}

.product:hover {
  border: 2px solid #666 ;
  transition: all 1s;
  
}
</style>

