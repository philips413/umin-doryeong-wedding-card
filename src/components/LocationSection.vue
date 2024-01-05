<template>
  <div id="location-section">
    <img src="../assets/img/locationSection.png" width="100%">
    <div class="map-icon-wrapper" style="display: flex; justify-content: space-between;text-align: center; margin: 22px 10% 22px 10%;padding-bottom: 100px">
      <a class="link_tag" href="kakaomap://search?q=웨딩시그니처" style="vertical-align: middle">
        <img src="@/assets/img/kakaomap.png" width="40px" height="40px" />
        <p>카카오맵</p>
      </a>
      <a class="link_tag" href="tmap://search?name=웨딩시그니처">
        <img src="@/assets/img/tmap.png" width="40px" height="40px" />
        <p>T맵</p>
      </a>
      <a class="link_tag" href="nmap://search?query=웨딩시그니처&appname=https://philips413.github.io/wedding/">
        <img src="@/assets/img/navermap.png" width="40px" height="40px" />
        <p>네이버맵</p>
      </a>
    </div>
  </div>
</template>
<script setup>

</script>

<style scoped>
  #location-section {
    background-size: 100%;
    max-width: 480px;
    max-height: 750px;
    width: 100%;
    height: 100vh;
  }
  .link_tag {
    color: #202121;
    text-decoration: none;
  }
</style>
