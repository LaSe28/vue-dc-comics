<template>
<div class="card">
  <div class="thumb">
    <img :src="img" alt="">
  </div>
  <h4>{{ title }}</h4>
</div>
</template>

<script>
export default {
  name: 'SlideMain',
  props: {
    img: String,
    title: String
  }
}
</script>

<style scoped lang="scss">
  .card{
    position: relative;
    color: white;
    width: calc((100% / 6) - 2rem);
    margin: 2rem 1rem;
    .thumb{
      height: 160px;
      overflow: hidden;
      img{
        width: 160px;
      }
    }
  }
  h4{
    position: absolute;
    top: 170px;
  }

</style>
