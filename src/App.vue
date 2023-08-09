<template>
  <h2>Volume (0 - 2)</h2>
  <h2>Current Volume - {{ volume }}</h2>
  <button @click="volume += 2"> + </button>
  <button @click="volume -= 2"> - </button>

  <input type="text" v-model="movie">
  <input type="text" v-model="movieInfo.title">
  <input type="text" v-model="movieInfo.info">
  <button @click="movieList.push('flash')">Add Movie</button>

</template>

<script>
export default {
  name: 'App.vue',
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo :{
        title : '',
        info : ''
      },
      movieList : ['superman', 'Batman','Thor']
    }
  },
  methods: {

  },
  computed: {

  },
  watch: {
    volume(value, lastValue) {
      if (value > lastValue && value == 16) {
        alert("higher volume can damage hearing")
      }
    },
    movie: {
      handler(newValue) {
        console.log("new Movie : ", newValue)
      },
      immediate : true
    },
    movieInfo:{
      handler(newValue){
        console.log(`The Title of movie ${newValue.title} and info ${newValue.info}`)
      },
      deep : true
    },
    movieList :{
      handler(newValue){
        console.log(`the new movie List ${newValue}`)
      },
      deep : true
    }
  }
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