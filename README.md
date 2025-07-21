# CoderTeam Crew

A collaborative multi-agent AI system built with [crewAI](https://crewai.com) that designs, implements, tests, and demos Python applications from requirements. CoderTeam demonstrates how specialized AI agents can work together to deliver production-ready code with minimal human input.

## 🚀 Features

- **Automated Design & Implementation**: Agents turn requirements into detailed designs and working Python modules
- **Frontend Prototyping**: Generates a Gradio UI to demo the backend
- **Automated Testing**: Produces unit tests for all generated code
- **Seamless Workflow**: Each agent builds on the previous agent’s output
- **Easy Customization**: Change requirements and agent roles with simple config edits

## 📋 Prerequisites

- Python >= 3.10, < 3.14
- [UV](https://docs.astral.sh/uv/) package manager
- OpenAI API key

## 🛠️ Installation

1. **Install UV** (if not already installed):
   ```bash
   pip install uv
   ```

2. **Navigate to the project**:
   ```bash
   cd coder_team
   ```

3. **Install dependencies**:
   ```bash
   crewai install
   ```

4. **Set up environment variables**:
   Create a `.env` file in the project root and add your OpenAI API key:
   ```bash
   OPENAI_API_KEY=your_api_key_here
   ```

## 🎯 Quick Start

Run the CoderTeam crew with:
```bash
crewai run
```
This will generate a complete Python backend, Gradio UI, and unit tests for the default trading account management system.

## 📁 Project Structure

```
coder_team/
├── src/coder_team/
│   ├── config/
│   │   ├── agents.yaml      # Agent definitions and configurations
│   │   └── tasks.yaml       # Task definitions and workflows
│   ├── tools/
│   │   └── custom_tool.py   # Custom tools for agents
│   ├── crew.py              # Crew orchestration logic
│   └── main.py              # Entry point and requirements
├── output/                  # Generated code, UI, and tests
├── knowledge/               # Knowledge base and context
└── tests/                   # Test files
```

## ⚙️ Configuration

### Agents (`src/coder_team/config/agents.yaml`)
Defines the roles and goals for:
- Engineering Lead (design)
- Backend Engineer (implementation)
- Frontend Engineer (UI)
- Test Engineer (unit tests)

### Tasks (`src/coder_team/config/tasks.yaml`)
Specifies the workflow and output files for each agent.

## 🔧 Customization

Edit `src/coder_team/main.py` to change the requirements, module name, or class name:

```python
requirements = """Your custom requirements here..."""
module_name = "your_module.py"
class_name = "YourClass"
```

## 📊 Example Output

The crew generates:
- `output/accounts_design.md` – Technical design
- `output/accounts.py` – Python module
- `output/app.py` – Gradio UI
- `output/test_accounts.py` – Unit tests


