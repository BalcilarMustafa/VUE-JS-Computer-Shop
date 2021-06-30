<template>
  <div class="home">
   
    <HelloWorld msg="Welcome to Computer Shop"/>
     <img id= "still"  src="../assets/logo.png">
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>

#still {
width: 450px;
height: 350px;
}
</style>