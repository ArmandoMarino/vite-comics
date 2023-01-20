<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'vite-comics',
  data() {
    return {
      title: '',
    }
  },
  components: {
    AppHeader,
    AppJumbo,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  <AppFooter />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>