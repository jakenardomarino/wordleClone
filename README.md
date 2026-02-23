# Wordle Clone 🟩🟨⬛

A fully functional clone of the popular [New York Times Wordle](https://www.nytimes.com/games/wordle/index.html) word-guessing game, built with vanilla JavaScript on the frontend and a Node.js/Express backend. The game fetches a random 5-letter word each session and validates guesses against a dictionary — all via external APIs.

### Why This Project?
Wordle took the world by storm with its simple yet addictive mechanic: guess a 5-letter word in 6 tries, with color-coded feedback after each guess. This clone replicates the full experience — including the flip animations, color-coded keyboard, and win/loss messaging — while wiring up a real random word generator and dictionary validator on the backend. Now you can play as many times as you'd like!!

---

## Gameplay

- Guess the hidden 5-letter word in **6 attempts**
- After each guess, tiles flip and change color:
  - 🟩 **Green** — correct letter, correct position
  - 🟨 **Yellow** — correct letter, wrong position
  - ⬛ **Grey** — letter not in the word
- The on-screen keyboard tracks your used letters
- Only valid dictionary words are accepted

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| Frontend | HTML, CSS, Vanilla JavaScript |
| Backend | Node.js, Express |
| APIs | RapidAPI — Random Word API & Twinword Dictionary API |
| HTTP Client | Axios |
| Config | dotenv |

---

## Setup & Installation

### Prerequisites
- [Node.js](https://nodejs.org/) installed
- A free [RapidAPI](https://rapidapi.com/) account

### 1. Subscribe to the Required APIs
Log into RapidAPI and subscribe to both of the following (free tiers work):
- **[Random Words API](https://rapidapi.com/sheharyar566/api/random-words5/)** — generates the secret word each game
- **[Twinword Word Graph Dictionary API](https://rapidapi.com/twinword/api/twinword-word-graph-dictionary/)** — validates whether a guessed word exists

### 2. Clone the Repository
```bash
git clone https://github.com/your-username/wordleClone.git
cd wordleClone
```

### 3. Install Dependencies
```bash
npm i
```

### 4. Configure Environment Variables
Create a `.env` file in the root of the project:
```
RAPID_API_KEY = your_rapidapi_key_here
```
> Never commit your `.env` file. Make sure it is listed in your `.gitignore`.

### 5. Start the Backend Server
```bash
npm run start:backend
```
The backend will start on **http://localhost:8000/**

### 6. Launch the Game
Open your file explorer and copy the full path to `index.html`, then paste it directly into your browser's address bar. For example:
```
/Users/yourname/wordleClone/index.html
```

---

## 📁 Project Structure
```
wordleClone/
├── index.html       # Game UI structure
├── app.js           # Frontend logic (tiles, keyboard, flip animation, game state)
├── style.css        # Styling and tile flip animations
├── index.js         # Express backend (word fetching and word validation endpoints)
├── .env             # API key (not committed)
└── package.json
```

---

## 🔌 API Endpoints

| Endpoint | Method | Description |
| :--- | :---: | :--- |
| `/word` | GET | Returns a random 5-letter word to use as the secret word |
| `/check?word={guess}` | GET | Validates whether the guessed word exists in the dictionary |

---

## Credit
Credit for support on coding portions belongs to [Ania Kubow](https://github.com/kubowania).
