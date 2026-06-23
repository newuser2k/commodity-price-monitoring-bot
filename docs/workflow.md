# Workflow

This document describes the high-level workflow of the Commodity Price Monitoring & Alerting Bot.

The purpose of the workflow is to turn commodity price movements into structured business notifications that can support procurement, operations, logistics, and commercial decision-making.

## 1. Market Data Monitoring

The system monitors Brent oil price movements from a market data source.

The monitoring process can run on a regular schedule or near real time, depending on the business requirement.

The goal is not to predict the market, but to detect meaningful changes and provide timely visibility to users.

## 2. Price Evaluation

Incoming price data is evaluated against predefined conditions.

Examples of conditions may include:

* Price movement above or below a configured threshold
* Significant intraday change
* Change compared with the previous status update
* Repeated movement in the same direction
* Price approaching a business-relevant level
* Market movement requiring management attention

The alert logic should be configurable so that different teams can adjust it to their operational needs.

## 3. Event Classification

When a relevant movement is detected, the system classifies the event.

Example event types:

* Price increase
* Price decrease
* Threshold reached
* Volatility alert
* Daily status update
* Management summary
* Manual review required

Event classification helps users quickly understand what happened and why the notification was sent.

## 4. Structured Logging

Each relevant event is logged in a structured format.

A structured event log may include:

* Timestamp
* Instrument or commodity
* Current price
* Previous price
* Price change
* Event type
* Alert reason
* Notification status
* Optional business comment

Structured logging is important because it creates a history of market movements and alerts that can later be reviewed by procurement, operations, or management teams.

## 5. Telegram Notification

When an event meets the notification criteria, the system sends a concise Telegram message.

The message should be clear, business-friendly, and easy to understand.

A good notification should answer:

* What changed?
* How much did it change?
* Why is this relevant?
* Does the user need to review anything?

## 6. Human Review

The system is designed as a decision-support tool.

It does not replace business judgment.

Procurement, operations, or commercial managers can review the alert and decide whether any action is required, such as:

* Checking supplier quotations
* Reviewing procurement timing
* Updating a commercial team
* Preparing a customer communication
* Monitoring the next market movement
* Escalating the issue to management

## 7. Reporting

The system can also generate regular summaries.

Examples:

* Daily price summary
* Intraday status update
* Weekly market movement overview
* List of important alerts
* Management summary

Reporting helps teams move from fragmented updates to a more structured view of market-related events.

## 8. Possible Workflow Extensions

The same workflow can be extended to other external business signals, including:

* Other commodity prices
* FX rates
* Freight cost indicators
* Supplier price changes
* Inventory risk signals
* Contract trigger levels
* Market news summaries
* Procurement-related risk indicators

## Workflow Summary

The overall workflow is:

1. Monitor commodity price data.
2. Evaluate movements against configured conditions.
3. Classify relevant events.
4. Log events in a structured format.
5. Send Telegram notifications.
6. Keep the human decision-maker in control.
7. Generate summaries for review and reporting.

The key business value is faster visibility, better structure, and improved reaction time.
