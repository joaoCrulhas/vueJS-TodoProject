<template>
  <div class="hello">
        <input
         type="text" 
         placeholder="O que precisa ser feito?"
         v-on:keyup.enter ="addTask" >
 </div>
</template>

<script>
// SLIDE 48 DO LIVRO
import { Task } from '../models/Tasks.js'
export default {
  name: 'InputTask',
  methods: {
    addTask ($event) {
      let value = $event.target.value
      let task = new Task()
      task.completed = false
      task.title = value
      console.log(task)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
