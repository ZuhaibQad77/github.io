<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Daily Dose 🌟</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>🌟 Daily Dose</h1>
    <div class="quote-box">
      <p id="quote">Click the button to get motivated!</p>
      <span id="author"></span>
    </div>
    <button onclick="getQuote()">🔁 Show Another Quote</button>
    <p class="footer">Made with ❤️ by [YourName]</p>
  </div>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(to right, #4facfe, #00f2fe);
  color: #fff;
  margin: 0;
  padding: 0;
  text-align: center;
}

.container {
  padding: 60px 20px;
}

h1 {
  font-size: 3em;
  margin-bottom: 20px;
}

.quote-box {
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 30px;
  max-width: 600px;
  margin: 0 auto 30px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

#quote {
  font-size: 1.5em;
  font-style: italic;
  margin-bottom: 10px;
}

#author {
  display: block;
  font-size: 1em;
  font-weight: bold;
  margin-top: 10px;
  color: #ffea00;
}

button {
  background-color: #fff;
  color: #007acc;
  border: none;
  padding: 12px 25px;
  font-size: 1em;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s;
}

button:hover {
  background-color: #ffea00;
  color: #333;
}

.footer {
  margin-top: 50px;
  font-size: 0.9em;
  opacity: 0.7;
}
const quotes = [
  {
    text: "Success is not final, failure is not fatal: it is the courage to continue that counts.",
    author: "Winston Churchill"
  },
  {
    text: "Believe you can and you're halfway there.",
    author: "Theodore Roosevelt"
  },
  {
    text: "You are never too old to set another goal or to dream a new dream.",
    author: "C.S. Lewis"
  },
  {
    text: "Dream big and dare to fail.",
    author: "Norman Vaughan"
  },
  {
    text: "It always seems impossible until it's done.",
author: "Nelson Mandela"
  }
];

function getQuote() {
  const random = Math.floor(Math.random() * quotes.length);
  document.getElementById("quote").textContent = `"${quotes[random].text}"`;
  document.getElementById("author").textContent = `— ${quotes[random].author}`;
}

// Load a quote on page load
window.onload = getQuote;
