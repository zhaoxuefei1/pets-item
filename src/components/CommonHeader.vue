<template>
  <div class="common-header">
    <a-row>
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
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.common-header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: #f5f5f5;
  z-index: 9999;
  .ant-row {
    height: 36px;
    line-height: 36px;

    a {
      font-size: 12px;
      color: #666;
    }
  }
}
</style>