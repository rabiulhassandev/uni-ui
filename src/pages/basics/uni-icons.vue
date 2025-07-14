<template>
  <view class="container">
    <!-- Basic Icons -->
    <view class="section">
      <text class="section-title">Basic Icons</text>
      <view class="icon-row">
        <uni-icons type="contact" size="30" color="#2c3e50" />
        <uni-icons type="star" size="30" color="#f39c12" />
        <uni-icons type="heart" size="30" color="#e74c3c" />
      </view>
    </view>

    <!-- Interactive Icons -->
    <view class="section">
      <text class="section-title">Interactive Icons</text>
      <view class="icon-row">
        <uni-icons 
          :type="isLiked ? 'hand-thumbsup-fill' : 'hand-thumbsup'" 
          size="30"
          :color="isLiked ? '#2ecc71' : '#95a5a6'"
          @click="toggleLike"
          class="clickable-icon"
        />
        <uni-icons 
          :type="isFavorited ? 'star-fill' : 'star'" 
          size="30"
          :color="isFavorited ? '#f1c40f' : '#95a5a6'"
          @click="toggleFavorite"
          class="clickable-icon"
        />
      </view>
    </view>

    <!-- Icon with Badge -->
    <view class="section">
      <text class="section-title">Notification Icon</text>
      <view class="icon-with-badge">
        <uni-icons type="notification" size="30" color="#e74c3c" />
        <uni-badge text="3" type="error" size="small" absolute="topRight" />
      </view>
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue'

const isLiked = ref(false)
const isFavorited = ref(false)

const toggleLike = () => {
  isLiked.value = !isLiked.value
}

const toggleFavorite = () => {
  isFavorited.value = !isFavorited.value
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

.icon-row {
  display: flex;
  gap: 20px;
}

.icon-with-badge {
  position: relative;
  width: 30px;
}

.clickable-icon {
  cursor: pointer;
  transition: transform 0.2s;
}

.clickable-icon:active {
  transform: scale(0.9);
}
</style>