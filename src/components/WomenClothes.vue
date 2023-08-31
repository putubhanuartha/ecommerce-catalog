<template>
	<div class="container_women">
		<div class="content_container">
			<img
				src="https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg"
				alt=""
			/>
			<div class="right_container">
				<div class="top_content">
					<h2 class="title">
						Fjallraven - Foldsack No. 1 Backpack, Fits 15 Laptops
					</h2>
					<div class="category_rating_container">
						<p class="category">men's clothing</p>
						<div class="rating_container">
							<p>3.6/5</p>
							<div class="bullet_container">
								<img
									src="../assets/bullet.svg"
									alt=""
								/>
								<img
									src="../assets/bullet.svg"
									alt=""
								/>
								<img
									src="../assets/bullet.svg"
									alt=""
								/>
								<img
									src="../assets/bullet-void.svg"
									alt=""
								/>
								<img
									src="../assets/bullet-void.svg"
									alt=""
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
						Your perfect pack for everyday use and walks in the forest. Stash
						your laptop (up to 15 inches) in the padded sleeve, your everyday
					</p>
				</div>
				<div class="bottom_content">
					<img
						src="../assets/line.svg"
						class="line"
						alt=""
					/>
					<h5 class="price">$12.59</h5>
					<div class="button_container">
						<button>Buy Now</button>
						<button>Next Product</button>
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
	color: #720060;
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
}
.content_container {
	display: flex;
	align-items: center;
	gap: 1.7rem;
}
h5.price {
	color: #720060;
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
	background: #720060;
	color: #fff;
	font-family: Inter;
	font-size: 1.25rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
	flex: 1;
}
.button_container button:nth-child(1):hover {
	background-color: #a8008f;
}
.button_container button:nth-child(2) {
	flex: 1;
	border-radius: 0.25rem;
	border: 3px solid #720060;
	background: #fff;
	color: #720060;
	font-family: Inter;
	font-size: 1.25rem;
	font-style: normal;
	font-weight: 600;
	line-height: normal;
}
.button_container button:nth-child(2):hover {
	background: #ffebeb;
}
</style>
