<template>
  <div class="home">
    <!--Start Features-->

    <div id="services" class="features container">
      <h2>Services</h2>
      <p class="line"></p>
      <div class="row">
        <div class="service col-sm-5 col-lg-2">
          <i class="rounded-circle">&#10094;</i>
          <h3 class="service-title">Architekturvisualisierung</h3>
        </div>
        <div class="service col-sm-5 col-lg-2">
          <i class="rounded-circle">&#10094;</i>
          <h3 class="service-title">Innenraumvisualisierung</h3>
        </div>
        <div class="service col-sm-5 col-lg-2">
          <i class="rounded-circle">&#10094;</i>
          <h3 class="service-title">360° Panoramen</h3>
        </div>
        <div class="service col-sm-5 col-lg-2">
          <i class="rounded-circle">&#10094;</i>
          <h3 class="service-title">3D Grundrisse</h3>
        </div>
      </div>
    </div>
    <!--End Features-->

    <!--Start OverView-->

    <div id="overview" class="overview text-centir">
      <h2>OverView</h2>
      <p class="line"></p>
      <div class="container">
        <p>
          Mithilfe neuester Technologien erhalten Sie bei DAMAS für Ihr
          Neubauprojekt eine hochwertige 3D Visualisierung
        </p>
      </div>
    </div>
    <!--End OverView-->

    <!--Start Featured Work-->
    <div id="featured-work" class="featured-work">
      <h2>Featured Work</h2>
      <p class="line"></p>
      <div class="containier">
        <ul class="list row">
          <li class="col-md active">All</li>
          <li class="col-md">Berlin</li>
          <li class="col-md">Stautgart</li>
          <li class="col-md">Hamburg</li>
        </ul>
      </div>
    </div>
    <!--End Featured Work-->

    <div class="projects-sec">
      <div class="row">
        <img class="col-lg" src="project-1.jpg" alt="" />
        <img class="col-lg" src="project-2.jpg" alt="" />
        <img class="col-lg" src="project-3.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-4.jpg" alt="" />
        <img class="col-lg" src="project-5.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-9.jpg" alt="" />
        <img class="col-lg" src="project-10.jpg" alt="" />
        <img class="col-lg" src="project-11.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-7.jpg" alt="" />
        <img class="col-lg" src="project-8.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-14.jpg" alt="" />
        <img class="col-lg" src="project-13.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-17.jpg" alt="" />
        <img class="col-lg" src="project-15.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-16.jpg" alt="" />
        <img class="col-lg" src="project-12.jpg" alt="" />
        <img class="col-lg" src="project-18.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-19.jpg" alt="" />
        <img class="col-lg" src="project-20.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-21.jpg" alt="" />
        <img class="col-lg" src="project-22.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-23.jpg" alt="" />
        <img class="col-lg" src="project-24.jpg" alt="" />
        <img class="col-lg" src="project-25.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-26.jpg" alt="" />
        <img class="col-lg" src="project-27.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-28.jpg" alt="" />
        <img class="col-lg" src="project-29.jpg" alt="" />
        <img class="col-lg" src="project-30.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-31.jpg" alt="" />
        <img class="col-lg" src="project-32.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-33.jpg" alt="" />
        <img class="col-lg" src="project-34.jpg" alt="" />
        <img class="col-lg" src="project-35.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-36.jpg" alt="" />
        <img class="col-lg" src="project-37.jpg" alt="" />
        <img class="col-lg" src="project-38.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-39.jpg" alt="" />
        <img class="col-lg" src="project-40.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-41.jpg" alt="" />
        <img class="col-lg" src="project-42.jpg" alt="" />
        <img class="col-lg" src="project-43.jpg" alt="" />
      </div>
      <div class="row">
        <img class="col-lg" src="project-44.jpg" alt="" />
        <img class="col-lg" src="project-45.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: "HomeView",
  components: {},
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=News+Cycle&display=swap");
</style>
<style lang="scss">
$blueCol: #2c3e50;
$greenCol: #1b1b1b;
$LightgreenCol: #181818;
$pinkCol: #ffadad;
$whiteCol: #fdf8fa;
$SkyCol: #1cd6f4;
$fontSize: 1rem;
.home {
  max-width: 99.1%;
  text-align: center;
  h2 {
    margin-bottom: 3rem;
    font-family: "News Cycle", sans-serif;
    font-weight: bolder;
  }
  .line {
    background: $SkyCol;
    width: 4.5rem;
    height: 0.19rem;
    margin-top: -2.5%;
    border-radius: 22%;
    border-top-right-radius: 100%;
    margin-left: 47.5%;
    margin-bottom: 3rem;
  }
  .features {
    margin-top: 100px;
    max-width: 100%;
    max-height: 120rem;
  }
}
.container .row {
  justify-content: space-evenly;
}

.service {
  background: $greenCol;
  margin-bottom: 50px;
  padding: 15px;
  cursor: pointer;
  border-radius: 3%;

  i {
    background: $SkyCol;
    color: $whiteCol;

    padding: 5px 15px 5px 5px;
    font-size: 30px;
    margin-top: 70px;
  }
  h3,
  p {
    color: $whiteCol;
  }
  h3 {
    margin-top: 15px;
  }
}
.overview {
  height: 300px;
}
.featured-work {
  .list {
    list-style-type: none;
    padding: 100px 0px;
    margin-left: 0.1rem;
    margin-right: 0.1rem;
    li {
      padding: 10px;
      border: 1px solid $blueCol;
      margin-left: 10px;
      cursor: pointer;
      -webkit-transition: all 0.3s ease-in-out;

      -moz-transition: all 0.3s ease-in-out;

      -o-transition: all 0.3s ease-in-out;
    }
    li.active {
      background: $greenCol;
      color: $whiteCol;
    }
    li:hover {
      color: $whiteCol;
      background: $greenCol;
    }
  }
}

//Start Projects Section
.service-title {
  font-size: $fontSize;
}
.projects-sec {
  img {
    width: 20rem;
    height: 20rem;
    margin-bottom: 2rem;
    padding-right: 0;
    cursor: pointer;
  }
}
@media (max-width: 900px) {
  .home .line {
    margin-left: 45.5%;
  }
  .featured-work {
    .list {
      margin-left: 0.05rem;
      margin-right: 0rem;
      li {
        margin-left: 0;
      }
    }
  }
  .projects-sec {
    img {
      width: 26rem;
    }
  }
}
@media (max-width: 700px) {
  .home .line {
    margin-left: 41.5%;
  }
  .projects-sec {
    img {
      width: 100%;
    }
  }
}

//End Projects Section
</style>
