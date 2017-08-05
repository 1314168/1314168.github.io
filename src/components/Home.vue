<template>
  <div class="home">
    <router-link to="Hello">点击测试</router-link>
    <ul>
  
      <br>
      <li>
        <a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a>
      </li>
    </ul>
  
    <view bindtap="onClickCouponItem" data-coupon-id="{{item.couponId}}" class="coupon_item_container" v-for="itrm in couponList " :key="itrm" style="background-image:url({{item.couponItemBg}})">
      <!--logo图片-->
      <!-- <image mode='aspectFill' class="coupon_logo {{item.stock > 0 ? '': 'grey'}}" src="{{item.brandIcon}}"></image>
      <!--gif图片 -->
      <!-- <image mode='aspectFill' wx:if="{{item.isFeaturedSelection}}" class="bigBrand" src="{{item.bigBrandGif}}"></image> -->
      <!--主内容容器-->
      <!-- <view class="coupon_info_container"> -->
        <!--主标题-->
        <!-- <text class="coupon_title" style="color:{{item.stock > 0 ? '': '#999999'}}">{{item.couponTitle}}</text> -->
        <!--副标题-->
        <!-- <text class="coupon_subtitle" style="color:{{item.stock > 0 ? '': '#999999'}}">{{item.couponSubTitle}}</text> -->
  
        <!-- <view class="coupon_subview"> -->
          <p class="coupon_symbol" style="color:{{item.stock > 0 ? '': '#999999'}}">{{item.buttonCode == 'freeCoupon' ? '': '¥'}}</p>
          <!--价格-->
           <!-- <text class="coupon_price" style="color:{{item.stock > 0 ? '': '#999999'}}" hidden="{{item.buttonCode == 'freeCoupon'}}">{{item.salePrice}}</text> -->
  
          <!--距离-->
          <!-- <text class="coupon_distance" style="color:{{item.stock > 0 ? '': '#999999'}}">{{item.distance}}</text>  -->

        <!-- </view> -->
  
      <!-- </view>
      <view class="coupon_btn_container">
        <text class="coupon_btn" style="color:{{item.stock > 0 ? '': '#999999'}}">{{item.buttonDesc}}</text>
      </view> -->
    </view>
  
  </div>
</template>




<script>
export default {
  name: 'home',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

.container {
  width: 100%;
  /*height: 1200rpx;*/
  /*filter: blur(5px);*/
  z-index: 1;
}

.coupon_item_container {
  display: flex;
  height: 220rpx;
  margin: 14rpx 14rpx 0rpx 14rpx;
  /*border: 2rpx solid #f00;*/
  background-repeat: round;
  align-items: center;
  position: relative;
}

.coupon_logo {
  flex: none;
  background: #d8d8d8;
  border-radius: 6rpx;
  width: 180rpx;
  height: 180rpx;
  margin: 20rpx 20rpx 20rpx 20rpx;
}

.bigBrand {
  position: absolute;
  height: 32rpx;
  width: 104rpx;
  top: 0;
  left: 0;
  float: left;
}

.coupon_info_container {
  height: 164rpx;
  width: 442rpx;
  position: relative;
}

.coupon_title {
  letter-spacing: 0;
  font-size: 30rpx;
  color: #333;
  font-weight: bold;
  display: -webkit-box;
  overflow: hidden;
  line-height: 1.4;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}

.coupon_subtitle {
  letter-spacing: 0;
  font-size: 26rpx;
  margin-top: 5rpx;
  color: #999;
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
}

.coupon_btn_container {
  font-weight: bold;
  display: flex;
  flex-direction: column;
  height: 220rpx;
  width: 68rpx;
  justify-content: center;
  align-items: center;
  margin-left: 0rpx;
}

.coupon_btn {
  font-size: 30rpx;
  color: #fff;
  width: 32rpx;
  /* height: 200rpx; */
  text-align: center;
  /* line-height: 40rpx;
  margin-top: 30rpx;
  margin-bottom: 24rpx; */
  font-weight: bold;
  line-height: 36rpx;
}

.coupon_subview {
  display: flex;
  flex-direction: row;
  letter-spacing: 0;
  position: absolute;
  bottom: 0;
  left: 0;
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
  height: 40rpx;
  width: 398rpx;
}

.coupon_symbol {
  font-weight: bold;
  font-size: 26rpx;
  color: #fd6154;
}

.coupon_price {
  font-weight: bold;
  font-size: 36rpx;
  color: #fd6154;
  margin-right: 0;
  letter-spacing: 0;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
  text-align: right;
  line-height: 40rpx;
}

.coupon_distance {
  font-size: 20rpx;
  color: #999;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
  /*padding-left: 6rpx;*/
  vertical-align: middle;
  text-align: center;
  /*position: relative;*/
  justify-content: space-between;
  align-items: center;
  float: right;
  padding-left: 9rpx;
  margin: 12rpx 0 6rpx;
}

.coupon_saleCount {
  font-size: 20rpx;
  color: #999;
  /*padding-right: 6rpx;*/
  letter-spacing: 0;
  overflow: hidden;
  text-overflow: ellipsis;
  padding-right: 9rpx;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
  text-align: right;
  border-right: 1rpx solid #999;
  vertical-align: middle;
  justify-content: space-between;
  align-items: center;
  float: right;
  margin: 16rpx 0;
  line-height: 23rpx;
  height: 23rpx;
}

.hide_line {
  border-right: 0 solid #fff;
}

.grey {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: gray;
  opacity: 0.5;
}
</style>