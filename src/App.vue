<template>
  <h2>hello Compositio api</h2>
  <h3 ref="h">Sum of two numbers is  {{number}}</h3>
  <h3 >{{user}}</h3>
  <button @click="incerment">count{{count}}</button>
  <br>
  <input type="text" v-model="user.name">
  <br>
  <button @click="user.age++">add 1 to age</button>
  <refandReactive />
  <computed />
 <props />
</template>

<script>
import { ref } from '@vue/reactivity'
import refandReactive from './components/Ref-Reactive.vue'
import computed from './components/Computed-property.vue'
import props from './components/Props-composition.vue'

export default {
  components:{
      refandReactive,
      computed,
      props
   
  },
  setup(){
    let number1=20
    let number2=38
    let number=number1+number2

    let name=ref('Steve Smith')
    let age=ref(39)
let user={name,age}
 let count=0
const handleclick=()=>{
 
  console.log('you clicked me')
 
}
let h=ref(null)
 console.log(h)
 console.log(h.value)


 const incerment=()=>{
  console.log(count)
     count++
     h.value.classList.add("test")
     h.value.textContent='Hello ninja'
     name.value='Bob'
     age.value=34
 }

 
    return {user,number,handleclick,incerment,h}


  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
