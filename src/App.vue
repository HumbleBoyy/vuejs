<script>
   export default {
    data(){
      return {
        name: "John Doe",
        status:false,
        tasks:['task one', 'task two', 'task three'],
        link:"https://asadullohs.vercel.app/"
      }
    },
    methods:{
       toggleStatus(){
         if(this.status !== true){
            
         }
       }
    }
   }
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === true">User is active</p>
  <p v-else>User is not active</p>

  <h3>Tasks</h3>
  <ul>
    <li v-for="task in tasks" :key="index">{{ task }}</li>
  </ul>
  <a v-bind:href="link">Asadullohs</a>

  <button v-on:click="toggleStatus">Change status</button>
</template>

