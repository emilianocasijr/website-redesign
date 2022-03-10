<template>
  <div>{{ homeData[0][0] }}</div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      homeData: [],
    };
  },
  created() {
    this.getHomeData();
  },
  methods: {
    async getHomeData() {
      const serverHomeData = await axios.get(
        "https://5u3ndobng8.execute-api.us-east-1.amazonaws.com/staging/home"
      );

      this.homeData = serverHomeData.data;
      console.log(this.homeData.data[0][0]);
    },
    getHeroTitle() {
      return this.homeData.data[0][0];
    },
  },
  computed: {},
};
</script>
<style></style>
