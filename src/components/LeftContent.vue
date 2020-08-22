<template>
  <div>
    <Banner />
    <Categories />
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import Categories from "./Categories.vue";

export default {
  name: "left-content",
  components: {
    Banner,
    Categories
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
