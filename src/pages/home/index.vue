<template>
  <view class="content">
    <button @click="navigateToPage('basics/uni-badge')">uni-badge</button>
    <button @click="navigateToPage('basics/uni-icons')">uni-icons</button>
    <button @click="navigateToPage('basics/uni-tags')">uni-tags</button>
    <button @click="navigateToPage('basics/uni-link')">uni-link</button>
    <button @click="navigateToPage('basics/uni-text')">uni-text</button>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'

function navigateToPage(page : string) {
  uni.navigateTo({
    url: '/pages/' + page,
  })
}



</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
