# 🔬 ResearchMind — Multi-Agent AI Research System

ResearchMind is a multi-agent AI research system that automates web-based research using LangChain. It searches the web, extracts relevant information, generates a structured research report, and evaluates the report using an AI critic.

## Features

- Web search using Tavily
- LangChain multi-agent architecture
- Custom tool calling
- Web scraping with BeautifulSoup
- Automated research report generation
- LCEL-based Writer and Critic chains
- AI-powered report evaluation
- Streamlit web interface
- Downloadable research reports

## Architecture

```text
User
  ↓
Streamlit UI
  ↓
Search Agent + Tavily
  ↓
Reader Agent + Web Scraper
  ↓
Writer Chain (LCEL)
  ↓
Critic Chain (LCEL)
  ↓
Final Research Report


## TechStack

-Python
-LangChain
-LangChain Agents
-LCEL / Runnables
-Groq
-Tavily
-BeautifulSoup
-Requests
-Streamlit
-python-dotenv

## Project Structure
ResearchMind-Multi-Agent-AI/
│
├── app.py              # Streamlit user interface
├── agents.py           # Agents and LCEL chains
├── tools.py            # Web search and scraping tools
├── pipeline.py         # Research pipeline
├── requirements.txt    # Project dependencies
├── .env.example        # Environment variable template
├── .gitignore          # Ignored files and secrets
└── README.md           # Project documentation


Workflow:

Search Agent
Uses the Tavily search tool to find recent and relevant information about the user's research topic.

Reader Agent
Selects a relevant source from the search results and extracts deeper content using a custom web-scraping tool built with Requests and BeautifulSoup.

Writer Chain
Uses the collected search results and scraped content to generate a structured research report using an LCEL-based chain.

Critic Chain
Reviews the generated report and provides a score, strengths, areas for improvement, and a final verdict.


Author:
Aakriti Srivastava