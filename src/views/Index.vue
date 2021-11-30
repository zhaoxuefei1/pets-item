<template>
  <div class="index">
    <common-header></common-header>
    <div class="content-box">
      <div class="get-coupon">
        <a-row>
          <a-col
            class="coupon"
            :span="8"
            v-for="(payMessage, idx) in getCouponObj"
            :key="idx"
          >
            <img :src="getCouponBg" alt="" />
            <div class="pay-message">
              <p class="top-tips">
                <span class="way">{{ payMessage.way }}</span>
                <span class="pay-num">{{ payMessage.payNum }}</span>
              </p>
              <p class="pay-tips">{{ payMessage.payTips }}</p>
            </div>
          </a-col>
        </a-row>
      </div>
      <!-- <div class="dayily-show">
        <h2></h2>
        <ul>
          <li></li>
        </ul>
      </div> -->
    </div>
    <common-footer></common-footer>
    <div id="components-back-top-demo-custom">
      <a-back-top>
        <div class="ant-back-top-inner">123</div>
      </a-back-top>
      Scroll down to see the bottom-right
      <strong style="color: #1088e9"> green </strong>
      button.
    </div>
  </div>
</template>

<script>
import CommonHeader from "../components/CommonHeader.vue";
import CommonFooter from "../components/CommonFooter.vue";
import getCouponBg from "../assets/images/bgImg.webp";
import middleBg from "../assets/images/middleBg.webp";
export default {
  components: { CommonHeader, CommonFooter },
  data() {
    return {
      getCouponBg,
      middleBg,
      current: ["mailOne"],
      getCouponObj: [
        {
          way: "¥",
          payNum: 20,
          payTips: "满199元可用",
        },
        {
          way: "¥",
          payNum: 30,
          payTips: "满269元可用",
        },
        {
          way: "¥",
          payNum: 50,
          payTips: "满389元可用",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.index {
  margin-top: 36px;
  margin-bottom: 415px;
  .content-box {
    height: 2000px;
    background: url("../assets/images/bg.jpg") repeat top, transparent;

    .get-coupon {
      padding-top: 850px;

      .coupon {
        position: relative;

        .pay-message {
          position: absolute;
          top: 5%;
          left: 50%;
          transform: translateX(-50%);

          p {
            color: #9dd0f7;
            font-weight: bold;
          }

          .top-tips {
            margin-top: -10px;
          }

          .way {
            font-size: 43px;
          }

          .pay-num {
            font-size: 98px;
          }

          .pay-tips {
            font-size: 30px;
            margin-top: -50px;
          }
        }
      }
    }

    // .dayily-show {
    //   font-size: 20px;
    // }
  }

  #components-back-top-demo-custom .ant-back-top {
    bottom: 100px;
  }
  #components-back-top-demo-custom .ant-back-top-inner {
    height: 40px;
    width: 40px;
    line-height: 40px;
    border-radius: 4px;
    background-color: #1088e9;
    color: #fff;
    text-align: center;
    font-size: 20px;
  }
}
</style>