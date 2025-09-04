<svelte:head>
    <title>About - Michelle's Svelte Site</title>
    <meta name="description" content="About Page" />
</svelte:head>

<div class="container">
    <header class="header">
        <h1>About Michelle</h1>
    </header>

    <main class="main-content">
        <div class="card">
            <h2>My name's Michelle!</h2>
            <p>I am Mexican American. I love Wallows. I speak Spanish. Other stuff I can fill out myself instead of Zach.</p>
        </div>
    </main>
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
	
	.card p {
		font-size: 1.1rem;                    /* Readable paragraph text */
		line-height: 1.6;                     /* Comfortable line spacing */
		margin: 0;                             /* Remove default margins */
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