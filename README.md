# Meta-Agent Building System

An autonomous AI system that builds, tests, and deploys production-ready AI agents from plain English requirements.

## Overview

The Meta-Agent Factory takes natural language requirements and automatically:
- Generates complete agent code with LangGraph/CrewAI/Direct LLM
- Creates comprehensive test suites
- Builds Docker containers
- Generates Kubernetes deployments with auto-scaling
- Implements monitoring and observability
- Handles multi-tenancy and cost tracking

## Key Features

- **Autonomous Test-Fix Loop**: Automatically fixes code until all tests pass
- **Production-First**: Every agent is deployment-ready from day one
- **Scale-to-Zero**: Agents cost $0 when idle using KEDA autoscaling
- **Multi-Framework**: Supports LangGraph, CrewAI, and Direct LLM patterns
- **Observable**: Built-in OpenTelemetry tracing and Prometheus metrics

## Repository Structure

See [REPO_LAYOUT.md](REPO_LAYOUT.md) for the complete directory structure.

## Getting Started

```bash
# Clone the repository
git clone https://github.com/Instabidsai/Meta-agent-building-system.git

# Navigate to the project
cd Meta-agent-building-system

# Start building agents!
```

## Example Usage

"Build me an agent that monitors Slack for questions about our product and answers them using our knowledge base"

The system will:
1. Identify required secrets (SLACK_TOKEN, OPENAI_API_KEY)
2. Create repository: `instabids-agents/slack-support-bot`
3. Generate complete agent code with worker loop
4. Create and run comprehensive tests
5. Build and validate Docker container
6. Generate Kubernetes manifests with autoscaling
7. Deliver production-ready system

## Documentation

- [Agent Build Runbook](tracking/AGENT_BUILD_RUNBOOK.md)
- [Model Selection Guide](tracking/AI_MODEL_SELECTION_GUIDE.md)
- [Session Logs](tracking/sessions/)

## Built Agents

Check the `examples/` directory for agents built by this system.
