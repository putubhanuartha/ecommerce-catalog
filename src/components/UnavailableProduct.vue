<template>
	<div class="container_unavail">
		<img
			src="../assets/sad-face.png"
			alt=""
		/>
		<div class="text_container">
			<p>This product is unavailable to show</p>
			<button>Next Product</button>
		</div>
	</div>
</template>
<style scoped>
.container_unavail {
	position: absolute;
	z-index: 9999;
	left: 50%;
	transform: translate(-50%, -50%);
	top: 50%;
	padding: 3rem 2rem;
	border-radius: 0.625rem;
	background: #fff;
	box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
	min-height: 25rem;
}
.container_unavail img {
	position: relative;
	max-width: 43rem;
	left: 2.5rem;
	top: 2rem;
}
.container_unavail .text_container {
	min-width: 25rem;
	position: absolute;
	top: 50%;
	left: 50%;
	z-index: 9999;
	transform: translate(-50%, -50%);
}

.container_unavail .text_container p {
	text-align: center;
}
.container_unavail .text_container button {
	margin: 1rem auto;
	display: block;
	width: 100%;
	padding: 0.3rem;
	border-radius: 0.25rem;
	border: 3px solid #000;
	background: #fff;
	transition: all 0.2s;
}
.container_unavail .text_container button:hover{
	background: #000;
	color: #fff;
}
</style>
