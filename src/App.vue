<template>
  <div id="app">
    <header class="nav shadow w-full bg-black p-6 py-6 text-white">
      <div class="flex flex-row mx-auto">
        <RouterLink class="block" :to="{ name: 'home' }">
          <LogoSvg class="logo md:transform-gpu md:transition-transform md:hover:scale-110 md:hover:rotate-3" width="40" height="40" />
        </RouterLink>
      </div>
    </header>

    <div>
      <router-view/>
    </div>
  </div>
</template>

<script>
import LogoSvg from './components/svg/LogoSvg';

export default {
  components: { LogoSvg },
};
</script>

<style scoped>
.logo {
  will-change: transform;
}
</style>
