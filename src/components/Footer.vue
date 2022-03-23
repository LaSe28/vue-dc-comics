<template>
<footer>
  <div class="container footer-container">
    <div class="list-container">
      <ul>
        <h3>dc comics</h3>
        <li v-for="(element, index) in dcComics" :key="index">
          <a href="">{{element.text}}</a>
        </li>
      </ul>
      <ul>
        <h3>shop</h3>
        <li v-for="(element, index) in shop" :key="index">
          <a href="">{{element.text}}</a>
        </li>
      </ul>
      <ul>
        <h3>dc</h3>
        <li v-for="(element, index) in dc" :key="index">
          <a href="">{{element.text}}</a>
        </li>
      </ul>
      <ul>
        <h3>sites</h3>
        <li v-for="(element, index) in sites" :key="index">
          <a href="">{{element.text}}</a>
        </li>
      </ul>
    </div>
    <div class="image-container">
      <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
  </div>
  <div class="footer-bottom">
    <div class="container">
      <button>SIGN-UP NOW!</button>
      <div class="social">
        <h3>Follow us</h3>
        <img src="../assets/img/footer-facebook.png" alt="">
        <img src="../assets/img/footer-twitter.png" alt="">
        <img src="../assets/img/footer-youtube.png" alt="">
        <img src="../assets/img/footer-pinterest.png" alt="">
        <img src="../assets/img/footer-periscope.png" alt="">
      </div>
    </div>
  </div>
</footer>
</template>

<script>
export default {
  name: 'FooterDc',
  data () {
    return {
      dcComics: [
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
      ],
      shop: [
        {
          text: 'Shop DC'
        },
        {
          text: 'Shop DC Collectibles'
        }
      ],
      dc: [
        {
          text: 'Terms of Use'
        },
        {
          text: 'Privacy policy (New)'
        },
        {
          text: 'Ad Choises'
        },
        {
          text: 'Advertising'
        },
        {
          text: 'Jobs'
        },
        {
          text: 'Subscriptions'
        },
        {
          text: 'Talent Workshops'
        },
        {
          text: 'CPSC Certificates'
        },
        {
          text: 'Ratings'
        },
        {
          text: 'Shop Help'
        },
        {
          text: 'Contact Us'
        }
      ],
      sites: [
        {
          text: 'DC'
        },
        {
          text: 'MAD Magazine'
        },
        {
          text: 'DC Kids'
        },
        {
          text: 'DC Universe'
        },
        {
          text: 'DC Power Visa'
        }
      ]
    }
  }
}
</script>
<style scoped lang="scss">
  @import '../assets/styles/partials/variables';
  footer{
    background: url(../assets/img/footer-bg.jpg);
    .footer-container{
      display: flex;
      justify-content: space-between;
      height: 370px;
      overflow: hidden;
      .image-container{
        align-self: center;
      }
    }
    .list-container{
      height: 370px;
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      align-items: flex-start;
      padding-top: 2rem;
      padding-bottom:2rem ;
      h3{
        text-transform: uppercase;
        color: white;
        margin-top: .5rem;
        margin-bottom: .5rem;
      }
    }
    ul{
      margin-right:.5rem;
      li{
        list-style: none;
        a{
          text-decoration: none;
          color: grey;
        }
      }
    }
  }
  .footer-bottom{
    height: 6rem;
    background-color: #303030;
    button{
      padding: .5rem;
      border: 2px solid $main-blue;
      background-color:#303030;
      color: white;
    }
    .container{
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      .social{
        display: flex;
        align-items: center;
        h3{
          color: $main-blue;
          padding: 1rem;
          text-transform: uppercase;
        }
        img{
          margin: .5rem;
        }
      }
    }
  }
</style>
