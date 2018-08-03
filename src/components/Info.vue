<template>
    <div v-if="show" class="info">
        <h1 class="info-title">Why was this made?</h1>
        <div class="info-container">
            <div class="info-text">
                <p>Because Paul in the Build Room is extremely lazy and doesn't like to walk back into the kitchen and check if there is coffee.</p>
                <p>But then Paul remembered a couple of computer scientists from Cambridge University had the same issue as he did back in 1991. So the scientists invented the worlds first webcam just to solve this issue.</p>
                <p>So Paul decided to do the same thing and set up a webcam so the whole office could look and see if there is a pot of joe from the comfort of their own chairs.</p>
            </div>
            <div class="yt-video">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/QB7qWQ9fn1k?start=41" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
            </div>
            <svg class="coffee-svg" viewBox="0 0 100 100">
                <path class="path1" style="opacity:0.98999999;fill:none;fill-rule:evenodd;stroke: #8c714c;stroke-width:3;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;" d="m 44.723054,16.479541 c 0.92549,1.65178 1.268192,2.795163 1.18513,4.179142 -0.08306,1.383979 -1.741801,2.64392 -1.746507,4.303892 -0.0047,1.659972 0.998004,3.118762 0.998004,3.118762"></path>
                <path class="path2" d="m 45.159681,28.081337 c 0,0 -1.002704,-1.45879 -0.998004,-3.118762 0.0047,-1.659972 1.663447,-2.919913 1.746507,-4.303892 0.08306,-1.383979 -0.25964,-2.527362 -1.18513,-4.179142" style="opacity:0.98999999;fill:none;fill-rule:evenodd;stroke: #8c714c;stroke-width:3;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;"></path>
                <path class="path-cup" style="fill:none;fill-fill-rule:evenodd;stroke: #8c714c;stroke-width:3;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" d="m 33.080286,47.337558 c 0,0 0.433879,12.382418 1.350852,16.734298 0.916973,4.35188 3.992016,10.978044 3.992016,10.978044"></path>
                <g id="g1590" style="fill: #8c714c">
                <path class="path-cup" d="m 70.8,43 c -1.5,-1.7 -3.6,-2.8 -5.8,-3.1 0,-1.2 0,-2.2 -0.1,-3.1 -0.1,-2.2 -1.8,-3.9 -4,-3.9 h -31.5 c -2.2,0 -4,1.7 -4,3.9 -0.3,9.5 -0.3,32.8 7,43.7 1.1,1.7 3.1,2.7 5.2,2.7 h 15.2 c 2.1,0 4,-1 5.2,-2.7 1.2,-1.8 2.3,-4.1 3.1,-6.5 h 0.7 c 4.9,0 9.1,-3.7 9.6,-8.5 l 1.8,-14.9 c 0.3,-2.8 -0.6,-5.5 -2.4,-7.6 z m -15.4,35.8 c -0.6,0.9 -1.6,1.4 -2.7,1.4 h -15.2 c -1.1,0 -2.1,-0.5 -2.7,-1.4 -7,-10.5 -6.7,-34.7 -6.5,-41.9 0,-0.5 0.5,-1 1,-1 h 31.5 c 0.6,0 1,0.4 1,1 0.4,7.2 0.6,31.4 -6.4,41.9 z m 14.8,-28.6 -1.8,14.9 c -0.4,3.3 -3.2,5.7 -6.4,5.9 2.5,-9 3,-20.1 3,-28 1.4,0.3 2.6,1 3.5,2.1 1.3,1.4 1.9,3.2 1.7,5.1 z" id="path1584" inkscape:connector-curvature="0" style="fill: #8c714c"></path>
                <path class="path-cup" d="m 33.1,42.8 c 0,0 0,0 0,0 0.8,0 1.5,-0.7 1.5,-1.5 0,-1.1 0,-1.7 0,-1.7 0,-0.8 -0.6,-1.5 -1.4,-1.6 -0.8,0 -1.5,0.6 -1.6,1.4 0,0 0,0.6 0,1.8 0,0.9 0.7,1.6 1.5,1.6 z" id="path1588" inkscape:connector-curvature="0" style="fill: #8c714c"></path>
                </g>
            </svg>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Info',
  data(){
    return {
      show: false
    }
  },
  created() {
      setTimeout(()=>{
        this.show = true;
      }, 2000)
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
    .info {
        background: #291c12;
        display: block;
        position: relative;
        margin-top: 11vh;
        padding-top: 4vh;
        padding-bottom: 2vh;
        animation: grow 3s ease;
        height: 120vh;
        overflow: hidden;
    }
    .info-title {
        text-align: center;
        animation: fadeIn 1s ease;
        font-size: 4em;
    }
    .info-container {
        color: #291c12;
        background: #bf9c6b;
        padding: 5vh;
        margin: 1vh 30vh;
        border-radius: 15px;
        max-height: 80vh;
        overflow: hidden;
    }
    .coffee-svg {
        position: relative;
        left: -24vw;
        bottom: 57vh;
        z-index: 1;
        margin: 10em;
    }
    .info-text {
        position: relative;
        z-index: 2;
        margin-bottom: 2em;
    }
    .yt-video {
        position: relative;
        margin: 0 2em auto;
        z-index: 2;
    }

    @keyframes grow {
        0% {
            height: 20vh;
        }
        100% {
            height: 120vh;            
        }
    }

    @keyframes fadeIn {
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;            
        }
    }
</style>
