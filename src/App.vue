<script>
   export default {
    data(){
      return {
        name: "John Doe",
        status:"active",
        tasks:['task one', 'task two', 'task three'],
        link:"https://asadullohs.vercel.app/"
      }
    },
    methods:{
       toggleStatus(){
         if(this.status === 'active'){
            this.status = 'pending'
         }else if (this.status === 'pending'){
              this.status = 'inactive'
         }else{
            this.status = 'active'
         }
       }
    }
   }
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">It is pending</p>
  <p v-else>User is not active</p>

  <h3>Tasks</h3>
  <ul>
    <li v-for="task in tasks" :key="index">{{ task }}</li>
  </ul>
  <a v-bind:href="link">Asadullohs</a>

  <!-- <button v-on:click="toggleStatus">Change status</button> -->
  <button @:click="toggleStatus">Change status</button>
</template>

