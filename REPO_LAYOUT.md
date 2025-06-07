# Meta-Agent Building System - Repository Layout

```
Meta-agent-building-system/
├── .github/
│   └── workflows/
│       └── update-layout.yml    # Auto-updates this file on push
├── core/                        # Core factory components
│   ├── builder.py               # Main agent builder logic
│   └── validator.py             # Test validation framework
├── examples/                    # Example agents built by factory
│   ├── chat-sales-agent/        # Demo conversational agent
│   └── rss-monitor/            # Simple monitoring agent
├── factory-tools/              # Build and deployment utilities
│   ├── builders/
│   │   ├── docker_builder.py
│   │   └── k8s_manifest_generator.py
│   ├── validators/
│   │   ├── test_runner.py
│   │   └── performance_checker.py
│   └── analyzers/
│       ├── error_parser.py
│       └── log_analyzer.py
├── generators/                 # Code generation templates
│   ├── agent_generator.py
│   ├── api_generator.py
│   └── test_generator.py
├── templates/                  # Agent blueprint templates
│   ├── base-agent/            # Standard agent structure
│   │   ├── agent/
│   │   │   ├── __init__.py
│   │   │   ├── logic.py
│   │   │   ├── tools.py
│   │   │   └── config.py
│   │   ├── jobs/
│   │   │   └── worker.py
│   │   ├── api/
│   │   │   └── main.py
│   │   ├── tests/
│   │   │   ├── test_unit.py
│   │   │   ├── test_integration.py
│   │   │   └── test_performance.py
│   │   ├── k8s/
│   │   │   ├── deployment.yaml
│   │   │   ├── configmap.yaml
│   │   │   ├── keda-scaler.yaml
│   │   │   └── vault-injection.yaml
│   │   ├── Dockerfile.template
│   │   ├── requirements.txt.template
│   │   └── README.md.template
│   ├── patterns/              # Reusable code patterns
│   │   ├── worker_loop.py
│   │   ├── api_health.py
│   │   ├── token_tracker.py
│   │   └── error_handler.py
│   └── k8s-base/             # K8s infrastructure templates
│       ├── keda-config.yaml
│       ├── vault-policy.hcl
│       └── namespace-setup.yaml
├── tests/                     # Factory test suite
│   ├── test_builder.py
│   ├── test_generators.py
│   └── test_validators.py
├── tracking/                  # Build history and metrics
│   ├── agents/               # Individual agent tracking
│   │   └── sales-discovery-bot.md
│   ├── sessions/             # Build session logs
│   │   └── 2025-06-07-sales-discovery-bot.md
│   ├── migrations/           # Database schemas
│   │   └── 001_initial_schema.sql
│   ├── models.py             # SQLAlchemy models
│   └── patterns.json         # Successful pattern library
├── README.md                 # Project documentation
└── REPO_LAYOUT.md           # This file (auto-generated)
```

## Key Directories

### `/templates`
Contains all the blueprint templates used to generate new agents. The `base-agent` folder has the standard structure every agent follows.

### `/factory-tools`
Build utilities that handle Docker builds, test execution, and Kubernetes manifest generation.

### `/tracking`
Stores build history, session logs, and successful patterns for continuous improvement.

### `/generators`
Python modules that generate agent code, API endpoints, and test suites based on requirements.

### `/core`
The main factory logic that orchestrates the entire build process.

## Quick Commands

- **Build an agent**: Use the templates and generators
- **Track progress**: Check `/tracking/sessions/`
- **Find examples**: Look in `/examples/`

Generated on: 2025-06-07
