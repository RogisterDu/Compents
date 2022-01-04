<template>
  <view class="steps-area">
    <view v-for="(item, index) in List" :key="index" class="steps" :style="{'--linecolor':index < Step - 1?'#005bab':'#E3E3E3'}">
      <view class="serial-number">
        <view :class="['circle',index <Step?'':'actvie-circle']">{{ index + 1 }}</view>
      </view>
      <view :class="['step-title',index <Step?'':'actvie-title']">{{ item }}</view>
    </view>
  </view>
</template>

<script>
import './index.scss'
export default {
  setup(props) {
    const List = ['账号注册', '基本信息', '业务信息', '提交审核']
    return {
      List
    }
  },
  props: {
    Step: {
      type: Number,
      default: 1
    }
  }
}
</script>

<style>
</style>