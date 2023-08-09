<template>
  <h2>Volume (0 - 2)</h2>
  <h2>Current Volume - {{ volume }}</h2>
  <button @click="volume += 2"> + </button>
  <button @click="volume -= 2"> - </button>
</template>

<script>
export default {
  name: 'App.vue',
  data() {
    return {
      volume: 0
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
    }
  }
}
</script>