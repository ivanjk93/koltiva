<template>
  <main class="main-carousel">
    <div class="bg1"></div>
    <div class="container-carousel">
      <img class="image-carousel padding-right-10" src="../assets/frame1.png" />
      <img class="image-carousel padding-right-10" src="../assets/frame2.png" />
      <img class="image-carousel padding-right-10" src="../assets/frame3.png" />
      <img class="image-carousel padding-right-10" src="../assets/frame4.png" />
      <img class="image-carousel padding-right-10" src="../assets/frame5.png" />
      <img class="image-carousel" src="../assets/frame6.png" />
    </div>
    <div class="bg2"></div>
  </main>
</template>

<style scoped>
.main-carousel {
  margin-top: -170px !important;
}
.bg1 {
  background-color: #7fb77e;
  height: 20px;
  border-radius: 0% 0% 50% 50%;
  position: relative;
  z-index: 1;
}
.bg2 {
  background-color: #fafafa;
  height: 25px;
  border-radius: 50% 50% 0% 0%;
  position: relative;
  z-index: 1;
  margin-top: -25px;
}
.container-carousel {
  display: flex;
  overflow-x: auto;
  cursor: pointer;
  position: relative;
  margin-top: -20px;
  z-index: 0;
  padding: 0;
}
.image-carousel {
  object-fit: cover;
  width: 300px;
  min-width: 300px;
  height: 300px;
}
.padding-right-10 {
  padding-right: 10px;
}

@media only screen and (max-width: 575px) {
  .main-carousel {
    margin-top: -90px !important;
  }
  .bg1 {
    background-color: #7fb77e;
    height: 20px;
    border-radius: 0% 0% 50% 50%;
    position: relative;
    z-index: 1;
  }
  .bg2 {
    background-color: #fafafa;
    height: 25px;
    border-radius: 50% 50% 0% 0%;
    position: relative;
    z-index: 1;
    margin-top: -20px;
  }
  .container-carousel {
    display: flex;
    overflow-x: auto;
    cursor: pointer;
    position: relative;
    margin-top: -20px;
    z-index: 0;
    padding: 0;
  }
  .image-carousel {
    object-fit: cover;
    width: 100px;
    min-width: 100px;
    height: 130px;
  }
}
</style>