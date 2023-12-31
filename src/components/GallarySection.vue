<script>
import {Carousel, Pagination, Slide} from "vue3-carousel";
import {defineComponent} from "vue";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: 'Auto-play',
  components: {
    Carousel,
    Slide,
    Pagination
  },
  data() {
    return {
      images: [
        {id: 13, imagePosition: 'img13url'},
        {id: 4, imagePosition: 'img4url'},
        {id: 9, imagePosition: 'img9url'},
        {id: 10, imagePosition: 'img10url'},
        {id: 2, imagePosition: 'img2url'},
        {id: 1, imagePosition: "img1url"},
        {id: 3, imagePosition: 'img3url'},
        {id: 5, imagePosition: 'img5url'},
        {id: 6, imagePosition: 'img6url'},
        {id: 7, imagePosition: 'img7url'},
        {id: 8, imagePosition: 'img8url'},
        {id: 11, imagePosition: 'img11url'},
        {id: 12, imagePosition: 'img12url'}
      ]
    }
  }
})
</script>

<template>
  <div style="text-align: center; font-size: 35px; margin-top: 10px; margin-bottom: 10px;">
    Gallary
  </div>
  <div id="gallary-section">
    <Carousel :itemsToShow="1" :wrapAround="true" :transition="500">
      <Slide v-for="(img, _idx) in images" :key="`slider_image_${_idx}`">
        <div :class="`carousel__item ${img.imagePosition}` "></div>
      </Slide>
      <template #addons>
        <Pagination />
      </template>
    </Carousel>
  </div>
</template>

<style scoped>
  #gallary-section{
    min-height: 200px;
    width: 100vw;
  }
  .carousel__slide {
    padding: 5px;
  }

  .carousel__viewport {
    perspective: 500px;
  }

  .carousel__track {
    transform-style: preserve-3d;
  }

  .carousel__slide--sliding {
    transition: 0.5s;
  }

  .carousel__slide {
    opacity: 0.9;
    transform: rotateY(-20deg) scale(0.9);
  }

  .carousel__slide--active ~ .carousel__slide {
    transform: rotateY(20deg) scale(0.9);
  }

  .carousel__slide--prev {
    opacity: 1;
    transform: rotateY(-10deg) scale(0.95);
  }

  .carousel__slide--next {
    opacity: 1;
    transform: rotateY(10deg) scale(0.95);
  }

  .carousel__slide--active {
    opacity: 1;
    transform: rotateY(0) scale(1.1);
  }
  .img1url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/1BD0AE67-1B80-422C-91BB-F9A3FE98A400.jpg");
    background-repeat: no-repeat;
  }
  .img2url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/AAF0CB11-61E3-476A-BEE8-644F84E6A853.jpg");
    background-repeat: no-repeat;
  }
  .img3url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/3FF53CA9-2A15-403F-AEA0-030CD8699025.jpg");
    background-repeat: no-repeat;
  }
  .img4url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/5EEE44D4-8310-41E3-844B-D5E8786D1EE7.jpg");
    background-repeat: no-repeat;
  }
  .img5url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/6DC97E31-632A-4709-BB2D-BFABF9072E2C.jpg");
    background-repeat: no-repeat;
  }
  .img6url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/6E4474C3-143D-4F14-8B89-9A6133BAFC7C.jpg");
    background-repeat: no-repeat;
  }
  .img7url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/8F39C789-2792-4BD4-BF3B-B295D1390BD3.jpg");
    background-repeat: no-repeat;
  }
  .img7url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/9AE6FF0E-E9C2-4A26-8FBC-0ED34CF8E44B.jpg");
    background-repeat: no-repeat;
  }
  .img8url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/35B6C4B5-F341-4EE5-8044-1456676E06B7.jpg");
    background-repeat: no-repeat;
  }
  .img9url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/97A3BD18-F728-4F5C-B290-10985BE242F4.jpg");
    background-repeat: no-repeat;
  }
  .img10url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/557B365A-F019-4F9A-9EA8-6CB583A768AF.jpg");
    background-repeat: no-repeat;
  }
  .img11url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/DEBF1C32-4960-470C-ABA8-A2B8759534DC.jpg");
    background-repeat: no-repeat;
  }
  .img12url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/D1745ABA-3396-43BD-AF9A-4B1E01CF8724.jpg");
    background-repeat: no-repeat;
  }
  .img13url {
    width: 480px;
    height: 480px;
    background-size: 100%;
    background-image: url("@/assets/img/gallary/D7D71FCE-D596-4BA6-A2C5-84AD7BD97938.jpg");
    background-repeat: no-repeat;
  }
</style>
