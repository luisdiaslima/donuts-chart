<template>
  <div class="graphic">
    <div class="graphic__background-line" />

    <div class="graphic__lines">
      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>dom</h2>
      </div>

      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>seg</h2>
      </div>

      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>ter</h2>
      </div>

      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>qua</h2>
      </div>

      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>qui</h2>
      </div>

      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>sex</h2>
      </div>
  
      <div class="graphic__lines__line">
        <span :style="{ height: randomNumber() }" />
        <h2>sab</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
const randomNumber = (() => {
  return Math.floor(Math.random() * 101) + '%'
})
</script>

<style lang="scss" scoped>
@import "./styles.scss";
</style>