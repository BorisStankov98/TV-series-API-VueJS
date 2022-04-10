<template>
<form @submit.prevent="onSubmit">
        <input placeholder="Type a show" class="inp" type="text" v-model="myInput">
        <button class="btn"  @click=callApi()>Search</button>
        </form>
</template>

<script>
import axios from 'axios';
export default{
    name:'menu',
    data(){
        return{
        moviesB:[],
        myInput:''
        }
    },
    props:{
    },
    methods:{
     callApi(){
         axios.get(`https://api.tvmaze.com/singlesearch/shows?q=${this.myInput}`)
        .then((res)=>{
            this.moviesB.push(res)
            this.$emit("clicked",this.moviesB)
            this.myInput=''
}) 
},

}
}
</script>
