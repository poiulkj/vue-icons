<template>
    <div>
      <home-header :city="city"></home-header>
      <home-swiper :list="swiperList"></home-swiper>
      <home-icons :list="iconList"></home-icons>
      <home-recommend></home-recommend>
      <Weekend></Weekend>
    </div>
</template>

<script>
import HomeHeader from './component/header'
import HomeSwiper from './component/swiper'
import HomeIcons from './component/icon'
import HomeRecommend from './component/recommend'
import Weekend from './component/weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    Weekend
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: []
    }
  },
  methods: {
    getHomeInfo(){
      axios.get('/api/index.json')
      .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      const rest = res.data
      console.log(rest.ret)
      console.log(rest.data.swiperList)
       if(rest.ret && rest.data){
        this.city = rest.data.city
        this.swiperList = rest.data.swiperList
        this.iconList = rest.data.iconList
       }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped>

</style>
