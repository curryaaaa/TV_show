<template>
	<view>
		<view class="uni-margin-wrap" @touchmove.stop.prevent="moveStop" v-if="type==1">
			<swiper class="swiper" circular autoplay=true interval='2000' duration="1500">
				<swiper-item v-for="item in src_image">
					<image style="width: 100%;height: 100vh;" :src="item"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="uni-padding-wrap uni-common-mt" v-if="type==2">
			<view>
				<video style="width: 100%;height: 100vh;" autoplay=true loop=true :src='src_video' controls></video>
			</view>
		</view>
		<view v-if="type==3">
			<web-view :src="URL"></web-view>
		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				type: 1,
				src_image: [
					'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
					'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
					'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
					'https://fuss10.elemecdn.com/9/bb/e27858e973f5d7d3904835f46abbdjpeg.jpeg',
					'https://fuss10.elemecdn.com/d/e6/c4d93a3805b3ce3f323f7974e6f78jpeg.jpeg',
					'https://fuss10.elemecdn.com/3/28/bbf893f792f03a54408b3b7a7ebf0jpeg.jpeg',
					'https://fuss10.elemecdn.com/2/11/6535bcfb26e4c79b48ddde44f4b6fjpeg.jpeg'
				],
				src_video: "https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/2minute-demo.mp4",
				URL: 'https://www.baidu.com/'
			}
		},
		onReady: function(res) {
			// #ifndef MP-ALIPAY
			this.videoContext = uni.createVideoContext('myVideo')
			// #endif
		},
		mounted() {
			// plus.screen.lockOrientation( 'landscape-secondary');
			// plus.screen.lockOrientation( 'landscape-primary');
		},
		methods: {
		
		}
	}
</script>
<style>
	.uni-margin-wrap {
		height: 100vh;
		width: 100%;
	}

	.swiper {
		height: 100%;
	}

	.uni-padding-wrap {
		height: 100vh;
		width: 100%;
	}
</style>