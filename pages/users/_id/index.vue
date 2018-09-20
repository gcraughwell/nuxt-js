<template>
<h1> 1 user with id {{ $route.params.id }} </h1>
</template>
<script>
export default {
validate(data) {
  console.log(data);
  return /^\d+$/.test(data.params.id)
},
layout: 'users'
}

</script>
