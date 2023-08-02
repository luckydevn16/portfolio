<template>
  <div class="intro-animation-wrapper delay-3">
    <div id="stage">
      <div id="shape" class="cube backfaces">
        <div class="plane one">
          <img src="../assets/img/technologies/react.png" alt="react">
        </div>
        <div class="plane two">
          <img src="../assets/img/technologies/html-5.png" alt="html">
        </div>
        <div class="plane three">
          <img src="../assets/img/technologies/css.png" alt="css">
        </div>
        <div class="plane four">
          <img src="../assets/img/technologies/javascript.png" alt="javascript">
        </div>
        <div class="plane five">
          <img src="../assets/img/technologies/vue.png" alt="vue">
        </div>
        <div class="plane six">
          <img src="../assets/img/technologies/jquery.png" alt="jquery">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IntroAnimation'
}
</script>

<style>
.intro-animation-wrapper {
  background-repeat: no-repeat;
  width: 100%;
  perspective: 800;
  -webkit-perspective: 800;
  perspective-origin: 50% 225px;
  -webkit-perspective-origin: 50% 225px;
  min-height: 26rem;
  overflow: visible;
}

#stage {
  width: 100%;
  height: 2rem;
  transition: transform 2s;
  -webkit-transition: -webkit-transform 2s;
  transform-style: preserve-3d;
  -webkit-transform-style: preserve-3d;
}

#shape {
  position: relative;
  top: 5rem;
  margin: 0 auto;
  height: 12.5rem;
  width: 12.5rem;
  transform-style: preserve-3d;
  -webkit-transform-style: preserve-3d;
}

.plane {
  position: absolute;
  height: 12.5rem;
  width: 12.5rem;
  border: 2px solid #2196F3;
  border-radius: 12px;
  -webkit-border-radius: 12px;
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  color: black;
  background-color: rgba(0, 0, 0, 0.99);
  transition: transform 2s, opacity 2s;
  -webkit-transition: -webkit-transform 2s, opacity 2s;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  display: grid;
  place-items: center center;
}

.plane img {
  width: 60%;
  height: auto;
}

#shape.backfaces .plane {
  backface-visibility: hidden;
  -webkit-backface-visibility: visible;
}

#shape {
  animation: spin 24s linear infinite;
  -webkit-animation: spin 24s linear infinite;
}

@keyframes spin {
  from {
    transform: rotateY(0);
    -webkit-transform: rotateY(0);
  }

  to {
    transform: rotateY(-360deg);
    -webkit-transform: rotateY(-360deg);
  }
}


/* ---------- cube styles ------------- */

.cube>.one {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) rotateX(90deg) translateZ(100px);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) rotateX(90deg) translateZ(100px);
}

.cube>.two {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) translateZ(100px);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) translateZ(100px);
}

.cube>.three {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) rotateY(90deg) translateZ(100px);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) rotateY(90deg) translateZ(100px);
}

.cube>.four {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) rotateY(180deg) translateZ(100px);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) rotateY(180deg) translateZ(100px);
}

.cube>.five {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) rotateY(-90deg) translateZ(100px);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) rotateY(-90deg) translateZ(100px);
}

.cube>.six {
  opacity: 0.5;
  transform: scale3d(1.2, 1.2, 1.2) rotateX(-90deg) translateZ(100px) rotate(180deg);
  -webkit-transform: scale3d(1.2, 1.2, 1.2) rotateX(-90deg) translateZ(100px) rotate(180deg);
}


/* ---------- ring styles ------------- */

.ring>.one {
  transform: translateZ(380px);
  -webkit-transform: translateZ(380px);
}

.ring>.two {
  transform: rotateY(30deg) translateZ(380px);
  -webkit-transform: rotateY(30deg) translateZ(380px);
}

.ring>.three {
  transform: rotateY(60deg) translateZ(380px);
  -webkit-transform: rotateY(60deg) translateZ(380px);
}

.ring>.four {
  transform: rotateY(90deg) translateZ(380px);
  -webkit-transform: rotateY(90deg) translateZ(380px);
}

.ring>.five {
  transform: rotateY(120deg) translateZ(380px);
  -webkit-transform: rotateY(120deg) translateZ(380px);
}

.ring>.six {
  transform: rotateY(150deg) translateZ(380px);
  -webkit-transform: rotateY(150deg) translateZ(380px);
}

@media (max-width: 400px) {
  .intro-animation-wrapper {
    min-height: 55vh;
  }
}
</style>