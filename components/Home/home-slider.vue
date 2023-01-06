<template>
  <div id="homepage-slider" class="st-slider">

    <input type="radio" class="radio" id="slide1"/>
    <input type="radio" class="radio" id="slide2"/>
    <input type="radio" class="radio" id="slide3"/>
    <input type="radio" class="radio" id="play1" checked=""/>

    <div class="images">
      <div class="images-inner">
        <div class="image-slide">
          <img class="image bg-yellow" src="../../public/img/zeeland.webp" alt="">
        </div>
        <div class="image-slide">
          <img class="image bg-blue" src="../../public/img/melon.webp" alt="">
        </div>
        <div class="image-slide">
          <img class="image bg-red" src="../../public/img/palm.webp" alt="">
        </div>
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
  width: 100%;
  height: 495px;
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
  width: 100%;
}

.images-inner {
  width: 500%;
  transition: all 800ms cubic-bezier(0.770, 0.000, 0.175, 1.000);
  transition-timing-function: cubic-bezier(0.770, 0.000, 0.175, 1.000);
}

.image-slide {
  width: 20%;
  float: left;
}

.image-slide,


  /* Move slides overflowed container */
#slide1:checked ~ .images .images-inner {
  margin-left: 0;
}

#slide2:checked ~ .images .images-inner {
  margin-left: -100%;
}

#slide3:checked ~ .images .images-inner {
  margin-left: -200%;
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
  animation: slide 12300ms infinite;
}

/* Calculate AUTOPLAY for SLIDES - END */


</style>