<template>
  <div id="location-section">
    <img src="../assets/img/locationSection.png" width="100%">
    <div class="map-icon-wrapper" style="display: flex; justify-content: space-between;text-align: center; margin: 22px 10% 22px 10%;">
      <a class="link_tag" href="kakaomap://search?q=웨딩시그니처&lat=37.5526889&lon=126.9173249" style="vertical-align: middle">
        <img src="@/assets/img/kakaomap.png" width="40px" height="40px" />
        <p>카카오맵</p>
      </a>
      <a class="link_tag" href="tmap://search?name=웨딩시그니처">
        <img src="@/assets/img/tmap.png" width="40px" height="40px" />
        <p>T맵</p>
      </a>
      <!-- 37.5526889 126.9173249 -->
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
    width: 100%;
  }
  .link_tag {
    color: #202121;
    text-decoration: none;
  }
</style>
