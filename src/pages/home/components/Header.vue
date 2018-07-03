<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont city-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color:#fff
    .header-left
      width:.64rem
      float:left
      .back-icon
        text-align:center
        font-size:0.4rem
        display :block
    .header-input
      flex:1
      height:0.64rem
      line-height:0.64rem
      margin-top:0.12rem
      margin-left:0.2rem
      background:#fff
      border-radius 0.1rem
      color:#ccc
      padding-left:0.2rem
    .header-right
      min-width:1.04rem
      float:right
      text-align:center
      color: #fff
      padding: 0 .1rem
      .city-icon
        font-size:.24rem
        margin-left:-.04rem
</style>
