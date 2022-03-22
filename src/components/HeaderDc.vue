<template>
  <header class="container">
    <img src="../assets/img/dc-logo.png" alt="">
    <ul>
      <li v-for="(link, index) in links" :key="index"><a href="">{{link.text}}</a></li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'HeaderDc',
  data () {
    return {
      links: [
        {
          text: 'Characters'
        },
        {
          text: 'Comics'
        },
        {
          text: 'Movies'
        },
        {
          text: 'TV'
        },
        {
          text: 'Games'
        },
        {
          text: 'Collectibles'
        },
        {
          text: 'Videos'
        },
        {
          text: 'Fans'
        },
        {
          text: 'News'
        },
        {
          text: 'Shop'
        }
      ]
    }
  }
}
</script>
<style scoped lang="scss">
  header{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  li {
    list-style: none;
    display: inline;
    padding: 1rem;
  }
</style>
