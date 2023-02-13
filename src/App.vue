<template>
  <div id="app">
    <!--Developer Basim Ajoub-->
    <nav class="navbar navbar-expand-lg" id="navbar">
      <div class="container nav-container">
        <div class="container-fluid row">
          <div class="logo-container col-md-12 col-lg-5 col-sm-12">
            <div class="row col-lg-6 col-md-12 col-sm-12">
              <div class="logo-name row col-lg-12 col-md-10 col-sm-10">
                <!--<img class="img-logo col-5" src="" alt="" />-->
                <a class="navbar-brand col-lg-12 col-sm-12 col-md-12" href="#">
                  <span class="brand-name-1">SABINE HAHM</span><br />
                  <span class="brand-name-2"
                    >Physiotherapeutin und Heilpraktikerin</span
                  >
                </a>
              </div>
              <button
                class="navbar-toggler btn-outline-success col-md-2 col-sm-2"
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
          <div class="navbar-collapse collapse col-lg-7" id="nav-btn">
            <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link" href="#about-me">Über mich</a>
              </li>
              <li class="nav-item">
                <div class="dropdown">
                  <a
                    class="btn dropdown-toggle"
                    href="#"
                    role="button"
                    id="dropdownMenuButton"
                    data-toggle="dropdown"
                    @click="dropdownButton()"
                  >
                    Leistungen
                  </a>
                  <div class="dropdown-menu" id="dropdownMenuLink">
                    <a class="dropdown-item" href="#massagen">Massagen</a>
                    <a class="dropdown-item" href="#therapie"
                      >Manuelle Therapie</a
                    >
                    <a class="dropdown-item" href="#kinesiologisches">
                      Kinesiologisches Taping
                    </a>
                    <a class="dropdown-item" href="#lymphdrainage"
                      >Manuelle Lymphdrainage</a
                    >
                    <a class="dropdown-item" href="#schröpfen">Schröpfen</a>
                    <a class="dropdown-item" href="#ernährung"
                      >Ernährung nach fünf Elementen</a
                    >
                    <a class="dropdown-item" href="#akupunktur">Akupunktur</a>
                    <a class="dropdown-item" href="#moxibution">Moxibution</a>
                    <a class="dropdown-item" href="#arzneimittel"
                      >Chinesische Kräutertherapie</a
                    >
                    <a class="dropdown-item" href="#chinesische">
                      TUINA - Chinesische Heilmassage
                    </a>
                    <a class="dropdown-item" href="#gutscheine">
                      Geschenk-Gutscheine
                    </a>
                    <a
                      class="dropdown-item"
                      href="https://pdfhost.io/v/UrAK6a0~v_Preise_PDF"
                      target="_blank"
                      >Preise</a
                    >
                  </div>
                </div>
              </li>
              <li class="nav-item">
                <div class="dropdown">
                  <a
                    class="btn dropdown-toggle"
                    href="#"
                    role="button"
                    @click="dropdownKurseButton()"
                  >
                    Kurse
                  </a>
                  <div class="dropdown-menu" id="dropdownKurseLink">
                    <a
                      class="dropdown-item"
                      href="https://www.docdroid.net/sACDlOy/pmr-kurs-docx"
                      target="_blank"
                      >PMR</a
                    >
                    <a
                      class="dropdown-item"
                      href="https://www.docdroid.net/dYHX8pO/nordicwalking-kurs-docx"
                      target="_blank"
                      >Nordic Walking</a
                    >
                    <a
                      class="dropdown-item"
                      href="https://www.docdroid.net/SM2ZgFY/qigong-kurse-docx"
                      target="_blank"
                      >Qigong</a
                    >
                    <a
                      class="dropdown-item"
                      href="https://www.docdroid.net/6OwEQPE/vortrage-ernahrung-und-tcm-docx"
                      target="_blank"
                      >Vorträge</a
                    >
                  </div>
                </div>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#galarie">Galerie </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#footer">kontakt</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#open-time-map">Öffnungszeiten</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
    <div id="slider" class="slider">
      <div class="overlay"></div>
      <div class="img-container" tag="div">
        <div v-for="i in [currentIndex]" :key="i">
          <img id="slider-img" class="slider-img" :src="currentImg" />
          <h1 class="title-text">{{ currentTitle }}</h1>
        </div>
      </div>
      <a class="prev" @click="prev" href="#">&#10094; </a>
      <a class="next" @click="next" href="#">&#10095; </a>
    </div>
    <!--Start Container-->
    <router-view />
    <!--End Container-->

    <div id="footer" class="footer">
      <div class="container">
        <div class="row footer-row">
          <div class="footer-company-logo col-md-6 col-lg-6 col-sm-12">
            <div class="company-info text-start">
              <h2>
                <a class="navbar-brand" href="#">
                  <span class="brand-name-1">Sabine Hahm</span><br />
                  <span class="brand-name-2"
                    >Physiotherapeutin und Heilpraktikerin</span
                  >
                </a>
              </h2>
              <p>Das Herz im Himmel, den Himmel im Herzen.</p>
            </div>
          </div>

          <div class="footer-contact col-md-6 col-lg-6 col-sm-12">
            <div class="contact-container">
              <h2>Kontakt</h2>
              <p class="line"></p>
              <ul class="list">
                <li class="fw-bold">
                  Email:
                  <span class="fw-normal">
                    <a href="mailto: infos@kp-tcm-hahm.de" target="_blank"
                      >infos@kp-tcm-hahm.de</a
                    ></span
                  >
                </li>
                <li class="fw-bold">
                  Adresse:
                  <span class="fw-normal">
                    Alte Feldmark 11a, 14532 Stahnsdorf</span
                  >
                </li>
                <li class="fw-bold">
                  Telefonnummer:
                  <span class="fw-normal"
                    ><a href="tel:+4915773584878">+49 (0) 15 773 584 878</a>
                  </span>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-sm-12 col-md-12 col-lg-12 rights">
            <a
              href="https://www.disclaimer.de/disclaimer.htm?farbe=FFFFFF/000000/000000/000000"
              target="_blank"
              class="disclaimer"
              >Disclaimer
            </a>
            <p class="text-white">©2022 SABINE HAHM All Rights Reserved</p>
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
      images: ["slider-1.png", "slider-2.png", "slider-3.png", "slider-4.png"],
      title: [
        "Komplementäre Physiotherapie",
        "Traditionelle Chinesische Medizin",
        "NordicWalking",
        "QiGong",
      ],
      timer: null,
      currentIndex: 0,
    };
  },
  methods: {
    startSlide: function () {
      setInterval(this.next, 5000);
    },
    next: function () {
      this.currentIndex += 1;
    },
    prev: function () {
      this.currentIndex -= 1;
    },
    dropdownButton: function () {
      let $dropdownMenu = document.getElementById("dropdownMenuLink");
      let $dropdownKurse = document.getElementById("dropdownKurseLink");
      // eslint-disable-next-line no-empty
      if ($dropdownMenu.style.display === "block") {
        $dropdownMenu.style.display = "none";
      } else {
        $dropdownKurse.style.display = "none";
        $dropdownMenu.style.display = "block";
      }
    },
    dropdownKurseButton: function () {
      let $dropdownMenu = document.getElementById("dropdownMenuLink");
      let $dropdownKurse = document.getElementById("dropdownKurseLink");
      // eslint-disable-next-line no-empty
      if ($dropdownKurse.style.display === "block") {
        $dropdownKurse.style.display = "none";
      } else {
        $dropdownMenu.style.display = "none";
        $dropdownKurse.style.display = "block";
      }
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
  justify-content: flex-start;
  @media (max-width: 1000px) {
    margin-bottom: 0.5rem;
  }
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
    //change background: rgba(0, 0, 0, 0.589);
  }
}
.navbar {
  padding: 30px;
  background: #6d9886;
  background: linear-gradient(to top left, $greenCol, $LightgreenCol);
  border-bottom: 2.5px solid $SkyCol;
  .dropdown {
    .dropdown-toggle {
      border: none;
    }
    .dropdown-menu {
      background: white;
      background: rgba(246, 246, 246, 0.81);
      @media (max-width: 1000px) {
        background: none;
      }
      border: none;
      a {
        padding: 0.5rem;
        color: $blueCol;
        border-bottom: 1px solid rgba(44, 62, 80, 0.27);
        margin-left: 0;
        &:hover {
          background: white;
        }
      }
    }
  }
  .nav-container {
    max-width: 100%;
    @media (max-width: 400px) {
      .logo-name{
        padding-left: 0;
        a{
        margin-left: 4px !important;
        margin-right: 0!important;
      }
      }
      .logo-container{
        padding-left: 0 !important;
      }
    }
    .container-fluid {
      width: 100%;
      justify-content: flex-start !important;
      .navbar-collapse {
        @media (max-width: 1000px) {
          margin-top: 1rem;
        }
      }
    }
  }
  .navbar-toggler {
    background: $SkyCol;
    height: 2rem;
    width: 2rem;
    margin-top: 0.5rem;
    padding: 0;
    @media (max-width: 1000px) {
      margin-left: 65%;
    }
    navbar-toggler-icon {
      font-size: 0.75rem;
    }
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
        color: black;
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
      font-size: 1rem;
      margin-left: 0.2rem;
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
  padding-bottom: 0.5rem;
  @media (max-width: 900px) {
    display: flex;
    flex-direction: column;
    padding-bottom: 0;
  }
  @media (max-width: 900px) {
    .footer-row {
      padding-left: 1rem;
      padding-right: 1rem;
    }
  }
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
  .footer-company-logo {
    display: flex;
    flex-direction: column;
    justify-content: center;
    @media (max-width: 900px) {
      order: 2;
    }
    .company-info {
      max-height: 70rem;
      p {
        color: $blueCol !important;
        font-weight: bold;
      }
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
  }
  .contact-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    @media (max-width: 900px) {
      width: 100%;
      align-items: start;
    }
    .line {
      background: $blueCol;
      width: 4.5rem;
      height: 0.19rem;
      margin-top: 0.5%;
      border-radius: 22%;
      border-top-right-radius: 100%;
      margin-left: 0.5%;
      @media (max-width: 900px) {
        margin-left: 4.5%;
      }
    }
    .list {
      margin-top: 2rem;
      text-align: left !important;
      margin-left: -2rem !important;
      list-style-type: none !important;
      li {
        text-align: left;
      }
    }
  }
  .rights {
    order: 3;
    padding-top: 3rem;
    color: white !important;
    .text-white {
      margin-top: 0.4rem;
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
  transition: ease-in-out 1s;
}
.fw-bold {
  color: white !important;
  padding-top: 0.3rem;
  padding-bottom: 0.3rem;
  span {
    margin-left: 0.2rem;
    color: $blueCol !important;
    font-weight: bold !important;
  }
  a {
    text-decoration: none;
    color: $blueCol !important;
  }
}
#carousel-inner,
#slider,
#carousel-item-1,
carousel-item-2,
#carousel-item-3 {
  transition: 0.8s ease-in-out;
}
.disclaimer {
  font-family: "News Cycle", sans-serif;
  font-weight: bolder;
  color: $blueCol;
  transition: ease-in-out 0.4s;
  &:hover {
    color: $whiteCol;
  }
}
</style>
