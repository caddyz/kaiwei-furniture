<template>
  <div>
    <div class="top-search">
      <div class="definite" @click="skipSearch">
        <i-icon type="search" size="18" color="#80848f"/>
        <div>搜索户型/大小</div>
      </div>
    </div>
    <swiper :images="images" />
    <div class="nav_list">
      <div data-index="1" @click="indexRouter(e)">
        <img src="/static/img/bank.png" class="nav_icon"/>
        <div class="nav_text">报价</div>
      </div>
      <div data-index="2" @click="indexRouter(e)">
        <img src="/static/img/bookmark.png" class="nav_icon"/>
        <div class="nav_text">案例</div>
      </div>
    </div>
    <div class="partition"></div>
    <div class="index_content">
      <panel :ti="motto"/>
      <card :goods="goods"/>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'
import swiper from '@/components/swiper'
import panel from '@/components/panel'
export default {
  mpType: 'page',
  config: {
    usingComponents: {
      'i-icon': '../../static/iview/icon/index',
      'i-button': '../../static/iview/button/index'
    }
  },

  data () {
    return {
      motto: '精选案例',
      goods: [{
        id: 1,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 2,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 3,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 4,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 5,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 6,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }, {
        id: 7,
        coverImg: 'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png',
        title: '五室两厅建安费发',
        desc: 120
      }],
      images: [
        {
          url:
            'https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png'
        },
        {
          url:
            'https://img-oss.yunshanmeicai.com/goods/default/e83c8f0f-4acc-4729-bcbb-294f2b314977.jpg'
        }
      ]
    }
  },

  components: {
    card,
    swiper,
    panel
  },

  methods: {
    skipSearch () {
      const url = '/pages/counter'
      this.$router.push(url)
    },
    indexRouter (e) {
      console.log('1223')
      console.log('获取到的id：', e.currentTarget.dataset.index)
      // const index = parseInt(e.target.dataset.id)
      // switch (index) {
      //   case 1 :
      //     console.log('hh')
      //     break
      //   case 2 :
      //     console.log('222')
      //     break
      // }
    }
    // getUserInfo () {
    //   // 调用登录接口
    //   wx.login({
    //     success: () => {
    //       wx.getUserInfo({
    //         success: (res) => {
    //           this.userInfo = res.userInfo
    //         }
    //       })
    //     }
    //   })
    // },

  }
}
</script>

<style scoped lang="less">
  @import "../style/pub.css";

  .top-search{
    width: 100%;
    height: 70rpx;
    display: flex;
    display: -webkit-flex;
    align-items:center;
    justify-content:center;
  }
  .definite{
    width: 80%;
    height: 70%;
    background-color: whitesmoke;
    border-radius: 30rpx;
    display: flex;
    flex-direction: row;
    justify-content: center;
    i-icon{
      display: flex;
      align-items: center;
      color: #CDCDCD;
    }
    div {
      font-size: 24rpx;
      display: flex;
      align-items: center;
      color: #CDCDCD;
    }
  }
  .nav_list {
    margin-top: 30rpx;
    color: #404040;
    display: flex;
    font-size: 26rpx;
    justify-content: space-around;
    padding: 17rpx 50rpx;
    .nav_icon {
      height: 80rpx;
      margin: 0 auto;
      width: 80rpx;
      margin-bottom: 14rpx;
    }
    .nav_text {
      font-size: 26rpx;
      text-align: center;
    }
  }
  .index_content {
    width: 90%;
    margin: 0 auto;
  }
</style>
