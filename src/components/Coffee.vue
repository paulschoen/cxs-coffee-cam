<template>
  <div class="coffee">
    <div class="border">
      <!-- Just need IP Address for Camera -->
      <!-- <iframe class="video" src="{{IP Address Goes Here}}" frameborder="0"></iframe> -->
      <div class="video"></div>
    </div>
    <div class="ocean">
      <div class="wave"></div>
      <div class="wave"></div>
    </div>
    <h1 class="title">ConnXus Coffee Cam</h1>
  </div>
</template>

<script>
export default {
  name: 'Coffee',
  props: {
    msg: String
  }
}
</script>

<style scoped>

.video {
  height: 61vh;
  width: 42vw;
  z-index: 50;
  display: block;
  margin: auto;
  position: relative;
}

.title {
  z-index: 50;
  position: relative;
  font-size: 4em;
}

.ocean { 
  height: 20%;
  width:100%;
  position:absolute;
  bottom:0;
  left:0;
  background: #291c12;
  animation: fillup 5s ease;
}

.wave {
  background: url(../assets/wave.svg) repeat-x; 
  position: absolute;
  top: -198px;
  width: 6400px;
  height: 198px;
  opacity: 0.5;
  animation: wave 7s cubic-bezier( 0.36, 0.45, 0.63, 0.53) infinite;
  transform: translate3d(0, 0, 0);
}

.wave:nth-of-type(2) {
  top: -160px;
  animation: wave 7s cubic-bezier( 0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
  opacity: 1;
}

@keyframes fillup {
  0% {
    bottom: -50vh;
  }
  
  100% {
    bottom: 0;
  }
}

@keyframes wave {
  0% {
    margin-left: 0;
  }
  100% {
    margin-left: -1600px;
  }
}

@keyframes swell {
  0%, 100% {
    transform: translate3d(0,-25px,0);
  }
  50% {
    transform: translate3d(0,5px,0);
  }
}
</style>
