# ResearchAgent.ai

An AI-powered multi-agent research assistant that can plan, search, analyze, and write comprehensive research reports, with optional email delivery.

---

## Overview

This is a system of specialized AI agents that collaborate to handle the entire research pipeline. From planning queries to searching for information, compiling structured results, and generating polished reports, the system automates deep research tasks that would otherwise take hours of manual work.

---

## Features

- Deep Research – Gathers and analyzes information across multiple sources
- Automated Writing – Produces clear, structured summaries and reports
- Email Integration – Packages findings and sends them via email
- Task Planning – Breaks down complex queries into structured steps
- Multi-Agent Collaboration – Specialized agents work together under a central manager

---

## Architecture

The project is organized into specialized agents:

- planner_agent.py – Breaks down user queries into structured research tasks
- search_agent.py – Retrieves relevant information from online sources
- deep_research.py – Handles multi-step, multi-source exploration
- writer_agent.py – Summarizes results into human-readable reports
- email_agent.py – Formats and sends reports by email
- research_manager.py – Coordinates all agents and manages workflows

---

## Tech Stack

- Python
- OpenAI API for reasoning and writing
- Requests for web access
- Pydantic for structured outputs
- Custom multi-agent orchestration

---

## Installation

Requirements:
- Python 3.10+

Clone the repository:
    git clone https://github.com/<your-username>/ResearchAgent.ai.git
    cd ResearchAgent.ai

Install dependencies:
    pip install -U python-dotenv openai requests pydantic

---

## Configuration

Create a `.env` file in the root directory with the following:

    OPENAI_API_KEY=sk-your-key
    EMAIL_USER=your-email@example.com       # optional, if using email agent
    EMAIL_PASS=your-app-password            # optional, recommended to use an app password

---

## Usage

Run the research manager:
    python research_manager.py

Example workflow:
1. Provide a research question, e.g. "What are the latest breakthroughs in quantum computing applications for healthcare?"
2. The Planner Agent breaks the query into smaller tasks.
3. The Search Agent gathers relevant information.
4. The Writer Agent compiles a structured report.
5. (Optional) The Email Agent sends the report to a configured email address.

---

## Use Cases

- Academic research and literature review
- Market and trend analysis
- Competitive intelligence gathering
- Automated report generation
- Personal knowledge management

---

## Privacy Notes

- Web data is collected via search APIs and HTTP requests.
- Email delivery requires secure app passwords or SMTP relay.
- All language model calls are handled through your configured OpenAI API key.

---

## License

This project is licensed under the MIT License.

---

## Acknowledgments

- OpenAI for language models
- Pydantic for structured data handling
- Python Requests for web interaction
