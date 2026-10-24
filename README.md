<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#081426">
<title>BET FIXED SITE | Correct Score Predictions</title>

<style>
:root {
  --bg: #081426;
  --panel: #12213a;
  --panel2: #192b47;
  --gold: #f5c542;
  --green: #20d889;
  --text: #f5f7fb;
  --muted: #9aabc4;
  --red: #ff6262;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  font-family: Arial, sans-serif;
  padding-bottom: 85px;
}

header {
  background: linear-gradient(135deg,#102d50,#081426);
  padding: 22px 16px;
  border-bottom: 1px solid #263b58;
}

.brand {
  color: var(--gold);
  font-size: 23px;
  font-weight: 900;
  letter-spacing: .5px;
}

.subtitle {
  color: var(--muted);
  margin-top: 6px;
  font-size: 13px;
}

.container {
  max-width: 650px;
  margin: auto;
  padding: 16px;
}

.hero {
  padding: 20px;
  border-radius: 16px;
  background: linear-gradient(135deg,#174d42,#12213a);
  margin-bottom: 20px;
}

.hero h1 {
  font-size: 24px;
  margin: 0 0 10px;
}

.hero p {
  color: #d0dfed;
  line-height: 1.5;
}

.badge {
  display: inline-block;
  color: #081426;
  background: var(--gold);
  border-radius: 20px;
  padding: 6px 10px;
  font-size: 11px;
  font-weight: bold;
}

.section-title {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 22px 0 12px;
}

.section-title h2 {
  font-size: 18px;
  margin: 0;
}

.card {
  background: var(--panel);
  border: 1px solid #253955;
  border-radius: 14px;
  padding: 16px;
  margin-bottom: 13px;
}

.league {
  color: var(--muted);
  font-size: 12px;
  margin-bottom: 12px;
}

.teams {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  gap: 8px;
  text-align: center;
}

.team {
  font-weight: bold;
  line-height: 1.4;
}

.vs {
  color: var(--muted);
  font-size: 12px;
}

.match-time {
  color: var(--muted);
  font-size: 12px;
  margin-top: 12px;
}

.prediction {
  background: #0a182b;
  border-radius: 10px;
  padding: 12px;
  margin-top: 14px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.score {
  color: var(--green);
  font-size: 23px;
  font-weight: 900;
}

.locked {
  color: var(--gold);
  font-size: 12px;
  font-weight: bold;
}

button {
  cursor: pointer;
  border: 0;
  border-radius: 9px;
  padding: 12px 15px;
  font-weight: bold;
  font-size: 14px;
}

button:disabled {
  opacity: .6;
  cursor: wait;
}

.btn-gold {
  background: var(--gold);
  color: #081426;
}

.btn-green {
  background: var(--green);
  color: #081426;
}

.btn-dark {
  background: var(--panel2);
  color: white;
  border: 1px solid #354b69;
}

.btn-full { width: 100%; }

input, select {
  width: 100%;
  padding: 13px;
  border-radius: 9px;
  border: 1px solid #344965;
  background: #09172a;
  color: white;
  margin: 8px 0 14px;
  font-size: 15px;
}

label {
  display: block;
  font-size: 13px;
  color: #d5dfed;
}

.notice {
  padding: 13px;
  border-radius: 9px;
  background: #1a2c45;
  color: #d4e1f1;
  font-size: 13px;
  line-height: 1.5;
  margin: 12px 0;
}

.status {
  font-size: 13px;
  line-height: 1.5;
  margin-top: 12px;
  overflow-wrap: anywhere;
}

.hidden { display: none !important; }

nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 10;
  display: flex;
  justify-content: space-around;
  padding: 10px 5px calc(10px + env(safe-area-inset-bottom));
  background: #0d1b30;
  border-top: 1px solid #2a3d57;
}

nav button {
  background: transparent;
  color: var(--muted);
  padding: 8px;
  font-size: 12px;
}

nav button.active { color: var(--gold); }

footer {
  text-align: center;
  color: var(--muted);
  padding: 25px 10px;
  font-size: 11px;
}

@media (max-width: 380px) {
  .hero h1 { font-size: 21px; }
  .container { padding: 12px; }
}
</style>
</head>

<body>

<header>
  <div class="brand">⚽ BET FIXED SITE</div>
  <div class="subtitle">Football Correct Score Predictions</div>
</header>

<main class="container">

  <section id="home-page">
    <div class="hero">
      <span class="badge">DAILY FOOTBALL PREDICTIONS</span>
      <h1>Welcome to BET FIXED SITE</h1>
      <p>
        Explore football correct-score predictions.
        Check free selections or unlock premium selections
        through the official payment process.
      </p>
      <button class="btn-gold" onclick="showPage('games-page')">
        View Predictions
      </button>
    </div>

    <div class="section-title">
      <h2>Today's Predictions</h2>
      <span class="badge">FOOTBALL</span>
    </div>

    <div id="home-games"></div>
  </section>

  <section id="games-page" class="hidden">
    <div class="section-title">
      <h2>All Predictions</h2>
    </div>
    <div id="all-games"></div>
  </section>

  <section id="payment-page" class="hidden">
    <div class="hero">
      <h1>Premium Access</h1>
      <p>Choose a package and continue to secure checkout.</p>
    </div>

    <div class="card">
      <label for="package">Select package</label>
      <select id="package">
        <option value="100">Daily Premium — GHS 1.00</option>
        <option value="500">Weekly Premium — GHS 5.00</option>
        <option value="1000">Premium Package — GHS 10.00</option>
      </select>

      <label for="phone">Mobile Money number</label>
      <input
        id="phone"
        type="tel"
        inputmode="tel"
        autocomplete="tel"
        placeholder="Enter your phone number"
      >

      <button id="pay-button"
              class="btn-gold btn-full"
              onclick="startPayment()">
        Continue to Payment
      </button>

      <div id="payment-message" class="status" role="status"></div>

      <div class="notice">
        Your premium access should only be activated after the
        payment provider or backend verifies your transaction.
      </div>
    </div>
  </section>

  <section id="history-page" class="hidden">
    <div class="section-title">
      <h2>Prediction History</h2>
    </div>
    <div id="history-list"></div>
  </section>

  <section id="results-page" class="hidden">
    <div class="section-title">
      <h2>Premium Predictions</h2>
    </div>
    <div id="premium-content"></div>
  </section>

</main>

<footer>
  BET FIXED SITE · Football predictions are estimates, not guarantees.
  Please bet responsibly.
</footer>

<nav>
  <button data-page="home-page" class="active"
          onclick="showPage('home-page',this)">⌂<br>Home</button>
  <button data-page="games-page"
          onclick="showPage('games-page',this)">⚽<br>Games</button>
  <button data-page="payment-page"
          onclick="showPage('payment-page',this)">₵<br>Payment</button>
  <button data-page="history-page"
          onclick="showPage('history-page',this)">◷<br>History</button>
</nav>

<script>
/*
  BET FIXED SITE CONFIGURATION

  Public website:
  - Uses BACKEND_URL to contact your backend.
  - Never put the Dreamo Pay secret key in this file.

  Replace BACKEND_URL after deploying your backend.
*/
const BACKEND_URL = "https://YOUR-BACKEND-URL";

/*
  Replace these example matches with your actual predictions.
  Do not advertise predictions as guaranteed or "fixed" results.
*/
const games = [
  {
    id: "game-001",
    league: "Example League",
    time: "18:30",
    home: "Team A",
    away: "Team B",
    score: "1 - 0",
    type: "free"
  },
  {
    id: "game-002",
    league: "Example League",
    time: "19:00",
    home: "Team C",
    away: "Team D",
    score: "2 - 1",
    type: "premium"
  },
  {
    id: "game-003",
    league: "Weekend Selection",
    time: "20:00",
    home: "Team E",
    away: "Team F",
    score: "1 - 1",
    type: "premium"
  }
];

function showPage(pageId, button) {
  document.querySelectorAll("main section").forEach(section => {
    section.classList.add("hidden");
  });

  document.getElementById(pageId).classList.remove("hidden");

  document.querySelectorAll("nav button").forEach(btn => {
    btn.classList.remove("active");
  });

  const activeButton = button ||
    document.querySelector(`nav button[data-page="${pageId}"]`);

  if (activeButton) activeButton.classList.add("active");

  if (pageId === "history-page") renderHistory();
  if (pageId === "results-page") renderPremium();
}

function makeGameCard(game) {
  const card = document.createElement("article");
  card.className = "card";

  const league = document.createElement("div");
  league.className = "league";
  league.textContent = game.league;

  const teams = document.createElement("div");
  teams.className = "teams";

  const home = document.createElement("div");
  home.className = "team";
  home.textContent = game.home;

  const vs = document.createElement("div");
  vs.className = "vs";
  vs.textContent = "VS";

  const away = document.createElement("div");
  away.className = "team";
  away.textContent = game.away;

  teams.append(home, vs, away);

  const time = document.createElement("div");
  time.className = "match-time";
  time.textContent = "Kick-off: " + game.time;

  const prediction = document.createElement("div");
  prediction.className = "prediction";

  const left = document.createElement("div");

  const label = document.createElement("div");
  label.className = "league";
  label.textContent = game.type === "free"
    ? "FREE PREDICTION"
    : "PREMIUM PREDICTION";

  const score = document.createElement("div");
  score.className = game.type === "free" ? "score" : "locked";
  score.textContent = game.type === "free"
    ? game.score
    : "🔒 PREMIUM";

  left.append(label, score);

  const button = document.createElement("button");

  if (game.type === "free") {
    button.className = "btn-green";
    button.textContent = "View";
    button.onclick = () => {
      addHistory(game.id, "Viewed free prediction");
      alert("Prediction: " + game.score);
    };
  } else {
    button.className = "btn-gold";
    button.textContent = "Unlock";
    button.onclick = () => {
      showPage("payment-page");
    };
  }

  prediction.append(left, button);
  card.append(league, teams, time, prediction);

  return card;
}

function renderGames() {
  const home = document.getElementById("home-games");
  const all = document.getElementById("all-games");

  home.replaceChildren();
  all.replaceChildren();

  games.forEach(game => {
    const card = makeGameCard(game);
    all.appendChild(card.cloneNode(true));
    home.appendChild(card);
  });
}

function addHistory(id, action) {
  let history = JSON.parse(
    localStorage.getItem("betfix_history") || "[]"
  );

  history.unshift({
    id,
    action,
    date: new Date().toLocaleString()
  });

  localStorage.setItem(
    "betfix_history",
    JSON.stringify(history.slice(0, 50))
  );
}

function renderHistory() {
  const list = document.getElementById("history-list");
  list.replaceChildren();

  const history = JSON.parse(
    localStorage.getItem("betfix_history") || "[]"
  );

  if (!history.length) {
    const message = document.createElement("div");
    message.className = "notice";
    message.textContent = "Your prediction activity will appear here.";
    list.appendChild(message);
    return;
  }

  history.forEach(item => {
    const card = document.createElement("div");
    card.className = "card";

    const action = document.createElement("div");
    action.textContent = item.action;

    const date = document.createElement("div");
    date.className = "league";
    date.textContent = item.date;

    card.append(action, date);
    list.appendChild(card);
  });
}

function renderPremium() {
  const container = document.getElementById("premium-content");
  container.replaceChildren();

  const message = document.createElement("div");
  message.className = "notice";
  message.textContent =
    "Premium predictions will appear here after the backend " +
    "verifies your purchase. This browser page alone cannot " +
    "confirm a payment.";
  container.appendChild(message);
}

async function startPayment() {
  const button = document.getElementById("pay-button");
  const message = document.getElementById("payment-message");
  const phone = document.getElementById("phone").value.trim();
  const amount = Number(document.getElementById("package").value);

  if (!phone) {
    message.textContent = "Enter your Mobile Money number.";
    return;
  }

  if (BACKEND_URL.includes("YOUR-BACKEND-URL")) {
    message.textContent =
      "Payment backend not configured yet. Deploy the backend " +
      "and replace BACKEND_URL in this file.";
    return;
  }

  button.disabled = true;
  message.textContent = "Starting secure payment…";

  try {
    const response = await fetch(
      BACKEND_URL.replace(/\/$/, "") + "/api/create-payment",
      {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          phone,
          amount,
          currency: "GHS"
        })
      }
    );

    const result = await response.json();

    if (!response.ok) {
      throw new Error(result.message || "Payment could not start.");
    }

    if (result.checkout_url) {
      window.location.assign(result.checkout_url);
      return;
    }

    message.textContent =
      result.message || "Payment request received. Check your phone.";
  } catch (error) {
    message.textContent =
      error.message || "Could not connect. Please try again.";
  } finally {
    button.disabled = false;
  }
}

renderGames();
renderHistory();
</script>

</body>
</html>
