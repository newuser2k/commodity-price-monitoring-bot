# Commodity Price Monitoring & Alerting Bot

A Telegram-based automation case study for monitoring Brent oil price movements, sending structured alerts, and supporting procurement, operations, supply chain, and commercial decision-making.

## Overview

Commodity price movements can directly affect procurement decisions, supplier quotations, contract timing, logistics costs, commercial planning, and margin control.

This project demonstrates how a lightweight monitoring and alerting workflow can convert external market data into structured Telegram notifications, event logs, and business-friendly summaries.

The goal is not to predict markets or provide financial advice. The goal is to improve visibility, structure, and reaction time for business teams exposed to commodity-driven cost changes.

## Business Use Case

The system is designed as a decision-support workflow for:

* Procurement teams
* Supply chain managers
* Operations managers
* Commercial teams
* Business development managers
* Logistics coordinators
* Management teams

The workflow can help teams monitor Brent oil price movements and use structured alerts for procurement timing, supplier quotation review, logistics cost awareness, commercial planning, and management reporting.

## Key Capabilities

* Brent oil price monitoring
* Telegram alerts
* Intraday status updates
* Daily summaries
* Structured event logging
* Business-friendly notification format
* Human-in-the-loop decision support
* Optional AI-assisted summaries
* Extendable workflow for other commodities, FX rates, supplier price indicators, or logistics cost signals

## Project Structure

```text
commodity-price-monitoring-bot/
├── README.md
├── docs/
│   ├── project-summary.md
│   ├── business-context.md
│   ├── workflow.md
│   ├── architecture.md
│   └── ai-automation-angle.md
└── examples/
    ├── telegram-alert-example.md
    ├── daily-summary-example.md
    └── event-log-example.json
```

## Documentation

* [Project Summary](docs/project-summary.md)
  Executive overview of the project, business problem, solution, value, and portfolio relevance.

* [Business Context](docs/business-context.md)
  Explanation of why commodity price monitoring matters for procurement, operations, supply chain, logistics, and commercial teams.

* [Workflow](docs/workflow.md)
  High-level workflow from market data monitoring to alert classification, logging, Telegram notifications, reporting, and human review.

* [Architecture](docs/architecture.md)
  Modular architecture overview covering market data input, monitoring engine, alert rules, event logging, Telegram notifications, reporting, and configuration.

* [AI and Automation Angle](docs/ai-automation-angle.md)
  Explanation of how AI and automation can support business workflows without replacing human decision-making.

## Examples

* [Telegram Alert Example](examples/telegram-alert-example.md)
  Example Telegram notifications for price increase alerts, price decrease alerts, daily status updates, and management summaries.

* [Daily Summary Example](examples/daily-summary-example.md)
  Example daily market summary formats for management, procurement, and commercial teams.

* [Structured Event Log Example](examples/event-log-example.json)
  Example JSON structure for logged commodity price events and notification records.

## Example Workflow

1. Brent oil price data is monitored.
2. Price movements are evaluated against configured alert rules.
3. Relevant events are classified.
4. Events are logged in a structured format.
5. Telegram notifications are sent when required.
6. Daily or intraday summaries are generated.
7. Human users review the information and decide whether any business action is needed.

## Business Value

This type of workflow can help teams:

* Reduce manual monitoring
* Improve reaction time to market changes
* Support procurement timing decisions
* Improve supplier negotiation preparation
* Increase visibility for operations and management
* Create a structured history of relevant market events
* Make external market signals easier to understand for non-specialist users
* Improve communication between procurement, operations, commercial teams, and management

## AI-Assisted Extension

AI can be added as an optional support layer to:

* Summarize market movements in business-friendly language
* Classify alerts by business relevance
* Prepare management summaries
* Draft procurement review notes
* Highlight repeated patterns
* Generate weekly reporting comments
* Convert raw event logs into clear operational updates

The AI layer is designed to support human decision-making, not replace it.

## Possible Extensions

The same concept can be extended to monitor:

* Other commodities
* FX rates
* Supplier price changes
* Freight and logistics cost indicators
* Inventory risk signals
* Contract price triggers
* Market news summaries
* Procurement-related external risk indicators
* Google Sheets, CRM, ERP, or dashboard integrations

## Portfolio Relevance

This case study demonstrates the ability to connect business experience with practical automation.

It is especially relevant to roles in:

* Business Development
* Operations Management
* Supply Chain Management
* Procurement
* Logistics
* Commercial Operations
* AI-assisted business process automation

## Positioning

This project should be positioned as:

**Business workflow automation for commodity price monitoring, alerts, reporting, and decision support.**

It should not be positioned as a trading product, financial advice tool, or investment recommendation system.

## Disclaimer

This project is presented as a business automation and market monitoring case study.

It is not financial advice, not an investment recommendation, and not a trading product.
