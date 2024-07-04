<template>
  <div>
    <div class="category">
      <div class="category-menu">About me</div>
      <div class="category-menu">Skill</div>
      <div class="category-menu">Project</div>
      <div class="category-menu">Archiving</div>
    </div>
    <!-- <router-link to="/about">Go to About</router-link> -->
  </div>
</template>

<script>
export default {
  name: "HomePage",
};
</script>

<style>
.category {
  width: 100vw;
  color: white;
  background-color: navy;
  position: fixed;
  display: flex;
}

.category-menu {
  font-size: 2rem;
}
</style>
