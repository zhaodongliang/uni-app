<!--
 * @Author: Z
 * @Date: 2020-01-13 18:13:20
 * @LastEditTime : 2020-01-13 18:28:25
 * @FilePath: \my-projectf:\project\project-uni\sjzb-app\src\pages\home\home.vue
 -->
<template>
  <div class="bigbox">
    <div class="swiper-wrap">
      <swiper
        class="swiper"
        autoplay="true"
        interval="3000"
        easing-function="easeOutCubic"
        duration="600"
        bindchange="swiperChange"
        circular="true"
      >
        <template v-for="item in movies">
          <swiper-item :key="item.moviesId">
            <image
              :src="item.adverImage"
              :class="[nowIndex==index?'swiper-change':'',slide-image]"
              data-type="{item.adverImage=='https://zhuzubao.com/group1/M00/00/1E/rBAADF37qfWAdr8IAAzxa3LSsY0558.png'?'activity':''}"
              data-wheel-id="item.skuId"
              @click="planting"
            />
          </swiper-item>
        </template>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      movies: [
        {
          id: "03D3C0E71DAB4750AAB49E1B7F822080",
          adverNo: "5588812",
          adverName: "领0元电影票",
          adverLocation: "2",
          adverImage:
            "https://zhuzubao.com/group1/M00/00/1E/rBAADF37qfWAdr8IAAzxa3LSsY0558.png",
          adverStatute: 0,
          adverClick: "0",
          adverLink: "活动时间：2019.12.20 -2020.01.15",
          adverRemark: "活动时间：2019.12.20 -2020.01.15",
          createTime: "2019-12-20 00:49:27",
          creatorId: "0E7AAE639E9549B6B335494A39C65CE9",
          modifyTime: "2019-12-20 15:50:38",
          modifierId: "0E7AAE639E9549B6B335494A39C65CE9",
          isDel: 0,
          generateOrder: null,
          upTop: "0",
          skuId: ""
        },
        {
          id: "32EC5D953383489AB52F17363CAA362A",
          adverNo: "4499073",
          adverName: "￥99元任性无限换戴",
          adverLocation: "2",
          adverImage:
            "https://zhuzubao.com/group1/M00/00/00/rBAADF4EDY-ALNynABCjRm3BmFw518.png",
          adverStatute: 0,
          adverClick: "0",
          adverLink: "100",
          adverRemark: "全场珠宝任性选",
          createTime: "2019-07-29 12:53:47",
          creatorId: "0E7AAE639E9549B6B335494A39C65CE9",
          modifyTime: "2019-12-26 09:32:08",
          modifierId: "0E7AAE639E9549B6B335494A39C65CE9",
          isDel: 0,
          generateOrder: null,
          upTop: "0",
          skuId: "BE91AD97089F48B78891C305D8B94972"
        }
      ]
    }
  }
}
</script>
<style>
.goodBox {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  background-color: #fff;
  align-items: center;
  border-bottom: 4px #fff solid;
  z-index: 99;
}

.home {
  flex: 0 0 58rpx;
  width: 70rpx;
  height: 50rpx;
  margin: 0 12rpx;
}

.home > image {
  width: 100%;
  height: 100%;
}

.titles {
  color: rgb(199, 161, 121);
  margin: 0 20rpx;
  padding-bottom: 4px;
}

.t-titles {
  margin-bottom: 4rpx;
  font-size: 16px;
}

.b-titles {
  font-size: 7px;
}
.goodsbox-warp {
  flex: 1;
  background-color: #ebebeb;
  border-radius: 40rpx;
  padding-left: 30rpx;
  font-size: 30rpx;
  color: #888;
  display: flex;
  align-items: center;
}
.goodsbox-warp .img-view {
  width: 30rpx;
  height: 30rpx;
  margin-right: 10rpx;
}
.goodsbox-warp .img-view image {
  display: block;
}
.searchs {
  color: #333;
  font-size: 15px;
  font-weight: 400;
}

.xtb {
  width: 30rpx;
  height: 30rpx;
  display: inline-block;
  position: absolute;
  top: 18rpx;
  left: 6%;
  z-index: 99;
}

.xtbimg {
  width: 100%;
  height: 100%;
  float: left;
}

/*  */

.bigbox {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  font-family: "ArialMT", "Arial";
}

.hengxiang {
  display: flex;
}

.huanhang {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-around;
}

.top-r {
  width: 95%;
  height: 100rpx;
  margin: 0 auto;
  display: flex;
}

.t-r-l {
  width: 40%;
  height: 100rpx;
  color: #333;
  font-weight: 650;
  font-size: 32rpx;
  line-height: 100rpx;
  font-family: "PingFangSC-Semibold", "PingFang SC Semibold", "PingFang SC";
}

