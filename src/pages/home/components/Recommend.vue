<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img :src="item.imgUrl" alt="" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Recommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/7d/7dca9c37a87479eba3.img.jpg_200x200_f62f78bd.jpg',
          title: '世茂云上厦门观光厅',
          desc: '福建省厦门市思明区大学路世茂海峡大厦B座'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg',
          title: '白水洋(AAAAA景区)',
          desc: '福建省宁德市西北部屏南县境内'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1711/fe/fe517fa5a183e4bca3.img.jpg_200x200_1afe21c0.jpg',
          title: '厦门老院子景区(AAAA景区)',
          desc: '福建省厦门市集美区华夏路9号'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/e5/e563e6454d1771c2a3.img.jpg_200x200_9c5b5a22.jpg',
          title: '厦门方特梦幻王国',
          desc: '福建省厦门市同安区石浔南路1111号'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1506/f6/f6b727f036fe5d6d.water.jpg_200x200_a3c26b4d.jpg',
          title: '鼓浪屿(AAAAA景区)',
          desc: '福建省厦门市思明区鼓浪屿'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top:.2rem
    line-height:.8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #cccccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
