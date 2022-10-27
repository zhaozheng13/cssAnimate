<template>
	<view class="box">
		<view class="balloon">
			<view class="envelope">
				<span></span>
				<span></span>
			</view>
		</view>
	</view>

</template>

<script>
</script>

<style>
	.box{
		margin:0;
		width: 300px;
		height:500px;
		display: flex;
		align-items: center;
		justify-content: center;
		background: linear-gradient(deepskyblue,skyblue,lightblue 20%);
	}
	.balloon{
		font-size: 16px;
		width: 12em;
		height:19em;
		display: flex;
		flex-direction: column;
		align-items: center;
		/* animation: drift 2s infinite alternate; */
	}
	@keyframes drift {
		to{
			transform: translateY(-10%);
		}
	}
	.envelope{
		position: relative;
		width: inherit;
		height: 16em;/*高度不够，用来将盖子下面的倒三角截成倒梯形*/
		overflow: hidden;
		border:1px solid red;
	}
	.envelope span{
		position: absolute;
		width: inherit;
		height: 12em;
		border-radius: 50%;
		background-color: orange;
	}
	.envelope span::before{
		content: '';
		position:absolute;
		width:0;
		height:0;
		border-width: 10em 5.5em 0em 5.5em;
		border-style: solid;
		border-color: orange transparent transparent transparent;
		left:calc(50% - 5.5em);
		top:8.45em
	}
	.envelope span:nth-child(2){/*这里的两个span元素其实是重叠的相同的图案，这里将第二个span元素进行压缩和变色，是为了形成两幅图案的色彩叠加效果*/
	  transform:scaleX(0.4);
	  filter:brightness(0.85) contrast(1.4);/*滤镜效果：前者调整明亮程度；后者是对比度设置*/
	}
</style>