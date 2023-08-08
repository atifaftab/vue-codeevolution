<template>
  <!-- <h1>{{ firstName }} {{ middleName }} {{ lastName }}</h1> -->
  <h1>{{ computedName }}</h1>
  <!-- <h2 >TOTAL - {{ item.reduce((total,curr) =>(total  = total + curr.price),0) }}</h2> -->
  <button @click="item.push({id : 4,title : 'Camera',price : 50})">add item</button>
  <h3>computed Total - {{ total }}</h3>
  <h4>{{ reduceMethod() }}</h4>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Mohammad',
      lastName: 'Aftab',
      middleName: 'Atif',
      item: [
        {
          id: 1,
          title: 'TV',
          price: 100
        },
        {
          id: 2,
          title: 'Phone',
          price: 200
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300
        }

      ],
      arr: [1, 2, 3, 4, 5]

    }
  },
  methods: {

    reduceMethod() {
      console.log('accumulator' + " " + 'currentValue' + " " + 'currentIndex' + " [" + 'array' + "]")
      this.arr.reduce((accumulator, currentValue, currentIndex, array) => {
        console.log(accumulator + " " + currentValue + " " + currentIndex + " [" + array + "]")
        return accumulator + currentValue
      }, 0)
    }
  },
  computed: {
    computedName() {
      return `${this.firstName} ${this.middleName} ${this.lastName}`
    },
    total() {
      // return this.item.reduce((total, curr) => (total = total + curr.price),0)
      return this.item.reduce((total, curr) => (total + curr.price), 0)
    }
  }
}
</script>