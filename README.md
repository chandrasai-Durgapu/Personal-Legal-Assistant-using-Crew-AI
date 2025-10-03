# Personal-Legal-Assistant-using-Crew-AI
An AI-powered legal assistant built with **CrewAI**.  
This system lets users describe legal issues in natural language; it processes the input via multiple autonomous agents that introspect, retrieve legal knowledge (statutes, precedents), and draft documents or answers. The output is then presented via a user interface.



---

## 🧰 Tech Stack

This project leverages the following technologies:

- **Python 3.10+** — Core language for development  
- **CrewAI** — Framework for orchestrating multi-agent AI workflows  
- **LangChain** — For chaining LLM prompts and retrieval augmentation  
- **OpenAI API** — Large language model provider powering the AI assistant  
- **GROQ API** — Specialized retrieval over large, complex data sets  
- **Tavily API** — Legal document automation and drafting services  
- **Chroma Vector Store** — Embedding storage and semantic search  
- **python-dotenv** — Environment variable management  
- **Streamlit** — User interface framework for building interactive web apps  
- **Pinecone** *(optional)* — Scalable vector database for similarity search  

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/chandrasai-Durgapu/Personal-Legal-Assistant-using-Crew-AI.git
cd Personal-Legal-Assistant-using-Crew-AI
2. Create & Activate Virtual Environment
bash
Copy code
python3 -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy code
pip install -r requirements.txt
4. Configure Environment Variables
Create a .env file in the root directory with the following variables:

env
Copy code
OPENAI_API_KEY=<your_openai_api_key>
GROQ_API_KEY=<your_groq_api_key>
TAVILY_API_KEY=<your_tavily_api_key>
IPC_JSON_PATH=<your_ipc_json_path>
PERSIST_DIRECTORY_PATH=<persist_directory_path_for_vector_store>
IPC_COLLECTION_NAME=<ipc_collection_name>
Example values (replace with your actual paths and keys):
env
Copy code
# IPC_JSON_PATH="D:/work/2_yt_pycharm/code_prep/ai-legal-assistant-crewai/ipc.json"
# PERSIST_DIRECTORY_PATH="D:/work/2_yt_pycharm/code_prep/ai-legal-assistant-crewai/chroma_vectordb"
# IPC_COLLECTION_NAME="ipc_collection"
Make sure your application loads these variables properly, for example using python-dotenv.

5. Run the Application
bash
Copy code
streamlit run app.py
Then open your browser at the indicated URL (usually localhost:8501).

🧩 Agent Architecture & Workflow
The system is structured into several agents, each handling a specific task:

Case Intake Agent
Parses user’s description into structured form (fact, parties, issue).

Statute / Section Agent
Uses retrieval-augmented generation to find relevant legal statutes (e.g., IPC sections).

Precedent Search Agent
Queries a legal case database or vector store to find relevant precedents.

Drafting Agent
Combines intake, statutes, and precedent information to generate legal drafts or advice.

These agents are orchestrated via CrewAI, passing outputs between each other to produce a final response.

⚠️ Disclaimer
⚠️ This tool is for informational and educational purposes only.
It does not constitute legal advice. Always consult a qualified legal professional before acting on any generated content.

📄 License
MIT License — see the LICENSE file.

👤 Author
Chandrasai Durgapu
GitHub: @chandrasai-Durgapu

vbnet
Copy code

If you want me to add or tweak anything else, just say!



Get smarter responses, upload files and images, and more.

Log in

Sign up for free

## Clone the Repository
```bash
git clone https://github.com/chandrasai-Durgapu/Personal-Legal-Assistant-using-Crew-AI.git
cd Personal-Legal-Assistant-using-Crew-AI
```
---
## Set Up Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```
---
## Install Dependencies
```bash
pip install -r requirements.txt
```
---
## Set Up Environment Variables

Create a .env file in the root directory and add the necessary environment variables:
```bash
GROQ_API_KEY=your_groq_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
IPC_JSON_PATH=/full/path/to/ipc.json
PERSIST_DIRECTORY_PATH=/full/path/to/persist_dir
IPC_COLLECTION_NAME=your_ipc_collection_name
```
---
## Run the Assistant
```bash
python main.py
```
---
## Core Components

agents/: Contains the definitions of various AI agents responsible for different tasks within the legal assistance process.

tasks/: Houses the task definitions that agents will execute, outlining specific objectives and workflows.

tools/: Includes utility functions and tools that support the agents and tasks.

app.py: Serves as the main application entry point, initializing and managing the execution of agents and tasks.

crew.py: Defines the coordination logic for the AI agents, ensuring they work together effectively.

main.py: Acts as the script to launch the application, setting up necessary configurations and starting the agent workflows.

requirements.txt: Lists all the Python dependencies required to run the project.

README.md: Provides an overview of the project, setup instructions, and usage guidelines.
