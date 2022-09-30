<template>
  <main class="mt-20 mb-20">
    <div class="container-promo">
      <div class="mb-15 pl-5 text-center">
        <p class="text-header-promo1 mb-0">{{ text1 }}</p>
        <p class="text-header-promo2 mb-0">{{ text2 }}</p>
      </div>
      <div class="container-fluid px-0">
        <div
          class="col-6 col-xs-6 col-sm-6 col-md-3 col-lg-3 pa-5"
          v-for="(detail, index) in details"
          :key="index"
          @mouseover="detail.active = true"
          @mouseleave="detail.active = false"
        >
          <div class="promos-detail">
            <img
              class="image-detail mb-30"
              :src="detail.url"
              :alt="'photo' + index"
            />
            <div class="custom-detail-icon"></div>
            <p class="pl-10 text-box-detail2 mb-10">{{ detail.title }}</p>
            <p class="pl-10 text-box-detail3 mb-4">{{ detail.text }}</p>
            <div class="custom-box-detail">
              <p class="pl-10 text-box-detail1 mb-4">
                View Details <i class="bi bi-chevron-right"></i>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      text1: "MUS ULTRICES.",
      text2: "Tortor et lectus.",
      details: [
        {
          url: "../src/assets/detail1.png",
          title: "Dui nulla.",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          url: "../src/assets/detail2.png",
          title: "Fermentum.",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          url: "../src/assets/detail3.png",
          title: "Tortor quam.",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
        {
          url: "../src/assets/detail4.png",
          title: "Diam nisi in.",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  font-family: "Poppins", sans-serif;
}
.container-promo {
  padding: 20px;
}
.text-header-promo1 {
  color: #7fb77e;
  font-size: 1.2rem;
  font-weight: 700;
}
.text-header-promo2 {
  color: #000;
  font-size: 1.9rem;
  font-weight: bolder;
}
.image-detail {
  width: 40px;
  margin-top: 20px;
  z-index: 1;
  filter: brightness(0) invert(1);
}
.margin-right-10 {
  margin-right: 10px;
}
.custom-detail-icon {
  width: 20px;
  padding: 3rem;
  border-radius: 50%;
  position: absolute;
  top: 10px;
  left: 39.2%;
  z-index: 0;
  background-color: #c6ebc5;
}
.custom-box-detail {
  background-color: #ffffff;
  backdrop-filter: blur(2px);
  width: 100%;
  height: 50px;
  position: absolute;
  bottom: 0;
  left: 0;
  border-radius: 10px;
  padding: 20px;
}
.text-box-detail1 {
  font-size: 1rem;
  color: #000;
  font-weight: bolder;
}
.text-box-detail2 {
  font-size: 1.5rem;
  color: #000;
  font-weight: 800;
}
.promos-detail {
  background-color: #ffffff;
  height: 250px;
  text-align: center;
  border-radius: 15px;
  cursor: pointer;
}
.promos-detail:hover {
  background-color: #c6ebc5;
}
.promos-detail:hover .custom-detail-icon {
  width: 20px;
  padding: 3rem;
  border-radius: 50%;
  position: absolute;
  top: 10px;
  left: 39.2%;
  z-index: 0;
  background-color: #ffffff;
}
.promos-detail:hover .image-detail {
  width: 40px;
  margin-top: 20px;
  z-index: 1;
  filter: brightness(1) invert(0);
}
.button {
  font-size: 1rem;
  background-color: #7fb77e;
  border: 1px solid #7fb77e;
  border-radius: 3px;
  color: #ffffff;
  padding: 5px 15px;
}
.mb-30 {
  margin-bottom: 30px;
}
.mb-20 {
  margin-bottom: 20px;
}
.mb-0 {
  margin-bottom: 0px;
}
.mt-20 {
  margin-top: 20px;
}
.mt-13 {
  margin-top: 13px;
}
.mt-10 {
  margin-top: 10px;
}
.mb-15 {
  margin-bottom: 15px;
}
.mb-10 {
  margin-bottom: 10px;
}
.mb-5 {
  margin-bottom: 5px;
}
.mb-4 {
  margin-bottom: 4px;
}
.pa-5 {
  padding: 5px;
}
.pa-0 {
  padding: 0px;
}
.px-10 {
  padding: 0px 10px;
}
.px-5 {
  padding: 0px 5px;
}
.px-0 {
  padding: 0px 0px;
}
.pl-10 {
  padding-left: 10px;
}
.pl-5 {
  padding-left: 5px;
}
.pl-2 {
  padding-left: 2px;
}
i.bi.bi-arrow-right-short::before {
  padding: 8px;
  font-size: 20px;
}

@media only screen and (max-width: 575px) {
  main {
    font-family: "Poppins", sans-serif;
  }
  .container-promo {
    padding: 20px;
  }
  .text-header-promo1 {
    color: #7fb77e;
    font-size: 0.5rem;
    font-weight: 700;
  }
  .text-header-promo2 {
    color: #000;
    font-size: 0.8rem;
    font-weight: bolder;
  }
  .custom-detail-icon {
    width: 20px;
    padding: 3rem;
    border-radius: 50%;
    position: absolute;
    top: 10px;
    left: 32%;
    z-index: 0;
    background-color: #c6ebc5;
  }
  .custom-box-detail {
    background-color: #ffffff;
    backdrop-filter: blur(2px);
    width: 100%;
    height: 50px;
    position: absolute;
    bottom: 0;
    left: 0;
    border-radius: 10px;
    padding: 0px;
  }
  .text-box-detail1 {
    font-size: 1rem;
    color: #000;
    font-weight: bolder;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .text-box-detail2 {
    font-size: 1rem;
    color: #000;
    font-weight: 800;
  }
  .text-box-detail3 {
    font-size: 0.8rem;
    color: #b5b5b5;
    font-weight: 800;
  }
  .promos-detail {
    background-color: #ffffff;
    height: 220px;
    text-align: center;
    border-radius: 15px;
    cursor: pointer;
  }
  .promos-detail:hover {
    background-color: #c6ebc5;
  }
  .promos-detail:hover .custom-detail-icon {
    width: 20px;
    padding: 3rem;
    border-radius: 50%;
    position: absolute;
    top: 10px;
    left: 32%;
    z-index: 0;
    background-color: #ffffff;
  }
  .promos-detail:hover .image-detail {
    width: 40px;
    margin-top: 20px;
    z-index: 1;
    filter: brightness(1) invert(0);
  }
  .button {
    font-size: 0.5rem;
    background-color: #7fb77e;
    border: 1px solid #7fb77e;
    border-radius: 3px;
    color: #ffffff;
    padding: 3px 10px;
  }
  .image-detail {
    width: 40px;
    margin-top: 20px;
    z-index: 1;
    filter: brightness(0) invert(1);
  }
  .margin-right-10 {
    margin-right: 10px;
  }
  i.bi.bi-arrow-right-short::before {
    padding: 1.5px;
    font-size: 8px;
  }
}
</style>