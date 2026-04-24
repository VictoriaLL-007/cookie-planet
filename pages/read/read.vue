<template>
  <swiper indicator-dots circular>
    <swiper-item v-for="(img,i) in pages" :key="i">
      <image :src="img" mode="widthFix" style="width:100%"></image>
    </swiper-item>
  </swiper>
</template>

<script>
export default {
  data() {
    return { pages: [] }
  },
  onLoad(e) {
    this.pages = JSON.parse(e.pages)
  }
}
</script>