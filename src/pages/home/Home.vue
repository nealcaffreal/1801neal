<template>
 <div class="hello">{{msg}}</div>
 <index-header/>
</template>

<script>
import Header from "./header.vue";	
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    },
    components:{
    	"index-header" : header
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello{background: red}
</style>
