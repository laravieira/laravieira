<template>
  <div class="particles">
    <vue-particles
        class="particles-canvas"
        color="#C600CC"
        :particleOpacity="0.4"
        :particlesNumber="100"
        shapeType="circle"
        :particleSize="3"
        linesColor="#600ABF"
        :linesWidth="1"
        :lineLinked="true"
        :lineOpacity="0.4"
        :linesDistance="150"
        :moveSpeed="2"
        :hoverEffect="true"
        hoverMode="grab"
        :clickEffect="true"
        clickMode="push"
    ></vue-particles>
  </div>
</template>
<script>
export default {
  name: 'Particles',
}
//var canvas = document.getElementsByClassName("particles-js-canvas-el")[0];
//canvas.width = window.innerWidth;
//canvas.height = window.innerHeight;
</script>

<style scoped>

.particles {
  background-color: rgba(0,0,0,0);
  /*background: url("/img/background.png") no-repeat;/**/
  background: radial-gradient(circle, #110718, #190F1C);
  background-size: cover;
  position: fixed;
  z-index: -2;
  top: -10px;
  right: -10px;
  bottom: -10px;
  left: -10px;
}
.particles-canvas {
  background-color: rgba(0,0,0,0);
  position: absolute;
  z-index: -1;
  width: 100vw;
  height: 100vh;
  top: 0px;
  right: 0px;
  bottom: 0px;
  left: 0px;
  border:none;
  padding: 0px;
}
</style>
