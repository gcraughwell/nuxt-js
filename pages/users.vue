<!--
users.vue is a templating for all user pages, everything on this
page will show on all other user pages <nuxt-child/> shows were the child should go.  -->

<template>
  <div>
  <input class="input" type="text" v-model="userId">
<button class="button" @click="onLoadUser">Load User</button>
<nuxt-child />
</div>
</template>
<script>
import Logo from '~/components/Logo.vue'

export default {
data() {
  return {
    userId: ''
  }
},
methods: {
  onLoadUser(){
this.$router.push("/users/" + this.userId);
  }
},
//add layout for updated layout style it will replace the exsisting
layout: 'users'

}
</script>

<style>
.button {
background-color: pink;
border: none;
color: white;
},
.input {
     border: none;
     padding: 5px;
     margin: 4px 2px;
}
</style>
