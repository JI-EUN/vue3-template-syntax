<template>
    <h1 :class="{active:isActive}" @click="activate">hello? ({{isActive}})</h1>
</template>

<script>
export default {
    data(){
        return{
            //Getter,Setter
            isActive:false
        }
    },
    methods:{
        activate(){
            this.isActive = true
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