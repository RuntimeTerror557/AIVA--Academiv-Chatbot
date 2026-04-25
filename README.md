AIVA: Adaptive Intelligent Virtual Assistant
Intelligent Interaction, Instituted.
AIVA is a domain-specific, RAG-powered academic mentor designed for students at NIET (Autonomous). It transforms static, unstructured syllabus PDFs and institutional portals into a dynamic, conversational knowledge ecosystem, ensuring 100% grounded and factual academic guidance.

🚀 Key Features
Verified Grounding: Uses a Retrieval-Augmented Generation (RAG) pipeline to eliminate hallucinations. Every answer is anchored in official NIET documentation.

Hybrid Search: Combines Vector Similarity (for conceptual queries) with BM25 Keyword Matching (for precise subject codes like CAS0103).

Zen-Minimalist UI: A high-impact, glassmorphism dashboard built with React 19 and Tailwind CSS to reduce "Search Fatigue."

Automated Ingestion: Integrated with Firecrawl to automatically sync and parse branch-wise syllabi from institutional portals.

Socratic Mentorship: Programmed to guide students through Course Outcomes (COs) rather than just providing flat data.

🛠️ Technical Stack
LLM Engine: Gemini 1.5 Flash (1M+ Context Window)

Orchestration: Dify.ai

Data Pipeline: Firecrawl (Headless Crawler) + Markdown Parser

Frontend: React 19, Tailwind CSS, Framer Motion

Deployment: Vercel (Frontend) / Dify Cloud (Backend)

🏗️ System Architecture
AIVA follows a modular, decoupled architecture:

Ingestion: Firecrawl extracts data -> Parsed to Markdown -> Parent-Child Chunking.

Retrieval: Hybrid Search (Dense + Sparse) identifies the most relevant syllabus snippets.

Generation: Gemini 1.5 Flash reasons over the context to produce a formatted response.

Interaction: RESTful API handshake connects the reasoning engine to the React frontend.


🔧 Installation & Setup
Clone the Repo:

Bash
git clone https://github.com/YourUsername/AIVA.git
cd AIVA
Install Dependencies:

Bash
npm install
Environment Variables: Create a .env file and add your Dify/Gemini API keys:

Code snippet
VITE_DIFY_API_KEY=your_key_here
VITE_DIFY_BASE_URL=your_url_here
Run Development Server:

Bash
npm run dev
📜 License
Distributed under the MIT License. See LICENSE for more information.

🛡️ Responsible Use & Ethics
AIVA is an academic assistant, not a replacement for official institutional authority. All high-stakes academic decisions should be cross-verified with the NIET Registrar’s Office. This project adheres to ethical AI guidelines, prioritizing data grounding over generative creativity.
