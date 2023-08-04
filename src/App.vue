<template>

<h2 v-if="num == 5">This is heading</h2>
</template>
<script>
export default{
    name : 'App',
    data(){
      return{
         num : 5
      }
    }
}
</script>