<template>
  <div id="app">
    <svg class="sky"></svg>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "App",
  mounted() {
    this.makeStars();
    window.addEventListener("resize", this.makeStars);
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.makeStars);
  },
  methods: {
    makeStars() {
      const $sky = this.$el.querySelector(".sky");

      // 브라우저 가장 큰 크기
      const maxSize = Math.max(window.innerWidth, window.innerHeight);

      // 랜덤한 X 위치 값
      const getRandomX = () => Math.random() * maxSize;

      // 랜덤한 Y 위치 값
      const getRandomY = () => Math.random() * maxSize;

      // 랜덤한 크기 (circle는 반지름이 크기)
      const randomRadius = () => Math.random() * 0.7 + 0.6;

      // 임의의 값
      const _size = Math.floor(maxSize / 2);

      const htmlDummy = new Array(_size)
        .fill()
        .map(() => {
          return `<circle class='star'
            cx=${getRandomX()}
            cy=${getRandomY()}
            r=${randomRadius()}
            className="star" />`;
        })
        .join("");

      $sky.innerHTML = htmlDummy;
    },
  },
};
</script>

<style>
#app {
  width: 100vw;
  height: 100vh;
  background: linear-gradient(to right, #111, #0e0f19);
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

.sky {
  width: 100vw;
  height: 100vw;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: moveStar 240s linear infinite;
}

/* 별 */
.sky .star {
  fill: #fff;
  stroke: none;
  stroke-width: 0;
}

/* 별 이동효과 */
@keyframes moveStar {
  from {
    transform: translate(-50%, -50%) rotate(0);
  }

  to {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
</style>
