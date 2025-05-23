# Weather Time Agent (ADK + Gemini)

This is a simple AI agent built with [Google's Agent Developer Kit (ADK)](https://google.github.io/adk-docs/) and the Gemini API. It answers basic questions about the weather and current time in a city — currently supporting "New York" as a demo.

---

## Features

- Built using [Google ADK](https://github.com/google/adk)
- Uses Gemini 2.0 Flash model
- Two tools:
  - `get_weather(city: str)` – Returns mock weather for New York
  - `get_current_time(city: str)` – Returns current time using `zoneinfo`
- Cleanly structured using a Python package layout (`agents/`)

---

##  Folder Structure

my-adk-agent/

├── .venv/ # Virtual environment (not tracked by Git)

├── .env # API key (excluded from Git)

├── .gitignore

├── agents/

│ ├── init.py # Exposes agent from weather_agent.py

│ └── weather_agent.py # Defines the ADK Agent and tools

└── requirements.txt # (optional) Freeze your Python deps


---

##  Setup Instructions

```bash
# Clone the repo
git clone https://github.com/your-username/weather-adk.git
cd weather-adk

# Create virtual environment
python -m venv .venv
source .venv/bin/activate   # or .venv\Scripts\activate on Windows

# Install ADK + dependencies
pip install google-adk

# Set your Gemini API key
echo "GOOGLE_API_KEY=your_key_here" > .env

# Run the agent UI
adk web

Visit http://localhost
