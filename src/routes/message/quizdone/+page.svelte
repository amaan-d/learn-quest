<body>
	<div class="card">
		<div class="header">
			<div class="image">
				<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<g id="SVGRepo_bgCarrier" stroke-width="0" />
					<g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round" />
					<g id="SVGRepo_iconCarrier">
						<path
							d="M20 7L9.00004 18L3.99994 13"
							stroke="#000000"
							stroke-width="1.5"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
					</g>
				</svg>
			</div>
			<div class="content">
				<span class="title">Quiz submitted</span>
				<p class="message">
					Your quiz has been finished. A PDF should have started downloading. This PDF contains your quiz results.
				</p>
			</div>
			<div class="actions">
				<button onclick="location.replace('/')" class="history" type="button">Back to Home Page</button>
			</div>
		</div>
	</div>
</body>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');
	body {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 100vh;
		margin: 0;
		background-color: #f0f0f0; /* Optional, for better background contrast */
	}

	.card {
		overflow: hidden;
		position: relative;
		text-align: left;
		border-radius: 0.5rem;
		max-width: 290px;
		box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
		background-color: #fff;
		margin-left: auto;
		margin-right: auto;
		font-family: 'Inter';
	}

	.header {
		padding: 1.25rem 1rem 1rem 1rem;
	}

	.image {
		display: flex;
		margin-left: auto;
		margin-right: auto;
		background-color: #e2feee;
		flex-shrink: 0;
		justify-content: center;
		align-items: center;
		width: 3rem;
		height: 3rem;
		border-radius: 9999px;
		animation: animate 0.6s linear alternate-reverse infinite;
		transition: 0.6s ease;
	}

	.image svg {
		color: #0afa2a;
		width: 2rem;
		height: 2rem;
	}

	.content {
		margin-top: 0.75rem;
		text-align: center;
	}

	.title {
		color: #066e29;
		font-size: 1rem;
		font-weight: 600;
		line-height: 1.5rem;
	}

	.message {
		margin-top: 0.5rem;
		color: #595b5f;
		font-size: 0.875rem;
		line-height: 1.25rem;
	}

	.actions {
		margin: 0.75rem 1rem;
	}

	.history {
	display: inline-flex;
	padding: 0.5rem 1rem;
	background-color: #1aa06d;
	color: #ffffff;
	font-size: 1rem;
	line-height: 1.5rem;
	font-weight: 500;
	justify-content: center;
	width: 100%;
	border-radius: 0.375rem;
	border: none;
	box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
	cursor: pointer;
	transition: transform 0.3s ease, background-color 0.3s ease; /* Smooth transition */
}

.history:hover {
	transform: scale(1.05); /* Scale up the button slightly */
	background-color: #179c5c; /* Darken the background on hover */
}


	@keyframes animate {
		from {
			transform: scale(1);
		}

		to {
			transform: scale(1.09);
		}
	}
</style>
