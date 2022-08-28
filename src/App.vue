<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg" id="navbar">
      <div class="container nav-container">
        <div class="container-fluid row">
          <div class="logo-container col-md-12 col-lg-6">
            <div class="row col-lg-6 col-sm-12">
              <div class="logo-name row col-lg-12 col-sm-6">
                <img class="img-logo col-5" src="DAMAS-2.jpg" alt="image" />
                <a class="navbar-brand col-6" href="#">
                  <span class="brand-name-1">SABINE HAHM</span><br />
                  <span class="brand-name-2">Mithilfe Mithilfe</span>
                </a>
              </div>
              <button
                class="navbar-toggler btn-outline-success col-md-6 col-sm-6"
                data-bs-toggle="collapse"
                data-bs-target="#nav-btn"
                aria-controls="#nav-btn"
                aria-expanded="false"
                aria-label="Toggle navigation"
              >
                <span class="navbar-toggler-icon"></span>
              </button>
            </div>
          </div>
          <div class="navbar-collapse collapse col-lg-6" id="nav-btn">
            <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <router-link class="router-link" to="/">StartSeite</router-link>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#services"> Leistungen </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#featured-work"> Galarie </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#footer"> kontacte</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
    <div id="slider" class="slider">
      <div class="overlay"></div>
      <transition-group class="img-container" name="fade" tag="div">
        <div v-for="i in [currentIndex]" :key="i">
          <img class="slider-img" :src="currentImg" />
          <h1 class="title-text">{{ currentTitle }}</h1>
        </div>
      </transition-group>
      <a class="prev" @click="prev" href="#">&#10094; </a>
      <a class="next" @click="next" href="#">&#10095; </a>
    </div>
    <!--Start Container-->
    <router-view />
    <!--End Container-->

    <div id="footer" class="footer">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="company-info text-start">
              <img src="DAMAS-2.jpg" alt="img-logo" />
              <h2>
                <a class="navbar-brand" href="#">
                  <span class="brand-name-1">Sabine Hahm</span><br />
                  <span class="brand-name-2">Mithilfe Mithilfe</span>
                </a>
              </h2>
              <p>
                Mithilfe Mithilfe Mithilfe Mithilfe Mithilfe Mithilfe Mithilfe
              </p>
            </div>
          </div>
          <div class="col-md-4">
            <div class="map-container">
              <h2>Standort</h2>
              <div class="location-window">
                <iframe
                  class="map"
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2435.6673359080555!2d13.182737799999998!3d52.37645179999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47a85ebf7ac8a765%3A0x560bb7549b4cd811!2sAlte%20Feldmark%2011A%2C%2014532%20Stahnsdorf!5e0!3m2!1sen!2sde!4v1661696115280!5m2!1sen!2sde"                  style="border: 0"
                  allowfullscreen=""
                  loading="lazy"
                ></iframe>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="contact-container">
              <h2>Kontakt</h2>
              <ul class="list">
                <li class="fw-bold">Adresse: <span class="fw-normal"> Alte Feldmark 11a, 14532 Stahnsdorf </span>.</li>
                <li class="fw-bold">Telefonnummer: <span class="fw-normal"> +49 (0) 15 773 584 878 </span>.</li>
                <li class="fw-bold">Email: <span class="fw-normal"> kp-tcm.hahm@gmail.com </span>.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "app",
  data() {
    return {
      images: ["slider-1.png", "slider-2.png", "slider-3.png"],
      title: ["Komplementäre Physiotherapie", "Traditionelle Chinesische Medizin", "NordicWalking"],
      timer: null,
      currentIndex: 0,
    };
  },
  methods: {
    startSlide: function () {
      this.timer = setInterval(this.next, 5000);
    },

    next: function () {
      this.currentIndex += 1;
    },
    prev: function () {
      this.currentIndex -= 1;
    },
  },
  mounted() {
    this.startSlide();
    //to calculate window height to adjust the slider
    var windoHT = window.innerHeight;
    var NavBarHT = document.getElementById("navbar").offsetHeight;
    var SliderHtT = windoHT - NavBarHT;
    document.getElementById("carousel-inner").style.height = SliderHtT + "px";
    document.getElementById("slider").style.height = SliderHtT + "px";
    document.getElementById("carousel-item-1").style.height = SliderHtT + "px";
    document.getElementById("carousel-item-2").style.height = SliderHtT + "px";
    document.getElementById("carousel-item-3").style.height = SliderHtT + "px";
    // end calculate window height to adjust the slider Dynamically
  },

  computed: {
    currentImg: function () {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    },
    currentTitle: function () {
      return this.title[Math.abs(this.currentIndex) % this.title.length];
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=News+Cycle&display=swap");
</style>
<style lang="scss">
$blueCol: #2c3e50;
$greenCol: #6d8b74;
$LightgreenCol: #c4dfaa;
$pinkCol: #ffadad;
$whiteCol: #fdf8fa;
$SkyCol: #c4dfaa;
$fontSize: 4rem;
$fontSizeTitle: 2rem;
//for scroll bar Start
/* Works on Firefox */
* {
  scrollbar-width: 8px;
  scrollbar-color: $SkyCol $greenCol;
  scroll-behavior: auto;
}

/* Works on Chrome, Edge, and Safari */
*::-webkit-scrollbar {
  width: 20px;
}

*::-webkit-scrollbar-track {
  background: $greenCol;
}

*::-webkit-scrollbar-thumb {
  background-color: $SkyCol;
  border-radius: 20px;
  border: 3px solid $greenCol;
}
//End Scroll bar
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #f6f6f6;
  scroll-behavior: smooth;
}
.logo-container {
  display: flex;
  flex-direction: row;
  justify-content: start;
}
#slider {
  //background: red;
  position: relative;
  font-family: "Bebas Neue", cursive;
  letter-spacing: 0.15rem;
  h1 {
  }
  .img-container {
    width: 100%;
    height: 100%;
  }
  .title-text {
    max-width: 500px;
    position: absolute;
    z-index: 10;
    top: 20%;
    left: 6%;
    color: $whiteCol;
  }
  .overlay {
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 10;
    background: rgba(0, 0, 0, 0.589);
  }
}
.navbar {
  padding: 30px;
  background: #6d9886;
  background: linear-gradient(to top left, $greenCol, $LightgreenCol);
  border-bottom: 2.5px solid $SkyCol;

  .nav-container {
    max-width: 100%;
  }
  .navbar-toggler {
    background: $SkyCol;
  }
  .navbar-nav {
    text-transform: uppercase;
    font-family: "News Cycle", sans-serif;
    letter-spacing: 0.15rem;
    .router-link {
      font-weight: bold;
      color: $SkyCol;
      display: block;
      padding: 0.5rem 1rem;
      padding-right: 0.5rem;
      padding-left: 0.5rem;
      text-decoration: none;
      transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
        border-color 0.15s ease-in-out;
      &.router-link-exact-active {
        color: $SkyCol;
      }
    }
    a {
      font-weight: bold;
      color: $whiteCol;
      text-decoration: none;
      &.router-link-exact-active {
        color: $SkyCol;
      }
    }
    a,
    .router-link {
      font-size: 15px;
      margin-left: 20px;
    }
  }
}
.navbar-brand {
  text-align: left;
  font-family: "Bebas Neue", cursive;
  .brand-name-1 {
    color: $whiteCol;
    font-size: 2.1rem;
    letter-spacing: 0.25rem;
  }
  .brand-name-2 {
    color: $whiteCol;
    font-size: 1.2rem;
    letter-spacing: 0.15rem;
  }
  a {
    text-decoration: none;
  }
}

