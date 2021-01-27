<template>
  <div class="common-footer">
    <a-row class="top-show-box">
      <a-col :span="24">
        <div class="top-box">
          <span href="#"><img :src="GFSQ" alt="" />官方授权</span>
          <a-divider type="vertical" />
          <span href="#"><img :src="ZPBZ" alt="" />正品保证</span>
          <a-divider type="vertical" />
          <span href="#"><img :src="QTWLY" alt="" />七天无理由退换</span>
          <a-divider type="vertical" />
          <span href="#"><img :src="SHBZ" alt="" />售后保障</span>
        </div>
      </a-col>
    </a-row>
    <a-row class="bottom-show-box">
      <a-col :span="13" class="bottom-show-left">
        <a-row>
          <a-col :span="6">
            <ul>
              <li v-for="(item, idx) in servePro" :key="idx">{{ item }}</li>
            </ul>
          </a-col>
          <a-col :span="6">
            <ul>
              <li v-for="(pay, idx) in payWay" :key="idx">{{ pay }}</li>
            </ul>
          </a-col>
          <a-col :span="6"
            ><ul>
              <li v-for="(bSer, idx) in businessServe" :key="idx">
                {{ bSer }}
              </li>
            </ul></a-col
          >
          <a-col :span="6"
            ><ul>
              <li v-for="(wlps, idx) in logisticsDistribution" :key="idx">
                {{ wlps }}
              </li>
            </ul></a-col
          >
        </a-row>
      </a-col>
      <a-col :span="5" class="bottom-show-right">
        <ul>
          <li class="telTitle">{{ footerMessage.telTitle }}</li>
          <li class="telNum">{{ footerMessage.telNum }}</li>
          <li class="telTime">{{ footerMessage.telTime }}</li>
          <li class="telPeople">{{ footerMessage.telPeople }}</li>
        </ul>
      </a-col>
    </a-row>
  </div>
</template>

<script>
import GFSQ from "@/assets/images/gfsq.webp";
import ZPBZ from "@/assets/images/zpbz.webp";
import QTWLY from "@/assets/images/qtwly.webp";
import SHBZ from "@/assets/images/shbz.webp";
export default {
  data() {
    return {
      GFSQ,
      ZPBZ,
      QTWLY,
      SHBZ,
      servePro: [
        "服务保障",
        "正品保证",
        "七天无理由退换",
        "退货返运费",
        "7X15小时客服服务",
      ],
      payWay: ["支付方式", "公司转账", "货到付款", "在线支付", "分期付款"],
      businessServe: [
        "商家服务",
        "商家服务",
        "培训中心",
        "广告服务",
        "服务市场",
      ],
      logisticsDistribution: [
        "物流配送",
        "免运费",
        "海外配送",
        "EMS",
        "211限时达",
      ],
      footerMessage: {
        telTitle: "全国客服热线",
        telNum: "000-0000-000",
        telTime: "上午 8:00-12：00    下午 13：00-19：00",
        telPeople: "客服中心",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.common-footer {
  // width: 100%;
  // position: fixed;
  // left: 0;
  // bottom: 0;
  // z-index: 999;
  padding: 40px 20px;
  background-color: #333333;

  .top-show-box {
    height: 100px;
    line-height: 100px;

    .top-box span {
      display: inline-block;
      width: 20%;
      font-size: 16px;
      vertical-align: middle;
      color: rgb(183, 183, 183);
    }

    img {
      vertical-align: middle;
      margin-right: 20px;
    }
  }

  .bottom-show-box {
    margin-top: 35px;

    .bottom-show-left {
      margin-left: 195px;

      li {
        text-align: left;
        font-size: 12px;
        color: rgb(102, 102, 102);
        height: 40px;
        line-height: 40px;

        &:first-child {
          font-size: 16px;
          color: rgb(183, 183, 183);
        }
      }
    }

    .bottom-show-right {
      padding-top: 20px;
      float: right;
      margin-right: 100px;
      li {
        height: 30px;
        line-height: 30px;
        color: #999;
        text-align: right;
      }

      .telTitle {
        font-size: 16px;
        font-weight: bold;
      }

      .telNum {
        color: #999;
        font-weight: bold;
      }
    }
  }
}
</style>