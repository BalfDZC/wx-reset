<template>
  <view>
    <view class="serch">
      <view class="serch-in">
        <icon class="search-icon" type="search" size="30rpx"></icon>搜索
      </view>
    </view>

    <swiper
  indicator-dots="true"
  autoplay="autoplay"
  interval="5000"
  duration="1000"
  indicator-color="rgba(0, 0, 0, .3)"
  indicator-active-color="#fff"
  circular
>
  <block v-for="(item,index) in imgUrls" :key="index">
    <swiper-item>
      <image :src="item" class="slide-image" mode="aspectfill"></image>
    </swiper-item>
  </block>
</swiper>
  </view>
</template>

<script>
export default {
  data() {
    return {
      imgUrls: [
        "https://lg-igjc8p1o-1256763078.cos.ap-shanghai.myqcloud.com/upload/banner1.png",
        "https://lg-igjc8p1o-1256763078.cos.ap-shanghai.myqcloud.com/upload/banner2.png",
        "https://lg-igjc8p1o-1256763078.cos.ap-shanghai.myqcloud.com/upload/banner3.png"
      ],

    };
  }
};
</script>

<style>
.serch {
  background: #eb4450;
  padding: 20rpx;
}
.serch-in {
  height: 60rpx;
  background: #fff;
  border-radius: 10rpx;
  color: #ccc;
  text-align: center;
  font-size: 30rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}
.search-icon {
  margin-right: 20rpx;
}
.slide-image{
  width: 750rpx;
  height: 340rpx;
}
swiper{
  height: 340rpx;
}
</style>
