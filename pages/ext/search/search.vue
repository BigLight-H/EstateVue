<template>
    <view class="search-base">
        <view class="search-block">
            <view class="search-ico-wapper">
				<!-- <uni-icons class="search-ico" type="search" size="23" color="#C0C0C0"></uni-icons> -->
            </view>
            <input type="text" value="" placeholder="点击输入搜索内容" class="search-text" maxlength="10" focus/>
            <view class="search-ico-wapper1" @click="searchGo">
				<uni-icons class="search-ico" type="search" size="20" color="#C0C0C0"></uni-icons>
            </view>
        </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {

            }
        },
        methods: {
			searchGo(){
				uni.navigateTo({
					url: '/pages/list/list'
				});
			}
        }
    }
</script>

<style>
/* 搜索框 */
.search-ico, .search-ico-1{
    width: 40upx;
    height: 40upx;
}
.search-text{
    font-size: 14px;
    background-color: #ffffffbf;
    height: 60upx;
    width: 480upx;
}
.search-block{
    display: flex;
    flex-direction: row;
    padding-left: 106upx;
    position: absolute;
	/*  #ifdef  MP-WEIXIN  */
	top: 12%;
	z-index: 2;
	/*  #endif  */
	/*  #ifdef  H5  */
	top: 9%;
	z-index: 1;
	/*  #endif  */
	
}
.search-ico-wapper{
    background-color: #ffffffbf;
    display: flex;
    flex-direction:column;
    justify-content: center;
    padding: 0upx 5upx 0upx 20upx;
    border-bottom-left-radius:18px;
    border-top-left-radius: 18px;
}
.search-ico-wapper1{
    background-color: #ffffffbf;
    display: flex;
    flex-direction:column;
    justify-content: center;
    padding: 0upx 20upx 0upx 0upx;
    border-bottom-right-radius:18px;
    border-top-right-radius: 18px;
}
</style>
