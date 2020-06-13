<template>
	<view>
		<view class="navBar" :style="{marginTop:statusBarHeight+'px'}">
			<view class="content">
				<view class="icon">
					
				</view>
				<view class="text">
					uni-app,vue
				</view>
			</view>
		</view>
		<!--导航栏高度 fixed定位 占位符-->
		<view style="height:45px">
			
		</view>
		<!--手机内置状态栏高度 占位符-->
		<view :style="{height:statusBarHeight+'px'}">
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				statusBarHeight:20
			};
		},
		created(){
			//H5 状态栏高度为0
			const info = uni.getSystemInfoSync()
			this.statusBarHeight=info.statusBarHeight
		}
	}
</script>

<style lang="scss">
	.navBar{
		height:45px;
		width:100%;
		padding:0 15px;
		position: fixed;
		top:0;
		left:0;
		background-color: $base-color;
		box-sizing: border-box;
		display: flex;
		justify-content: center;
		align-items: center;
		.content{
			display: flex;
			align-items: center;
			width: 100%;
			background-color: white;
			.icon{
				width:30px;
				height:30px;
				
			}
			.text{
				font-size: 12px;
			}
		}
	}
</style>
