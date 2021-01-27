<template>
  <div class="common-footer">
    <a-row>
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
    };
  },
};
</script>

<style lang="scss" scoped>
</style>