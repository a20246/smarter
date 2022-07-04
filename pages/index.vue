<template>
  <div class="card-site">
    <Card v-for="item in data" :key="item.id" :info="item" />
  </div>
</template>

<script>
import Card from "~/components/Card.vue";
import axios from "axios";
export default {
  asyncData({ params }) {
    return axios
      .get(`https://event.smarter.com.tw/api/spa/bestseller/interview`)
      .then((res) => {
        res = res.data;
        if (res.status === "success") {
          return { data: res.data };
        }
      });
  },
  components: {
    Card,
  },
  data() {
    return {};
  },
  mounted() {},
};
</script>

<style scoped>
.card-site {
  margin: 5rem auto;
  width: 1029px;
  display: flex;
  justify-content: space-between;
}
</style>
