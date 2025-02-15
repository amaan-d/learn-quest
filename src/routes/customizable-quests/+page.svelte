
<!-- Add your meta tags, stylesheets, and fonts links here -->
<link href="https://fonts.googleapis.com/css?family=Pacifico" rel="stylesheet" />
<link
	href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css"
	rel="stylesheet"
	integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC"
	crossorigin="anonymous"
/>
<link
	rel="stylesheet"
	href="https://fonts.googleapis.com/css?family=Varela+Round&amp;display=swap"
/>
<link
	href="https://fonts.googleapis.com/css2?family=Poppins:wght@500&amp;display=swap"
	rel="stylesheet"
/>
<!-- Phone numbers and navigation container -->

<!-- Header -->
<div class="header">
	<div class="bg-text">
		<div class="section-background parallax">
			<!-- Add a div for the parallax effect -->
			<br />
			<br />
			<h1>
				Welcome to <img
					width="300px"
					src="./LearnQuest_Custom.png"
					alt="LearnQuest Custom"
				/>
			</h1>
		</div>
	</div>
</div>
<br />
<!-- Containers -->

<div class="container" id="home">
	<h2>Enter Your LearnQuest Activity Code</h2>
	<p>Please enter the custom code provided by your teacher to access the activity.</p>
	<form class="d-flex align-items-center" id="codeForm">
		<input
			style="width: 150px; background: #dee2e6; border: 3px gray solid; border-radius: 10px;"
			type="text"
			class="form-control"
			placeholder="Code"
			id="codeInput"
			required
		/>
		<button
			type="submit"
			style="margin-left: 10px; width: 35px; height: 35px; border-radius: 50%; background-color: #198754; border: none; color: white; display: flex; justify-content: center; align-items: center;"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="16"
				height="16"
				fill="currentColor"
				class="bi bi-send"
				viewBox="0 0 16 16"
			>
				<path
					d="M15.854.146a.5.5 0 0 1 .11.54l-5.819 14.547a.75.75 0 0 1-1.329.124l-3.178-4.995L.643 7.184a.75.75 0 0 1 .124-1.33L15.314.037a.5.5 0 0 1 .54.11ZM6.636 10.07l2.761 4.338L14.13 2.576zm6.787-8.201L1.591 6.602l4.339 2.76z"
				/>
			</svg>
		</button>
	</form>
	<div id="warning" style="color:red; margin-left: 10px; margin-top: 3px;">
		<span><img src="" alt="" /></span>
	</div>

	<!-- Link to external JS file -->
	<!-- Link to external JS file -->
	<!-- Link to external JS file -->
	<!-- Link to external JS file -->
	<script src="./formScript.js"></script>
</div>

<div style="margin-top: 20px;" class="container" id="home">
	<h2>Create A LearnQuest Activity</h2>
	<p>
		Click below to create your very own, customizable LearnQuest activity for anyone to use!
	</p>
	<button type="button" class="btn">Make a quest in 3 modes:</button>
	<div class="btn-group" role="group">
		<button type="button" class="btn btn-primary">QuestRunner</button>
		<button
			type="button"
			class="btn btn-warning"
			onClick="location.replace('/customizable-quests/questmaker')"
		>
			Regular Quiz
		</button>
		<button type="button" class="btn btn-success">Timed Quiz</button>
	</div>
	<br />
	QuestRunner
	<ul>
		<li>This is the platformer available by LearnQuest.</li>
		<li>Will allow users to save the progress on any level they have done in the past.</li>
	</ul>
	Regular Quiz
	<ul>
		<li>
			This is simple quiz that students can take to learn their material. No gaming involved.
		</li>
		<li>Students can see their answers at the very end of the quiz.</li>
		<li>Students can lose points for not answering the question.</li>
	</ul>
	Timed Quiz
	<ul>
		<li>
			This is simple quiz that students can take to learn their material. No gaming involved.
		</li>
		<li>Students can see their answers at the very end of the quiz.</li>
		<li>
			You can set at time limit for students to complete the test. All incomplete answers will
			automatically be submitted.
		</li>
	</ul>
</div>
<div class="nbutton-container">
	<button onclick="location.replace('/')" class="nbutton">
	  <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
		<path fill="#ffffff" d="M575.8 255.5c0 18-15 32.1-32 32.1l-32 0 .7 160.2c0 2.7-.2 5.4-.5 8.1l0 16.2c0 22.1-17.9 40-40 40l-16 0c-1.1 0-2.2 0-3.3-.1c-1.4 .1-2.8 .1-4.2 .1L416 512l-24 0c-22.1 0-40-17.9-40-40l0-24 0-64c0-17.7-14.3-32-32-32l-64 0c-17.7 0-32 14.3-32 32l0 64 0 24c0 22.1-17.9 40-40 40l-24 0-31.9 0c-1.5 0-3-.1-4.5-.2c-1.2 .1-2.4 .2-3.6 .2l-16 0c-22.1 0-40-17.9-40-40l0-112c0-.9 0-1.9 .1-2.8l0-69.7-32 0c-18 0-32-14-32-32.1c0-9 3-17 10-24L266.4 8c7-7 15-8 22-8s15 2 21 7L564.8 231.5c8 7 12 15 11 24z"/>
	  </svg>
	  <span>BACK TO HOME</span>
	</button>
  </div>

<style>
	/* Reset some default styles */

	/* Container styles */
	.container {
		max-width: 800px;
		margin: 0 auto;
		padding: 20px;
		background-color: #c8aeb9;
		border-radius: 5px;
		transition: transform 0.5s ease-in-out;
	}

	.container h2,
	.container p {
		font-family: 'Varela Round', sans-serif;
	}

	.container h2 {
		font-size: 24px;
		color: purple;
	}

	.container p {
		font-size: 16px;
		line-height: 1.6;
	}

	.section-background {
		background-attachment: fixed;
		background-position: center;
		background-size: cover;
		height: 35vh;
		width: 100%;
		text-align: center;
	}

	.parallax {
		background-image: url('background.png');
	}

	.nbutton-container {
	display: flex;
	background-color: rgba(245, 73, 144);
	width: 100%;
	align-items: center;
	justify-content: space-around;
	bottom: 0;
	position: sticky;
  }

  .nbutton {
	outline: 0 !important;
	border: 0 !important;
	height: 50px;
	background-color: transparent;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	color: white;
	transition: all ease-in-out 0.3s;
	cursor: pointer;
  }

  .nbutton svg {
	margin-bottom: 5px;
  }

  .nbutton span {
	font-size: 12px;
	width: 100%;
  }

  .nbutton:hover {
	transform: translateY(-3px);
  }

</style>
