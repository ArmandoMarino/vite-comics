<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';

export default {
  name: 'vite-comics',
  data() {
    return {
      title: '',
    }
  },
  components: {
    AppHeader,
    AppJumbo
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>