img {
  height: 600px;
  width: 100%;
}
.img-logo {
  width: 5rem;
  height: 5rem;
  margin-right: 0.6rem;
}
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}

.next {
  right: 0;
  z-index: 11;
}

.prev {
  left: 0;
  z-index: 11;
}
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.507);
}

.footer {
  background: $greenCol;
  max-height: 120rem;
  padding: 4rem 0rem;
  p,
  li {
    color: $SkyCol;
  }
  h2 {
    font-size: $fontSizeTitle;
    color: $whiteCol;
    font-family: "News Cycle", sans-serif;
    letter-spacing: 0.1rem;
  }
  .company-info {
    max-height: 70rem;
    img {
      width: 4rem;
      height: 4rem;
      margin-bottom: 1rem;
    }
    .navbar-brand {
      font-size: 2rem;
      .brand-name-2 {
        font-size: 1.25rem;
      }
    }
  }
  .contact-container {
    .list {
      margin-top: 3rem;
      margin-left: 1.5rem;
      text-align: left;
      list-style-type: none;
    }
  }
  .map-container {
    .location-window {
      width: 100%;
      height: 12rem;
      .map {
        width: 100%;
        height: 100%;
        margin-top: 1rem;
        border-radius: 8%;
      }
    }
  }
}
@media (max-width: 700px) {
  .map-container,
  .contact-container,
  .company-info {
    margin-bottom: 5rem;
  }
}
.slider-img {
  aspect-ratio: 3/4;
  object-fit: cover;
  object-position: center;
}
.fw-bold {
  color: white !important;
  span {
    color: $LightgreenCol !important;
  }
}
</style>
