<template>
  <div class="index">
    <common-header></common-header>
    <a-row>
      <a-col :span="24">
        <div class="nav-container">
          <div class="home">宠物用品</div>
          <div class="nav-box">
            <a-menu v-model="current" mode="horizontal">
              <a-menu-item key="mailOne">
                <a-icon type="mail" />首页
              </a-menu-item>
              <a-menu-item key="mailTwo">
                <a-icon type="mail" />口粮推荐</a-menu-item
              ><a-menu-item key="mailThree">
                <a-icon type="mail" />新品宝贝</a-menu-item
              ><a-menu-item key="mailFour">
                <a-icon type="mail" />全部商品
              </a-menu-item>
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
        <div class="content-box"></div>
      </a-col>
    </a-row>
    <common-footer></common-footer>
  </div>
</template>

<script>
import CommonHeader from "../components/CommonHeader.vue";
import CommonFooter from "../components/CommonFooter.vue";
export default {
  components: { CommonHeader, CommonFooter },
  data() {
    return {
      current: ["mailOne"],
    };
  },
};
</script>

<style lang="scss" scoped>
.index {
  margin-top: 36px;
  margin-bottom: 415px;
  // .ant-col {
  // background-color: #ccc;
  // }

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
  .content-box {
    height: 2000px;
    background: url("../assets/images/bg.jpg") repeat top, transparent;
  }
}
</style>