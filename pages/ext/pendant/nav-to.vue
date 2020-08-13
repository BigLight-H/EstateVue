<template>
    <view class="prohibition">
		<!-- #ifdef MP-WEIXIN -->
			<view class="demo" :style="'height:' +  demo.height + 'px;' + 'padding-top:' + demo.top + 'px;padding-bottom:10rpx'">
			    <view class="left" :style="'top:' + demo.top + 'px'">
					<uni-icons type="back" size="30" color="#bfbfbf"></uni-icons>
			    </view>
			    测试辣
			</view>
		<!-- #endif -->
		<!-- #ifdef H5 -->
			<view class="demo" :style="'height:35px'">
			    <view class="left" @click="goBack">
					<uni-icons type="back" size="30" color="#bfbfbf"></uni-icons>
			    </view>
			    测试辣
			</view>
		<!-- #endif -->
    </view>
</template>

<script>
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
    export default {
		components: {uniIcons},
        data () {
            return {
                demo: {
                    top: 0,
                    height: 0
                }
            }
        },
        created () {
            const demo = uni.getMenuButtonBoundingClientRect()
            this.demo.top = demo.top
            this.demo.height = demo.height
        },
		methods: {
			goBack(){
				this.$router.back();
			}
		}
    }
</script>

<style lang="scss">
	.prohibition {
		position: fixed;
		left: 0;
		right: 0;
		top: 0;
		z-index: 2;
		.demo{
		    position: relative;
		    display: flex;
		    align-items: center;
		    justify-content: center;
		    background: #FFFFFF;
		    font-size: 26rpx;
		    .left{
		        float: left;
		        position: absolute;
		        width: max-content;
		        height: max-content;
		        top: 0;
		        bottom: 0;
		        left: 20rpx;
		        margin: auto;
		    }
		}
	}
</style>