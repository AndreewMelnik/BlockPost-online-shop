<template>
  <div class="home-welcome">
    <div class="wrapper__main">
      <div class="welcome__cards">
        <div class="welcome__card-pic">
          <img class="welcome__card-thumb" src="../../public/img/love-img.webp" alt="love-img"/>
        </div>
        <div class="tour__card-caption">
          <div class="tour__card-caption-text">
            <h5>Новая коллекция</h5>
            <h1>ДЕКОР<br>
              ДЛЯ<br>
              ДУШИ</h1>
          </div>
        </div>
      </div>
      <div class="sale__cards">
        <div class="sale__card-pic">
          <img class="sale__card-thumb" src="../../public/img/bg1.webp" alt="love-img"/>
        </div>
        <div class="sale__card-pic">
          <img class="sale__card-thumb" src="../../public/img/bg2.webp" alt="love-img"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home-caption"
}
</script>

<style scoped>
.welcome__cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.welcome__card-thumb {
  object-fit: cover;
  object-position: 50% 50%;
  padding-top: 125px;
  width: 100%;
  height: 895px;
}

.tour__card-caption {
  background-color: rgb(213, 234, 236);
  padding-top: 125px;
}

.tour__card-caption-text {
  position: relative;
  left: 90px;
  margin: 182px 0 0 calc((100% - 490px) * 0);
}

.tour__card-caption h5 {
  line-height: 1.1em;
  font-size: 26px;
  letter-spacing: 0.05em;
  font-family: "'Times New Roman Italic'";
  font-style: italic;
}

.tour__card-caption h1 {
  line-height: 1em;
  font-size: 100px;
  font-family: "PlayfairDisplay"
}

.sale__cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin-top: 90px;
  justify-items: center

}

.sale__card-thumb {
  /*object-fit: cover;*/
  object-position: 50% 50%;
  width: 470px;
  height: 380px;
}
</style>