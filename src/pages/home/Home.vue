<template>
	<div class="root">
		
	    <index-header/> 
		<index-swiper/>

		</div>
		
	</div>
</template>

<script type="text/javascript">
	import header from "./Header.vue" ;
	import swiper from "./Swiper.vue"
	
	export default{
		
		data() {
			return {
				
			}
		},
		components:{
			"index-header":header,
			"index-swiper":swiper
			
		}
	}
</script>

<style>

   html{
   	font-size:13.333vw;
   }
   body{
   	max-width: 540px;
   	min-width: 320px;
   }
  .header{
  	height: 2.12rem;
  	width: 100%;
  	background: red;
  	font-size:0.16rem;
  }

  

  
  
  

  
</style>