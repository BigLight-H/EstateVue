<template>
	<view class="search-base">
		<nav-ext></nav-ext>
		<view class="lists">
			<view>
				<text>搜索:</text>
			</view>
			<view class="search-list">
				<view class="search-div" @click="goDetail">
					<view class="search-img">
						<image src="https://s1.ax1x.com/2020/08/12/avWGgH.png" alt="">
						<view class="search-img-icon">
							<uni-icons class="search-ico" type="heart-filled" size="16" color="#ff0000"></uni-icons>
						</view>
					</view>
					<view class="search-div-font">
						<view>
							<view>$ 400,000</view>
						</view>
						<view class="search-div-font-child">
							<view>woshiaha</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>我首付多少</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>价格</view>
							<view>1111</view>
						</view>
					</view>
				</view>
				<view class="search-div">
					<view class="search-img">
						<image src="https://s1.ax1x.com/2020/08/12/avWGgH.png" alt="">
						<view class="search-img-icon">
							<uni-icons class="search-ico" type="heart-filled" size="16" color="#ff0000"></uni-icons>
						</view>
					</view>
					<view class="search-div-font">
						<view>
							<view>$ 400,000</view>
						</view>
						<view class="search-div-font-child">
							<view>woshiaha</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>我首付多少</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>价格</view>
							<view>1111</view>
						</view>
					</view>
				</view>
				<view class="search-div">
					<view class="search-img">
						<image src="https://s1.ax1x.com/2020/08/12/avWGgH.png" alt="">
						<view class="search-img-icon">
							<uni-icons class="search-ico" type="heart-filled" size="16" color="#ff0000"></uni-icons>
						</view>
					</view>
					<view class="search-div-font">
						<view>
							<view>$ 400,000</view>
						</view>
						<view class="search-div-font-child">
							<view>woshiaha</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>我首付多少</view>
							<view>1111</view>
						</view>
						<view class="search-div-font-child">
							<view>价格</view>
							<view>1111</view>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view v-bind:class="search_search">
			<view v-bind:class="search_div">
				<view class="search-search-div-child">
					<view @click="showSearch">
						<uni-icons type="search" size="16" color="#00aaff"></uni-icons>
					</view>
				</view>
				<view v-bind:class="search">
					<view class="">
						<input type="text" class="search-input" placeholder="输入关键词...">
						<view class="search-input-btns">
							<button type="primary" class="search-input-btn" @click="showSearch">取&nbsp;&nbsp;&nbsp;&nbsp;消</button>
							<button type="primary" class="search-input-btn">提&nbsp;&nbsp;&nbsp;&nbsp;交</button>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import navExt from '../ext/pendant/nav-to.vue'
	export default {
		components: {
			navExt
		},
		data() {
			return {
				search:'search-search-div-child2',
				show:false,
				search_div:'search-search-div',
				search_search:'search-search'
			}
		},
		methods: {
			showSearch() {
				if(this.show) {
					this.search = 'search-search-div-child2'
					this.search_div = 'search-search-div'
					this.search_search = 'search-search'
					this.show = false
				} else {
					this.search = 'search-search-div-child2 search-search-div-child2-copy'
					this.show = true
					this.search_div = 'search-search-div-h'
					this.search_search = 'search-search-copy'
				}
			},
			goDetail() {
				uni.navigateTo({
					url: '/pages/detail/detail'
				});
			}
		}
	}
</script>

<style>
	page {
		background-color: #FFFFFF !important;
	}
	.search-base {
		position: relative;
	}
	.lists {
		margin: 2rem 1rem 0 1rem;
	}
	.search-img {
		position: relative;
		width: 50%;
	}
	.search-img image {
		width: 100%;
		border-radius: 20rpx;
		height: 256rpx;
	}
	.search-ico {
		position: absolute;
		top: 24rpx;
		right: 24rpx;
	}
	.search-div {
		display: flex;
		justify-content: space-between;
		border-bottom: .04rem solid #d8d5d5;
		padding-bottom: 1rem;
		padding-top: 1rem;
	}
	.search-div:last-child {
		border-bottom: none;
	}
	.search-div-font {
		width: 50%;
		padding: 1rem 0 0 .3rem;
	}
	.search-div-font view {
		display: flex;
		justify-content: space-between;
	}
	.search-div-font-child {
		font-size: 26rpx;
	}
	.search-div-font-child view:first-child {
		font-weight: bold;
	}
	.search-div-font-child view:last-child {
		color: #808080;
	}
	.search-div-font view:first-child {
		font-weight: bold;
		margin-bottom: .1rem;
	}
	.search-search {
		position: fixed;
		left: 0;
		right: 0;
		bottom: 0;
		z-index: 3;
	}
	.search-search-copy {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		z-index: 3;
		background-color: #a0a0a059;
	}
	.search-search-div {
		position: fixed;
		bottom: 0;
		left: 0;
		right: 0;
		height: 1.5rem;
	}
	.search-search-div-h {
		position: fixed;
		bottom: 0;
		left: 0;
		right: 0;
		height: 8rem;
	}
	
	.search-search-div-child view {
		width: 20%;
		margin: 0 auto;
		background-color: #FFFFFF;
		border-radius: 60rpx 60rpx 0 0 ;
		height: 1.5rem;
		box-shadow: 0px 0px 20upx #888888;
	}
	.search-search-div-child {
		text-align: center;
		width: 100%;
	}
	.search-search-div-child2 {
		width: 100%;
		display: none;
	}
	.search-search-div-child2-copy {
		display: block !important;
	}
	

	.search-search-div-child2 view {
		height: 5rem;
		background-color: #FFFFFF;
		border-radius: 60rpx 60rpx 0 0;
		padding: 1rem 2rem;
	}
	.search-input {
		border-radius: 24rpx;
		border: .04rem solid #b1b1b1;
		height: 1.5rem;
		padding: .1rem .5rem .1rem .5rem;
		background-color: #f5f5f5;
		border-color: #f5f5f5;
		outline: none;
	}
	.search-input-btn {
		height: 1.5rem;
		font-size: 24upx;
		border: none;
		border-radius: 24rpx;
		width: 100%;
	}
	.search-input-btns {
		display: flex;
		width: 100%;
		justify-content: space-between;
		padding: 0 !important;
		margin-top: 1rem;
	}
	.search-input-btn:first-child{
		margin-right: 1rem;
		background-color: #b7b7b7;
		border-color: #b7b7b7;
	}
	.search-input-btn:last-child{
		margin-left: 1rem;
		background-color: #589ff8;
		border-color: #589ff8;
	}
</style>
