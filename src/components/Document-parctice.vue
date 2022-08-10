<template>
  <h2>Document Practice</h2>
  <h2>Checked names:{{message}}</h2>
 <label for="aa">Jack</label>
 <input type="checkbox" id="aa" value="jack" v-model="message">
 <label for="bb">Bob</label>
 <input type="checkbox" id="bb" value="bob" v-model="message">
 
 <label for="cc">Tom</label>
 <input type="checkbox" id="cc" value="tom" v-model="message">
 
 <label for="dd">Steve</label>
 <input type="checkbox" id="dd" value="steve" v-model="message">
 
</template>

<script>
import { ref } from '@vue/reactivity'

export default {
 setup(){
    const message=ref([])
    return {
       message
    }
 }
}
</script>

<style scoped>

</style>