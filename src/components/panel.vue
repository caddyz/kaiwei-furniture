<template>
  <div class="pre">
    <div class="pre-doc">{{ti}}</div>
  </div>
</template>
<script>
  export default {
    props: ['ti']
  }
</script>
<style scoped lang="less">
  .pre {
    text-align: center;
    font-size: 30rpx;
    padding: 30rpx 0rpx;
    position: relative;
  }
  .pre-doc{
    display: inline-block;
    position: relative;
    z-index: 999;
    width: 190rpx;
    background-color: white;
  }
  .pre:before {
    content: '';
    height: 1rpx;
    width: 460rpx;
    position: absolute;
    background: #dbdbdb;
    top: 50rpx;
    margin: 0 auto;
    left: 0;
    right: 0;
  }
</style>
