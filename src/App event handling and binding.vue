<template>
<h2>{{ name }}</h2>
<!-- <button v-on:click="name = 'Batman'">click to change</button> -->
<button @click ="changeName, increment(1, $event)">click to change</button>

<h2>{{ count }}</h2>
<button @click="increment(1, $event)">increase 1</button>
<button @click="increment(5)">increase 5</button>
<button @click="decrement(1)">decrease 1</button>
<button @click="decrement(5)">decrease 5</button>
<!-- <button v-on:click="count-=1">decrease</button> -->
</template>

<script>
   export default{
      name: 'App',
      data(){
         return{
            name : 'Atif',
            count : 0
         }
      },
      methods : {
         increment(val,event){
            console.log(event)
            return this.count+=val;
         },
         decrement(val){
            return this.count-=val;
         },
         changeName(event){
            console.log(event)
            return this.name = 'Batman';
         }
      }
   }
</script>