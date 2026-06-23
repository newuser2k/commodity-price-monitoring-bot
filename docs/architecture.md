# Architecture

This document describes the high-level architecture of the Commodity Price Monitoring & Alerting Bot.

The architecture is intentionally lightweight and modular. The goal is to show how external market data can be turned into structured alerts, logs, and business notifications for procurement, operations, and commercial teams.

## Architecture Goals

The system is designed around the following goals:

* Simple deployment
* Clear separation between data input, alert logic, logging, and notification delivery
* Configurable alert rules
* Structured event history
* Human-in-the-loop decision support
* Easy extension to other commodities, FX rates, supplier price indicators, or logistics cost signals

## High-Level Components

### 1. Market Data Input

This component receives or retrieves Brent oil price data from an external market data source.

Its role is to provide the current price and relevant market status information to the monitoring logic.

Typical input data may include:

* Commodity name
* Current price
* Previous price
* Timestamp
* Price change
* Market session status
* Optional reference levels

### 2. Monitoring Engine

The monitoring engine evaluates incoming price data against configured conditions.

Its role is to detect meaningful price movements and decide whether an event should be created.

Examples of monitoring conditions:

* Price moved more than a configured threshold
* Price reached a predefined business-relevant level
* Intraday price change became significant
* Repeated movement occurred in the same direction
* A management review alert should be generated

### 3. Alert Rules

Alert rules define when a notification should be sent.

The rules should be configurable so that the system can be adapted for different business needs.

Example rule categories:

* Price increase alerts
* Price decrease alerts
* Volatility alerts
* Daily status updates
* Threshold-based alerts
* Manual review alerts
* Management summary alerts

### 4. Event Logger

The event logger stores relevant market events in a structured format.

This creates a history of important movements, alerts, and system decisions.

A structured event may include:

* Timestamp
* Commodity
* Current price
* Previous price
* Change amount
* Change percentage
* Event type
* Alert reason
* Notification status
* Optional business comment

Structured logs can later be used for reporting, review, audit, or process improvement.

### 5. Telegram Notification Layer

The Telegram notification layer sends clear and concise messages to users.

Notifications should be business-friendly and easy to understand.

A good notification should explain:

* What changed
* Why it matters
* Whether a review is needed
* What type of event was detected

The goal is not to overload users with raw data, but to deliver useful and structured updates.

### 6. Reporting Layer

The reporting layer can generate summaries based on logged events.

Possible reports:

* Daily price summary
* Intraday status update
* Weekly movement overview
* List of important alerts
* Management summary
* Procurement review summary

Reports help teams move from fragmented market updates to structured business visibility.

### 7. Configuration Layer

The configuration layer stores adjustable business parameters.

Examples:

* Monitored commodity
* Alert thresholds
* Notification frequency
* Telegram chat settings
* Reporting schedule
* Business-relevant price levels
* Alert severity settings

Configuration makes the system easier to adapt without changing the core logic.

## Data Flow

The simplified data flow is:

1. Market data is received.
2. The monitoring engine evaluates the latest price movement.
3. Alert rules determine whether an event is relevant.
4. Relevant events are written to structured logs.
5. Telegram notifications are sent when required.
6. Reports are generated from logged events.
7. Human users review alerts and decide whether any business action is needed.

## Example Architecture Diagram

```text
Market Data Source
        |
        v
Market Data Input
        |
        v
Monitoring Engine
        |
        v
Alert Rules
        |
        +------------------+
        |                  |
        v                  v
Event Logger        Telegram Notifications
        |
        v
Reporting Layer
        |
        v
Business Review / Human Decision-Making
```

## Human-in-the-Loop Design

The system is designed to support human decision-making, not replace it.

The bot can detect, structure, and communicate relevant market movements, but final business decisions remain with procurement, operations, commercial, or management teams.

Examples of human decisions:

* Review supplier quotations
* Contact suppliers
* Adjust procurement timing
* Escalate a cost risk
* Prepare a commercial update
* Monitor the next market movement
* Update management reporting

## Possible Technical Stack

A lightweight implementation may use:

* Python for monitoring logic
* Telegram Bot API for notifications
* JSONL or database storage for structured event logs
* Scheduled jobs or background workers for regular monitoring
* Markdown or dashboard-style summaries for reporting
* Configuration files or environment variables for adjustable settings

## Extension Opportunities

The architecture can be extended to support:

* Multiple commodities
* FX rate monitoring
* Supplier price tracking
* Freight rate indicators
* Market news summaries
* Procurement risk scoring
* CRM or ERP integration
* Google Sheets reporting
* Management dashboards

## Summary

The architecture demonstrates how a simple automation system can convert external market data into structured business alerts and reports.

The main value comes from faster visibility, better structure, and improved operational awareness.
