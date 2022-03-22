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
  @import '@/assets/styles/partials/variables';
  header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 7rem;
  }
  li {
    padding: 1rem;
    list-style: none;
    display: inline;
    text-transform: uppercase;
    a{
      padding-bottom: 2.7rem;
      border-bottom: 5px solid transparent;
      text-decoration: none;
      color: black;
      line-height: 7rem;
      &:hover{
      border-color: $main-blue;
      color: $main-blue;
      }
    }
  }
</style>
