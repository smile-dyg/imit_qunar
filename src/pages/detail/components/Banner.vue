<template>
<div>
  <div class="banner" @click="handleBannerClick()">
      <img class="banner-img" src="https://imgs.qunarzz.com/p/tts6/1810/9d/1c7f2df203247a02.jpg_r_390x260x95_069a22f9.jpg">
      <div class="banner-info">
          <div class="banner-title">大连圣亚海洋世界</div>
          <div class="banner-number">
            <span class="iconfont banner-icon">&#xe692;</span>39
          </div>
      </div>
  </div>
  <common-gallary :imgs="imgs" v-show="showGallary" @close="handleBannerClose"></common-gallary>
</div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://imgs.qunarzz.com/p/tts6/1810/9d/1c7f2df203247a02.jpg_r_390x260x95_069a22f9.jpg',
        'https://imgs.qunarzz.com/sight/p0/1902/da/daee1d3f534baec8a3.water.jpg_710x360_36d53257.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleBannerClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
