<template>
  <div class="category">
    <div class="category-menu">About me</div>
    <div class="category-menu">Skill</div>
    <div class="category-menu">Project</div>
    <div class="category-menu">Archiving</div>
  </div>
</template>

<script>
export default {
  name: "MainCategory",
};
</script>

<style>
.category {
  width: 100vw;
  color: white;
  /* background-color: navy; */
  position: fixed;
  display: flex;
  justify-content: space-around;
  padding: 20px 0;
}

.category-menu {
  width: 25%;
  font-size: 2rem;
  cursor: pointer;
  text-align: center;
}

.category-menu:hover {
  font-size: 2.1rem;
  text-shadow: 2px 2px 5px rgba(255, 255, 255, 1);
}
</style>
