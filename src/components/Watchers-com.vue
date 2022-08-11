<template>
  <h2>Watchers in Composition API</h2>
  <h2>Ask a yes/no question</h2>
  <input type="text" v-model="question">
  <h3>{{answer}}</h3>
 <h1> {{sum}}</h1>
</template>

<script setup>
import { ref } from '@vue/reactivity'
import { watch } from '@vue/runtime-core'
    const  question=ref('')
    const answer=ref('question usually contain a question mark')
    watch(question, async(newquestion)=>{
        if(newquestion.indexOf('?')>-1){
            answer.value='Thinking..........'
        }
    })

   
</script>

<style>

</style>