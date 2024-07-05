<template>
  <div class="main-text">
    <h1 class="text"></h1>
    <span class="blink"></span>
  </div>
</template>

<script>
export default {
  name: "MainText",

  mounted() {
    const content = "안녕하세요 프론트엔드 개발자 \n 문성준입니다.";
    const text = document.querySelector(".text");
    let i = 0;

    function typing() {
      if (text) {
        let txt = content[i++];
        text.innerHTML += txt === "\n" ? "<br/>" : txt;
        if (i > content.length) {
          text.textContent = "";
          i = 0;
        }
      }
    }
    setInterval(typing, 200);
  },
};
</script>

<style></style>
