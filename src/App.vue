<template>
  <div id="app">
    <HeaderDc/>
    <ContentDc/>
    <FooterDc/>
  </div>
</template>

<script>
import HeaderDc from './components/Header-dc.vue'
import ContentDc from './components/Main.vue'
import FooterDc from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    HeaderDc,
    ContentDc,
    FooterDc
  }
}
</script>

<style lang="scss">
@import 'assets/styles/style.scss';
</style>
