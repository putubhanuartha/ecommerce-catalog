<script>
export default {
	props: ["objState", "data"],
};
</script>
<template>
	<div class="container_women">
		<div class="content_container">
			<img
				:src="data.image"
				:alt="data.category"
			/>
			<div class="right_container">
				<div class="top_content">
					<h2 class="title">
						{{ data.title }}
					</h2>
					<div class="category_rating_container">
						<p class="category">{{ data.category }}</p>
						<div class="rating_container">
							<p>{{ data.rating.rate }}</p>
							<div class="bullet_container">
								<img
									v-for="n in Math.floor(data.rating.rate)"
									v-bind:src="
										objState.id === 0
											? '/src/assets/woman_assets/bullet.svg'
											: '/src/assets/men_assets/bullet.svg'
									"
								/>
								<img
									v-for="n in 5 - Math.floor(data.rating.rate)"
									v-bind:src="
										objState.id === 0
											? '/src/assets/woman_assets/bullet-void.svg'
											: '/src/assets/men_assets/bullet-void.svg'
									"
								/>
							</div>
						</div>
					</div>
					<img
						src="../assets/line.svg"
						class="line"
						alt=""
					/>
					<p class="text">
						{{ data.description }}
					</p>
				</div>
				<div class="bottom_content">
					<img
						src="../assets/line.svg"
						class="line"
						alt=""
					/>
					<h5 class="price">${{ data.price }}</h5>
					<div class="button_container">
						<button>Buy Now</button>
						<button @click="$emit('handleIncrement')">Next Product</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<style scoped>
.top_content {
	display: flex;
	flex-direction: column;
	gap: 10px;
}
.bottom_content {
	display: flex;
	flex-direction: column;
	gap: 10px;
}
.container_women {
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
h2.title {
	color: v-bind("objState.color");
	font-family: Inter;
	font-size: 1.75rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
}
p.category {
	color: #3f3f3f;
	font-family: Inter;
	font-size: 1.125rem;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
}

p.text {
	color: #1e1e1e;
	font-family: Inter;
	font-size: 1.25rem;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
	max-height: 10rem;
	overflow-y: scroll;
}
.content_container {
	display: flex;
	align-items: center;
	gap: 1.7rem;
}
h5.price {
	color: v-bind("objState.color");
	font-family: Inter;
	font-size: 1.75rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
}
.content_container img {
	object-fit: cover;
	height: 300px;
	width: 300px;
}
.category_rating_container {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.rating_container {
	display: flex;
	align-items: center;
	gap: 3px;
}
.right_container {
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	min-height: 25rem;
}
img.line {
	width: 100%;
	height: 4px;
}
.bullet_container {
	display: flex;
	gap: 0.3rem;
}
.bullet_container img {
	width: 12px;
	height: 12px;
}
.button_container {
	display: flex;
	gap: 5px;
}
.button_container button {
	padding: 5px;
	cursor: pointer;
}
.button_container button:nth-child(1) {
	border-radius: 0.25rem;
	background: v-bind("objState.color");
	color: #fff;
	font-family: Inter;
	font-size: 1.25rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
	flex: 1;
	transition: all 0.2s;
}
.button_container button:nth-child(1):hover{
	border-radius: 20px;
}

.button_container button:nth-child(2) {
	flex: 1;
	border-radius: 0.25rem;
	border: 3px solid v-bind("objState.color");
	background: #fff;
	color: v-bind("objState.color");
	font-family: Inter;
	font-size: 1.25rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
	transition: all 0.2s;
}
.button_container button:nth-child(2):hover {
	background: v-bind("objState.color");
	color: #fff;
}
</style>
