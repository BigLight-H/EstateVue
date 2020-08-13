<template>
	<view class="home-page">
		<nav-ext></nav-ext>
		<search-ext></search-ext>
		<swiper-ext></swiper-ext>
		<view class="home-info">
			<view class="home-info-view">
				<uni-icons type="chat" size="11"></uni-icons>
				<text>热点资讯</text>
			</view>
			<view class="home-info-view">
				<uni-icons type="gear" size="11"></uni-icons>
				<text>购房工具</text>
			</view>
		</view>
		<view class="home-con-one">
			<view class="home-con-one-title">
				<view>热门</view>
				<view class="home-more">更多</view>
			</view>
			<scroll-view id="tab-bar" class="scroll-h" :scroll-x="true" :show-scrollbar="false" :scroll-into-view="scrollInto">
			    <view v-for="(tab,index) in tabBars" :key="tab.id" class="uni-tab-item" :id="tab.id" :data-current="index" @click="ontabtap">
					<image src="https://s1.ax1x.com/2020/08/06/agL9v4.png" mode=""></image>
					<text class="tab-bar-text-one">我是标题</text>
					<text class="tab-bar-text-two">我是235副标题</text>
			    </view>
			</scroll-view>
		</view>
		<view class="home-con-two">
			<view class="home-con-one-title">
				<view>热门</view>
				<view class="home-more">更多</view>
			</view>
			<scroll-view id="tab-bar" class="scroll-h" :scroll-x="true" :show-scrollbar="false" :scroll-into-view="scrollInto">
			    <view v-for="(tab,index) in tabBars" :key="tab.id" class="uni-tab-item-two" :id="tab.id" :data-current="index" @click="ontabtap">
					<image src="https://s1.ax1x.com/2020/08/06/agxrCt.png" mode=""></image>
					<view class="home-money">$ 50000</view>
					<view class="home-house-intro">
						<view class="home-house-num">3 室</view>
						<view class="home-house-num">2 厅</view>
					</view>
			    </view>
			</scroll-view>
		</view>
		<view class="home-con-three">
			<view class="home-con-one-title">
				<view>热门</view>
				<view class="home-more">更多</view>
			</view>
			<view>
				<view class="home-con-list">
					<image src="https://s1.ax1x.com/2020/08/12/avN7TI.png" mode=""></image>
					<view class="home-con-list-child">
						<view>1111</view>
						<view>1111</view>
					</view>
					<view class="home-con-list-child">
						<view>2222</view>
						<view>2222</view>
					</view>
					<view class="home-con-list-child">
						<view>3333</view>
						<view>3333</view>
					</view>
				</view>
				<view class="home-con-list">
					<image src="https://s1.ax1x.com/2020/08/12/avN7TI.png" mode=""></image>
					<view class="home-con-list-child">
						<view>1111</view>
						<view>1111</view>
					</view>
					<view class="home-con-list-child">
						<view>2222</view>
						<view>2222</view>
					</view>
					<view class="home-con-list-child">
						<view>3333</view>
						<view>3333</view>
					</view>
				</view>
				<view class="home-con-list">
					<image src="https://s1.ax1x.com/2020/08/12/avN7TI.png" mode=""></image>
					<view class="home-con-list-child">
						<view>1111</view>
						<view>1111</view>
					</view>
					<view class="home-con-list-child">
						<view>2222</view>
						<view>2222</view>
					</view>
					<view class="home-con-list-child">
						<view>3333</view>
						<view>3333</view>
					</view>
				</view>
				<view class="home-con-list">
					<image src="https://s1.ax1x.com/2020/08/12/avN7TI.png" mode=""></image>
					<view class="home-con-list-child">
						<view>1111</view>
						<view>1111</view>
					</view>
					<view class="home-con-list-child">
						<view>2222</view>
						<view>2222</view>
					</view>
					<view class="home-con-list-child">
						<view>3333</view>
						<view>3333</view>
					</view>
				</view>
				<view class="home-con-list">
					<image src="https://s1.ax1x.com/2020/08/12/avN7TI.png" mode=""></image>
					<view class="home-con-list-child">
						<view>1111</view>
						<view>1111</view>
					</view>
					<view class="home-con-list-child">
						<view>2222</view>
						<view>2222</view>
					</view>
					<view class="home-con-list-child">
						<view>3333</view>
						<view>3333</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import swiperExt from '../ext/swiper-dot/swiper-dot.nvue'
	import navExt from '../ext/pendant/nav-to.vue'
	import searchExt from '../ext/search/search.vue'
	export default {
		components: {
			swiperExt,
			navExt,
			searchExt
		},
		data() {
			return {
				tabBars: [{
				    name: '关注',
				    id: 'guanzhu'
				}, {
				    name: '推荐',
				    id: 'tuijian'
				}, {
				    name: '体育',
				    id: 'tiyu'
				}, {
				    name: '热点',
				    id: 'redian'
				}, {
				    name: '财经',
				    id: 'caijing'
				}, {
				    name: '娱乐',
				    id: 'yule'
				}, {
				    name: '军事',
				    id: 'junshi'
				}, {
				    name: '历史',
				    id: 'lishi'
				}, {
				    name: '本地',
				    id: 'bendi'
				}]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	page {
		background-color: #efefef !important;
	}
	
	.home-info {
		display: flex;
		justify-content: space-evenly;
	}
	.home-info view {
		width: 50%;
		font-size: .6rem;
		text-align: center;
		background-color: #FFFFFF;
	}
	.home-info-view {
		line-height: 2rem;
		background-color: #FFFFFF;
	
	}
	.home-info-view text {
		margin-left: .3rem;
		background-image: linear-gradient(135deg,red,blue);
		-webkit-background-clip:text;
	}
	.home-con-one {
		background-color: #FFFFFF;
		margin-top: .6rem;
	}
	.home-con-two {
		background-color: #FFFFFF;
		height:11rem;
	}
	.home-con-one-title {
		display: flex;
		justify-content:space-between;
	}
	.home-con-one-title view:first-child {
		font-size: 1.3rem;
		padding: .8rem;
	}
	.home-con-one-title view:last-child {
		padding: .8rem;
		color: #C0C0C0;
	}
	.home-con-one-image view {
		margin-left: 1rem;
		width: 4rem;
		float: left;
	}
	.home-con-one-image image {
		width: 100%;
		border-radius: 16rpx;
	}
	.home-con-one-image {
		white-space:nowrap;
		overflow: auto;
		width: 100%;
	}
	
	.tabs {
	    flex: 1;
	    flex-direction: column;
	    overflow: hidden;
	    background-color: #ffffff;
	    /* #ifdef MP-ALIPAY || MP-BAIDU */
	    height: 100vh;
	    /* #endif */
	}
	
	.scroll-h {
	    width: 750rpx;
	    height: 450rpx;
	    flex-direction: row;
	    /* #ifndef APP-PLUS */
	    white-space: nowrap;
	    /* #endif */
	    /* flex-wrap: nowrap; */
	    /* border-color: #cccccc;
		border-bottom-style: solid;
		border-bottom-width: 1px; */
	}
	
	.line-h {
	    height: 1rpx;
	    background-color: #cccccc;
	}
	
	.uni-tab-item {
	    /* #ifndef APP-PLUS */
	    display: inline-block;
	    /* #endif */
	    flex-wrap: nowrap;
		padding-left: 26rpx;
		padding-right: 12rpx;
		height: auto;
		width: 290rpx;
		position: relative;

	}
	.uni-tab-item-two {
	    /* #ifndef APP-PLUS */
	    display: inline-block;
	    /* #endif */
	    flex-wrap: nowrap;
		padding-left: 26rpx;
		padding-right: 12rpx;
		height: auto;
		width: 243rpx;
		position: relative;
	}
	.uni-tab-item image {
		width: 100%;
		border-radius: 25rpx;
		/*  #ifdef  H5  */
		height: 222px !important;
		/*  #endif  */
	}

	.uni-tab-item-two image {
		width: 100%;
		border-radius: 25rpx;
		height:180rpx ;
	}
	
	.uni-tab-item-title {
	    color: #555;
	    font-size: 30rpx;
	    height: 500rpx;
	    line-height: 500rpx;
	    flex-wrap: nowrap;
	    /* #ifndef APP-PLUS */
	    white-space: nowrap;
	    /* #endif */
	}
	
	.uni-tab-item-title-active {
	    color: #007AFF;
	}
	
	.swiper-box {
	    flex: 1;
	}
	
	.swiper-item {
	    flex: 1;
	    flex-direction: row;
	}
	
	.scroll-v {
	    flex: 1;
	    /* #ifndef MP-ALIPAY */
	    flex-direction: column;
	    /* #endif */
	    width: 750rpx;
	}
	
	.update-tips {
	    position: absolute;
	    left: 0;
	    top: 41px;
	    right: 0;
	    padding-top: 5px;
	    padding-bottom: 5px;
	    background-color: #FDDD9B;
	    align-items: center;
	    justify-content: center;
	    text-align: center;
	}
	
	.update-tips-text {
	    font-size: 14px;
	    color: #ffffff;
	}
	
	.refresh {
	    width: 750rpx;
	    height: 64px;
	    justify-content: center;
	}
	
	.refresh-view {
	    flex-direction: row;
	    flex-wrap: nowrap;
	    align-items: center;
	    justify-content: center;
	}
	
	.refresh-icon {
		width: 30px;
		height: 30px;
		transition-duration: .5s;
		transition-property: transform;
		transform: rotate(0deg);
		transform-origin: 15px 15px;
	}
	
	.refresh-icon-active {
		transform: rotate(180deg);
	}
	
	.loading-icon {
		width: 20px;
		height: 20px;
		margin-right: 5px;
		color: #999999;
	}
	
	.loading-text {
	    margin-left: 2px;
	    font-size: 16px;
	    color: #999999;
	}
	
	.loading-more {
	    align-items: center;
	    justify-content: center;
	    padding-top: 10px;
	    padding-bottom: 10px;
	    text-align: center;
	}
	
	.loading-more-text {
	    font-size: 28rpx;
	    color: #999;
	}
	.tab-bar-text-one {
		position: absolute;
		left: 45rpx;
		bottom: 120rpx;
		color: #FFFFFF;
		font-size: 25rpx;
	}
	.tab-bar-text-two {
		position: absolute;
		left: 45rpx;
		bottom: 90rpx;
		color: #55aaff;
		font-size: 18rpx;
	}
	.home-house-intro{
		display: flex;
		justify-content: space-between;
	}
	.home-money {
		font-size: 28rpx;
		
	}
	.home-house-num {
		font-size: 24rpx;
		color: #55AAFF;
	}
	.home-house-num:last-child {
		margin-right: 2rem;
	}
	.home-more {
		font-size: 28rpx;
		line-height: 62rpx;
	}
	.home-con-three{
		background-color: #FFFFFF;
	}
	.home-con-list {
		text-align: center;
		margin: 0 1rem 0 1rem;
		padding: .5rem 0;
		border-bottom:.04rem solid #ddd;
		padding-bottom: 1.15rem;
		padding-top: 1.15rem;
		border-image: linear-gradient(#2b2b2b, #fff) 69 20;
	}
	.home-con-list:first-child {
		margin-top: 0;
		padding-top: 0;
	}
	.home-con-list:last-child {
		border-bottom:none;
		margin-bottom: 0;
		padding-bottom: 2.5rem;
	}
	.home-con-list image{
		width: 100%;
		border-radius: 20rpx;
	}
	.home-con-list-child {
		display: flex;
		justify-content:space-between;
		font-size: 28rpx;
		line-height: 1.15rem;
	}
	.home-con-list-child view:first-child {
		font-weight: bold;
	}
	.home-con-list-child view:last-child {
		color: #999999;
	}
</style>
