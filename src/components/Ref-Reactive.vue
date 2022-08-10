<template>
<h2>Ref</h2>
<h3>{{user1.name}} -{{user1.age}}</h3><br>
<button @click="updateuser1">update user1</button>
  <h2>Reactive</h2>
  <h3>{{user2.name}} -{{user2.age}}</h3>
  <button @click="updateuser2">update user2</button>
</template>

<script>
import { ref,reactive } from '@vue/reactivity'
export default {
  setup(){
    const user1=ref({name:'Tom',age:23})
   const user2=reactive({name:'Shubham',age:24})
    const updateuser1=()=>{
      user1.value.name="Rahul"
      user1.value.age=20
    }
    const updateuser2=()=>{
      user2.name="Shivam"
      user2.age=25
    }
     return {user1,updateuser1,user2,updateuser2}
  }
}
</script>

<style>

</style>