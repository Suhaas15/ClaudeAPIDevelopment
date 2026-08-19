# Building with the Claude API

This repository contains my Jupyter notebooks and hands-on exercises from the **Building with the Claude API** course. It documents my progress learning how to build conversational applications with Anthropic's Python SDK.

## What I've learned

- Sending requests with the Claude Messages API
- Maintaining conversation history with user and assistant messages
- Using system prompts to guide Claude's role and behavior
- Adjusting temperature to control response variation
- Streaming responses as they are generated
- Controlling output with assistant prefilling and stop sequences

## Notebooks

| Notebook | Topic |
| --- | --- |
| [001_requests.ipynb](001_requests.ipynb) | Basic API requests and multi-turn conversations |
| [002_systemprompt.ipynb](002_systemprompt.ipynb) | Customizing behavior with system prompts |
| [003_temperature.ipynb](003_temperature.ipynb) | Exploring the temperature parameter |
| [004_streaming.ipynb](004_streaming.ipynb) | Streaming events and text responses |
| [005_controllingoutput.ipynb](005_controllingoutput.ipynb) | Prefilling responses and using stop sequences |

## Setup

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install anthropic python-dotenv jupyter
```

Create a `.env` file in the project directory:

```text
ANTHROPIC_API_KEY=your_api_key_here
```

Then start Jupyter:

```bash
jupyter notebook
```

> Keep `.env` out of version control so your API key is never committed.

## Model compatibility

Most notebooks use Claude Sonnet 4.6. The output-control notebook uses Claude Sonnet 4.5 because assistant prefilling is not supported by Claude 4.6 and newer models. Available model IDs may change, so they can be checked with `client.models.list()`.

## Status

This is a learning repository and will continue to grow as I progress through the course.
