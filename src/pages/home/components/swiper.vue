<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="list in swiperList" :key="list.id">
        <img class="swiper-img" :src="list.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      },
      swiperList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/ftejia/1810/b6/8c85590caf3462.jpg'
      }, {
        id: '002',
        imgUrl: 'https://img1.qunarzz.com/vc/c7/96/36/99702a2268e46d72c419fd7e5f.jpg_624x355x92.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper>>>.swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow:hidden;
    width:100%;
    height:0
    padding-bottom:54.487%
    .swiper-img
      width:100%

</style>
