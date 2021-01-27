<template>
  <div class="index">
    <common-header></common-header>
    <a-row>
      <a-col :span="24"> col-24 </a-col>
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
    return {};
  },
};
</script>

<style lang="scss" scoped>
.index {
  margin-top: 36px;
  .ant-col {
    background-color: #ccc;
  }
}
</style>