

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
				<button class="btn btn-secondary" on:click={decrement}>-</button>
				<!-- Reactive display of current count value -->
				<span class="count">{count}</span>
				<!-- Increment button with event handler -->
				<button class="btn btn-primary" on:click={increment}>+</button>
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
		<p>Made with ❤️ using Svelte</p>
	</footer>
</div>

<!-- ===== COMPONENT STYLING ===== -->
<!-- Styles are scoped to this component only, preventing conflicts -->
<style>
	/* ===== MAIN CONTAINER ===== */
	.container {
		min-height: 100vh;                    /* Full viewport height */
		display: flex;                        /* Flexbox layout */
		flex-direction: column;               /* Stack children vertically */
		background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  /* Beautiful gradient background */
		color: white;                         /* White text for contrast */
		/* Removed padding-top since navigation is now in layout */
	}
	
	/* ===== HEADER STYLING ===== */
	.header {
		text-align: center;                   /* Center align header content */
		padding: 4rem 2rem 2rem;             /* Generous spacing around content */
	}
	
	.header h1 {
		font-size: 3rem;                     /* Large, prominent title */
		margin: 0 0 1rem;                    /* Remove default margins, add bottom spacing */
		background: linear-gradient(45deg, #fff, #f0f0f0);  /* Gradient text effect */
		-webkit-background-clip: text;       /* Clip background to text (WebKit browsers) */
		-webkit-text-fill-color: transparent; /* Make text transparent to show gradient */
		background-clip: text;                /* Modern browsers support */
	}
	
	.subtitle {
		font-size: 1.2rem;                   /* Slightly larger than body text */
		opacity: 0.9;                         /* Subtle transparency for hierarchy */
		margin: 0;                            /* Remove default margins */
	}
	
	/* ===== MAIN CONTENT LAYOUT ===== */
	.main-content {
		flex: 1;                              /* Take remaining space */
		display: flex;                        /* Flexbox for card layout */
		flex-direction: column;               /* Stack cards vertically */
		align-items: center;                  /* Center cards horizontally */
		gap: 2rem;                            /* Consistent spacing between cards */
		padding: 0 2rem 2rem;                /* Side and bottom padding */
	}
	
	/* ===== CARD COMPONENT STYLING ===== */
	.card {
		background: rgba(255, 255, 255, 0.1); /* Semi-transparent white background */
		backdrop-filter: blur(10px);          /* Modern glassmorphism effect */
		border-radius: 20px;                  /* Rounded corners for modern look */
		padding: 2rem;                        /* Generous internal spacing */
		text-align: center;                   /* Center card content */
		max-width: 500px;                     /* Limit card width for readability */
		width: 100%;                          /* Full width up to max-width */
		box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);  /* Subtle shadow for depth */
		border: 1px solid rgba(255, 255, 255, 0.2);  /* Subtle border for definition */
	}
	
	.card h2 {
		margin: 0 0 1.5rem;                   /* Remove top margin, add bottom spacing */
		font-size: 1.8rem;                    /* Prominent card titles */
	}
	
	/* ===== COUNTER COMPONENT STYLING ===== */
	.counter {
		display: flex;                        /* Horizontal button layout */
		align-items: center;                  /* Vertically center buttons and count */
		justify-content: center;              /* Horizontally center the group */
		gap: 1rem;                            /* Consistent spacing between elements */
		margin: 1rem 0;                       /* Vertical spacing around counter */
	}
	
	.count {
		font-size: 2rem;                      /* Large, prominent count display */
		font-weight: bold;                    /* Make count stand out */
		min-width: 3rem;                      /* Ensure consistent width */
		text-align: center;                   /* Center the number */
	}
	
	/* ===== BUTTON STYLING ===== */
	.btn {
		padding: 0.75rem 1.5rem;             /* Comfortable button sizing */
		border: none;                         /* Remove default button borders */
		border-radius: 50px;                  /* Fully rounded buttons */
		font-size: 1.2rem;                   /* Readable button text */
		font-weight: bold;                    /* Bold text for emphasis */
		cursor: pointer;                      /* Hand cursor on hover */
		transition: all 0.3s ease;           /* Smooth transitions for all changes */
		min-width: 3rem;                      /* Ensure consistent button width */
	}
	
	.btn-primary {
		background: linear-gradient(45deg, #4CAF50, #45a049);  /* Green gradient for increment */
		color: white;                         /* White text for contrast */
	}
	
	.btn-secondary {
		background: linear-gradient(45deg, #f44336, #da190b);  /* Red gradient for decrement */
		color: white;                         /* White text for contrast */
	}
	
	.btn:hover {
		transform: translateY(-2px);          /* Lift button slightly on hover */
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);  /* Enhanced shadow on hover */
	}
	
	/* ===== FEATURES LIST STYLING ===== */
	.features {
		list-style: none;                     /* Remove default list bullets */
		padding: 0;                           /* Remove default padding */
		margin: 0;                            /* Remove default margins */
		text-align: left;                     /* Left-align list items */
	}
	
	.features li {
		padding: 0.5rem 0;                    /* Vertical spacing between items */
		font-size: 1.1rem;                   /* Slightly larger than body text */
	}
	
	/* ===== FOOTER STYLING ===== */
	.footer {
		text-align: center;                   /* Center footer content */
		padding: 2rem;                        /* Generous padding around footer */
		opacity: 0.8;                         /* Subtle transparency for hierarchy */
	}
	
	/* ===== RESPONSIVE DESIGN ===== */
	/* Adjust layout for smaller screens */
	@media (max-width: 768px) {
		.header h1 {
			font-size: 2rem;                 /* Smaller title on mobile */
		}
		
		.card {
			margin: 0 1rem;                  /* Add side margins on mobile */
		}
	}
</style>

