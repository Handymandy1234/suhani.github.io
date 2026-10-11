<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Suhani 💖</title>
<!-- Beautiful Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@500;700&display=swap" rel="stylesheet">
<!-- Confetti Library for the final page -->
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

<style>
/* CSS styling for a colorful, beautiful look */
* {
box-sizing: border-box;
margin: 0;
padding: 0;
font-family: 'Quicksand', sans-serif;
}

body {
/* Colorful animated background */
background: linear-gradient(-45deg, #ff9a9e, #fecfef, #a1c4fd, #c2e9fb);
background-size: 400% 400%;
animation: gradientBG 15s ease infinite;
height: 100vh;
display: flex;
justify-content: center;
align-items: center;
overflow: hidden;
color: #333;
}

@keyframes gradientBG {
0% { background-position: 0% 50%; }
50% { background-position: 100% 50%; }
100% { background-position: 0% 50%; }
}

.container {
width: 90%;
max-width: 600px;
position: relative;
}

.page {
display: none; /* Hide all pages by default */
flex-direction: column;
align-items: center;
text-align: center;
background: rgba(255, 255, 255, 0.6);
backdrop-filter: blur(15px);
-webkit-backdrop-filter: blur(15px);
border-radius: 25px;
padding: 40px 30px;
box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.2);
border: 1px solid rgba(255, 255, 255, 0.7);
animation: fadeIn 0.5s ease forwards;
}

.page.active {
display: flex; /* Show only the active page */
}

@keyframes fadeIn {
from { opacity: 0; transform: translateY(20px) scale(0.95); }
to { opacity: 1; transform: translateY(0) scale(1); }
}

h1 {
font-family: 'Fredoka One', cursive;
color: #ff6b6b;
font-size: 2.5rem;
margin-bottom: 10px;
letter-spacing: 1px;
}

h2 {
color: #4a4e69;
margin-bottom: 20px;
font-size: 1.5rem;
}

p {
font-size: 1.1rem;
line-height: 1.6;
margin-bottom: 20px;
}

/* Buttons */
.btn {
background: linear-gradient(135deg, #ff758c 0%, #ff7eb3 100%);
color: white;
border: none;
padding: 15px 30px;
font-size: 1.2rem;
font-weight: 700;
border-radius: 50px;
cursor: pointer;
transition: transform 0.2s, box-shadow 0.2s;
margin-top: 15px;
width: 100%;
max-width: 300px;
}

.btn:hover {
transform: translateY(-3px);
box-shadow: 0 10px 20px rgba(255, 117, 140, 0.4);
}

.btn.secondary {
background: linear-gradient(135deg, #89f7fe 0%, #66a6ff 100%);
}

/* Quiz Options */
.quiz-option {
background: rgba(255, 255, 255, 0.9);
border: 2px solid transparent;
padding: 15px;
margin: 10px 0;
border-radius: 15px;
cursor: pointer;
width: 100%;
font-weight: 700;
color: #4a4e69;
transition: all 0.3s;
}

.quiz-option:hover {
border-color: #ff7eb3;
background: #fff0f5;
transform: scale(1.02);
}

.quiz-option.selected {
background: #ff7eb3;
color: white;
border-color: #ff758c;
}

/* Photo Placeholders */
.photo-box {
width: 100%;
height: 250px;
background-color: rgba(255,255,255,0.5);
border: 3px dashed #ff7eb3;
border-radius: 15px;
display: flex;
justify-content: center;
align-items: center;
margin-bottom: 20px;
overflow: hidden;
color: #ff7eb3;
font-weight: bold;
}

.photo-box img {
width: 100%;
height: 100%;
object-fit: cover; /* Keeps image looking good */
}

.hidden-message {
display: none;
color: #ff6b6b;
font-weight: bold;
margin-top: 15px;
font-size: 1.2rem;
animation: fadeIn 0.3s ease forwards;
}
</style>
</head>
<body>

<div class="container">

<!-- PAGE 1: Welcome -->
<div id="page1" class="page active">
<h1>Hey Suhani! 💖</h1>
<p>Welcome to your personal 23rd Birthday Experience.</p>
<p>I didn't want to just give you a card, so I made this tiny corner of the internet just for you. Ready to go down memory lane (and take a highly unscientific quiz)?</p>
<button class="btn" onclick="nextPage('page2')">Let's Go! ✨</button>
</div>

<!-- PAGE 2: Fun Quiz Question 1 -->
<div id="page2" class="page">
<h2>Question 1 🕵️‍♀️</h2>
<p>At 23 years old, what is your most defining superpower?</p>

<div class="quiz-option" onclick="selectOption(this, 'msg1')">A) Sleeping for 12 hours straight</div>
<div class="quiz-option" onclick="selectOption(this, 'msg1')">B) Stealing my clothes and denying it</div>
<div class="quiz-option" onclick="selectOption(this, 'msg1')">C) Complaining about back pain like a 60-year-old</div>
<div class="quiz-option" onclick="selectOption(this, 'msg1')">D) Being a pretty awesome sister (sometimes)</div>

