<template>
<div>
  <h3>
    <nuxt-link to="/">Products</nuxt-link>
  <!-- <input type="text" v-model="userId">
  <button @click="onLoadUser">Load User</button> -->

<nuxt-link to="/products/1/" >Product 1</nuxt-link>
<nuxt-link to="/products/2/" >Product 2</nuxt-link>

</h3>
</div>
</template>
<script>
export default {
data() {
  return {
    userId: ''
  }
},
methods: {
  onLoadUser(){
this.$router.push("/products/" + this.userId)
},
}
}
</script>
