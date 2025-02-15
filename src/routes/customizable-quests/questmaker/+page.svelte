<script>
	import 'bootstrap/dist/css/bootstrap.min.css';
	import './questmaker.css';
</script>

<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Quiz Maker</title>
	</head>
	<body>
		<div class="container mt-5">
			<h4 class="mb-4">Create Your Quiz</h4>
			<form id="quizForm">
				<div class="mb-3 form-section">
					<label for="quizTitle" class="form-label required">Quiz Title</label>
					<input
						type="text"
						class="form-control"
						id="quizTitle"
						name="quizTitle"
						placeholder="Enter the quiz title"
						required
					/>
					<label for="name" class="form-label required">Your Name</label>
					<input
						type="text"
						class="form-control"
						id="name"
						name="name"
						placeholder="Enter your name"
						required
					/>
					<label for="email" class="form-label required">Your Email</label>
					<input
						type="email"
						class="form-control"
						id="email"
						name="email"
						placeholder="Enter your email"
						required
					/>
				</div>

				<!-- Questions Section -->
				<div id="questions-container">
					<h4 class="mb-4">Questions</h4>
					<div class="mb-3 form-section question" id="question1">
						<label for="question1Text" class="form-label required">Question 1</label>
						<input
							type="text"
							class="form-control"
							id="question1Text"
							name="question1Text"
							placeholder="Enter the question"
							required
						/>
						<div class="mb-3">
							<label class="form-label required">Answer Choices</label>
							<input
								type="text"
								class="form-control"
								id="answer1A"
								name="answer1A"
								placeholder="Enter Answer A"
								required
							/>
							<input
								type="text"
								class="form-control"
								id="answer1B"
								name="answer1B"
								placeholder="Enter Answer B"
								required
							/>
							<input
								type="text"
								class="form-control"
								id="answer1C"
								name="answer1C"
								placeholder="Enter Answer C (optional)"
							/>
							<input
								type="text"
								class="form-control"
								id="answer1D"
								name="answer1D"
								placeholder="Enter Answer D (optional)"
							/>
						</div>
						<label for="correctAnswer1" class="form-label required">
							Select Correct Answer
						</label>
						<select
							class="form-select"
							id="correctAnswer1"
							name="correctAnswer1"
							required
						>
							<option value="">-- Select Correct Answer --</option>
							<option value="A">Answer A</option>
							<option value="B">Answer B</option>
							<option value="C">Answer C</option>
							<option value="D">Answer D</option>
						</select>
					</div>
				</div>

				<!-- Add More Questions Button -->
				<button type="button" class="btn btn-secondary mb-3" id="addMoreQuestions">
					Add More Questions
				</button>
				<button type="submit" class="btn btn-primary mb-3">
					Create <span>OR</span>
					Save Quiz
				</button>
			</form>
		</div>

		<!-- Success Modal -->
		<div
			class="modal fade"
			id="successModal"
			tabindex="-1"
			aria-labelledby="successModalLabel"
			aria-hidden="true"
		>
			<div class="modal-dialog">
				<div class="modal-content">
					<div class="modal-header">
						<h5 class="modal-title" id="successModalLabel">
							Press Submit or Save!
						</h5>
						<button
							type="button"
							class="btn-close"
							data-bs-dismiss="modal"
							aria-label="Close"
						/>
					</div>
					<div class="modal-body">
						<span class="text" />
						<span style="visibility: hidden;" id="quizLink" />
					</div>
					<div class="modal-footer" id="modal-footer">
						<button
							type="submit"
							class="btn btn-primary"
							onclick="submit()"
							aria-label="Submit"
						>
							Create Quiz
						</button>
						<button
							type="save"
							class="btn btn-info"
							onclick="save()"
							aria-label="Submit"
						>
							Save Progress
						</button>
					</div>
				</div>
			</div>
		</div>
		<div class="nbutton-container">
			<button onclick="location.replace('/customizable-quests')" class="nbutton">
			  <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
				<path fill="#ffffff" d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z"/>
			  </svg>
			  <span>BACK</span>
			</button>
			<button onclick="location.replace('/')" class="nbutton">
			  <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
				<path fill="#ffffff" d="M575.8 255.5c0 18-15 32.1-32 32.1l-32 0 .7 160.2c0 2.7-.2 5.4-.5 8.1l0 16.2c0 22.1-17.9 40-40 40l-16 0c-1.1 0-2.2 0-3.3-.1c-1.4 .1-2.8 .1-4.2 .1L416 512l-24 0c-22.1 0-40-17.9-40-40l0-24 0-64c0-17.7-14.3-32-32-32l-64 0c-17.7 0-32 14.3-32 32l0 64 0 24c0 22.1-17.9 40-40 40l-24 0-31.9 0c-1.5 0-3-.1-4.5-.2c-1.2 .1-2.4 .2-3.6 .2l-16 0c-22.1 0-40-17.9-40-40l0-112c0-.9 0-1.9 .1-2.8l0-69.7-32 0c-18 0-32-14-32-32.1c0-9 3-17 10-24L266.4 8c7-7 15-8 22-8s15 2 21 7L564.8 231.5c8 7 12 15 11 24z"/>
			  </svg>
			  <span>HOME</span>
			</button>
		  </div>
		<script
			src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"
		></script>
		<script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app-compat.js"></script>
		<script
			src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore-compat.js"
		></script>

		<script>
			function save() {
				let quizLink = document.getElementById('quizLink');
				quizLink.style.visibility = 'hidden';
				document.querySelector('.text').innerHTML = "<p>Your quiz has been successfully saved! If you return to the app later, your form progress will still be available.<br>However, you won't be able to create another 'Regular Quiz' on this device until you submit this form and start a new one.</p><span style='visibility: hidden;' id='quizLink'></span>";
				document.querySelector('.modal-title').innerHTML = "Your quiz has been saved!";
				document.querySelector('.modal-footer').innerHTML = "<button type='button' class='btn btn-secondary' data-bs-dismiss='modal' aria-label='Close'>Close</button";
			}

			function submit() {
				document.querySelector('.text').innerHTML = "<p>Your quiz has been created! If you close this message without clicking 'Reset' and click 'Submit' again, a new link will be generated. Rest assured, the old link will still be valid.<br>Refreshing the page will preserve your form data, but if you'd like to start with a blank form next time, click the 'Reset' button below.<br><br><button onclick='localStorage.removeItem(\"quizData\");' class='btn btn-warning'>Reset</button><br><br>Here's the link to your submitted quiz:</p>";
				document.querySelector('.modal-title').innerHTML = "Your quiz has been submitted!";
				document.querySelector('.modal-footer').innerHTML = "<button type='button' class='btn btn-secondary' data-bs-dismiss='modal' aria-label='Close'>Close</button";

				let quizLink = document.getElementById('quizLink');
				quizLink.style.visibility = 'visible';
			}
			// Initialize Firebase
			const firebaseConfig = {
				apiKey: 'AIzaSyAznAZx-vJNIzBEZs6Ha2BNBpbbr1GlZH0',
				authDomain: 'learnquest---quizmaker.firebaseapp.com',
				projectId: 'learnquest---quizmaker',
				storageBucket: 'learnquest---quizmaker.appspot.com',
				messagingSenderId: '309131964781',
				appId: '1:309131964781:web:153bc4f6dbbea5d53a6a64',
			};
			firebase.initializeApp(firebaseConfig);
			const db = firebase.firestore();

			// Save form data to localStorage
			function saveToLocalStorage() {
				const formData = new FormData(document.getElementById('quizForm'));
				const data = {
					title: formData.get('quizTitle'),
					creator: formData.get('name'),
					email: formData.get('email'),
					questions: [],
				};

				for (let i = 1; i <= questionCount; i++) {
					const questionText = formData.get(`question${i}Text`);
					const correctAnswer = formData.get(`correctAnswer${i}`);
					if (questionText && correctAnswer) {
						data.questions.push({
							text: questionText,
							answers: {
								A: formData.get(`answer${i}A`),
								B: formData.get(`answer${i}B`),
								C: formData.get(`answer${i}C`) || null,
								D: formData.get(`answer${i}D`) || null,
							},
							correct: correctAnswer,
						});
					}
				}

				localStorage.setItem('quizData', JSON.stringify(data));
			}

			// Retrieve form data from localStorage
			function loadFromLocalStorage() {
				const savedData = localStorage.getItem('quizData');
				if (!savedData) return;
				const data = JSON.parse(savedData);

				document.getElementById('quizTitle').value = data.title || '';
				document.getElementById('name').value = data.creator || '';
				document.getElementById('email').value = data.email || '';

				// Load questions dynamically and their respective inputs
				data.questions.forEach((question, index) => {
					if (index > 0) {
						questionCount++;
						addNewQuestion();
					}
					document.getElementById(`question${index + 1}Text`).value = question.text;
					document.getElementById(`answer${index + 1}A`).value = question.answers.A;
					document.getElementById(`answer${index + 1}B`).value = question.answers.B;
					document.getElementById(`answer${index + 1}C`).value = question.answers.C || '';
					document.getElementById(`answer${index + 1}D`).value = question.answers.D || '';
					document.getElementById(`correctAnswer${index + 1}`).value = question.correct;
				});
			}

			// Add More Questions Functionality
			let questionCount = 1;
			document.getElementById('addMoreQuestions').addEventListener('click', function () {
				if (questionCount < 10) {
					questionCount++;
					addNewQuestion();
				} else {
					alert('You can only add up to 10 questions.');
				}
			});

			// Create a new question dynamically
			function addNewQuestion() {
				const questionContainer = document.createElement('div');
				questionContainer.classList.add('mb-3', 'form-section', 'question');
				questionContainer.id = `question${questionCount}`;
				questionContainer.innerHTML = `
				<label for="question${questionCount}Text" class="form-label required">Question ${questionCount}</label>
				<input type="text" class="form-control" id="question${questionCount}Text" name="question${questionCount}Text" placeholder="Enter the question" required />
				<div class="mb-3">
					<label class="form-label required">Answer Choices</label>
					<input type="text" class="form-control" id="answer${questionCount}A" name="answer${questionCount}A" placeholder="Enter Answer A" required />
					<input type="text" class="form-control" id="answer${questionCount}B" name="answer${questionCount}B" placeholder="Enter Answer B" required />
					<input type="text" class="form-control" id="answer${questionCount}C" name="answer${questionCount}C" placeholder="Enter Answer C (optional)" />
					<input type="text" class="form-control" id="answer${questionCount}D" name="answer${questionCount}D" placeholder="Enter Answer D (optional)" />
				</div>
				<label for="correctAnswer${questionCount}" class="form-label required">Select Correct Answer</label>
				<select class="form-select" id="correctAnswer${questionCount}" name="correctAnswer${questionCount}" required>
					<option value="">-- Select Correct Answer --</option>
					<option value="A">Answer A</option>
					<option value="B">Answer B</option>
					<option value="C">Answer C</option>
					<option value="D">Answer D</option>
				</select>
				`;

				document.getElementById('questions-container').appendChild(questionContainer);
			}

			// Handle form submission
			document.getElementById('quizForm').addEventListener('submit', async function (e) {
				e.preventDefault();

				const formData = new FormData(this);
				let quizData = {
					title: formData.get('quizTitle'),
					creator: formData.get('name'),
					email: formData.get('email'),
					questions: [],
				};

				for (let i = 1; i <= questionCount; i++) {
					let questionText = formData.get(`question${i}Text`);
					let correctAnswer = formData.get(`correctAnswer${i}`);
					if (!questionText || !correctAnswer) continue;
					quizData.questions.push({
						text: questionText,
						answers: {
							A: formData.get(`answer${i}A`),
							B: formData.get(`answer${i}B`),
							C: formData.get(`answer${i}C`) || null,
							D: formData.get(`answer${i}D`) || null,
						},
						correct: correctAnswer,
					});
				}

				try {
					let docRef = await db.collection('quizzes').add(quizData);
					// Show the modal with the success message
					const quizLink = `/quiz.html?id=${docRef.id}`;
					document.getElementById('quizLink').innerHTML = `<a href="${quizLink}">Click to access the quiz</a>`;


					// Show the success modal
					const successModal = new bootstrap.Modal(
						document.getElementById('successModal'),
					);
					successModal.show();
				} catch (error) {
					location.replace('/message/QMfail');
				}
			});

			document.getElementById('quizForm').addEventListener('save', async function (e) {
				e.preventDefault();

				const formData = new FormData(this);
				let quizData = {
					title: formData.get('quizTitle'),
					creator: formData.get('name'),
					email: formData.get('email'),
					questions: [],
				};

				for (let i = 1; i <= questionCount; i++) {
					let questionText = formData.get(`question${i}Text`);
					let correctAnswer = formData.get(`correctAnswer${i}`);
					if (!questionText || !correctAnswer) continue;
					quizData.questions.push({
						text: questionText,
						answers: {
							A: formData.get(`answer${i}A`),
							B: formData.get(`answer${i}B`),
							C: formData.get(`answer${i}C`) || null,
							D: formData.get(`answer${i}D`) || null,
						},
						correct: correctAnswer,
					});
				}

				try {
					let docRef = await db.collection('quizzes').add(quizData);
					// Show the modal with the success message
					const quizLink = `/quiz.html?id=${docRef.id}`;
					document.getElementById('quizLink').textContent = quizLink;

					// Show the success modal
					const successModal = new bootstrap.Modal(
						document.getElementById('successModal'),
					);
					successModal.show();
				} catch (error) {
					location.replace('/message/QMfail');
				}
			});

			// Load data when the page is loaded
			window.addEventListener('load', function () {
				loadFromLocalStorage();
			});

			// Save data whenever a user interacts with the form
			document.getElementById('quizForm').addEventListener('input', saveToLocalStorage);
		</script>
	</body>
</html>
