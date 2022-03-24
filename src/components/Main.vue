<template>
<main>
  <div class="jumbo"></div>
  <div style="background-color: #1c1c1c;">
    <div style="position: relative;" class="container slides">
      <div class="small-banner">CURRENT SERIES</div>
      <SlideMain v-for="game in games" :key="game.series" class="game"
      :img="game.thumb"
      :title="game.series"/>
    </div>
    <div style="text-align: center;">
      <button>LOAD MORE</button>
    </div>
  </div>
  <div class="menu">
    <div class="container">
      <ul>
        <li v-for="(element, index) in services" :key="index">
          <img :src="element.img">
          <a href="">{{element.text}}</a>
        </li>
      </ul>
    </div>
  </div>
</main>
</template>

<script>
import SlideMain from './SlideMain.vue'
import img1 from '../assets/img/buy-comics-digital-comics.png'
import img2 from '../assets/img/buy-comics-merchandise.png'
import img3 from '../assets/img/buy-comics-subscriptions.png'
import img4 from '../assets/img/buy-comics-shop-locator.png'
import img5 from '../assets/img/buy-dc-power-visa.svg'

export default {
  name: 'contentDc',
  components: {
    SlideMain
  },
  data () {
    return {
      services: [
        {
          text: 'Digital Comics',
          img: img1
        },
        {
          text: 'dc merchandise',
          img: img2
        },
        {
          text: 'subscription',
          img: img3
        },
        {
          text: 'comic shop locator',
          img: img4
        },
        {
          text: 'dc power visa',
          img: img5
        }
      ],
      games: [
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
          price: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
          price: '$2.99',
          series: 'Batgirl',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$3.99',
          series: 'Batman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
          price: '$3.99',
          series: 'Batman/Superman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
          price: '$4.99',
          series: 'Batman/Superman Annual',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
          price: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
          price: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
          price: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
          price: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel'
        }
      ]
    }
  }
}
</script>
<style scoped lang="scss">
  @import '../assets/styles/partials/variables';
  .jumbo{
    background: url(../assets/img/jumbotron.jpg);
    height: 500px;
    background-size: cover;
  }
  .small-banner{
    position: absolute;
    top: -25px;
    left: 0;
    height: 50px;
    width: 250px;
    line-height: 50px;
    vertical-align: middle;
    background-color: $main-blue;
    color: white;
    font-size: 1.5rem;
    text-align: center;
  }
  ul{
    display: flex;
    justify-content: space-around;
    height: 7rem;
    align-items: center;
  }
  li{
    display: flex;
    align-items: center;
    list-style: none;
    text-transform: uppercase;
    a{
      padding-top: 2rem;
      padding-bottom: 2rem;
      text-decoration: none;
      color: white;
    }
    img{
      height: 25px;
      margin: .5rem;
    }
  }
  .slides{
    display: flex;
    flex-wrap: wrap;
    padding: 3rem;
    justify-content: center;
  }
  button{
    margin: 1rem;
    padding: 0.5rem 2rem;
    border: none;
    background-color: $main-blue;
    color: white;
  }
  .menu{
    background-color: $main-blue;
  }
</style>
