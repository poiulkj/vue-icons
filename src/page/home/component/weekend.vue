<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of weekendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
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
        name: 'Weekend',
        data () {
          return {
            weekendList:[
              {
                id: '001',
                imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/7562a402aa7261ac3725ce5e7c8bf362.jpg',
                title: '出游',
                desc: '周末去哪儿'
              },{
                id: '002',
                imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/7562a402aa7261ac3725ce5e7c8bf362.jpg',
                title: '出游',
                desc: '周末去哪儿'
              }
            ]
          }
        }
    }
</script>

<style lang="stylus" scoped>
  .title
    line-height: 1.8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .3rem
    .item-title
      line-height: 1.54rem
      font-size: .32rem
    .item-desc
      line-height: 1.4rem
      color: #ccc
</style>
