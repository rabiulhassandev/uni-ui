<template>
    <view class="content">
        <!-- Section Title -->
        <view class="section-title">Notification Badges</view>
        
        <!-- Notification Examples -->
        <view class="badge-group">
            <uni-badge size="small" :text="100" absolute="topRight" type="error" :is-dot="false">
                <button type="default" class="btn">Inbox</button>
            </uni-badge>
            
            <uni-badge size="small" :text="5" absolute="rightBottom" type="primary">
                <button type="default" class="btn">Messages</button>
            </uni-badge>
            
            <uni-badge size="small" absolute="topRight" type="success" is-dot>
                <button type="default" class="btn">New Activity</button>
            </uni-badge>
        </view>
        
        <!-- Section Title -->
        <view class="section-title">Status Indicators</view>
        
        <!-- Status Examples -->
        <view class="badge-row">
            <uni-badge text="Active" type="success" size="small"></uni-badge>
            <uni-badge text="Pending" type="warning" size="small"></uni-badge>
            <uni-badge text="Expired" type="error" size="small"></uni-badge>
            <uni-badge text="Draft" type="default" size="small"></uni-badge>
        </view>
        
        <!-- Section Title -->
        <view class="section-title">Inverted Style Badges</view>
        
        <!-- Inverted Examples -->
        <view class="badge-row">
            <uni-badge text="VIP" type="primary" :inverted="true"></uni-badge>
            <uni-badge text="Pro" type="success" :inverted="true"></uni-badge>
            <uni-badge text="New" type="error" :inverted="true"></uni-badge>
        </view>
        
        <!-- Section Title -->
        <view class="section-title">Custom Badges</view>
        
        <!-- Custom Examples -->
        <view class="badge-row">
            <uni-badge text="Hot" custom-style="background-color: #ff6b81; color: white;"></uni-badge>
            <uni-badge text="Sale" custom-style="background-color: #ff9f43; color: white;"></uni-badge>
            <uni-badge text="50%" custom-style="background-color: #2e86de; color: white; font-weight: bold;"></uni-badge>
        </view>
    </view>
</template>

<style>
    .content {
        padding: 20px;
        display: flex;
        flex-direction: column;
        gap: 25px;
    }
    
    .section-title {
        font-size: 16px;
        font-weight: bold;
        color: #333;
        margin-bottom: 10px;
        padding-bottom: 5px;
        border-bottom: 1px solid #eee;
    }
    
    .badge-group, .badge-row {
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
        align-items: center;
    }
    
    .btn {
        margin: 0;
        padding: 0 15px;
    }
</style>