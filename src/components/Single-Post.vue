<template>
  <h2>Subchild components</h2>
  <h3 v-for="items in post" :key="items.id">
  {{items.author}}</h3>
</template>

<script>
export default {
  props:["post"]
}
</script>

<style>

</style>