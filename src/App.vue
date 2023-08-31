<script>
import WomenClothes from "./components/WomenClothes.vue";
import MenClothes from "./components/MenClothes.vue";
export default {
	components: { WomenClothes, MenClothes },
};
</script>

<template>
	<div class="container">
		<div class="pattern_container">
			<img
				src="../public/background/bg-pattern-woman.svg"
				alt="background-pattern-woman"
			/>
		</div>
		<WomenClothes />
	</div>
</template>

<style scoped>
.container {
	display: flex;
	position: relative;
	min-height: 100vh;
}
.container .pattern_container {
	height: 60vh;
	background-color: #fde2ff;
	position: fixed;
	top: 0;
	right: 0;
	left: 0;
}
.pattern_container img {
	width: 100%;
	height: 60vh;
	object-fit: cover;
}
</style>
