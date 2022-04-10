<template>
    <header>
        <h1 style="color:white; font-weight:normal"> {{title}}</h1>
    </header>
</template>

<script>

export default{
    name: 'Header',
    props:{
        title:{
            type:String,
        }
    }
}
</script>