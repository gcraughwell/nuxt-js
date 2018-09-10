<!-- 
users.vue is a templating for all user pages, everything on this
page will show on all other user pages <nuxt-child/> shows were the child should go.  -->

<template>
  <div>
  <input type="text" v-model="userId">
<button @click="onLoadUser">Load User</button>
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
}
}
</script>
