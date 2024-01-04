<template>
  <img class="flower-leaf" :src="imageUrl" :style="cssVars" />
</template>

<script>

import fallingLoveLeaf1 from "@/assets/img/love/love-leaf-1.png";
import fallingLoveLeaf2 from "@/assets/img/love/love-leaf-2.png";
import fallingLoveLeaf3 from "@/assets/img/love/love-leaf-3.png";
import fallingLoveLeaf4 from "@/assets/img/love/love-leaf-4.png";
import fallingLoveLeaf5 from "@/assets/img/love/love-leaf-5.jpeg";
import fallingLoveLeaf6 from "@/assets/img/love/love-leaf-6.jpeg";

export default {
  name: "FlowerLeaf",
  data (){
    return {
      images: [
        {url: fallingLoveLeaf1},
        {url: fallingLoveLeaf2},
        {url: fallingLoveLeaf3},
        {url: fallingLoveLeaf4},
        {url: fallingLoveLeaf5},
        {url: fallingLoveLeaf6}
      ]
    }
  },
  computed: {
    cssVars() {
      const fallDelay = Math.random() * 12;
      const shakeDelay = Math.random() * 3;

      const shakeDegree = Math.random() * 360;

      const leftPosition = Math.random() * 100;
      const translateX = Math.random() * (80 - 20) + 20;

      const fallDuration = Math.random() * (16 - 9) + 9;
      const shakeDuration = Math.random() * (3 - 2) + 2;

      return {
        "--fall-delay": fallDelay + "s",
        "--shake-delay": shakeDelay + "s",

        "--shake-degree": shakeDegree + "deg",

        "--left-position": leftPosition + "%",
        "--translate-x": translateX + "px",

        "--fall-duration": fallDuration + "s",
        "--shake-duration": shakeDuration + "s",
      };
    },
    imageUrl() {
      const imageNumber = Math.floor(Math.random() * (6 - 1) + 1);
      return this.images[imageNumber].url;
    },
  },
};
</script>

<style lang="scss" scoped>
.flower-leaf {
  z-index: 100;
  left: var(--left-position);
  -webkit-animation-delay: var(--fall-delay), var(--shake-delay);
  animation-delay: var(--fall-delay), var(--shake-delay);
  position: fixed;
  top: -10%;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  cursor: default;
  -webkit-animation-name: flowerleafs-fall, flowerleafs-shake;
  -webkit-animation-duration: var(--fall-duration), var(--shake-duration);
  -webkit-animation-timing-function: linear, ease-in-out;
  -webkit-animation-iteration-count: infinite, infinite;
  -webkit-animation-play-state: running, running;
  animation-name: flowerleafs-fall, flowerleafs-shake;
  animation-duration: var(--fall-duration), var(--shake-duration);
  animation-timing-function: linear, ease-in-out;
  animation-iteration-count: infinite, infinite;
  animation-play-state: running, running;
}

@-webkit-keyframes flowerleafs-fall {
  0% {
    top: -10%;
  }
  100% {
    top: 100%;
  }
}
@-webkit-keyframes flowerleafs-shake {
  0% {
    -webkit-transform: translateX(0px) rotate(0deg);
    transform: translateX(0px) rotate(0deg);
  }
  50% {
    -webkit-transform: translateX(var(--translate-x))
    rotate(var(--shake-degree));
    transform: translateX(var(--translate-x)) rotate(var(--shake-degree));
  }
  100% {
    -webkit-transform: translateX(0px) rotate(0deg);
    transform: translateX(0px) rotate(0deg);
  }
}
@keyframes flowerleafs-fall {
  0% {
    top: -10%;
  }
  100% {
    top: 100%;
  }
}
@keyframes flowerleafs-shake {
  0% {
    transform: translateX(0px) rotate(0deg);
  }
  50% {
    transform: translateX(var(--translate-x)) rotate(var(--shake-degree));
  }
  100% {
    transform: translateX(0px) rotate(0deg);
  }
}
</style>
