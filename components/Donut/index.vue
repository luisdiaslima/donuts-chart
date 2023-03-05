<template>
<div class="skill">
  <div class="outer">
    <div class="inner">
      <div class="result">
        <span>50%</span>
        <p>alcançada</p>
      </div>
    </div>
  </div>
  <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="200px" height="200px">
    <defs>
      <linearGradient id="GradientColor" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="15.98%" stop-color="#CE9FFC" />
        <stop offset="82.85%" stop-color="#7367F0" />
      </linearGradient>
    </defs>
    <circle cx="100" cy="100" r="83" stroke-linecap="round" />
  </svg>
</div>

</template>

<script>

export default {
}
</script>

<style lang="scss" scoped>
.skill {
  width: 200px;
  height: 200px;
  position: relative;
}

.outer {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 200px;
  height: 200px;
  border-radius: 50%;
  background: #464556;
}

.inner {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  background: #363447;
  display: flex;
  align-items: center;
  justify-content: center;
}

.result {
  color: #FFFFFF;
  text-align: center;

  span {
    font-size: 34px;
    font-weight: 700;
    font-size: 34px;
  }

  p {
    font-weight: 400;
    font-size: 16px;
    margin: 0;
  }
}

circle {
  fill: none;
  stroke: url(#GradientColor);
  stroke-width: 33px;
  stroke-dasharray: 518;
  stroke-dashoffset: 518;
  animation: anim 1s linear forwards;
}

svg {
  transform: rotate(270deg);
  position: absolute;
  top: 0;
  left: 0;
}

@keyframes anim {
  100% {
    stroke-dashoffset: calc(518 - 518 * 0.5);
  }
}

</style>