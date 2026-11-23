# sql-data-analyst-p01
SQL agent built via langraph for data analysis on CSV datasets. 
SQL Agent with LangGraph and Streamlit
Overview
This project implements a conversational SQL agent using LangGraph and Streamlit. The agent can:

List available database tables
Retrieve table schemas
Generate SQL queries from natural-language questions with detailed reasoning
Check generated SQL for common mistakes and rewrite if needed
Execute queries against a SQLite database and stream results back to the user
Support configurable filters to refine query results


Features
Agentic workflow built as a LangGraph state graph
Natural-language reasoning step separated from SQL generation
Error-checking phase to catch SQL pitfalls (NULL handling, quoting, joins, etc.)
Configurable loop between generate → check → run phases
Streamlit UI for interactive chat and result display
Prerequisites
Python 3.10
Streamlit
LangGraph (or your installed package)
sqlite3 (standard Python library)
Installation
Clone the repository:
git clone https://github.com/animesh1012/data_analyst_agent.git
cd sql-langgraph-agent
Create a virtual environment and install dependencies:
python -m venv .venv
source .venv/bin/activate   # on macOS/Linux
.\.venv\Scripts\activate  # on Windows
pip install -r requirements.txt
Running the Agent
Launch the Streamlit app:

streamlit run SQL_AGENT_APP.py
Open the displayed URL (usually http://localhost:8501) in your browser. Ask your SQL questions in the chat—e.g. "Show me the top 5 countries based on covid cases"—and watch as the agent:

Lists tables
Fetches schemas
Plans its SQL in English (no code)
Generates and checks the SQL
Executes it and returns the results
Code Structure
├── SQL_AGENT_APP.py                             # Streamlit application entrypoint
├── sql_agentic_flow_cookbook.ipynb              # Experiment Jupyter Notebook
├── requirements.txt                             # Python dependencies
├── README.md                                    # Project documentation (this file)
└── covid_19_report.db                           # Sample SQLite database (You can use any db)
└── worldometer_data.csv                         # Sample data used in demo (You can use any db)
