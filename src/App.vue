<template>
  <div id="app"> 
    <router-view/>
  </div>
</template>

<script>

export default {
  name: 'App'
}
</script>

<style> 
  @import "../static/css/reset.css";
  @import "../static/iconfont/iconfont.css";
  @import "../node_modules/swiper/dist/css/swiper.css";
	#app {
	  width: 100%;
	  height: 100%;
	} 
</style>