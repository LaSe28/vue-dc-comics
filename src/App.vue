<template>
  <div id="app">
    <HeaderDc/>
    <ContentDc/>
  </div>
</template>

<script>
import HeaderDc from './components/Header-dc.vue'
// eslint-disable-next-line
import ContentDc from './components/Main.vue'

export default {
  name: 'App',
  components: {
    HeaderDc,
    ContentDc
  }
}
</script>

<style lang="scss">
@import 'assets/styles/style.scss';
</style>
