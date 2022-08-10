<template>
  <h2>Props in compositin api</h2>
  <h2>{{bookdetails}}</h2>
  <child  :bookdetails="bookdetails"/>
</template>

<script>
import { ref } from '@vue/reactivity'
import child from './Post-List.vue'
export default {
    components:{
        child
    },
 setup(){
    const bookdetails=ref([{id:1,name:'thie main concept of vue3',author:'the good boy smart bot akash'},
   {id:2,name:'all about typescript and nuxt3 for creating a good looking webste', author:'the main in boy shival gupta'} ])

   return {bookdetails}
 }
}
</script>

<style>

</style>