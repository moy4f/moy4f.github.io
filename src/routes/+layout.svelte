
<script>
	// Import global CSS that applies to all pages
	import '../app.css';
	import '../static/page_format.css';
	
	// Import SvelteKit stores for navigation
	import { page } from '$app/stores';
	
	// Reactive variable to track current path
	$: currentPath = $page.url.pathname;
</script>

<!-- ===== GLOBAL NAVIGATION BAR ===== -->
<!-- This navigation appears on EVERY page automatically -->
<nav class="navigation">
	<div class="nav-container">
		<div class="nav-brand">✨ Michelle's Site</div>
		<ul class="nav-menu">
			<li><a href="/" class="nav-link" class:active={currentPath === '/'}>Home</a></li>
			<li><a href="/about" class="nav-link" class:active={currentPath === '/about'}>About</a></li>
			<li><a href="/projects" class="nav-link" class:active={currentPath === '/projects'}>Projects</a></li>
			<li><a href="/contact" class="nav-link" class:active={currentPath === '/contact'}>Contact</a></li>
		</ul>
	</div>
</nav>

<!-- Main layout wrapper - all page content gets injected here -->
<main>
	<!-- <slot /> is a Svelte component that renders child content -->
	<!-- Each page's content will be inserted here -->
	<slot />
</main>

<style>
	/* ===== GLOBAL NAVIGATION STYLING ===== */
	/* This styling applies to the navigation on ALL pages */
	.navigation {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(10px);
		border-bottom: 1px solid rgba(255, 255, 255, 0.2);
		z-index: 1000;
	}

	.nav-container {
		max-width: 1200px;
		margin: 0 auto;
		padding: 1rem 2rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.nav-brand {
		font-size: 1.5rem;
		font-weight: bold;
		color: white;
	}

	.nav-menu {
		display: flex;
		list-style: none;
		gap: 2rem;
		margin: 0;
		padding: 0;
	}

	.nav-link {
		color: white;
		text-decoration: none;
		padding: 0.5rem 1rem;
		border-radius: 25px;
		transition: all 0.3s ease;
	}

	.nav-link:hover,
	.nav-link.active {
		background: rgba(255, 255, 255, 0.2);
		transform: translateY(-2px);
	}

	/* Add padding to main content to account for fixed navigation */
	main {
		padding-top: 80px;
	}

	@media (max-width: 768px) {
		.nav-menu {
			gap: 1rem;
		}
		
		.nav-container {
			padding: 1rem;
		}
	}
</style>
