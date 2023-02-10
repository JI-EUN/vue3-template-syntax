<template>
    <button @click="handler">click</button>
   <ul>
    <li v-for="{id,name} in newFruits" :key="id">{{name}} - {{id}}</li>
   </ul>
</template>

<script>
import shortid  from 'shortid'

export default {
    data(){
        return{
            fruits:['Apple','Orange','Banana']
        }
    },
    computed:{
        newFruits(){
            return this.fruits.map( fruit=>({
                id:shortid.generate(),
                name:fruit
            }) )
        }
    },
    methods:{
        handler(){
            this.fruits.push('Cherry')
        }
    }
}
</script>

<style scoped>
    .active{
        color:red;
        font-weight: bold;;
    }
</style>