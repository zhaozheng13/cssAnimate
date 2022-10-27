<template>
	<view class="example1">
		<ul>
			<li>home</li>
			<li>products</li>
			<li>services</li>
			<li>contact</li>
		</ul>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.example1{
		height: 400px;
		width: 500px;
		display: flex;
		align-items: center;
		justify-content: center;
		background: cornsilk;
		ul{
			list-style-type: none;
			padding: 0;
		}
		ul li{
			width: 15em;
			height: 3em;
			// border:1px solid red;
			font-size: 16px;
			border-radius: 0.5em;
			line-height: 3em;
			margin: 0.5em;
			color: white;
			box-shadow: 0 0 1em rgba(0, 0, 0, .2);
			font-family: sans-serif;
			text-transform: capitalize;
			transition: 0.3s;
			cursor: pointer;
			box-sizing: border-box;
		}
		ul li:nth-child(odd){
			background: linear-gradient(to right,orange,tomato);
			text-align: left;
			padding-left: 10%;
			transform: perspective(500px) rotateY(45deg);
		}
		ul li:nth-child(even){
			background: linear-gradient(to left,orange,tomato);
			text-align: right;
			padding-right: 10%;
			transform: perspective(500px) rotateY(-45deg);
		}
		ul li:nth-child(odd):hover{
			transform: perspective(200px) rotateY(45deg);
			padding-left: 5%;
		}
		ul li:nth-child(even):hover{
			transform: perspective(200px) rotateY(-45deg);
			padding-right: 5%;
		}
	}
</style>