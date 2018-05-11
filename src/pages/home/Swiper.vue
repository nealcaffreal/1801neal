<template>
  <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
    <swiper-slide>
    	   <div><img src="https://img1.qunarzz.com/des-mis/ad/1805/e1/ef8151f2979f23.jpg"/></div>
    </swiper-slide>
    <swiper-slide>
    	   <div><img src="https://img1.qunarzz.com/des-mis/ad/1805/da/7cfb946d0c35.jpg"/></div> 
    </swiper-slide>
    <swiper-slide>
    	   <div><img src="https://img1.qunarzz.com/desmisact/images/1804/76/a6f62a01620aa7.jpg"/></div> 
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination swiper-personalize"  slot="pagination"></div>

 
  </swiper>
</template>

<script>
  // swiper options example:
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOption: {
          // NotNextTick is a component's own property, and if notNextTick is set to true, the component will not instantiate the swiper through NextTick, which means you can get the swiper object the first time (if you need to use the get swiper object to do what Things, then this property must be true)
          // notNextTick是一个组件自有属性，如果notNextTick设置为true，组件则不会通过NextTick来实例化swiper，也就意味着你可以在第一时间获取到swiper对象，假如你需要刚加载遍使用获取swiper对象来做什么事，那么这个属性一定要是true
          notNextTick: true,
          // swiper configs 所有的配置同swiper官方api配置
          autoplay: 3000,
          
         
          autoHeight: true,
          pagination : '.swiper-pagination',
         
          prevButton:'.swiper-button-prev',
          nextButton:'.swiper-button-next',

          onTransitionStart(swiper){
            console.log(swiper)
          },
          // more Swiper configs and callbacks...
          // ...
        }
      }
    },
    // you can find current swiper instance object like this, while the notNextTick property value must be true
    // 如果你需要得到当前的swiper对象来做一些事情，你可以像下面这样定义一个方法属性来获取当前的swiper对象，同时notNextTick必须为true
    computed: {
      swiper() {
        return this.$refs.mySwiper.swiper
      }
    },
    mounted() {
      // you can use current swiper instance object to do something(swiper methods)
      // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
      console.log('this is current swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script>
<style >
	  
</style>