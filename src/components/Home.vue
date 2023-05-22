<script>
import gsap from "gsap";
import Draggable from "gsap/Draggable";

export default {
  mounted() {
    Draggable.create(".rectangle", {
      type: "x,y",
      edgeResistance: 0.65,
      bounds: "#shape",
      inertia: true,
    });
  },
};
</script>

<template>
  <div class="home">
    <h1>The<br />Blueprint<br />Architect's<br />Studio</h1>
    <div class="shapes" id="shape">
      <div class="rectangle"></div>
      <div class="star"></div>
      <div class="ellipse"></div>
      <div class="cube"></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=MuseoModerno:wght@800&display=swap");
* {
  font-family: "MuseoModerno", cursive;
  overflow-y: hidden;
}

.home {
  height: 100vh;
  background-color: #82d75d;

  .shapes {
    .rectangle {
      position: absolute;
      top: 0;
      left: 0;
      width: 300px;
      height: 350px;
      border: #0449a6 3px solid;
      border-bottom-left-radius: 80px;
      backdrop-filter: blur(10px);
      rotate: -45deg;
      clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
    }
  }

  h1 {
    font-size: 240px;
    color: #0449a6;
    line-height: 1;
  }
}
</style>
