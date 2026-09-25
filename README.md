# NexaGuard — Autonomous Infrastructure Defense Mesh

Designed and developed by **Nikhil Chary Sriramoju**.

A digital-twin security platform that fuses cyber and physical threat detection: live 3D facility view, a real multi-agent (Recon → Triage → Response) reasoning chain powered by Groq's free LLM API, client-side RAG grounding, and real in-browser CNN image classification (TensorFlow.js MobileNet).

## Run it locally
Just open `nexaguard.html` in a browser — no build step, no server.

## Deploy to GitHub Pages (2 minutes)
1. Create a new GitHub repo (e.g. `nexaguard`).
2. Upload `nexaguard.html` and rename it to `index.html`.
3. Go to **Settings → Pages**, set source to the `main` branch, root folder.
4. Your live link appears at `https://<your-username>.github.io/nexaguard/`.

## Get a free Groq API key
1. Go to https://console.groq.com/keys and sign up (free tier).
2. Create a key (starts with `gsk_`).
3. Paste it into the "Groq key" field in the top-right of the page.
   The key is stored only in your browser's `localStorage` and is sent only to `api.groq.com` — never to any other server.

## What's real vs. illustrative
- **Multi-agent reasoning**: real — three live Groq LLM calls (Recon, Triage, Response), chained.
- **RAG retrieval**: real, simplified — client-side keyword-overlap retrieval over an embedded knowledge base (swap in a real vector DB for production).
- **CNN vision**: real — MobileNet runs actual inference in the browser on any photo you upload.
- **3D digital twin**: real, procedurally generated Three.js scene, driven by the live triage severity.
- **Docker mesh**: reference architecture — GitHub Pages only serves static files, so the containers aren't running behind the page, but the included `docker-compose.yml` snippet is a genuine, runnable starting point for the backend services this design implies.

## Talking points for HR / reviewers
- Shows integration skill: LLM agent orchestration, retrieval grounding, computer vision, and 3D visualization in one coherent product, not four disconnected demos.
- Fully client-side and free to run — no infrastructure cost to evaluate it.
- Honest about scope: the README and UI are explicit about what's live inference vs. reference architecture, which is itself worth pointing out in an interview.
