# IT System Monitoring and AI Automation

## Project Overview

This project demonstrates an IT system monitoring and automation workflow built using Python, Flask, SQLite, n8n, and Ollama.

The application collects CPU and memory utilization metrics, stores system-check history in a local SQLite database, and sends monitoring data to an n8n webhook. The workflow evaluates the metrics against configured thresholds and generates alerts when high resource usage is detected.

An Ollama-powered AI Agent is also being explored to analyze alerts, identify possible causes, and recommend troubleshooting actions.

## Key Features

- **System Monitoring:** Collects CPU and memory utilization.
- **Python Flask Application:** Provides a simple dashboard to trigger system checks.
- **SQLite Database:** Stores monitoring history locally.
- **n8n Workflow Automation:** Receives monitoring data through a webhook and evaluates threshold conditions.
- **Conditional Alerts:** Identifies high CPU or memory utilization.
- **AI-Powered Analysis:** Uses a local Ollama model to provide possible reasons and recommended actions for detected issues.

## Technologies Used

- Python
- Flask
- SQLite
- n8n
- Webhooks and REST APIs
- Ollama (Llama 3.2)
- JSON

## Workflow

1. The user triggers a system check from the dashboard.
2. The Flask application collects CPU and memory metrics.
3. The application stores the results in SQLite.
4. Monitoring data is sent to an n8n webhook.
5. n8n evaluates the metrics against configured thresholds.
6. When an issue is detected, the AI Agent can analyze the alert and suggest troubleshooting actions.
7. The workflow can return a response through the Respond to Webhook node.

## Project Structure

```text
IT-Automation-App/
├── app.py
├── index.html
├── automation.db
├── ai-system-monitoring-workflow.json
└── README.md
```

**Note:** `automation.db` is a local runtime database and should not be committed if it contains private data. The database is listed above for illustration only.

## Learning Outcomes

- Building a simple Python Flask application
- Integrating applications with n8n using webhooks
- Creating conditional automation workflows
- Working with JSON data and REST API requests
- Storing and retrieving monitoring history using SQLite
- Exploring local AI Agent integration for troubleshooting recommendations

## Current Status

This is a learning project and local prototype. The workflow and AI integration are being developed and tested locally. It is not presented as a production monitoring platform.

## Future Improvements

- Add a monitoring history dashboard
- Improve error handling and workflow reliability
- Add configurable thresholds
- Enhance AI-generated troubleshooting recommendations
- Explore additional monitoring and notification integrations
