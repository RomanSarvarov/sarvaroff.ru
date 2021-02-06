<template>
  <div class="roman relative flex-none pointer-events-none select-none">
    <img
      class="roman__picture"
      src="/images/me.png"
      alt="Роман Сарваров"
      width="300"
      height="531"
    />
  </div>
</template>

<script>
export default {
  name: 'TheRoman',
};
</script>

<style lang="scss">
.roman::before {
  content: '';
  @apply absolute left-0 bottom-0 w-full h-1/6 bg-gradient-to-t from-white;
}
</style>
