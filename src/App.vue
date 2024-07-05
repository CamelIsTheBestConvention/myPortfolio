<template>
  <div id="app">
    <!-- uri에 따라 해당 컴포넌트가 router-view를 대신함 -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
#app {
  width: 100vw;
  height: 100vh;
  background-color: black;
  font-family: "WantedSans";
  overflow-y: scroll;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

#app::-webkit-scrollbar {
  display: none; /* Chrome, Safari, Opera*/
}

@font-face {
  font-family: "WantedSans";
  src: url("assets/fonts/EF_watermelonSalad\(ttf\).ttf") format("truetype");
  font-weight: 400;
}
</style>
