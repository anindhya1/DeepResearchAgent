# ResearchAgent.ai

An AI-powered multi-agent research assistant that can plan, search, analyze, and write comprehensive research reports, with optional email delivery.

**Live demo:** https://huggingface.co/spaces/Anindhya/DeepResearchTool

---

## Overview

ResearchAgent.ai is a system of specialized AI agents that collaborate to handle the entire research pipeline. From planning queries to searching for information, compiling structured results, and generating polished reports, the system automates deep research tasks that would otherwise take hours of manual work.

Each agent focuses on a single role (planner, searcher, writer, emailer), and a central manager coordinates them into a seamless workflow. This modular approach makes the system extensible and easy to adapt to new domains.

---

## Features

- **Deep Research** – multi-step, multi-source exploration for complex questions  
- **Automated Writing** – structured, well-formatted summaries and reports  
- **Email Integration** – send reports directly via email  
- **Task Planning** – planner agent breaks down broad questions into actionable tasks  
- **Multi-Agent Collaboration** – orchestrated agents specialize and coordinate  

---

## Architecture

The project is organized into specialized agents:

- `planner_agent.py` – breaks down user queries into structured tasks  
- `search_agent.py` – retrieves relevant information from online sources  
- `deep_research.py` – manages multi-step exploration logic  
- `writer_agent.py` – generates structured, human-readable reports  
- `email_agent.py` – formats and sends reports via email  
- `research_manager.py` – coordinates all agents and orchestrates workflows  

This architecture follows a **multi-agent pattern**, where each module has a single responsibility but can be reused and composed into larger workflows.

---

## Tech Stack

- Python 3.10+  
- OpenAI API – reasoning, writing, and task planning  
- Requests – web access and API calls  
- [Pydantic](https://docs.pydantic.dev/) – schema-based input/output validation for agent interactions  
- Asyncio (`async`/`await`) – non-blocking research and web queries (where supported)  
- Custom orchestration – lightweight manager to sequence agents  

---

## Installation

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

1. Provide a research question, e.g. *"What are the latest breakthroughs in quantum computing applications for healthcare?"*  
2. The Planner Agent decomposes the query into sub-tasks.  
3. The Search Agent retrieves information from relevant sources.  
4. The Writer Agent compiles a structured report.  
5. (Optional) The Email Agent formats and delivers the report to your inbox.  

---

## Key Concepts Implemented

### Pydantic Schemas
- Used to define structured agent inputs and outputs.
- Ensures validation and parsing of intermediate data passed between agents.
- Makes the system robust against LLM-generated errors.

### Asynchronous Execution
- `async` and `await` are leveraged where supported (e.g., search and API calls).
- Enables non-blocking research tasks and faster multi-source exploration.

### Multi-Agent Orchestration
- Planner, Search, Writer, and Email agents each have a single responsibility.
- A central manager coordinates them into a coherent workflow.
- This separation of concerns makes the system composable and extensible.

### Extensibility
- New agents (e.g., summarizers, visualizers, database connectors) can be added by following the same modular pattern.
- Tools and APIs can be swapped or extended with minimal changes.

---

## Use Cases

- Academic research and literature review  
- Market and trend analysis  
- Competitive intelligence gathering  
- Automated business or technical report generation  
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
- Pydantic for structured validation  
- Python Requests for web interaction  
