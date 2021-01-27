<template>
  <div class="common-header">
    <a-row class="top-nav">
      <a-col :span="12">
        <div class="left-box">
          <a href="#">首页</a>
          <a-divider type="vertical" />
          <a href="#">注册</a>
          <a-divider type="vertical" />
          <a href="#"
            ><a-icon
              type="wechat"
              theme="filled"
              :style="{ fontSize: '14px', color: '#66c650' }"
            />微信登陆</a
          >
        </div>
      </a-col>
      <a-col :span="12">
        <div class="right-box">
          <a href="#">我的资料</a>
          <a-divider type="vertical" />
          <a href="#"><a-icon type="heart" theme="filled" />收藏本站</a>
          <a-divider type="vertical" />
          <a href="#">我的订单</a>
          <a-divider type="vertical" />
          <a href="#"><a-icon type="shopping" />购物车 (0)</a>
        </div>
      </a-col>
    </a-row>
    <a-row class="bottom-nav">
      <a-col :span="24">
        <div class="nav-container">
          <div class="home">宠物用品</div>
          <div class="nav-box">
            <a-menu v-model="current" mode="horizontal">
              <a-menu-item class="nav" key="mailOne"> 首页 </a-menu-item>
              <a-menu-item class="nav" key="mailTwo"> 口粮推荐</a-menu-item
              ><a-menu-item class="nav" key="mailThree"> 新品宝贝</a-menu-item
              ><a-menu-item class="nav" key="mailFour"> 全部商品 </a-menu-item>
            </a-menu>
          </div>
          <div class="shop-box">
            <a href="#"
              ><a-icon
                :style="{
                  fontSize: '20px',
                  marginRight: '8px',
                  color: '#6091e2',
                }"
                type="shopping-cart"
              />购物车</a
            >
          </div>
        </div>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: ["mailOne"],
    };
  },
};
</script>

<style lang="scss" scoped>
.common-header {
  background-color: #fff;
  .top-nav {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    height: 36px;
    line-height: 36px;
    background-color: #f5f5f5;
    z-index: 9999;

    a {
      font-size: 12px;
      color: #666;
    }
  }
  .bottom-nav {
    .nav-container {
      position: relative;
      width: 1200px;
      margin: 0 auto;
      height: 100px;
      line-height: 100px;
      background-color: #fff;

      & > div {
        float: left;
      }

      .home {
        font-size: 22px;
        color: rgb(25, 114, 209);
        font-weight: bold;
      }

      .nav-box {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);

        .nav {
          font-size: 16px;
          color: #4d4d4d;
        }
      }

      .shop-box {
        float: right;

        a {
          display: inline-block;
          border: 1px solid #e6e6e6;
          background-color: #fff;
          height: 42px;
          line-height: 42px;
          padding: 0 40px 0 54px;
          color: #919191;
          font-size: 12px;
        }
      }
    }
  }
}
</style>