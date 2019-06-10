<template>
    <div class="wraper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" v-bind:key="item.id">
          <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"></div>
    </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list:Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        observer: true,
        observeParents: true,
        loop: true
      },
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #ccc
.swiper-img
  width: 100%
  height: 10rem
.wrapper
  width: 100%
  overflow: hidden
  height: 0
  padding-bottom: 53%
  background: #ccc
</style>
