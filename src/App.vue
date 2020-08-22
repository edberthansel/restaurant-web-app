<template>
  <div>
    <Header />

    <div class="row">
      <div class="col-8">
        <LeftContent />
      </div>
      <div class="col-4">
        <RightContent />
      </div>
    </div>

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import LeftContent from "./components/LeftContent.vue";
import RightContent from "./components/RightContent.vue";

export default {
  name: "App",
  components: {
    Header,
    LeftContent,
    RightContent
  },
};
</script>
