<template>
<h2>{{ add(2,1,1) }}</h2>
<h2>{{ multiply(baseValue) }}</h2>
</template>

<script>
    export default{
        name : 'App',
        data(){
            return{
                baseValue : 10 ,
                baseMultiplier : 5
            }
        },
        methods: {
            add(a,b,c){
                return (a+b+c)*this.baseValue;
            },
            multiply(a){
                return a*this.baseMultiplier;
            }
        }
    }
</script>