<template>
<div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="item border-bottom"  v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img :src="item.imgUrl" alt="" class="item-img">
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: '//img1.qunarzz.com/sight/p0/1606/23/237ad24ea960b2f290.water.jpg_256x160_23b4be66.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/sight/p0/1606/23/237ad24ea960b2f290.water.jpg_256x160_23b4be66.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: '//img1.qunarzz.com/sight/p0/1606/23/237ad24ea960b2f290.water.jpg_256x160_23b4be66.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .title
      margin-top .2rem
      line-height .8rem
      background #eee
      text-indent .2rem
    .item-img-wrapper
      overflow hidden
      height 0
      padding-bottom 33.9%
      .item-img
        width 100%
    .item-info
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
</style>
