# ✨ Lumina

**Full-stack AI chat assistant** with streaming answers, saved and searchable conversation history, web search with citations and image generation.

**Live demo:** [gemini-clone-five-mu.vercel.app](https://gemini-clone-five-mu.vercel.app)

## Features

- **Streaming chat** with Google Gemini, rendered as Markdown with code highlighting and LaTeX math
- **Accounts and auth**: sign-up and login with hashed passwords (bcrypt) and JWT sessions
- **Conversation history** stored in PostgreSQL (Neon), searchable and restorable
- **Web search with citations** through Tavily (optional)
- **Image generation** with Google Imagen
- Responsive UI built with React, TypeScript and Tailwind CSS

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | React 18, TypeScript, Vite, Tailwind CSS 4, React Router, react-markdown |
| Backend | Node.js, Express, TypeScript (tsx) |
| Database | PostgreSQL on Neon (serverless driver) |
| Auth | JWT, bcrypt |
| AI | Google Gemini API (`@google/genai`), Imagen, Tavily search |

## Project structure

```
src/       React frontend
server/    Express API and database access
public/    Static assets
```

## Running locally

Requires Node.js 18 or later and a PostgreSQL database (Neon works out of the box).

```bash
git clone https://github.com/mrahulsit/lumina.git
cd lumina
npm install
cp .env.example .env   # add DATABASE_URL, JWT_SECRET and GEMINI_API_KEY
npm run server         # API on http://localhost:3001
npm run dev            # Vite frontend
```

Optional: set `TAVILY_API_KEY` for web search and `GEMINI_IMAGE_MODEL` for image generation.

## Author

**Rahul Mishra** · Full Stack Developer · [mrahuls.in](https://www.mrahuls.in) · [LinkedIn](https://www.linkedin.com/in/rahulmishra-dev)
