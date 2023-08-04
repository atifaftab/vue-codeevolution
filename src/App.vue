<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" /> -->
    <div><h2>{{intro}} {{ name }}</h2></div>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <button class="button" :disabled="isDisabled" >Enter</button>

    <h2 :id="headingId">Welcome to Batcave</h2>
    <h2 class="underline">underlined</h2>
    <h2 class="underline" :class="status">Status</h2>
    <h2 :class="isPromoted && 'promoted'">Movie</h2>
    <h2 :class="isSoldOut ? 'sold-out' : 'new'">new releases</h2>
    <h2 :class="['new','promoted']">I am green and Italic</h2>
    <h2 :class="[isPromoted && 'promoted',isSoldOut ? 'sold-out' : 'new']">Array with conditional  </h2>
    <h2 :class="
    {
      promoted : isPromoted,
      new : !isSoldOut,
      'sold-out' : isSoldOut
    }" >Object conditions</h2>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return{
      name : 'Atif',
      intro : 'I am',
      headingId : 'Welcome to Batcave',
      isDisabled : false,
      status : 'danger',
      isPromoted : true,
      isSoldOut : true
    };
  },
  // components: {
  //   HelloWorld
  // }
}
</script>
<style>
.button{
  text-align: center;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new{
  color: green;
}
.sold-out{
  color: red;
}
</style>