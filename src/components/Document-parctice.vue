<template>
  <h2>Document Practice</h2>
  <h2>Checked names:{{message}}</h2>
 <label for="aa">Jack</label>
 <input type="checkbox" id="aa" value="jack" v-model.lazy="message">
 <label for="bb">Bob</label>
 <input type="checkbox" id="bb" value="bob" v-model.lazy="message">
 
 <label for="cc">Tom</label>
 <input type="checkbox" id="cc" value="tom" v-model.lazy="message">
 
 <label for="dd">Steve</label>
 <input type="checkbox" id="dd" value="steve" v-model.lazy="message">
 <h2>Please choose:..{{data}}</h2>
 <label for="one">One</label>
 <input type="radio" id="one" name="btn" value="One" v-model.trim="data">
 <label for="two">Two</label>
 <input type="radio" id="two" name="btn" value="Two" v-model.trim="data">
 <h2>Dropdown</h2>
 <h2>Selected value:{{dropvalue}}</h2>
 <select v-model.lazy="dropvalue" >
   <option disabled value="">Choose course</option>
   <option >Javascript</option>
   <option >React</option>

   <option >Python</option>
   <option >Vue3</option>
   <option >c++</option>
   <option >Java</option>

 </select>
 
</template>

<script>
import { ref } from '@vue/reactivity'

export default {
 setup(){
    const message=ref([])
    const data=ref('One')
    const dropvalue=ref('')
    return {
       message,data,dropvalue
    }
 }
}
</script>

<style scoped>

</style>