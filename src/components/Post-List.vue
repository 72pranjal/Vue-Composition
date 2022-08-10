<template>
  <h2>Child components</h2>
   <h3 v-for="items in bookdetails" :key="items.id">
  
   {{items.name}}
  </h3>
  <subchild  :post="bookdetails"/>
</template>

<script>
import subchild from './Single-Post.vue'
export default {
    components:{
        subchild
    },
   props:["bookdetails"],
   setup(props){
    console.log(props.bookdetails)

   }
}
</script>

<style>

</style>