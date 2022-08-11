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
    const bookdetails=ref([])
    const error =ref(null)
    const load=async() =>{
      try{
        let data=await fetch('http://localhost:3000/posts')
        console.log(data)
        if(!data.ok){
          throw Error('no data available')
        }
        bookdetails.value = await data.json()
        console.log(data.json())
      }
      catch(err){
          error.value=err.message
          console.log(error.message)
      }
     
    }
   return {bookdetails,load}
 }
}
</script>

<style>

</style>