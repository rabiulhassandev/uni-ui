<template>
  <view class="container">
    <!-- Basic Links -->
    <view class="section">
      <text class="section-title">Basic Links</text>
      <view class="link-group">
        <uni-link href="/pages/home/index" text="Go Home" />
        <uni-link href="/pages/about/index" text="About Page" />
      </view>
    </view>

    <!-- Styled Links -->
    <view class="section">
      <text class="section-title">Styled Links</text>
      <view class="link-group">
        <uni-link 
          href="https://uniapp.dcloud.io" 
          text="UniApp Docs" 
          color="#007AFF"
          showUnderline
          class="custom-link"
        />
        <uni-link
          href="https://github.com/dcloudio/uni-app"
          text="GitHub Repo"
          color="#333"
          :showUnderline="false"
          class="custom-link"
        />
      </view>
    </view>

    <!-- Icon Links -->
    <view class="section">
      <text class="section-title">Links with Icons</text>
      <view class="link-group">
        <uni-link href="mailto:contact@example.com" class="icon-link">
          <uni-icons type="email" size="16" color="#FF9500" />
          <text> Email Us</text>
        </uni-link>
        
        <uni-link href="tel:+1234567890" class="icon-link">
          <uni-icons type="phone" size="16" color="#34C759" />
          <text> Call Support</text>
        </uni-link>
      </view>
    </view>
  </view>
</template>

<script setup>
// No reactive state needed for these basic examples
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

.link-group {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.custom-link {
  font-size: 15px;
  font-weight: 500;
}

.icon-link {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #333;
}


/* Hover effects (will work on web, ignored on mobile) */
@media (hover: hover) {
  .icon-link:hover {
    opacity: 0.8;
  }
}
</style>