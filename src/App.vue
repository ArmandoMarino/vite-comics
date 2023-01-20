<script>
import AppHeader from './components/AppHeader.vue';
export default {
  name: 'vite-comics',
  data() {
    return {
      title: '',
    }
  },
  components: {
    AppHeader
  }
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>