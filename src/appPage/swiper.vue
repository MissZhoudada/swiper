<template>
  <div class="warp">
      <div v-show="!amLoading" class="swiper-content">
          <swiper :options="swiperOption" class="swipe-box">
              <swiper-slide v-for="(item,index) in itemList" :key="index+'c'">
                  <swiper-items/>
              </swiper-slide>
          </swiper>
      </div>      
  </div>
</template>
<script>
import 'swiper/dist/css/swiper.css';
import swiperItems from '../components/SwiperItem';
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  components:{
    swiperItems,
    swiper,
    swiperSlide
  },
  data(){
    return{
      itemList:[1,2,3,4,5,6,7,8],
      swiperOption: {
          spaceBetween: 20,//滑块靠右边的距离
          slidesPerView: "auto",
          centeredSlides: true//滑块居中
      }
    }
  }
}
</script>
<style scoped>
.warp{
    background: #030B2D;
    padding-top:20.67vw;
    height: calc(100% - 20.67vw);
    font-family: PingFangSC-Regular;
}
.swipe-box {
  height: 100%;
}
.swiper-slide {
  width: 77.87vw !important;
  background: url("../../static/img/chanpin_bg.png") no-repeat;
  background-size: cover;
  height:108.8vw;
  margin-top: 9.47vw;
}
.swiper-content{
    height: 133.33vw;  
    background: url("../../static/img/tuijian_bg.png") no-repeat;
    background-size: cover;  
    position: relative;
    top: 45%;
    left: 50%;
    transform: translate(-50%, -50%);
}

</style>