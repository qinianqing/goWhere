<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-image" :src="item.imageUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {pagination: '.swiper-pagination', loop: true},
      swiperList: [
        {
          id: '0001',
          imageUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/0645bd625b46216a55e3835d0f677ce2.jpg_750x200_1e9a0cbf.jpg'
        },
        {
          id: '0002',
          imageUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/fd8b0bd3839c89f319efae4271d5eecb.jpg_750x200_98b9a5fb.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: white;
.wrapper
  overflow: hidden;
  width: 100%;
  height: 0;
  background: #eee;
  padding-bottom: 27.25%;
  .swiper-image
    width: 100%
</style>
