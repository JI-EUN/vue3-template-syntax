<template>
    <h1 :style="[fontStyle,backgroundStyle]" @click="chageStyle">
        Hello
    </h1>
</template>

<script>
export default {
    data(){
        return{
           fontStyle:{
                color:'orange',
                fontSize:'30px'
           },
           backgroundStyle:{
            backgroundColor:'black'
           }
        }
    },
    methods:{
        chageStyle(){
            this.fontStyle.color='red'
            this.fontStyle.fontSize = '60px'
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