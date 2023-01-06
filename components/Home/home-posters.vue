<template>
  <div class="home-posters">
    <div class="wrapper__main">
      <div class="home__top-section">
        <div class="home-caption">
          <h2>СВЕЖИЕ</h2>
          <h2>ПОСТЕРЬI</h2>
          <h5>
            Летняя коллекция
          </h5>
          <p>Это текст. Кликните дважды,<br/>
            чтобы отредактировать и<br/>
            рассказать посетителям о себе.</p>
        </div>
        <home-slider/>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "home-posters"
}
</script>

<style lang="scss">

.home-caption {
  margin: 30px 0 0 270px;

  h5 {
    font-size: 26px;
    letter-spacing: 0.05em;
    font-family: "'Times New Roman Italic'";
    font-style: italic;
  }

  p {
    line-height: 1.7em;
  }
}

.home__top-section {
  display: grid;
  grid-template-columns: 1fr 1fr;

}

</style>
