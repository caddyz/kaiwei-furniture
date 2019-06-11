<template>
  <div class="item">
    <img class="item_image" :src="data.coverImg"/>
    <div class="title_wrap">户型： {{data.title}}</div>
    <div class="desc"> {{data.desc}}</div>
  </div>
  <!--<div class="item">
    <div class="card">
      &lt;!&ndash; banner图片 &ndash;&gt;
      <div class="img_wrap">
        <img class="item_image" :src="data.coverImg"/>
      </div>
      &lt;!&ndash; 内容区域 &ndash;&gt;
      <div class="cont_wrap">
        &lt;!&ndash; 标题 &ndash;&gt;
        <div class="title_wrap">
          <div class="title">
            {{data.title}}
          </div>
        </div>
        &lt;!&ndash; 描述 &ndash;&gt;
        <div class="desc">{{data.desc}}</div>
      </div>
    </div>
  </div>-->
</template>
<script>
  export default {
    // props: {
    //   data: {
    //     type: Object
    //   }
    // },
    data () {
      return {
        data: {
          coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
          title: '这个ces',
          desc: 'haaaaaaaaaaaaaaaaaaaaaaaaaaaaha哈啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊'
        }
      }
    }
  }
</script>
<style lang="less" scoped>
  .item{
    width: 80%;
    height: 80%;
    border-radius: 7rpx;
  }

  /* 当前 swiper-item*/
  .active_item .card{
    opacity: 1;
  }
  /* banner */
  .img_wrap{
    position: relative;
    background: #303030;
    /* 图片 */
    .item_image{
      display: block;
      width: 100%;
      height: 399rpx;
      border-radius: 7rpx 7rpx 0 0;
      z-index: 5;
      opacity: 0.7;
    }
  }

  /* 标题出处 */
  .title_wrap{
    width: 560rpx;
    height: 100rpx;
    margin: 0 auto;
    // padding-left: 130rpx;
    box-sizing: border-box;
    color: #b99c6d;
    border-bottom: 2rpx dotted #e4dcce;
    .title{
      position: relative;
      font-size: 30rpx;
      line-height: 35rpx;
      height: 70rpx;
      padding-top: 30rpx;
      overflow: hidden;
    }
  }
  // 描述
  .desc{
    width: 554rpx;
    height: 140rpx;
    margin: 0 auto;
    color:#666666;
    font-size: 24rpx;
    line-height: 28rpx;
    overflow: hidden;
    margin-top: 21rpx;
    text-align: justify;
  }
</style>
