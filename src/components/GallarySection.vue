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
      <!-- 웨딩   -->
      <swiper-slide>
        <img src="../assets/img/_gallery/wedding_001.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/wedding_002.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/wedding_003.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/wedding_004.jpeg" width="100%" >
      </swiper-slide>
      <!-- 웨딩 끝 -->
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_001.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_002.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_003.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_004.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_005.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_006.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_007.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/outer_008.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/inside_001.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/inside_002.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/inside_003.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/inside_004.jpeg" width="100%" >
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/img/_gallery/inside_005.jpeg" width="100%" >
      </swiper-slide>
    </swiper>
  </div>
</template>

<style scoped>
  #gallery-section{
    background-size: 100%;
    max-width: 480px;
    width: 100%;
  }
</style>