.t-r-r {
  width: 60%;
  height: 100rpx;
  color: #333;
  font-size: 28rpx;
  font-weight: 400;
  line-height: 100rpx;
  text-align: right;
  font-family: "PingFangSC-Regular", "PingFang SC";
}

.items {
  width: 100%;
  display: flex;
  position: relative;
}

.top-item {
  width: 100%;
  height: auto;
}

.t-item {
  width: 95%;
  height: 100rpx;
  margin: 0 auto;
  display: flex;
  position: relative;
  line-height: 100rpx;
}

.i-left {
  width: 50%;
  color: #333;
  font-size: 32rpx;
  font-weight: 650;
  font-family: "PingFangSC-Semibold", "PingFang SC Semibold", "PingFang SC";
}

.i-right {
  width: 50%;
  color: #333;
  font-size: 27rpx;
  font-weight: 400;
  text-align: right;
  font-family: "PingFangSC-Regular", "PingFang SC";
}
.ad-big {
  width: 100%;
  min-height: 200rpx;
  display: flex;
  justify-content: space-between;
  border-bottom: 2rpx #eee solid;
  padding: 0 10rpx;
  box-sizing: border-box;
  margin-bottom: 10rpx;
}
.ad-big image {
  height: 200rpx;
}
.ad-mini {
  width: 100%;
  box-sizing: border-box;
  padding: 0 10rpx;
  min-height: 200rpx;
  display: flex;
  justify-content: space-between;
  border-bottom: 2rpx #eee solid;
}
.ad-big image,
.ad-mini-content image {
  width: 100%;
}
.line {
  flex: 0 0 3px;
  background-color: #fff;
}
.ad-mini-content {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.cnxh-title {
  width: 100%;
  box-sizing: border-box;
  padding: 26px 132rpx;
}
.cnxh-title-content {
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
}
.cnxh-title-content text {
  font-size: 28rpx;
  color: #bdbaba;
  margin-bottom: 14px;
}
.row-line {
  width: 100%;
  height: 1px;
  background-color: #eaeaea;
}
.b-item {
  width: 100%;
  height: 100%;
  position: relative;
}

.top-items {
  width: 95%;
  height: 90rpx;
  margin: 0 auto;
  color: #333;
  line-height: 90rpx;
  align-items: center;
  font-size: 32rpx;
  font-weight: 650;
}

.bottom-items {
  width: 100%;
}

.pictuer {
  width: 95%;
  height: 450rpx;
  margin: 0 auto;
}

.guanggao_image {
  width: 100%;
  height: 100%;
  border-radius: 2%;
}

.lunbotu {
  width: 100%;
  height: 970rpx;
  position: relative;
}
.fixed-start {
  position: absolute;
  right: 0;
  bottom: -60rpx;
  width: 145rpx;
  height: 60rpx;
  background-color: #B49569;
  display: flex;
  justify-content: center;
  align-items: center;
  transform-origin: right top;
  transform: rotate(90deg);
  z-index: 2;
}
.fixed-start text {
  font-size: 18rpx;
  color: #fff;
  text-align: center;
}
.swiper-text-list {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 145rpx;
}
.swiper-text-list .swiper-text-content {
  position: absolute;
  right: 60rpx;
  height: 100%;
  display: flex;
  justify-content: flex-end;
  box-sizing: border-box;
  overflow-y: hidden;
}
.swiper-text-content > view {
  width: 570rpx;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.9);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column nowrap;
  transition: 0.5s all ease;
  opacity: 0;
  transform: translateY(100%);
}
.bigtext {
  font-size: 32rpx;
  font-weight: bold;
  color: #333;
  margin-bottom: 20rpx;
}
.minitext {
  font-size: 24rpx;
  color: #333;
}
.swiper {
  width: 100%;
  height: 970rpx;
}
.slide-image {
  height: 970rpx;
  transition: all 0.5s ease;
  transform: scale(0.8);
}
.swiper-change {
  transform: scale(1);
}
.Separate{
  width: 100%;
  margin: 8rpx 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 26rpx;
  color: #fff;
  font-weight: bold;
}
/* css3动画模块start */
.eject-wrap {
  position: relative;
  margin-bottom: 26rpx;
  min-height: 900rpx;
}
.ejectImg-wrap {
  height: 920rpx;
  position: relative;
}
.eject-img {
  width: 100%;
  height: 100%;
  overflow: hidden;
  position: absolute;
  z-index: 2;
}
.eject-img image {
  width: 125%;
  height: 125%;
  position: relative;
  left: 50%;
  top: 50%;
}
.ejcect-location {
  position: absolute;
  right: 60rpx;
  bottom: 0;
  height: 145rpx;
  width: 540rpx;
  background-color: rgba(255, 255, 255, 0.9);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column nowrap;
  z-index: 2;
  opacity: 0;
  box-sizing: border-box;
  padding: 0 50rpx;
  white-space: nowrap;
}
.ejcect-location text{
  max-width: 100%;
  overflow: hidden;
  text-overflow: ellipsis;
}
.ejcect-location .title-f {
  color: #333;
  font-size: 32rpx;
  font-weight: bold;
  margin-bottom: 14rpx;
}
.ejcect-location .title-l{
  font-size: 28rpx;
  color: #666;
}
.lightSpeedIn {
  animation-name: lightSpeedIn;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards;
  animation-duration: 1s;
  animation-iteration-count: 1;
}
.eject-commodity{
  display: flex;
  flex-flow: row nowrap;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  margin-top: 26rpx;
}
.commodity{
  flex: 0 0 50%;
}
.commodity-img{
  width: 100%;
}
.commodity-text{
  width: 100%;
  height: 160rpx;
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
  justify-content: center;
  font-size: 20rpx;
}
/* 斜切模块 */
.beveling-wrap{
  position: relative;
  height: 347rpx;
  overflow: hidden;
  margin-bottom: 10rpx;
}
.beveling-wrap text{
  position: absolute;
  z-index: 3;
  font-size: 42rpx;
  color: #fff;
  transition: .8s;
  pointer-events: none;
}
.beveling-wrap .text-top{
  top: 100rpx;
  left: 100rpx;
  transform: translateX(-100vw);
}
.beveling-wrap .text-bottom{
  bottom: 100rpx;
  right: 100rpx;
  transform: translateX(100vw)
}
.beveling-text-change{
  transform: translateX(0) !important;
}
.beveling-location{
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgb(0, 0, 0);
  opacity: .3;
  transition: .8s;
  z-index: 2;
  pointer-events: none;
}
.beveling-location-change{
  opacity: 0 !important;
}
.beveling-top{
  transform-origin: bottom left;
  transform: rotate(-24.5deg);
  border-bottom: #ebebeb 2rpx solid;
  left: 0;
}
.beveling-top image{
  width: 750rpx;
  height: 350rpx;
  transform: rotate(24.5deg);
position: absolute;
bottom: 0;
left: 0;
transform-origin:left bottom;
}
button::after {
  border: none;
  display: none;
}
.beveling-bottom{
  margin: 0;
  padding: 0;
  border: none;
  background: none;
  transform-origin: top right;
  transform: rotate(-24.5deg);
  border-top: #ebebeb 2rpx solid;
  right: 0;
}
.beveling-bottom image{
   width: 750rpx;
  height: 350rpx;
  transform: rotate(24.5deg);
position: absolute;
top: 0;
right: 0;
transform-origin:top right;
}
.beveling-top,
.beveling-bottom{
  width: calc(100vw * 1.2);
  height: 100%;
  position: absolute;
  overflow: hidden;
}
.beveling-wrap{

}
@keyframes lightSpeedIn {
  0% {
    -webkit-transform: translate3d(100%, 0, 0) skewX(-30deg);
    transform: translate3d(100%, 0, 0) skewX(-30deg);
    opacity: 0;
  }
  60% {
    -webkit-transform:skewX(20deg);
    transform:skewX(20deg);
  }
  60%,
  80% {
    opacity: 1;
  }
  80% {
    -webkit-transform: skewX(-5deg);
    transform: skewX(-5deg);
  }
  to {
    -webkit-transform: none;
    transform: none;
    opacity: 1;
  }
}
/* css3动画模块end */
.recommend {
  width: 100%;
  height: auto;
  display: flex;
  margin-top: 28rpx;
  padding-bottom: 36rpx;
  justify-content: space-around;
  /* border-bottom: 2px #eee solid; */
}

