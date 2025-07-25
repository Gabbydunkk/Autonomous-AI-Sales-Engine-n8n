# Autonomous-AI-Sales-Engine-n8n
Autonomous AI Sales Engine
A multi-agent system built in n8n that automates the entire top-of-funnel sales process, from live company discovery to hyper-personalized email outreach.
This project is a fully autonomous engine designed to identify and engage high-value leads. It leverages a team of specialist agents to scrape live data, enrich it, make intelligent decisions, and craft unique, personalized outreach for every single target.
🚀 Live Demo
(This is where we'll embed the YouTube link. For now, we'll put a placeholder. It's often better to link to a video than to embed a heavy GIF.)
Watch the 90-Second Live Demo on YouTube
![alt text](https://youtu.be/KzWZ4wB-CyI)

🏛️ The Architecture: A Multi-Agent System
This engine is not a single workflow; it's a modular, multi-agent pipeline. Each agent is a specialist with a dedicated role, ensuring the system is scalable, debuggable, and resilient.
(This is where you will upload and embed the Architecture Diagram you created in Excalidraw.)
![alt text]()
(How to use the placeholder above: In the GitHub editor, you can often just drag and drop your exported PNG file. It will upload the image and give you the correct link to paste here.)
The Agents:
Agent 1: The Company Hunter (Apify): The process begins by scraping LinkedIn for companies that are actively hiring for key roles, providing a powerful "buying signal."
Agent 2: The Enrichment Agent (Hunter.io): This agent takes the target companies and performs a "Targeted Directory Inquiry," finding a list of verified contacts in key decision-making departments (Sales, Marketing, Management).
Agent 3: The Scoring Agent (The "Brain"): A custom-coded agent that analyzes each contact using a multi-factor model (seniority, department, company size) to assign a lead score and a quality tag ("Hot", "Warm", "Cold").
Agent 4: The Gatekeeper (The "Bouncer"): A simple but crucial agent that routes leads based on their quality, ensuring that only high-value prospects proceed to the next stage.
Agent 5: The Content Beast (Google Gemini AI): This is the core generative AI. It takes the enriched, scored data and writes a unique, hyper-personalized email for each "Hot" lead, inferring their likely business challenges.
Agent 6: The Logger & The Messenger (Sheets & Gmail): The final agents log the entire interaction to a database for future analysis and then deliver the personalized email to the prospect.
🛠️ The Tech Stack
This project was built using a modern, powerful, and accessible tech stack:
Orchestration: n8n.io
Data Sourcing: Apify
Data Enrichment: Hunter.io
Generative AI: Google Gemini Pro
Database: Google Sheets
Outreach: Gmail
🧠 The Story: Overcoming Real-World Data Challenges
Building an autonomous system requires more than just connecting APIs; it demands resilience and creative problem-solving. A key challenge in this project was acquiring accurate lead data in a dynamic environment.
The Pivot:
Our initial approach involved scraping individual people's profiles. This proved to be unreliable due to API limitations and expired free trials.
The Solution:
We pivoted to a more robust, two-stage funnel:
First, we scrape companies that are actively hiring—a much more reliable data source.
Then, we use that company data to perform a highly-targeted directory enrichment with Hunter.io.
This "Company-First" approach is more resilient and mirrors how professional sales operations teams identify high-intent accounts. This pivot was a critical learning experience in building real-world, fault-tolerant automations.
🚀 Getting Started
(This is where you add the workflow.json file we talked about.)
The complete n8n workflow is available in this repository (workflow.json). You can import it into your own n8n instance to see the engine's full structure and logic. You will need to provide your own API keys for Apify, Hunter, and Google Gemini.
(End of README)
