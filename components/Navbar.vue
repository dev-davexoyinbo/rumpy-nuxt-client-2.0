<template>
	<div id="navbar" :class="{collapsed: collapsed}">
		<div class="brand">
			<div class="logo"></div>
			<div class="logo-text">
				<span>rumpy </span>
				<span>wines</span>
			</div>
		</div>
		<div class="hamburger-container" @click="toggleNavbar()">
			<i class="fas fa-bars"></i>
		</div>
		<!-- <div class="nav-links-container collapsed"> -->
		<div class="nav-links-container" :class="{collapsed: collapsed}">
			<div class="close-button-container" >
				<div class="close-button" @click="toggleNavbar()">
					<i class="fas fa-times"></i>
				</div>
			</div>
			<div class="nav-links">
				<div class="nav-link active">
				<i class="icon fas fa-store"></i> Product
				</div>
				<div class="nav-link">
				<i class="icon fas fa-hands-helping"></i> Help Center
				</div>
				<div class="nav-link">
				<i class="icon fas fa-user-alt"></i> Account
				</div>
				<div class="nav-link">
				<i class="icon fas fa-sign-in-alt"></i> Login
				</div>
				<div class="nav-link">
				<i class="icon fas fa-cart-arrow-down"></i> Cart
				</div>		
			</div>

		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			collapsed: false
		}
	},
	methods: {
		toggleNavbar() {
			this.collapsed = !this.collapsed
		}
	}
}
</script>

<style lang="scss" scoped>
@import '~assets/styles/components/navbar';
</style>