<template>
  <div>
   <Gxio></Gxio>
    </div>
</template>

<script>
import Gxio from "../src/components/Rapid.vue";
export default {
  name: 'App',
  components:{
     Gxio
  },
  data(){
    return{
    
    }
  },
  computed:{
filtered(){
  return this.items.filter(i=>i.body.includes(this.search))
}
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
