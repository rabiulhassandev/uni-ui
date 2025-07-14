<template>
  <view class="container">
    <!-- Text Headings -->
    <view class="section">
      <uni-text type="h1" bold>Main Title</uni-text>
      <uni-text type="h2">Section Heading</uni-text>
      <uni-text type="h3">Subheading</uni-text>
    </view>

    <!-- Text Styles -->
    <view class="section">
      <uni-text>Normal text</uni-text>
      <uni-text bold>Bold text</uni-text>
      <uni-text italic>Italic text</uni-text>
      <uni-text underline>Underlined text</uni-text>
      <uni-text selectable>Selectable text</uni-text>
    </view>

    <!-- Colored Text -->
    <view class="section">
      <uni-text color="red">Error message</uni-text>
      <uni-text color="green">Success message</uni-text>
      <uni-text color="#007AFF">Link-like text</uni-text>
      <uni-text color="#FF9500">Warning text</uni-text>
    </view>

    <!-- Text Sizes -->
    <view class="section">
      <uni-text size="12px">Small text (12px)</uni-text>
      <uni-text size="16px">Default text (16px)</uni-text>
      <uni-text size="20px">Large text (20px)</uni-text>
      <uni-text size="24px">Extra large text (24px)</uni-text>
    </view>

    <!-- Custom Text -->
    <view class="section">
      <uni-text custom-style="font-weight: bold; color: purple; text-decoration: underline;">
        Custom styled text
      </uni-text>
      <uni-text custom-style="background: #f5f5f5; padding: 8px; border-radius: 4px;">
        Text with background
      </uni-text>
    </view>
  </view>
</template>

<script setup>
// No reactive state needed for these basic examples
</script>

<style>
.container {
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.section {
  display: flex;
  flex-direction: column;
  gap: 12px;
  padding: 16px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}
</style>