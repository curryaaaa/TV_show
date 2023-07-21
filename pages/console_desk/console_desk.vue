<template>
	<view>
		<view>
			<view>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
			</view>
			<view>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
			</view>
			<view>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
				<image src="@/static/tv.png" mode="aspectFit" class="div_box"></image>
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
		
		mounted() {
			plus.screen.lockOrientation( 'landscape-primary');
		},
		methods: {
			
		},
	}
</script>

<style>
	.div_box {
		width: 20%;
		height: 25vh;
		background-color: ;
		flex-direction: #cdcdcd;
		display: inline-block;
		margin-top: 5vh;
		margin-left: 9vh;
	}
</style>