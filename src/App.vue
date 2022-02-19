<template>
  <div class="app">
    <Instance />
  </div>
</template>

<script>
import Instance from '@/views/Instance.vue'
export default {
  name: 'App',
  components: {
    Instance,
  },
}
</script>

<style lang="scss">
.app {
  width: 100%;
  height: 100vh;
  background: url('./assets/image/program-code-black-backgrounds.jpg') no-repeat
    center center;
  position: relative;
}
</style>
