<script>

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/navigation';

// import required modules
import { Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>

<template>
  <img src="../assets/img/galllery_title.jpeg" width="100%">
  <div id="gallery-section">
    <swiper
        :slidesPerView="1"
        :spaceBetween="30"
        :loop="true"
        :navigation="true"
        resistanceRatio="1"
        :modules="modules"
        class="mySwiper"
    >
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0064.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0068.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0525.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0158.jpg" width="100%" >
      </swiper-slide>
      <!-- 숲속에서! -->
      <!-- 밝기 조정 필요함 -->
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0765.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0783.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0757.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0282.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0248.jpg" width="100%" >
      </swiper-slide>
      <!-- 숲속에서! 끝 -->
      <!-- 집 안에서 -->
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0724.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0680.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0354.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0333.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0168.jpg" width="100%" >
      </swiper-slide>
      <!-- 집 안에서 끝 -->
      <!-- 강가에서 -->
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0574.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0566.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0596.jpg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/gallary/IMG_0520.jpg" width="100%" >
      </swiper-slide>
      <!-- 강가에서 끝-->
    </swiper>
  </div>
</template>

<style scoped>
  #gallery-section{
    background-size: 100%;
    max-width: 480px;
    max-height: 750px;
    width: 100%;
  }
</style>
