<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
               <div>
                   <img class="item-img" :src="item.imgUrl">
               </div>
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
        name: 'HomenRecommend',
        data () {
            return {
            recommendList: [{
             id: '001',
             imgUrl: 'https://imgs.qunarzz.com/p/p90/201308/23/5ce590745204c90193835fbb.jpg_144x96_2284a337.jpg',
             title: '海洋世界',
             desc: '主题公园'
          },{
             id: '002',
             imgUrl: 'https://imgs.qunarzz.com/p/p90/201308/23/5ce590745204c90193835fbb.jpg_144x96_2284a337.jpg',
             title: '海洋世界',
             desc: '主题公园'
          },{
             id: '003',
             imgUrl: 'https://imgs.qunarzz.com/p/p90/201308/23/5ce590745204c90193835fbb.jpg_144x96_2284a337.jpg',
             title: '海洋世界',
             desc: '主题公园'
          }]
            }
        }
    }
</script>

<style lang="stylus" scoped>
  .title
    margin-top: .5rem
    line-height: 1.8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 8rem
    .item-img
      width: 6rem
      height: 6rem
      padding: .3rem
    .item-info
      flex: 1
      padding: .3rem
      .item-title
        line-height: 2rem
        font-size: 1rem
      .item-desc
        line-height: 1.5rem
        color: #ccc
      .item-button
        line-height: 1.5rem
        margin-top: .3rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .1rem
        color: #fff
</style>