.c-recommend {
  flex: 1;
  height: auto;
}

.tuijian {
  width: 100%;
  position: relative;
  text-align: center;
  border-right: 1px #eee solid;
}

.tuijian:nth-child(3) {
  border: none;
}

.tuijian_title {
  font-size: 15px;
}

.timg {
  width: 120rpx;
  height: 120rpx;
  margin: 0 auto;
  margin-top: 35rpx;
}

.tuijianImage {
  width: 100%;
  height: 100%;
}

.selected {
  width: 100%;
  height: 60rpx;
  color: #333;
  font-size: 17px;
  margin-top: 13px;
  font-weight: 600;
  line-height: 60rpx;
  text-align: center;
  font-family: "苹方-简 中黑体";
}

.three {
  width: 100%;
  height: 60rpx;
  font-size: 14px;
  font-weight: 400;
  line-height: 60rpx;
  font-family: "苹方-简 常规体";
  color: rgba(153, 153, 153, 1);
}
.bindtap,
.bindtaps,
.bindtapss {
  width: 60%;
  height: 55rpx;
  margin: 0 auto;
  font-size: 30rpx;
  color: #c59d9e;
  margin-top: 5px;
  line-height: 55rpx;
  text-align: center;
  border-radius: 21px;
  font-family: "苹方-简 常规体";
  background: rgba(255, 255, 255, 1);
  box-shadow: 0px 0px 2px 0px rgba(208, 103, 103, 1);
}
.bindtap {
  color: #84a3c0;
  box-shadow: 0px 0px 3px 0px rgba(96, 148, 249, 1);
}
.bindtapss {
  color: #c96;
  box-shadow: 0px 0px 2px 0px rgba(249, 168, 77, 1);
}

