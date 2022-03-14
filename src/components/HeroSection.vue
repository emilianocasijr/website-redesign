<template>
  <div>
    <h1>
      {{ getHeroTitle }}
    </h1>
    <p class="subtitle">
      {{ getSubtitle }}
    </p>
    <div class="scroll-container">
      <div class="image-container">
        <img
          src="https://i2.lensdump.com/i/rP53Kz.md.webp"
          alt="rP53Kz.webp"
          class="hero-image"
        />
      </div>
    </div>
    <div class="hero-description">
      {{ getHeroDescription }}
    </div>
  </div>
</template>

<script>
// import axios from "axios";

export default {
  data() {
    return {};
  },

  props: ["homeData"],

  computed: {
    getHeroTitle() {
      return this.homeData[0][0];
    },

    getSubtitle() {
      return `${this.homeData[0][1]}`;
    },

    getHeroDescription() {
      return this.homeData[0][2];
    },
  },
};
</script>
<style lang="scss" scoped>
h1 {
  text-align: center;
  max-width: 600px;
  margin: 40px auto 8px auto;
  color: #e15100;
  font-family: "Inter", sans-serif;
  font-weight: 800;
  font-size: 48px;
}

.subtitle {
  text-align: center;
  color: #7e7e7e;
  font-family: "Roboto", sans-serif;
  margin-bottom: 35px;
}

.scroll-container {
  position: relative;
  margin-bottom: 50px;

  .image-container {
    max-width: 650px;
    max-height: 450px;
    background-color: #c4c4c4;
    margin: 0 auto;

    .hero-image {
      display: block;
      margin: 0 auto;
      max-height: 450px;
    }
  }
}

.hero-description {
  width: 95%;
  margin: auto;
  font-family: "Roboto", sans-serif;
}
</style>
