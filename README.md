# Chess AI Tutor

![Hero Screenshot](screenshots/Hero.jpg)

Chess AI Tutor is a hybrid chess analysis application that combines deterministic engine evaluation with LLM-based coaching to help users understand a position, not just calculate moves.

The system uses Stockfish for reliable position analysis and best-move generation, while a FastAPI backend and React frontend deliver an interactive coaching experience through structured explanations and a clean snapshot-based workflow.

---

## Live Demo

**Frontend-only demo:**  
https://chess-ai-tutor-react.web.app

> Full functionality requires running the backend locally.

---

## Why This Project

Most chess tools are strong at calculation but weak at teaching. Chess AI Tutor was built to bridge that gap by separating the system into two clear roles:

- **Stockfish** handles deterministic evaluation and move analysis
- **The LLM layer** turns engine output into more natural coaching and explanation

This hybrid design preserves analytical reliability while making the output more usable for learners.

---

## Features

### Chess Analysis
- Snapshot-based position evaluation  
- Stockfish best-move generation  
- Position analysis through a deterministic backend pipeline  
- Structured coaching responses based on engine-backed analysis  

### User Experience
- Interactive chessboard interface  
- Move history navigation  
- Chat-style analysis workflow  
- Clean two-panel React layout  
- Dark-mode UI built with Tailwind CSS  

### System Design
- Clear separation between engine logic and explanation logic  
- Deterministic analysis paired with model-assisted coaching  
- Modular frontend/backend architecture  
- Fast development workflow using Vite and FastAPI  

---

## Tech Stack

### Frontend
- React  
- Vite  
- Tailwind CSS  
- react-chessboard  

### Backend
- Python  
- FastAPI  
- Uvicorn  
- python-chess  
- Stockfish  

### AI Layer
- OpenAI GPT models  

---

## Architecture Overview

The application follows a hybrid architecture:

1. The user interacts with the board and selects or reaches a position  
2. The frontend sends the position data to the backend  
3. The backend uses Stockfish and chess logic libraries to evaluate the position and generate deterministic analysis  
4. The LLM layer converts the engine-backed analysis into more understandable coaching-oriented output  
5. The frontend displays the result in a chat-style interface  

This design keeps the system grounded in reliable chess computation while improving usability through natural-language explanation.

---

## Iteration and Development Journey

This project went through a meaningful architectural and UI evolution.

### Early Prototype
The first version was built in Flutter and helped validate the core idea: combining chess analysis with a more guided explanatory experience.

![Early UI](screenshots/early-1.jpg)

### Prototype Limitations
As development continued, UI state issues and move-list handling exposed friction in the original implementation. These problems made it harder to maintain a smooth analysis workflow and highlighted the need for a cleaner frontend structure.

![Prototype Move List](screenshots/prototype-move-1.jpg)
![Broken Move List](screenshots/mid-broken-1.jpg)
![Another Broken State](screenshots/mid-broken-2.jpg)

### React Rewrite
The project was later rewritten with React to improve maintainability, frontend control, and overall usability. The final structure made it easier to support move history, board interaction, chat-style responses, and a cleaner separation between interface concerns and backend analysis.

![React Final](screenshots/Hero.jpg)

The result is a more stable and more scalable MVP with stronger system boundaries and a clearer user experience.

---

## Installation

**Python version:** 3.10.x

### Clone the repository

```bash
git clone https://github.com/ChrisDevAI/chess-ai-tutor.git
cd chess-ai-tutor
```

---

## Backend Setup

```bash
cd chess-backend
py 3.10 -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
```

Rename `.env.example` to `.env` and add:

```env
OPENAI_API_KEY=your_key_here
```

Run the backend:

```bash
uvicorn main:app --reload --port 8000
```

---

## Frontend Setup

```bash
cd ../chess-frontend
npm install
npm run dev
```

---

## Project Status

This project is currently a functional MVP focused on snapshot-based analysis and coaching. Its main strength is the hybrid design: deterministic chess evaluation combined with natural-language instructional output.

Future improvements could include deeper lesson modes, richer evaluation controls, and broader training workflows, but the current version already demonstrates the core architecture effectively.

---

## License

MIT License

---

## Author

**Christopher Mena**  
Applied AI / ML Engineering Student  

- GitHub: https://github.com/ChrisDevAI  
- Website: https://chrisai.dev  
- LinkedIn: https://linkedin.com/in/ChrisDevAI

