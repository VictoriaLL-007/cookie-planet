<template>
  <view class="home">
    <view class="menu" @click="go('/pages/books/books')">英文绘本</view>
    <view class="menu" @click="go('/pages/musics/musics')">英文儿歌</view>
    <view class="menu" @click="go('/pages/read/read')">字母启蒙</view>
    <view class="menu" @click="go('/pages/my/my')">我的中心</view>
  </view>
</template>

<script>
export default {
  methods: {
    go(url) { uni.navigateTo({ url }) }
  }
}
</script>

<style scoped>
.home{padding:20px}
.menu{background:#42b983;color:#fff;margin:10px 0;padding:20px;border-radius:12px;text-align:center}
</style>