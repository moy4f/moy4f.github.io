<script lang="ts">
	// Contact page component
	let formData = {
		name: '',
		email: '',
		message: ''
	};
	
	function handleSubmit() {
		// Handle form submission
		console.log('Form submitted:', formData);
		alert('Thank you for your message! This is a demo form.');
	}
</script>

<svelte:head>
	<title>Contact - Michelle's Svelte Site</title>
	<meta name="description" content="Get in touch with Michelle" />
</svelte:head>

<div class="container">
	<header class="header">
		<h1>Get In Touch</h1>
		<p class="subtitle">I'd love to hear from you! Send me a message.</p>
	</header>
	
	<main class="main-content">
		<div class="contact-container">
			<div class="contact-info">
				<h2>Contact Information</h2>
				<div class="info-item">
					<span class="icon">📧</span>
					<div>
						<h3>Email</h3>
						<p>michelle@example.com</p>
					</div>
				</div>
				<div class="info-item">
					<span class="icon">📍</span>
					<div>
						<h3>Location</h3>
						<p>Kansas City, KS</p>
					</div>
				</div>
				<div class="info-item">
					<span class="icon">💼</span>
					<div>
						<h3>LinkedIn</h3>
						<p>https://www.linkedin.com/in/michelle-oliva-espinosa-b74285173/</p>
					</div>
				</div>
			</div>
			
			<div class="contact-form">
				<h2>Send a Message</h2>
				<form on:submit|preventDefault={handleSubmit}>
					<div class="form-group">
						<label for="name">Name</label>
						<input 
							type="text" 
							id="name" 
							bind:value={formData.name}
							required
						/>
					</div>
					
					<div class="form-group">
						<label for="email">Email</label>
						<input 
							type="email" 
							id="email" 
							bind:value={formData.email}
							required
						/>
					</div>
					
					<div class="form-group">
						<label for="message">Message</label>
						<textarea 
							id="message" 
							rows="5"
							bind:value={formData.message}
							required
						></textarea>
					</div>
					
					<button type="submit" class="submit-btn">Send Message</button>
				</form>
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
	
	.contact-container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 3rem;
	}
	
	.contact-info,
	.contact-form {
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(10px);
		border-radius: 20px;
		padding: 2rem;
		box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
		border: 1px solid rgba(255, 255, 255, 0.2);
	}
	
	h2 {
		font-size: 1.8rem;
		margin-bottom: 1.5rem;
		color: #f0f0f0;
	}
	
	.info-item {
		display: flex;
		align-items: center;
		gap: 1rem;
		margin-bottom: 1.5rem;
	}
	
	.icon {
		font-size: 2rem;
		width: 3rem;
		text-align: center;
	}
	
	.info-item h3 {
		font-size: 1.2rem;
		margin: 0 0 0.5rem;
		color: #f0f0f0;
	}
	
	.info-item p {
		margin: 0;
		opacity: 0.9;
	}
	
	.form-group {
		margin-bottom: 1.5rem;
	}
	
	label {
		display: block;
		margin-bottom: 0.5rem;
		font-weight: bold;
		color: #f0f0f0;
	}
	
	input,
	textarea {
		width: 100%;
		padding: 0.75rem;
		border: 1px solid rgba(255, 255, 255, 0.3);
		border-radius: 10px;
		background: rgba(255, 255, 255, 0.1);
		color: white;
		font-size: 1rem;
		transition: border-color 0.3s ease;
	}
	
	input:focus,
	textarea:focus {
		outline: none;
		border-color: #4CAF50;
	}
	
	input::placeholder,
	textarea::placeholder {
		color: rgba(255, 255, 255, 0.6);
	}
	
	.submit-btn {
		background: linear-gradient(45deg, #4CAF50, #45a049);
		color: white;
		border: none;
		padding: 1rem 2rem;
		border-radius: 25px;
		font-size: 1.1rem;
		font-weight: bold;
		cursor: pointer;
		transition: all 0.3s ease;
		width: 100%;
	}
	
	.submit-btn:hover {
		transform: translateY(-2px);
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
	}
	
	@media (max-width: 768px) {
		.contact-container {
			grid-template-columns: 1fr;
			gap: 2rem;
		}
		
		.header h1 {
			font-size: 2rem;
		}
	}
</style>
