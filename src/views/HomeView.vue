<template>
  <div class="home" v-if="dataFetched">
    <HeroSection :homeData="heroSectionData" class="heroSection" />
  </div>
</template>

<script>
import axios from "axios";
import HeroSection from "../components/HeroSection.vue";

export default {
  components: {
    HeroSection,
  },

  data() {
    return {
      heroSectionData: [],
      dataFetched: false,
    };
  },

  beforeRouteEnter(to, from, next) {
    console.log("view level beforerouteenter");
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
// .heroSection {
//   width: 100%;
// }
</style>
