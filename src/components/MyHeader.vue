<template>
<div>
    <h1> {{Name}} </h1>
</div>

</template>

<script>
export default {
    name:'MyHeader',
    props:{
        Name:String,
        myName:String
    }
}

</script>

<style>
div{
    text-align : center;
    margin:0px;
}
h1{
    font-color:#948979;
    font-size: 50px;
}
</style>