<div id="msg1" class="hidden-message">Honestly, it's all of the above. 😂</div>

<button id="btn1" class="btn secondary" style="display:none;" onclick="nextPage('page3')">Next Page ➡️</button>
</div>

<!-- PAGE 3: Memory 1 -->
<div id="page3" class="page">
<h1>Remember this? 📸</h1>

<!-- ADD YOUR PHOTO HERE: Replace the text inside the div with an <img> tag -->
<!-- Example: <div class="photo-box"><img src="your-photo-name.jpg" alt="Memory"></div> -->
<div class="photo-box">
[Put a funny/cute photo of you two here]
</div>

<p>Whether we are fighting over stupid things or laughing until we can't breathe, memories like this remind me why you're stuck with me forever.</p>
<button class="btn" onclick="nextPage('page4')">Next Question! ➡️</button>
</div>

<!-- PAGE 4: Fun Quiz Question 2 -->
<div id="page4" class="page">
<h2>Question 2 👑</h2>
<p>Who is clearly the favorite child?</p>

<div class="quiz-option" onclick="selectOption(this, 'msg2')">A) Me (The brilliant creator of this website)</div>
<div class="quiz-option" onclick="selectOption(this, 'msg2')">B) You (Suhani)</div>
<div class="quiz-option" onclick="selectOption(this, 'msg2')">C) The dog/cat (If applicable)</div>

<div id="msg2" class="hidden-message">Nice try! But today is your birthday, so I'll let you pretend it's you. 😉</div>

<button id="btn2" class="btn secondary" style="display:none;" onclick="nextPage('page5')">Next Page ➡️</button>
</div>

<!-- PAGE 5: Final Message & Confetti -->
<div id="page5" class="page">
<h1>Happy 23rd, Suhani! 🎉</h1>

<!-- ADD YOUR PHOTO HERE -->
<div class="photo-box">
[Put a beautiful picture of her here]
</div>

<p>I hope you have the most amazing 23rd year. Thank you for being you—beautiful, annoying, funny, and simply the best sister I could ask for. </p>
<p>I love you tons! Have the happiest birthday ever! 🎂💖</p>

<button class="btn" onclick="triggerConfetti()">Pop more confetti! 🎊</button>
<button class="btn secondary" onclick="nextPage('page1')" style="margin-top: 10px;">Play Again 🔄</button>
</div>

</div>

<!-- JavaScript to make everything work -->
<script>
// Function to move between pages
function nextPage(targetPageId) {
// Hide all pages
const pages = document.querySelectorAll('.page');
pages.forEach(page => {
page.classList.remove('active');
});

// Show target page
const target = document.getElementById(targetPageId);
target.classList.add('active');

// If it's the last page, shoot confetti automatically!
if (targetPageId === 'page5') {
triggerConfetti();
setTimeout(triggerConfetti, 1000); // shoot again a second later
}
}

// Function for the quiz options
function selectOption(element, messageId) {
// Remove 'selected' class from siblings
let siblings = element.parentNode.querySelectorAll('.quiz-option');
siblings.forEach(sib => sib.classList.remove('selected'));

// Add 'selected' to clicked option
element.classList.add('selected');

// Show the funny message
let msg = document.getElementById(messageId);
msg.style.display = 'block';

// Show the 'Next' button related to this page
let nextBtn = element.parentNode.querySelector('.btn.secondary');
if(nextBtn) {
nextBtn.style.display = 'block';
}
}

// Function to shoot beautiful confetti
function triggerConfetti() {
var duration = 3000;
var end = Date.now() + duration;

(function frame() {
confetti({
particleCount: 5,
angle: 60,
spread: 55,
origin: { x: 0 },
colors: ['#ff9a9e', '#fecfef', '#a1c4fd']
});
confetti({
particleCount: 5,
angle: 120,
spread: 55,
origin: { x: 1 },
colors: ['#ff9a9e', '#fecfef', '#a1c4fd']
});

if (Date.now() < end) {
requestAnimationFrame(frame);
}
}());
}
</script>
</body>
</html>
