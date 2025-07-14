<template>
  <view class="container">
    <!-- Basic Tags -->
    <view class="section">
      <text class="section-title">Basic Tags</text>
      <view class="tag-row">
        <uni-tag text="New" type="primary" />
        <uni-tag text="Success" type="success" />
        <uni-tag text="Warning" type="warning" />
        <uni-tag text="Error" type="error" />
      </view>
    </view>

    <!-- Sizes -->
    <view class="section">
      <text class="section-title">Tag Sizes</text>
      <view class="tag-row">
        <uni-tag text="Small" size="small" type="primary" />
        <uni-tag text="Default" type="primary" />
        <uni-tag text="Large" size="large" type="primary" />
      </view>
    </view>

    <!-- Custom Tags -->
    <view class="section">
      <text class="section-title">Custom Tags</text>
      <view class="tag-row">
        <uni-tag 
          text="Premium" 
          custom-style="background: linear-gradient(135deg, #f6d365 0%, #fda085 100%); color: #fff; font-weight: bold;" 
        />
        <uni-tag 
          text="Limited" 
          custom-style="background: #9b59b6; color: white; border: none;" 
        />
        <uni-tag 
          text="50% OFF" 
          custom-style="background: #e74c3c; color: white; border-radius: 15px;" 
        />
      </view>
    </view>

    <!-- Interactive Tags -->
    <view class="section">
      <text class="section-title">Interactive Tags</text>
      <view class="tag-row">
        <uni-tag 
          :text="isSelected ? 'Selected' : 'Select'" 
          :type="isSelected ? 'success' : 'default'" 
          @click="toggleSelection"
          class="clickable-tag"
        />
        <uni-tag 
          :text="`Likes: ${likeCount}`" 
          :inverted="isLiked"
          type="error" 
          @click="addLike"
          class="clickable-tag"
        />
      </view>
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue'

const isSelected = ref(false)
const isLiked = ref(false)
const likeCount = ref(42)

const toggleSelection = () => {
  isSelected.value = !isSelected.value
}

const addLike = () => {
  isLiked.value = !isLiked.value
  likeCount.value += isLiked.value ? 1 : -1
}
</script>

<style>
.container {
  padding: 20px;
}

.section {
  margin-bottom: 30px;
}

.section-title {
  font-size: 16px;
  font-weight: bold;
  color: #333;
  margin-bottom: 15px;
  display: block;
}

.tag-row {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  align-items: center;
}

.clickable-tag {
  cursor: pointer;
  transition: transform 0.2s;
}

.clickable-tag:active {
  transform: scale(0.95);
}
</style>