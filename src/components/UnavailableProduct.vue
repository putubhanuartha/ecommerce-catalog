<template>
	<div class="container_unavail">
		<img
			src=""
			alt=""
		/>
		<div>
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
	display: flex;
	align-items: center;
}
</style>
