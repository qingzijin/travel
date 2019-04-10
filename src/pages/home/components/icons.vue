<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(item, index) in pages" :key="index">
        <div class="icon" v-for="icon in item" :key="icon.id">
          <div class="icon-img">
            <img class="icon-img-content" src="../../../assets/images/xinjian.png" alt="">
          </div>
          <p>{{icon.text}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      icons: [
        {
          id: '001',
          imgUrl: 'src/assets/images/xinjian.png',
          text: '经典经典经典降低'
        },
        {
          id: '002',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '003',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '004',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '005',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '006',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '007',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '008',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '009',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '0010',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        },
        {
          id: '0011',
          imgUrl: '../../../assets/images/xinjian.png',
          text: '经典'
        }
      ]
    }
  },
  computed: {
    pages () {
      let pages = []
      this.icons.forEach((item, index) => {
        let page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    width: 100%
    height: 0
    padding-bottom: 50%
  .icon
    position: relative
    float:left
    width: 25%;
    height: 0;
    padding-bottom: 25%
    overflow:hidden
    .icon-img
      position: absolute;
      left: 0;
      top: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem
      .icon-img-content
        height: 100%;
        display: block;
        margin: 0 auto;
    p
      position: absolute
      bottom: 0
      left: 0
      right: 0
      text-align: center
      height:0.44rem
      line-height:0.44rem
      ellipsis()
</style>
