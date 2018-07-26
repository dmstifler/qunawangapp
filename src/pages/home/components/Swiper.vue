<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="img-swiper" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '#0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/b6/f13f0eed40308c02.jpg_750x200_d93f5052.jpg'
      }, {
        id: '#0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/97/f282eaa627305102.jpg_750x200_bfa4f1aa.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.7%
    background: #eee
    .img-swiper
      width: 100%
</style>
