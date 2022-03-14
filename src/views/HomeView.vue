<template>
  <div class="home" v-if="dataFetched">
    <HeroSection :homeData="heroSectionData" class="heroSection" />
    <AsideMostPopular class="aside" />
  </div>
</template>

<script>
import axios from "axios";
import HeroSection from "../components/HeroSection.vue";
import AsideMostPopular from "../components/AsideHeroSection.vue";

export default {
  components: {
    HeroSection,
    AsideMostPopular,
  },

  data() {
    return {
      heroSectionData: [],
      dataFetched: false,
    };
  },

  beforeRouteEnter(to, from, next) {
    const url =
      "https://5u3ndobng8.execute-api.us-east-1.amazonaws.com/staging/home";

    axios.get(url).then((res) => {
      if (res.data.length > 0) {
        next((vm) => {
          vm.setData(res.data); // Setting a property before the component loads
        });
      }
    });
  },

  methods: {
    setData(data) {
      this.heroSectionData = data;
      this.dataFetched = true;
    },
  },
};
</script>
<style lang="scss" scoped>
.home {
  display: flex;
  margin: 0 auto;
  width: 72%;
  justify-content: space-between;

  .heroSection {
    max-width: 920px;
  }

  .aside {
    max-width: 300px;
  }
}
</style>
