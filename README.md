# Personal-Legal-Assistant-using-Crew-AI
Personal-Legal-Assistant-using-Crew-AI
---
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
CREW_AI_API_KEY=your_crew_ai_api_key
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