/* .titles {
  width: 100%;
  height: 60rpx;
  position: absolute;
  left: 0rpx;
  bottom: -1rpx;
}

.titie-c {
  width: 100%;
  height: 60rpx;
  position: relative;
}

.titleimg {
  width: 100%;
  height: 100%;
}

.rune {
  width: 100%;
  height: 60rpx;
  color: #fff;
  font-size: 24rpx;
  font-weight: 400;
  position: absolute;
  top: 0rpx;
  left: 0rpx;
  line-height: 60rpx;
} */

.mask {
  width: 100%;
  height: 100%;
  z-index: 2;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
}

.swipers {
  width: 580rpx;
  height: 700rpx;
  position: absolute;
  top: 22%;
  left: 12%;
}

.b-boximg {
  width: 100%;
  height: 100%;
  border-radius: 20rpx;
}

.error {
  width: 100rpx;
  height: 100rpx;
  position: absolute;
  bottom: 135rpx;
  left: 44%;
}

.errorimg {
  width: 100%;
  height: 100%;
}

/* 下拉加载 */

scroll-view {
  width: 100%;
  height: 100%;
}

.floats {
  width: 100%;
  height: auto;
  display: flex;
  flex-wrap: wrap;
  padding-bottom: 40rpx;
  justify-content: space-between;
}

.list {
  width: 48%;
  height: auto;
  font-size: 10px;
  text-align: center;
  margin-bottom: 20rpx;
  border-radius: 20rpx;
  border: 1px #eee solid;
}

.cainixihuan_title {
  font-size: 15px;
}

.cimg {
  width: 60%;
  height: 200rpx;
  margin: 0 auto;
  margin-top: 20rpx;
}

.cainixihuanImage {
  width: 100%;
  height: 100%;
}

.b-name {
  width: 90%;
  height: 55rpx;
  color: #000;
  margin: 0 auto;
  font-size: 28rpx;
  font-weight: 400;
  text-align: left;
  margin-top: 20rpx;
  line-height: 40rpx;
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  text-overflow: ellipsis;
  -webkit-box-orient: vertical;
}

.b-price {
  width: 100%;
  height: 50rpx;
  display: flex;
  margin: 0 auto;
  line-height: 50rpx;
}

.xj {
  width: 55%;
  height: 50rpx;
  text-align: left;
  color: #d32017;
  font-size: 16px;
  font-weight: 400;
  padding-left: 10rpx;
  font-family: PingFangSC-Regular, PingFangSC;
}

.yj {
  width: 40%;
  height: 50rpx;
  color: #999;
  font-size: 13px;
  font-weight: 400;
  text-align: center;
  text-decoration: line-through;
}

.hasmore {
  width: 100%;
  height: 120rpx;
  align-items: center;
  align-self: center;
  justify-content: center;
  position: relative;
}

.load {
  width: 100%;
  height: 50rpx;
  color: #666;
  font-size: 28rpx;
  font-weight: 400;
  text-align: center;
  line-height: 50rpx;
}

.loadimg {
  width: 100%;
  height: 64rpx;
}

.loading {
  width: 64rpx;
  height: 64rpx;
  position: absolute;
  top: 10rpx;
  left: 44%;
}

.tips1 {
  width: 100%;
  height: 100rpx;
}

.more {
  color: #666;
  font-weight: 400;
  font-size: 30rpx;
  text-align: center;
  line-height: 100rpx;
}

/*  */

.posterMask {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 998;
}

.poster {
  height: auto;
  position: fixed;
  top: 17%;
  left: 11%;
  z-index: 999;
}

.banner {
  width: 580rpx;
  height: 900rpx;
  overflow: hidden;
}

.banner > image {
  width: 100%;
  height: 100%;
  display: flex;
}

.QRcode {
  width: 157rpx;
  height: 146rpx;
  position: absolute;
  bottom: 134rpx;
  left: 28%;
}

.l_h_img {
  width: 100%;
  height: 100%;
}

.savePoster {
  width: 580rpx;
  height: 80rpx;
  color: #fff;
  font-size: 16px;
  line-height: 80rpx;
  text-align: center;
  background-color: #ddbd96;
}

.loads {
  width: 100%;
  color: #999;
  font-size: 14px;
  line-height: 80rpx;
  text-align: center;
}

</style>