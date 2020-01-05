<!-- eslint-disable max-len -->
<template>
  <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1000 1000">
    <path :animated="animated" fill="#000000" d=" M 943.056 45 L 901.408 117.938 L 900.51 119.49 L 876.588 161.391 L 830.51 242.089 L 747.526 387.438 L 619.367 387.438 L 619.367 507.017 L 544.721 444.7 L 544.721 312.792 L 703.287 312.792 L 744.202 242.047 L 762.127 211.028 L 762.127 211.184 L 790.895 161.479 L 815.096 119.646 L 157.496 119.646 L 157.496 178.893 L 266.757 270.631 L 327.461 321.6 L 345.619 336.822 L 486.271 454.914 L 605.912 555.364 L 611.025 559.643 L 646.288 589.219 L 646.351 589.281 L 646.352 589.281 C 654.679 596.278 659.489 606.6 659.489 617.477 L 659.489 965.148 L 598.234 913.765 L 584.843 902.71 L 584.843 902.506 L 557.781 879.777 L 458.91 796.824 L 284.394 650.392 L 284.394 444.398 L 359.04 506.915 L 359.04 615.76 L 506.864 739.798 L 584.843 805.25 L 584.843 635.428 L 562.935 617.023 L 557.853 612.74 L 438.18 512.177 L 297.561 393.987 L 279.402 378.716 L 224.028 332.16 L 95.985 224.571 C 87.658 217.575 82.85 207.255 82.85 196.378 L 82.85 81.824 C 82.85 61.486 99.337 45 119.674 45 L 943.056 45 Z " />
  </svg>
</template>

<script>
export default {
  name: 'Trademark',
  props: {
    color: String,
    animated: Boolean,
  },
};
</script>

<style scoped lang="scss">
path {
  fill: var(--primary);

  &[animated=true] {
    stroke-width: 2;
    stroke: var(--primary);
    stroke-dasharray: 12000;

    animation: svg-animation 7.4s linear;
    @keyframes svg-animation {
      0% {
        fill: transparent;
        stroke-dashoffset: 12000;
        stroke-opacity: 0;
      }
      10% {
        stroke-dashoffset: 12000;
        stroke-opacity: 0;
      }
      40% {
        stroke-opacity: 1;
      }
      65% {
        fill: transparent;
      }
      100% {
        fill: var(--primary);
        stroke-dashoffset: 0;
      }
    }
  }
}
</style>
