<template>
  <div id="app">
    <Particles/>
    <div class="content">
      <img alt="Vue logo" src="./assets/logo.svg">
      <Message></Message>
    </div>
    <Foot></Foot>
  </div>
</template>

<script>
import Particles from '@/components/Particles.vue';
import Message from '@/components/Message.vue';
import Foot from '@/components/Foot';

export default {
  name: 'App',
  components: {
    Particles,
    Message,
    Foot,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;300;400;500;700&display=swap');
* {
  margin: 0px;
  padding: 0px;
  position: relative;
  z-index: 0;
}

#app {
  position: relative;
  width: 100vw;
  height-min: 100vh;
  top: 0px;
  right: 0px;
  bottom: 0px;
  left: 0px;
}
.content {
  padding-top: 10%;
  margin: 0px auto 0px auto;
  width: fit-content;
  pointer-events: none;
  text-align: center;
}
.content img {
  width: 150px;
  text-align: center;
}
</style>
