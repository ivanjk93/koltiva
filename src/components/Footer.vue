<template>
  <main>
    <div class="container mb-50">
      <div class="row">
        <div class="col-12 col-xs-12 col-sm-12 col-md-6 col-lg-6 pa-5 mb-20">
          <div class="container-fluid pl-45">
            <img class="image-information" :src="url" alt="photo" />
            <div class="custom-box-information text-center">
              <span class="custom-box-icon">
                <img class="iconrectangle" :src="icon" alt="icon" />
              </span>
              <p class="text-information1 mb-0 mt-20">{{ experience }}</p>
              <p class="text-information2">Experience</p>
            </div>
            <div class="custom-box-bottom">
              <img
                :src="url2"
                width="80"
                alt="photo"
                style="float: left; margin-right: 10px"
              />
              <p class="bottext1 mb-0">{{ text1 }}</p>
              <p class="bottext2">{{ text2 }}</p>
              <p class="bottext3">
                View Details <i class="bi bi-chevron-right"></i>
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 col-xs-12 col-sm-12 col-md-6 col-lg-6 pa-5">
          <div class="container-fluid px-40">
            <p class="infotext1 mb-0">NON NISL MAURIS</p>
            <p class="infotext2">Ultricies Sit Faucibus.</p>
            <div
              class="boxbotinfo mb-20"
              v-for="(info, index) in infos"
              :key="index"
            >
              <p class="mb-0">{{ info.header }}</p>
              <p class="mb-0" style="font-weight: 700; color: #000">
                {{ info.title }}
              </p>
              <p class="mb-0">
                <i class="bi bi-geo-alt-fill"></i> {{ info.location }}
              </p>
              <p class="profiledetails">
                Profile Details <i class="bi bi-chevron-right"></i>
              </p>
            </div>
            <button class="button-footer">
              Faucibus <i class="bi bi-chevron-right"></i>
            </button>
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
      url: "../src/assets/information1.png",
      url2: "../src/assets/information2.png",
      icon: "../src/assets/informationicon1.png",
      experience: "12 Years",
      text1: "Viverra sit turpis.",
      text2: "Pearl Dolphin",
      infos: [
        {
          header: "SIT.",
          title: "Suspendisse erat.",
          location: "Jakarta, Indonesia",
        },
        {
          header: "ERAT.",
          title: "Feugiat vitae.",
          location: "Jakarta, Indonesia",
        },
        {
          header: "SIT.",
          title: "Massa euismod.",
          location: "Jakarta, Indonesia",
        },
        {
          header: "ERAT.",
          title: "Lectus.",
          location: "Jakarta, Indonesia",
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
.image-information {
  width: 100%;
  border-radius: 20px;
}
.text-information1 {
  font-size: 1.5rem;
  font-weight: 700;
}
.text-information2 {
  font-size: 1.3rem;
}
.custom-box-information {
  width: 130px;
  height: auto;
  background-color: #ffffff;
  position: absolute;
  top: 30px;
  right: 0;
  padding: 35px 20px 15px 20px;
  border-radius: 20px;
  animation: rightleft 2s infinite;
  animation-direction: alternate;
}
@keyframes rightleft {
  0% {
    margin-right: -35px;
  }
  100% {
    margin-right: -10px;
  }
  0% {
    margin-right: -35px;
  }
}
.iconrectangle {
  width: 28px;
  height: auto;
}
.custom-box-icon {
  padding: 15px 15px 17px 15px;
  background-color: rgba(127, 183, 126, 0.15);
  border-radius: 50%;
}
.custom-box-bottom {
  background-color: #ffffff;
  width: 300px;
  padding: 20px;
  border-radius: 20px;
  position: absolute;
  bottom: 30px;
  left: 0;
}
.custom-box-bottom img {
  border-radius: 10px;
}
.footers:hover .custom-box-promo {
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
.button-footer {
  font-size: 1rem;
  background-color: #7fb77e;
  border: 1px solid #7fb77e;
  border-radius: 5px;
  color: #ffffff;
  padding: 10px 20px;
  margin-top: 30px;
}
.bottext1 {
  font-size: 1.3rem;
  margin-top: 15px;
}
.bottext2 {
  font-weight: 600;
  color: #000;
  margin-bottom: 20px;
}
.bottext3 {
  font-weight: 500;
  font-size: 1.3rem;
  color: #7fb77e;
}
.infotext1 {
  color: #7fb77e;
  font-size: 1.2rem;
  font-weight: 700;
}
.infotext2 {
  color: #000;
  font-size: 2.3rem;
  font-weight: 700;
  margin-bottom: 40px;
}
.boxbotinfo {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 20px;
}
.boxbotinfo:hover {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0px 0px 5px 0px #eaeaea;
}
.profiledetails {
  float: right;
  margin-top: -50px;
  font-size: 1.3rem;
  color: #7fb77e;
}
.mb-0 {
  margin-bottom: 0px;
}
.mt-20 {
  margin-top: 20px;
}
.mt-15 {
  margin-top: 15px;
}
.mt-13 {
  margin-top: 13px;
}
.mt-10 {
  margin-top: 10px;
}
.mb-50 {
  margin-bottom: 50px;
}
.mb-40 {
  margin-bottom: 40px;
}
.mb-30 {
  margin-bottom: 30px;
}
.mb-20 {
  margin-bottom: 20px;
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
.mb-3 {
  margin-bottom: 3px;
}
.mb-2 {
  margin-bottom: 2px;
}
.mb-1 {
  margin-bottom: 1px;
}
.mb-0 {
  margin-bottom: 0px;
}
.pa-5 {
  padding: 5px;
}
.pa-0 {
  padding: 0px;
}
.px-40 {
  padding: 0px 40px;
}
.px-30 {
  padding: 0px 30px;
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
.pl-45 {
  padding-left: 45px;
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

@media only screen and (max-width: 575px) {
  .custom-box-information {
    width: 130px;
    height: auto;
    background-color: #ffffff;
    position: absolute;
    top: 30px;
    right: 0;
    padding: 35px 20px 15px 20px;
    border-radius: 20px;
    animation: rightleft 2s infinite;
    animation-direction: alternate;
  }
  @keyframes rightleft {
    0% {
      margin-right: 0px;
    }
    100% {
      margin-right: 15px;
    }
    0% {
      margin-right: 0px;
    }
  }
  .infotext2 {
    color: #000;
    font-size: 2.3rem;
    font-weight: 700;
    margin-bottom: 20px;
  }
}
</style>