# Hospital Analytics Assistant

AI-powered Hospital Analytics Assistant built using **n8n**, **PostgreSQL**, **OpenAI**, **Slack**, and **QuickChart** to provide hospital quality analysis, comparisons, insights, and visualizations.

## Features

* Query hospital quality datasets using natural language
* Compare hospitals across different metrics
* Retrieve hospital information including:

  * Overall ratings
  * Mortality measures
  * Complication measures
  * Readmission measures
  * Maternal health measures
  * Timely and effective care measures
  * Emergency services
  * Ownership and hospital type
* Generate automatic insights
* Create charts dynamically for better visualization
* Send results directly to Slack
* Limit large outputs for readability

## Visualization Logic

* **1–5 rows**

  * Text response only

* **6–20 rows**

  * Text response + chart visualization

* **More than 20 rows**

  * Prompt user to request fewer records

## Tech Stack

* **n8n** – workflow orchestration
* **PostgreSQL** – hospital analytics database
* **OpenAI API** – natural language to SQL generation
* **Slack API** – chat interface
* **QuickChart API** – dynamic chart generation

## Database Tables

The workflow currently uses:

1. `hospital_general_information`
2. `unplanned_hospital_visits_hospital`
3. `complications_and_deaths_hospital`
4. `maternal_health_hospital`
5. `timely_and_effective_care_hospital`

## Example Questions

### Hospital comparisons

* Compare hospital ratings and complication scores in Texas hospitals
* Top 10 hospitals with highest mortality
* Show 5 hospitals with best readmission scores
* Compare emergency services across hospitals
* List hospitals with the highest ratings

### Maternal health

* Show hospitals with maternal health measures
* Compare maternal measures in Texas hospitals

### Quality metrics

* Top 10 hospitals with lowest complication rates
* Compare infection measures across hospitals
* Show hospitals with patient safety metrics

## Workflow Overview

Slack User Query

↓

OpenAI SQL Generation

↓

PostgreSQL Query Execution

↓

Insight Generation

↓

Conditional Visualization Logic

↓

QuickChart Generation

↓

Slack Response

## Project Structure

```text
hospital-analytics-assistant/
│
├── workflow.json
├── README.md
├── screenshots/
├── docs/
└── assets/
```

## Future Improvements

* Dashboard interface
* More chart types
* Predictive hospital analytics
* Trend analysis over time
* Export reports as PDF
* Advanced filtering options

## Author

Gayatri Nair
