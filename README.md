# Building with the Claude API

This repository contains my Jupyter notebooks and hands-on exercises from the **Building with the Claude API** course. It documents my progress learning how to build conversational applications with Anthropic's Python SDK.

## What I've learned

- Sending requests with the Claude Messages API
- Maintaining conversation history with user and assistant messages
- Using system prompts to guide Claude's role and behavior
- Adjusting temperature to control response variation
- Streaming responses as they are generated
- Controlling output with assistant prefilling and stop sequences
- Building evaluation datasets for prompt testing
- Grading model responses with both Claude and syntax validators
- Calculating aggregate evaluation scores across test cases
- Generating diverse test scenarios and solution criteria
- Running model evaluations concurrently
- Producing reusable JSON and HTML evaluation reports

## Notebooks

| Notebook | Topic |
| --- | --- |
| [001_requests.ipynb](001_requests.ipynb) | Basic API requests and multi-turn conversations |
| [002_systemprompt.ipynb](002_systemprompt.ipynb) | Customizing behavior with system prompts |
| [003_temperature.ipynb](003_temperature.ipynb) | Exploring the temperature parameter |
| [004_streaming.ipynb](004_streaming.ipynb) | Streaming events and text responses |
| [005_controllingoutput.ipynb](005_controllingoutput.ipynb) | Prefilling responses and using stop sequences |
| [006_prompteval.ipynb](006_prompteval.ipynb) | Building an introductory evaluation pipeline with model and syntax grading |
| [007_prompting.ipynb](007_prompting.ipynb) | Building a reusable, concurrent prompt evaluator with report generation |

## Evaluation artifacts

- [dataset.json](dataset.json) contains generated test scenarios, prompt inputs, and solution criteria for evaluating an athlete meal-planning prompt.
- [output.json](output.json) stores the generated responses, scores, and grading reasoning.
- [output.html](output.html) presents the evaluation results as a readable report with summary statistics.

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

The introductory notebooks use Claude Sonnet 4.6. The output-control notebook uses Claude Sonnet 4.5, while the evaluation notebooks use Claude Haiku 4.5. These 4.5 models support the assistant-prefilling technique demonstrated in the course, while Claude 4.6 and newer models do not. Available model IDs may change, so they can be checked with `client.models.list()`.

## Status

This is a learning repository and will continue to grow as I progress through the course.
