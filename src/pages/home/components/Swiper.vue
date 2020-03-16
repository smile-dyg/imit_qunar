<template>
  <div class="wrapper">
    <!-- 首页轮播图显示 -->
    <swiper :options="swiperOption" ref="mySwiper" v-if=showSwiper>
      <!-- v-for循环创建 -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <!-- 轮播图下方的点 -->
      <div  class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', // 显示轮播图下方的点
        loop: true// 支持循环轮播
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//imgs.qunarzz.com/vc/24/36/10/3fc94d042ae62de380581d4c98.jpg_92.jpg'
      }, {
        id: '0002',
        imgUrl: '//imgs.qunarzz.com/vc/44/e9/86/95bc36c9e1c06ebd68bdfe222e.jpg_92.jpg'
      }]
    }
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.swiper
    },
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff !important
  .wrapper// 固定轮播图的宽高，防止在页面刚刷新时抖动
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    .swiper-img
      width 100%
</style>
