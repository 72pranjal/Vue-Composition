<template>
  <h2>computed propertiy in composition API</h2>
  <input type="text" v-model="search">
  <h3>search terms {{search}}</h3>
  <h2 v-for="items in updatename" :key="items">{{items}}</h2>
  <button @click="handleclick">stop watching</button>
</template>

<script>
import { ref } from '@vue/reactivity'
import { computed, watch, watchEffect } from '@vue/runtime-core'
export default {
    setup(){
      const search=ref('')
      const stopwatch=watch(search,()=>{
        console.log('watch functio is run')
      })
      const stopeffect=watchEffect(()=>{
        console.log('watchEffect is run' ,search.value)
      })
        const names=ref(['Pranajl','Shubham',"shivam",'Satyam','Javed','Mohit','Ritik','Shidatt'])
        const updatename=computed(()=>{
          return names.value.filter((name)=>name.includes(search.value))
        })
        const handleclick=()=>{
          stopwatch()
          stopeffect()
        }
        return {names,search,updatename,handleclick}
    }
}
</script>

<style>

</style>