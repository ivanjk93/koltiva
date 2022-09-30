<template>
  <main class="container mt-20">
    <div class="row title1-library">
      <div class="col-4 col-xs-4 col-sm-4 col-md-4 col-lg-4 abso-contain">
        <div class="pl-5">
          <p class="text-header-library1 mb-0">{{ text1 }}</p>
          <p class="text-header-library2">{{ text2 }}</p>
          <p class="text-header-library3">{{ text3 }}</p>
          <button class="button-library">Sit tristique ></button>
        </div>
      </div>
      <div class="col-8 col-xs-8 col-sm-8 col-md-8 col-lg-8 cursor-pointer">
        <div class="row d-flex overflow-x">
          <div
            :class="
              library.active === true
                ? 'col-6 col-xs-6 col-sm-6 col-md-6 col-lg-6 pa-3 promos'
                : 'col-3 col-xs-3 col-sm-3 col-md-3 col-lg-3 pa-3 promos'
            "
            v-for="(library, index) in libraries"
            :key="index"
            @click="changingStatus(library.active, index)"
          >
            <img
              class="image-library"
              :src="library.url"
              :alt="'photo' + index"
            />
            <div class="custom-box-library" v-if="library.active === true">
              <span class="pl-10 library1"
                ><i class="bi bi-star-fill"></i> {{ library.rate }}</span
              >
              <span class="pl-2 library2">({{ library.view }}K+)</span>
              <p class="pl-10 library3 mb-5">{{ library.title }}</p>
              <p class="pl-10 library3">
                <i class="bi bi-geo-alt-fill"></i> {{ library.location }}
              </p>
              <div class="pa-0">
                <i class="bi bi-arrow-right-short animate"></i>
              </div>
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
      text1: "DICTUM BIBENDUM AMET SIT.",
      text2: "Lacus faucibus sed sed.",
      text3:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sit sed eleifend nullam facilisis. Sit imperdiet eget magnis orci morbi sapien vulputate cras. Leo rhoncus dui risus.",
      libraries: [
        {
          url: "../src/assets/library1.png",
          rate: "5.0",
          view: 7.6,
          title: "Aliquam at volutpat.",
          location: "Jakarta, Indonesia",
          active: true,
        },
        {
          url: "../src/assets/library2.png",
          rate: "5.0",
          view: 7.6,
          title: "Bind Balorant.",
          location: "Jakarta, Indonesia",
          active: false,
        },
        {
          url: "../src/assets/library3.png",
          rate: "5.0",
          view: 7.6,
          title: "Bind Balorant.",
          location: "Jakarta, Indonesia",
          active: false,
        },
        {
          url: "../src/assets/library4.png",
          rate: "5.0",
          view: 7.6,
          title: "Bind Balorant.",
          location: "Jakarta, Indonesia",
          active: false,
        },
      ],
    };
  },
  methods: {
    changingStatus($status, $index) {
      //   console.log($status, $index);
      if ($status === false) {
        this.libraries[$index].active = true;
      } else {
        this.libraries[$index].active = false;
      }
    },
  },
};
</script>

<style scoped>
* {
  font-family: "Poppins", sans-serif;
}
.d-flex {
  display: flex;
  z-index: 0;
}
.overflow-x {
  overflow-x: auto;
}
.title1-library {
  display: flex;
  align-items: center;
}
.abso-contain {
  position: relative;
  z-index: 1;
}
.text-header-library1 {
  color: #7fb77e;
  font-size: 1.2rem;
  font-weight: 700;
}
.text-header-library2 {
  color: #000;
  font-size: 1.9rem;
  font-weight: bolder;
}
.text-header-library3 {
  color: #656565;
  font-size: 1.2rem;
  font-weight: 400;
}
.button-library {
  font-size: 1rem;
  background-color: #7fb77e;
  border: 1px solid #7fb77e;
  border-radius: 3px;
  color: #ffffff;
  padding: 5px 15px;
}
.image-library {
  width: 100%;
  height: 350px;
  object-fit: cover;
}
.custom-box-library {
  background-color: #ffffff;
  backdrop-filter: blur(2px);
  width: 84%;
  height: 80px;
  position: absolute;
  bottom: 9%;
  left: 8%;
  border-radius: 8px;
  padding: 10px;
}
.library1 {
  font-size: 1rem;
  color: #000;
  font-weight: bolder;
}
.library2 {
  font-size: 1rem;
  color: #000;
  font-weight: 400;
}
.library3 {
  font-size: 1rem;
  color: #000;
  font-weight: 600;
  margin-top: -3px;
}
.animate {
  background-color: #c6ebc5;
  position: absolute;
  bottom: 8px;
  right: 3px;
  border-radius: 3px;
  font-size: 1rem;
}
.animate::before {
  background-color: #c6ebc5;
  position: absolute;
  bottom: 8px;
  right: 3px;
  border-radius: 3px;
  font-size: 1rem;
}
.cursor-pointer {
  cursor: pointer;
}
.mt-20 {
  margin-top: 20px;
}
.mb-15 {
  margin-bottom: 15px;
}
.mb-5 {
  margin-bottom: 5px;
}
.mb-4 {
  margin-bottom: 4px;
}
.mb-0 {
  margin-bottom: 0px;
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
.pa-3 {
  padding: 3px;
}
.pa-0 {
  padding: 0px;
}
i.bi.bi-arrow-right-short::before {
  padding: 8px;
  font-size: 20px;
}

@media only screen and (max-width: 575px) {
  .text-header-library1 {
    color: #7fb77e;
    font-size: 0.5rem;
    font-weight: 700;
  }
  .text-header-library2 {
    color: #000;
    font-size: 0.8rem;
    font-weight: bolder;
  }
  .text-header-library3 {
    color: #656565;
    font-size: 0.5rem;
    font-weight: 400;
  }
  .button-library {
    font-size: 0.5rem;
    background-color: #7fb77e;
    border: 1px solid #7fb77e;
    border-radius: 3px;
    color: #ffffff;
    padding: 3px 10px;
  }
  .image-library {
    width: 100%;
    height: 250px;
    object-fit: cover;
  }
  .custom-box-library {
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
  .library1 {
    font-size: 0.47rem;
    color: #000;
    font-weight: bolder;
  }
  .library2 {
    font-size: 0.47rem;
    color: #000;
    font-weight: 400;
  }
  .library3 {
    font-size: 0.47rem;
    color: #000;
    font-weight: 600;
    margin-top: -3px;
  }
  .image-library {
    width: 100%;
    height: 250px;
    object-fit: cover;
  }
  .animate {
    background-color: #c6ebc5;
    position: absolute;
    bottom: 8px;
    right: 3px;
    border-radius: 3px;
    font-size: 1rem;
  }
  .animate::before {
    background-color: #c6ebc5;
    position: absolute;
    bottom: 8px;
    right: 3px;
    border-radius: 3px;
    font-size: 1rem;
  }
  i.bi.bi-arrow-right-short::before {
    padding: 1.5px;
    font-size: 8px;
  }
}
</style>