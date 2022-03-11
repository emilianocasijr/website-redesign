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
      <svg
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        class="svg-triangle left"
        width="100"
        height="100"
      >
        <path d="M 5,50 97.5,5 97.5,95 Z" />
      </svg>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        class="svg-triangle right"
        width="100"
        height="100"
      >
        <path d="M 95,50 5,95 5,5 z" />
      </svg>
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
  .svg-triangle {
    filter: invert(86%) sepia(0%) saturate(1265%) hue-rotate(176deg)
      brightness(92%) contrast(93%);
    position: absolute;

    &.right {
      right: 15%;
      top: 40%;
    }

    &.left {
      left: 15%;
      top: 40%;
    }
  }
}

.hero-description {
  width: 50%;
  margin: auto;
  font-family: "Roboto", sans-serif;
}
</style>
