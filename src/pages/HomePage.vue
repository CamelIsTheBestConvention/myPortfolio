<template>
  <div>
    <MainCategory />
    <MainText />
  </div>
</template>

<script>
import MainCategory from "../components/MainCategory";
import MainText from "../components/MainText.vue";

export default {
  name: "HomePage",
  components: {
    MainCategory,
    MainText,
  },
};
</script>

<style></style>
