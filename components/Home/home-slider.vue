<template>
  <div id="homepage-slider" class="st-slider">

    <input type="radio" class="radio" id="slide1"/>
    <input type="radio" class="radio" id="slide2"/>
    <input type="radio" class="radio" id="slide3"/>
    <input type="radio" class="radio" id="play1" checked=""/>

    <div class="images">
      <div class="images-inner">
        <div class="image-slide">
          <img class="image" src="../../public/img/aloha-crop.webp" alt="">
        </div>
        <div class="image-slide">
          <img class="image" src="../../public/img/palm-crop.webp" alt="">
        </div>
        <div class="image-slide">
          <img class="image" src="../../public/img/coco-crop.webp" alt="">
        </div>
<!--        <div class="image-slide">-->
<!--          <img class="image" src="../../public/img/ananas-crop.webp" alt="">-->
<!--        </div>-->
<!--        <div class="image-slide">-->
<!--          <img class="image" src="../../public/img/vibes-crop.webp" alt="">-->
<!--        </div>-->
<!--        <div class="image-slide">-->
<!--          <img class="image" src="../../public/img/jungle-crop.webp" alt="">-->
<!--        </div>-->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home-slider"
}
</script>

<style scoped>
.image {
  width: 468px;
  height: 495px;
  object-fit:cover;
}

.radio {
  display: none;
}

.images {
  overflow: hidden;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  width: 468px;
}

.images-inner {
  width: 500%;
  transition: all 100ms cubic-bezier(1,0,0,1);;
  transition-timing-function: cubic-bezier(1,0,0,1);;
}

.image-slide {
  width: 20%;
  float: left;
}


  /* Move slides overflowed container */
#slide1:checked ~ .images .images-inner {
  margin-left: 0;
}

#slide2:checked ~ .images .images-inner {
  margin-left: -468px;
}

#slide3:checked ~ .images .images-inner {
  margin-left: -468px;
}


/* Calculate AUTOPLAY for SLIDES */
@keyframes slide {
  0%, 25.203252032520325% {
    margin-left: 0;
  }
  33.333333333333336%, 58.53658536585366% {
    margin-left: -100%;
  }
  66.66666666666667%, 91.869918699187% {
    margin-left: -200%;
  }
}


.st-slider > #play1:checked ~ .images .images-inner {
  animation: slide 10300ms infinite cubic-bezier(0.79,0.14,0.15,0.86);
}

/* Calculate AUTOPLAY for SLIDES - END */


</style>