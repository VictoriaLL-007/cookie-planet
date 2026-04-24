<template>
  <view>
    <view v-for="item in list" :key="item._id" class="item" @click="read(item)">
      <image :src="item.cover" mode="widthFix"></image>
      <text>{{item.title}}</text>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          _id:1,
          title:"Twinkle Twinkle",
          cover:"/static/cover1.jpg",
          pages: [
            "https://xxx.com/1.jpg",
            "https://xxx.com/2.jpg"
          ]
        }
      ]
    }
  },
  methods: {
    read(item) {
      uni.navigateTo({
        url:`/pages/read/read?pages=${JSON.stringify(item.pages)}`
      })
    }
  }
}
</script>

<style scoped>
.item{padding:15px;display:flex;align-items:center}
image{width:100px;height:100px;border-radius:8px;margin-right:10px}
</style>