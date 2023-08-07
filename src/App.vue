<template>
<h2 v-for="(name, index) in names">{{index}} {{ name }}</h2>
<h2 v-for="(name) in fullnames">{{ name.firstName }} {{ name.lastName }}</h2>
</template>
<script>
import { createApp } from 'vue';

export default{
    name: createApp,
    data(){
        return{
            names: ['name', 'game', 'fame'],  //array of 3 string
            fullnames:[                       //array of objects
                {firstName: 'Bruce', lastName: 'Wayne'},
                {firstName: 'Clark', lastName: 'Kent'},
                {firstName: 'Barry', lastName: 'Allen'},

            ],
            actors : [
                {
                    name : 'Ben Affleck', 
                    movies : 'bvs', 'jl'
                },
                {
                    name : 'SRK',
                    movies : 'pathan', 'khnh'
                },
            ]
        }
    }
}
</script>