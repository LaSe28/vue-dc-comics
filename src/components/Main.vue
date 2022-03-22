<template>
<main>
  <div style="height: 5rem; background-color: black;"></div>
  <div class="container">
    <ul>
      <li v-for="(element, index) in services" :key="index">
        <img :src="element.img" alt="">
        <a href="">{{element.text}}</a>
      </li>
    </ul>
  </div>
</main>
</template>

<script>
export default {
  name: 'contentDc',
  data () {
    return {
      services: [
        {
          text: 'Digital Comics',
          img: '../assets/img/buy-comics-digital-comics.png'
        },
        {
          text: 'dc merchandise',
          img: '../assets/img/buy-comics-merchandise.png'
        },
        {
          text: 'subscription',
          img: '../assets/img/buy-comics-subscription.png'
        },
        {
          text: 'comic shop locator',
          img: '../assets/img/buy-comics-shop-locator.png'
        },
        {
          text: 'dc power visa',
          img: '../assets/img/buy-dc-power-visa.svg'
        }
      ]
    }
  }
}
</script>
<style scoped lang="scss">
  @import '@/assets/styles/partials/variables';
  main{
    background-color: $main-blue;
  }
  ul{
    display: flex;
    justify-content: space-around;
    height: 7rem;
    align-items: center;
  }
  li{
    list-style: none;
    display: inline-block;
    text-transform: uppercase;
    a{
      padding-top: 2rem;
      padding-bottom: 2rem;
      text-decoration: none;
      color: white;
    }
    img{
      width: 30px;
    }
  }
</style>
