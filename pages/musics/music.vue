<template>
  <view>
    <audio :src="musicUrl" controls autoplay loop></audio>
  </view>
</template>

<script>
export default {
  data() {
    return {
      // musicUrl:"https://xxx.com/twinkle.mp3"
    }
  }
}
</script>