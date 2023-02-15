<template>
  <div>
    <b-button @click="submitt()" variant="primary">moni</b-button>{{response}}{{list}}
  </div>
</template>

<script>
import axios from 'axios';
export default {
    name:"RapiD",
data(){
    return{
list:[]
    }
},
mounted(){
this.submitt();
},
methods:{
    submitt(){
 axios.get('https://random-d.uk/api/v2').then((response)=>{
   return this.list= response.data ;
}).catch((error)=>{
    console.log(error)
})
    }
}
}
</script>

<style>

</style>