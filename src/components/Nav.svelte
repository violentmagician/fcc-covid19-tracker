<script lang="ts">
	export let section = '';
	let isOpen = false;
	function toggleNav() {
		isOpen = !isOpen;
	}
</script>

<nav class="navbar" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
		<a class="navbar-item" href="/">
			<img src="logo.jpg" alt="bulma-logo" width="28" height="28" />
		</a>

		<span
			role="button"
			class="navbar-burger"
			class:is-active={isOpen}
			aria-label="menu"
			aria-expanded="false"
			on:click={toggleNav}
		>
			<span aria-hidden="true" />
			<span aria-hidden="true" />
			<span aria-hidden="true" />
		</span>
	</div>

	<div class="navbar-menu" class:is-active={isOpen}>
		<div class="navbar-start">
			<a href="/" class="navbar-item" class:is-active={section === ''}> Home </a>
			<a href="/about" class="navbar-item" class:is-active={section === 'about'}> About </a>
		</div>
	</div>
</nav>

<style>
	@media (min-width: 769px) {
		nav {
			border-bottom: solid gray 1px;
		}
	}
</style>
