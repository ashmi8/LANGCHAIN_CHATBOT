# Langchain Chatbot

A minimal LangChain-based chatbot project scaffolded for local development and experimentation.

## Contents

- [Files of interest](#files-of-interest)
- [Requirements & environment](#requirements--environment)
- [Quick start](#quick-start)
- [Usage](#usage)
- [Project structure](#project-structure)
- [Troubleshooting](#troubleshooting)



## Files of interest

- Main app entry: [app.py](app.py)  
- Python dependencies: [requirements.txt](requirements.txt)  
- Local environment variables: [.env](.env)  
- Virtualenv (if present): `env/` folder

## Requirements & environment

1. Python 3.10+ is required.
2. (Recommended) Use the included virtual environment at `env/` or create a new one:

   ```sh
   python -m venv .venv
   source .venv/bin/activate   # macOS / Linux
   .venv\Scripts\activate      # Windows (PowerShell)
   ```

3. Install dependencies:

   ```sh
   pip install -r requirements.txt
   ```

4. Copy or create a `.env` file at the project root and add any required API keys or configuration values. Example keys this project commonly uses:
   - LANGCHAIN_API_KEY
   - GROQ_API_KEY

## Quick start

1. Activate your virtual environment.
2. Ensure dependencies are installed: `pip install -r requirements.txt`.
3. Start the app:

   ```sh
   streamlit run  app.py
   ```

4. Open the app according to the behavior implemented in [app.py](app.py) (CLI, HTTP server, or other).

## Usage

- Inspect [app.py](app.py) to see how the chatbot is wired (model selection, prompt templates, and runtime options).
- Configure environment-specific settings in [.env](.env) or your shell environment.
- If you use the included `env/` virtual environment, activate it before running commands.

## Project structure

Top-level files and directories:

- app.py — application entrypoint
- requirements.txt — dependency list
- .env — environment variables (git-ignored)
- env/ — optional virtual environment (git-ignored)

Third-party libraries used by this project are installed into the virtual environment; notable packages visible in the workspace include `langchain-core`, `langsmith`, and provider integrations (see `requirements.txt`).

## Troubleshooting

- Missing package errors: run `pip install -r requirements.txt` inside an activated virtual environment.
- Virtual environment activation issues: ensure Python version matches project requirements (3.10+).
- If API calls fail, verify keys in [.env](.env) and check provider dashboards for usage or permissions.

