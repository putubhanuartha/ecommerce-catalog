<script>
import CardClothes from "./components/CardClothes.vue";
import axios from "axios";
import UnavailableProduct from "./components/UnavailableProduct.vue";
const statusState = {
	womanSection: {
		id: 0,
		color: "#720060",
		backgroundColor: "#FDE2FF",
	},
	menSection: {
		id: 1,
		color: "#002772",
		backgroundColor: "#D6E6FF",
	},
	unavail: {
		id: 2,
	},
};
export default {
	components: { CardClothes, UnavailableProduct },
	data() {
		return {
			state: statusState.unavail,
			data: undefined,
			isError: false,
			productId: 1,
		};
	},
	watch: {
		productId: {
			async handler(newVal) {
				console.log(newVal);
				try {
					const response = await axios.get(
						`https://fakestoreapi.com/products/${newVal}`
					);
					if (response?.data) {
						this.data = response.data;
						const category = this.data.category;
						if (category === "men's clothing") {
							this.state = statusState.menSection;
						} else if (category === "women's clothing") {
							this.state = statusState.womanSection;
						} else {
							this.state = statusState.unavail;
						}
					}
				} catch (err) {
					console.error(err);
					this.isError = true;
				}
			},
			immediate: true,
		},
	},
	methods: {
		handleIncrement() {
			this.productId !== 20 ? this.productId++ : (this.productId = 1);
		},
	},
};
</script>

<template>
	<div class="container">
		<div class="pattern_container">
			<img
				src="/background/bg-pattern-woman.svg"
				alt="background-pattern-woman"
				v-if="state.id !== 2"
			/>
		</div>
		<div v-if="data">
			<CardClothes
				@handleIncrement="handleIncrement"
				:objState="state"
				v-if="state.id === 0 || state.id === 1"
				:data="data"
			/>
			<UnavailableProduct @handleIncrement="handleIncrement" v-else-if="state.id === 2" />
		</div>
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
	background-color: v-bind(
		"state.id === 2 ? '#D8D7D7' : state.backgroundColor "
	);
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
