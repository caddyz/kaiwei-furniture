<template>
  <div class="pr">
    <div class="item" v-for="(item,index) in goods" :key="index" @click="skip(item)">
      <div class="item_content">
        <div class="img_wrap">
          <img :src="item.coverImg"/>
        </div>
        <div class="title_wrap">户型：{{item.title}}</div>
        <div class="desc">大小：{{item.desc}}m²</div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    props: {
      goods: {
        type: Array
      }
    },
    methods: {
      skip (item) {
        console.log('获取id：', item.id)
      }
    }
  }
</script>
<style lang="less" scoped>
  .pr {
    display: flex;
    flex-wrap: wrap;
  }
  .item {
    width: 50%;
    height: 425rpx;
  }
  .item_content {
    height: 90%;
    width: 90%;
  }
  .img_wrap {
    width: 100%;
    height: 70%;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .title_wrap,.desc{
    height: 15%;
    width: 100%;
    font-size: 30rpx;
    overflow: hidden;
    display: flex;
    align-items: center;
  }
  .title_wrap {
    color: #b99c6d;
  }
</style>
