<route lang="json5">
{
  style: {
    navigationBarTitleText: '关于',
    navigationBarBackgroundColor: '#fff',
  },
}
</route>

<script lang="ts" setup>
import RequestComp from './components/request.vue'
import UploadComp from './components/upload.vue'

// 获取屏幕边界到安全区域距离
const { safeAreaInsets } = uni.getSystemInfoSync()
</script>

<template>
  <view
    class="bg-white overflow-hidden pt-8 px-16"
    :style="{ marginTop: safeAreaInsets?.top + 'px' }"
  >
    <view class="text-center text-30 mt-32">
      鸽友们好，我是
      <text class="text-red-500">菲鸽</text>
    </view>

    <RequestComp />
    <UploadComp />
  </view>
</template>

<style lang="scss" scoped>
.test-css {
  // mt-4=>1rem=>16px;
  margin-top: 16px;
}
</style>
