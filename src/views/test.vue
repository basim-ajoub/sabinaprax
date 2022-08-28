<div class="card-area">
<!--Start Card -->

<div class="card">
  <!--Start flip Card-->
  <div class="flip-card">
    <div class="flip-card__container">
      <!--Start flip Card Front Side-->
      <div class="card-front">
        <div class="card-front__text card-front__text--disc">
          <h2 class="card-front__heading">
            {{cardtitle}}
          </h2>
          <p class="card-front__text-price">
            {{cardcategory}}
          </p>
        </div>

        <div class="card-front__bt">
          <p class="card-front__text-view">
            {{$t("View me")}}
          </p>
        </div>
      </div>
      <!--End flip Card Front Side-->
      <!--Start flip Card Back Side-->
      <div class="card-back">
        <img class="image__container" :src="image" alt="image">
      </div>
      <!--End flip Card Back Side-->
    </div>
  </div>
  <!--Start flip Card Inside Side-->
  <div class="inside-page">
    <div class="inside-page__container">
      <h3 class="inside-page__heading">
        {{cardtitle}}
      </h3>
      <p class="inside-page__text">
        {{carddescription}}
      </p>
      <a href="#" class="inside-page__btn inside-page__btn--text">{{$t("Shop Now")}}</a>
    </div>
  </div>

</div>
<!--End flip Card Inside Side-->

</div>
</template>
<script>
import SfButton from "../../atoms/SfButton/SfButton.vue";
import SfHeading from "../../atoms/SfHeading/SfHeading.vue";
import SfImage from "../../atoms/SfImage/SfImage.vue";
export default {
  name: "SfCard",
  components: {
    SfButton,
    SfHeading,
    SfImage,
  },
  //props: ["image"],
  props:{
    image:{
      type: String,
      default: "",
    },
    cardtitle:{
      type: String,
      default: "",
    },
    carddescription:{
      type: String,
      default:"",
    },
    cardcategory:{
      type:String,
      default:"",
    },
  },
};
</script>
<style lang="scss">
.card-front__heading {
  font-size: var(--spacer-base);
  margin-top: var(--spacer-2xs);
}
//Star heading for inside Page
.inside-page__heading {
  padding-bottom: 1rem;
  width: 100%;
}
//End heading for inside Page
//Start Heading with Text front below
.inside-page__heading,
.card-front__text-view {
  font-size: 1rem;
  font-weight: 784;
  margin-top: 0rem;
  color: var(--_c-dark-primary);
}
//End Heading with Text front conver
.card-front__text {
  color: var(--c-white);
  font-family: var(--font-family--text-containe);
  letter-spacing: 0.7px;
}
//Start pricing text on card front cover
.card-front__text-price {
  font-size: 1.2rem;
  margin-top: -0.2rem;
}
//End pricing text on card front cover
//Start For inside bake text
.inside-page__text {
  color: var(--_c-dark-primary);
  height: 6rem;
  overflow-x: auto;
}
//End For inside bake text
.inside-page__btn {
  background-color: transparent;
  border: 3px solid var(--_c-dark-primary);
  border-radius: 10%;
  font-size: 1.2rem;
  font-weight: 600;
  margin-top: 0;
  overflow: hidden;
  padding: 0.7rem 0.75rem;
  position: relative;
  text-decoration: none;
  transition: 0.3s ease-in-out;
  width: 80%;
  z-index: 10;
  font-family: var(--font-family--text-containe);
  &::before {
    content: "";
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    transform: scaleY(0);
    transition: 0.3s ease-in-out;
    width: 100%;
    z-index: -1;
  }
}
.inside-page__btn--text {
  border-color: var(--_c-dark-primary);
  color: var(--_c-dark-primary);
  &::before {
    background-color:var(--_c-paige-primary);
  }
}
.inside-page__btn:hover {
  color: var(--c-white);
  &:hover::before {
    transform: scaleY(1);
  }
}
//Sarte Conatiner
.card-area {
  align-items: center;
  display: flex;
  flex-wrap: nowrap;
  height: 100%;
  justify-content: space-evenly;
  padding: var(--spacer-sm);
}
//End Container
.card {
  height: 15rem;
  position: relative;
  transition: all 1s ease;
  width: 15rem;
}
//Start outer container of flip card
.flip-card {
  height: 15rem;
  perspective: 100rem;
  position: absolute;
  right: 0;
  transition: 1s ease-in-out;
  visibility: hidden;
  width: 15rem;
  z-index: 20;
}
//End outer container of flip card
//Start to cange the situation of visibilty of the flip card to visbile from hidden
.flip-card > * {
  visibility: visible;
}//End to cange the situation of visibilty of the flip card to visbile from hidden
.flip-card__container {
  height: 100%;
  position: absolute;
  right: 0;
  transform-origin: left;
  @include for-mobile{
    transform-origin: bottom;//flip bottom
  }
  transform-style: preserve-3d;//make transform to 3d form origin left
  transition: all 1s ease;
  width: 100%;
}
//Start to hide the conatin of front or back card
.card-front,.card-back {
  backface-visibility: hidden;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
//Start style front card
.card-front {
  background-color: var(--c-white);
  height: 15rem;
  width: 15rem;
}
//End style front card
.card-front__text {
  align-items: center;
  clip-path: polygon(0 0, 100% 0, 100% 90%, 57% 90%, 50% 100%, 43% 90%, 0 90%);//shape ^
  display: flex;
  flex-direction: column;
  height: 12rem;
  justify-content: center;
  padding: calc(var(--spacer-xs) + var(--spacer-2xs));
}
.card-front__text--disc {
  background: linear-gradient(to bottom,var(--_c-braun-primary),var(--_c-paige-primary));
}
.card-front__bt {
  align-items: center;
  display: flex;
  justify-content: center;
}
//Start Image ocntainer
.image__container{
  height: auto;
  height: 99%;
  object-fit: cover;
  width: 100%;
}//End Image ocntainer
//Start Inside Page
.inside-page {
  background-color: var(--c-white);
  height: 100%;
  padding: 0rem;
  position: absolute;
  right: 0;
  transition: 1s ease-in-out;
  width: 15rem;
  z-index: 1;
}
//End Inside Page
.inside-page__container {
  align-items: center;
  display: flex;
  flex-direction: column;
  height: 100%;
  text-align: center;
  width: 100%;
}
.card-back {
  background-color: var(--c-white);
  @include for-desktop{
    transform: rotateY(180deg);
  }
  @include for-mobile{
    transform: rotateX(180deg);
  }
}
//Start Card Function
.card:hover {
  box-shadow:-.1rem 1.7rem 6.6rem -3.2rem rgba(0,0,0,0.75);
  width: 30rem;//to move the next card a side
  height: 15rem;
  @include for-mobile{//for mobile to macimaize the height to filp to bottom
    width: 15rem;
    height: 30rem;
  }
}
.card:hover .flip-card__container {
  @include for-desktop{
    transform: rotateY(-180deg);//for desk top to flip left
  }
  @include for-mobile{
    transform: rotateX(-180deg);//for mobile top to flip bottom
  }
}
</style>
Footer
