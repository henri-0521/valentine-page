<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Be My Valentine? ❤️</title>
<style>
  body {
    text-align: center;
    font-family: 'Arial', sans-serif;
    background-color: #ffe6eb;
    color: #d6336c;
  }

  h1 {
    margin-top: 50px;
    font-size: 2.5em;
  }

  .button-container {
    display: flex;
    justify-content: center;
    margin-top: 30px;
  }

  .yes-button, .no-button {
    padding: 15px 30px;
    margin: 0 15px;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    border: 3px solid #d6336c;
    border-radius: 10px;
    transition: all 0.3s ease;
  }

  .yes-button {
    background-color: #ff4d6d;
    color: white;
  }

  .yes-button:hover {
    background-color: #c9184a;
    border-color: #c9184a;
  }

  .no-button {
    background-color: #ffccd5;
    color: #d6336c;
  }

  .no-button:hover {
    background-color: #ffb3c1;
  }

  #yes-gif {
    display: none;
    margin-top: 20px;
    width: 300px;
    border-radius: 10px;
  }

  .gif-container {
    display: flex;
    justify-content: center;
    margin-top: 20px;
  }
</style>
</head>
<body>
  <h1 id="valentine-text">Will you be my Valentine? 💕</h1>
  <div class="button-container">
    <button class="yes-button" onclick="handleYesClick()">Yes ❤️</button>
    <button class="no-button" onclick="handleNoClick()">No 💔</button>
  </div>

  <!-- Centered GIF Container -->
  <div class="gif-container">
    <img id="yes-gif" src="https://media.giphy.com/media/26FLdmIp6wJr91JAI/giphy.gif" alt="Happy Valentine GIF">
  </div>

<script>
  let messages = [
    "Are you sure? 😢", 
    "Think again! 💘", 
    "Last chance! 💞", 
    "Please Jagiya? 🥺💕"
  ];
  let messagesIndex = 0;

  function handleNoClick() {
    const noButton = document.querySelector(".no-button");
    const yesButton = document.querySelector(".yes-button");

    noButton.textContent = messages[messagesIndex];
    messagesIndex = (messagesIndex + 1) % messages.length;
    
    const currentSize = parseFloat(window.getComputedStyle(yesButton).fontSize);
    yesButton.style.fontSize = `${currentSize * 1.5}px`;
  }

  function handleYesClick() {
    document.getElementById("valentine-text").textContent = "Yay! You said yes, Murkyotieeeee! 😍";
    document.querySelector(".button-container").style.display = "none"; // Hide buttons
    document.getElementById("yes-gif").style.display = "block"; // Show GIF
  }
</script>
</body>
</html>
# valentine-page
