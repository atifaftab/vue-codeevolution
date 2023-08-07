<template>
<template v-for="name in names" :key="name">
   <h2 v-if="name ==='Bruce'"> {{ name }}</h2>
</template>
</template>
<script>
export default{
   name: 'App',
      data(){
         return{
            names : ['Bruce', 'Clark', 'Arthur']
         }
      }
}
</script>