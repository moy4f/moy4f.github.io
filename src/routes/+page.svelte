

<script lang="ts">
	// ===== REACTIVE STATE MANAGEMENT =====
	// This variable automatically updates the UI when its value changes
	let count = 0;
	
	// ===== EVENT HANDLER FUNCTIONS =====
	// These functions are called when buttons are clicked
	function increment() {
		count += 1;  // Svelte automatically re-renders the component
	}
	
	function decrement() {
		count -= 1;  // The UI updates immediately when count changes
	}
	function increment_ten() {
		count += 10;
	}

	function decrement_ten() {
		count -= 10;
	}
	
	function clear() {
		count = 0;
	}
</script>

<!-- ===== PAGE METADATA ===== -->
<!-- svelte:head allows you to modify the document head for this specific page -->
<svelte:head>
	<title>Michelle's Svelte Site</title>
	<meta name="description" content="Welcome to Michelle's beautiful Svelte website!" />
</svelte:head>

<!-- ===== MAIN PAGE STRUCTURE ===== -->
<div class="container">
	<!-- ===== HEADER SECTION ===== -->
	<header class="header">
		<h1>✨ Welcome to Michelle's Site ✨</h1>
		<p class="subtitle">Built with Svelte and modern web technologies</p>
	</header>
	
	<!-- ===== MAIN CONTENT AREA ===== -->
	<main class="main-content">
		<!-- Interactive Counter Card -->
		<div class="card">
			<h2>Interactive Counter</h2>
			<div class="counter">
				<!-- Decrement button with event handler -->
				<button class="btn btn-secondary" on:click={decrement_ten}>-10</button>
				<button class="btn btn-secondary" on:click={decrement}>-</button>
				<!-- Reactive display of current count value -->
				<span class="count">{count}</span>
				<!-- Increment button with event handler -->
				<button class="btn btn-primary" on:click={increment}>+</button>
				<button class="btn btn-primary" on:click={increment_ten}>+10</button>
				<button class="btn btn-primary" on:click={clear}>Clear</button>
			</div>
		</div>
		
		<!-- Features List Card -->
		<div class="card">
			<h2>Features</h2>
			<ul class="features">
				<li>🚀 Fast and responsive</li>
				<li>🎨 Beautiful modern design</li>
				<li>⚡ Built with Svelte</li>
				<li>📱 Mobile-friendly</li>
			</ul>
		</div>
	</main>
	
	<!-- ===== FOOTER SECTION ===== -->
	<footer class="footer">
		<p>Lorem Ipsum or whatever</p>
	</footer>
</div>



