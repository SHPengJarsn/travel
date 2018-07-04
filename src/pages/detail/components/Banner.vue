<template>
  <div>
    <div class="banner" @click="handleGallaryClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201405/23/0265195fc4b7913a758674357c3cc8f6.jpg_600x330_8b674516.jpg">
      <div class="banner-info">
        <div class="banner-tittle">
          北京欢乐水魔方
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe626;</span>
          11
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="closeGallary"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/201405/23/0265195fc4b7913a758674357c3cc8f6.jpg_350x240_26541a3a.jpg', 'http://img1.qunarzz.com/sight/p0/1612/4e/4ea64b1974f97db9a3.water.jpg_350x240_58c7a455.jpg'],
      showGallary: false
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleGallaryClick () {
      this.showGallary = true
    },
    closeGallary () {
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
    background: yellow
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
        background: rgba(0, 0, 0, 0.8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
