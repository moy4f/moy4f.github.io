<svelte:head>
	<title>Works - Michelle's Svelte Site</title>
	<meta name="description" content="View Michelle's portfolio of web development projects" />
</svelte:head>

<div class="container">
	<header class="header">
		<h1>Uploads</h1>
		<p class="subtitle">Here are some of the documents I've uploaded</p>
	</header>
	
	<main class="main-content">
		<div class="projects-grid">
			<div class="project-card">
				<h2>Images</h2>
				<p>Photos, art, etc.</p>
				<div class="tech-stack">
					<span class="tech-tag">Svelte</span>
					<span class="tech-tag">CSS3</span>
					<span class="tech-tag">JavaScript</span>
				</div>
				<a href="#" class="project-link">Browse Images</a>
			</div>
			
			<div class="project-card">
				<h2>Documents</h2>
				<p>Texts written by latino people in the Kansas City Area</p>
				<div class="tech-stack">
					<span class="tech-tag">React</span>
					<span class="tech-tag">Node.js</span>
					<span class="tech-tag">MongoDB</span>
				</div>
				<a href="#" class="project-link">Browse Documents</a>
			</div>
			
			<div class="project-card">
				<h2>Notable People Profiles</h2>
				<p>People who have had great impact on our community</p>
				<div class="tech-stack">
					<span class="tech-tag">Vue.js</span>
					<span class="tech-tag">Firebase</span>
					<span class="tech-tag">TypeScript</span>
				</div>
				<a href="#" class="project-link">Browse Profiles</a>
			</div>
		</div>
	</main>
</div>

<style>
	.container {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
		color: white;
	}
	
	.header {
		text-align: center;
		padding: 4rem 2rem 2rem;
	}
	
	.header h1 {
		font-size: 3rem;
		margin: 0 0 1rem;
		background: linear-gradient(45deg, #fff, #f0f0f0);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
	}
	
	.subtitle {
		font-size: 1.2rem;
		opacity: 0.9;
		margin: 0;
	}
	
	.main-content {
		flex: 1;
		max-width: 1200px;
		margin: 0 auto;
		padding: 0 2rem 2rem;
	}
	
	.projects-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
		gap: 2rem;
	}
	
	.project-card {
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(10px);
		border-radius: 20px;
		padding: 2rem;
		box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
		border: 1px solid rgba(255, 255, 255, 0.2);
		transition: transform 0.3s ease;
	}
	
	.project-card:hover {
		transform: translateY(-5px);
	}
	
	.project-card h2 {
		font-size: 1.5rem;
		margin-bottom: 1rem;
		color: #f0f0f0;
	}
	
	.project-card p {
		font-size: 1.1rem;
		line-height: 1.6;
		margin-bottom: 1.5rem;
		opacity: 0.9;
	}
	
	.tech-stack {
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
		margin-bottom: 1.5rem;
	}
	
	.tech-tag {
		background: rgba(255, 255, 255, 0.2);
		padding: 0.25rem 0.75rem;
		border-radius: 15px;
		font-size: 0.9rem;
		border: 1px solid rgba(255, 255, 255, 0.3);
	}
	
	.project-link {
		display: inline-block;
		color: #4CAF50;
		text-decoration: none;
		font-weight: bold;
		transition: color 0.3s ease;
	}
	
	.project-link:hover {
		color: #45a049;
	}
	
	@media (max-width: 768px) {
		.projects-grid {
			grid-template-columns: 1fr;
		}
		
		.header h1 {
			font-size: 2rem;
		}
	}
</style>
