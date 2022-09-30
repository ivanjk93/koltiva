<template>
  <main>
    <div class="container-promo">
      <div class="mb-15 pl-5">
        <p class="text-header-promo1 mb-0">{{ text1 }}</p>
        <p class="text-header-promo2 mb-0">{{ text2 }}</p>
      </div>
      <div class="container-fluid px-0">
        <div
          class="col-4 col-xs-4 col-sm-4 col-md-4 col-lg-4 pa-5 promos"
          v-for="(promo, index) in promos"
          :key="index"
          @mouseover="promo.active = true"
          @mouseleave="promo.active = false"
        >
          <img class="image-promo" :src="promo.url" :alt="'photo' + index" />
          <div class="custom-box-promo">
            <span class="pl-10 text-box"
              ><i class="bi bi-star-fill"></i> {{ promo.rate }}</span
            >
            <span class="pl-2 text-box-promo2">({{ promo.view }}K+)</span>
            <p class="pl-10 text-box-promo3 mb-4">{{ promo.title }}</p>
            <p class="pl-10 text-box-promo3">
              IDR {{ promo.low_price }} - IDR {{ promo.high_price }}
            </p>
            <div class="pa-0" v-if="promo.active === true">
              <i class="bi bi-arrow-right-short animate"></i>
            </div>
          </div>
        </div>
      </div>
      <div class="container-fluid text-center">
        <button class="button mt-13">Mauris mattis eget ></button>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      text1: "NEC FEUGIAT FRINGILLA.",
      text2: "Volutpat dui.",
      promos: [
        {
          url: "../src/assets/promo1.png",
          rate: "5.0",
          view: 6.6,
          title: "Commodo Mattis.",
          low_price: "29.000",
          high_price: "259.999",
          active: false,
        },
        {
          url: "../src/assets/promo2.png",
          rate: "5.0",
          view: 6.6,
          title: "Sit ullamcorper nisl amet.",
          low_price: "29.000",
          high_price: "259.999",
          active: false,
        },
        {
          url: "../src/assets/promo3.png",
          rate: "5.0",
          view: 6.6,
          title: "Scelerisque venenatis.",
          low_price: "29.000",
          high_price: "259.999",
          active: false,
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
.image-promo {
  width: 100%;
}
.margin-right-10 {
  margin-right: 10px;
}
.custom-box-promo {
  background-color: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(2px);
  width: 84%;
  height: 100px;
  position: absolute;
  bottom: 9%;
  left: 8%;
  border-radius: 8px;
  padding: 20px;
}
.text-box {
  font-size: 1rem;
  color: #000;
  font-weight: bolder;
}
.text-box-promo2 {
  font-size: 1rem;
  color: #000;
  font-weight: 400;
}
.text-box-promo3 {
  font-size: 1rem;
  color: #000;
  font-weight: 600;
  margin-top: -3px;
}
.promos:hover .custom-box-promo {
  background-color: #ffffff;
  backdrop-filter: blur(2px);
  width: 84%;
  height: 100px;
  position: absolute;
  bottom: 9%;
  left: 8%;
  border-radius: 8px;
  padding: 20px;
}
.animate {
  background-color: #c6ebc5;
  position: absolute;
  bottom: 8px;
  right: 3px;
  border-radius: 4px;
  font-size: 1rem;
  animation: bottop 1s;
  animation-direction: alternate;
}
.animate::before {
  background-color: #c6ebc5;
  position: absolute;
  bottom: 8px;
  right: 3px;
  border-radius: 4px;
  font-size: 1rem;
  animation: bottop 1s;
  animation-direction: alternate;
}
@keyframes bottop {
  0% {
    bottom: 0px;
  }
  100% {
    bottom: 8px;
  }
}
.button {
  font-size: 1rem;
  background-color: #7fb77e;
  border: 1px solid #7fb77e;
  border-radius: 3px;
  color: #ffffff;
  padding: 5px 15px;
}
.mb-0 {
  margin-bottom: 0px;
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
  .custom-box-promo {
    background-color: rgba(255, 255, 255, 0.5);
    backdrop-filter: blur(2px);
    width: 84%;
    height: 50px;
    position: absolute;
    bottom: 9%;
    left: 8%;
    border-radius: 8px;
    padding: 0px;
  }
  .text-box {
    font-size: 0.47rem;
    color: #000;
    font-weight: bolder;
  }
  .text-box-promo2 {
    font-size: 0.47rem;
    color: #000;
    font-weight: 400;
  }
  .text-box-promo3 {
    font-size: 0.47rem;
    color: #000;
    font-weight: 600;
    margin-top: -3px;
  }
  .promos:hover .custom-box-promo {
    background-color: #ffffff;
    backdrop-filter: blur(2px);
    width: 84%;
    height: 50px;
    position: absolute;
    bottom: 9%;
    left: 8%;
    border-radius: 8px;
    padding: 0px;
  }
  .animate {
    background-color: #c6ebc5;
    position: absolute;
    bottom: 8px;
    right: 3px;
    border-radius: 4px;
    font-size: 1rem;
    animation: bottop 1s;
    animation-direction: alternate;
  }
  .animate::before {
    background-color: #c6ebc5;
    position: absolute;
    bottom: 8px;
    right: 3px;
    border-radius: 4px;
    font-size: 1rem;
    animation: bottop 1s;
    animation-direction: alternate;
  }
  @keyframes bottop {
    0% {
      bottom: 0px;
    }
    100% {
      bottom: 8px;
    }
  }
  .button {
    font-size: 0.5rem;
    background-color: #7fb77e;
    border: 1px solid #7fb77e;
    border-radius: 3px;
    color: #ffffff;
    padding: 3px 10px;
  }
  .image-promo {
    width: 100%;
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