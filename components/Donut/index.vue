<template>
  <div class="skill">
    <div class="outer">
      <div class="inner">
        <div class="result">
          <span>{{ fullPercentage }}</span>
          <p>alcançada</p>
        </div>
      </div>
    </div>
    <svg
      v-if="gradient"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="200px"
      height="200px"
    >
      <defs>
        <linearGradient id="GradientColor" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="15.98%" stop-color="#CE9FFC" />
          <stop offset="82.85%" stop-color="#7367F0" />
        </linearGradient>

        <linearGradient
          id="SecondGradientColor"
          x1="0%"
          y1="0%"
          x2="100%"
          y2="0%"
        >
          <stop offset="15.98%" stop-color="#DF9780" />
          <stop offset="82.85%" stop-color="#A66DE9" />
        </linearGradient>
      </defs>
      <circle
        :style="{ stroke: 'url(' + gradient + ')' }"
        cx="100"
        cy="100"
        r="83"
        stroke-linecap="round"
      />
    </svg>
  </div>
</template>

<script setup>
const props = defineProps({
  percentage: {
    type: String,
    required: true,
  },
  type: String,
  required: true,
});
const type = ref(props.type);
const strokeOffset = 518 - 518 * (props.percentage / 100);
const gradient = type.value === "primary" ? "#GradientColor" : "#SecondGradientColor";

const fullPercentage = computed(() => {
  return `${props.percentage}%`;
});
</script>

<style lang="scss" scoped>
@import "./styles.scss";

@keyframes anim {
  100% {
    stroke-dashoffset: v-bind("strokeOffset");
  }
}
</style>