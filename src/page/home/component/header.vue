<template>
    <div class="header">
       <div class="header-left">
          <svg-icon icon-class="arrow_left" ></svg-icon>
       </div>
       <div class="header-input">
           <span>
               <svg-icon icon-class="search"></svg-icon>
               输入城市/酒店/游玩主题
           </span>
       </div>
       <div>
           {{this.city}}
           <svg-icon icon-class="show_more"></svg-icon>
       </div>
    </div>
</template>

<script>
export default {
  name: 'homeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
.header
    height: 2rem
    display: flex
    line-height: 2rem
    background: #00bcd4
    color: #fff
    .header-left
      width: .64rem
      float: left
    .header-input
      flex: 1
      height: 1.5rem
      line-height: 1.5rem
      margin-top: .2rem
      margin-left: .6rem
      margin-right: .4rem
      padding-left: .6rem
      background: #fff
      border-radius: .5rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding: 0 .5rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>
