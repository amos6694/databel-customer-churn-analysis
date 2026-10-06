# Databel Customer Churn Analysis

## Project Objective

The objective of this project is to identify the main factors contributing to customer churn at Databel and translate those findings into practical customer-retention strategies.

**Business question:** Which customer demographics, service plans, usage patterns, and competitive factors are most strongly associated with churn, and how can Databel use these insights to improve retention?

## Executive Summary

This project analyzes customer churn for Databel, a telecommunications company, to identify the primary factors influencing customer retention and cancellations.

Using Excel-based data preparation, PivotTables, calculated fields, and customer segmentation techniques, the analysis evaluates churn patterns across customer demographics, service plans, usage behavior, and competitive factors.

The findings highlight several opportunities for Databel to reduce churn, improve customer satisfaction, and strengthen its competitive position through targeted retention strategies.

![Databel Churn Dashboard Overview](overview.png)

*Figure 1: Databel's customer churn dashboard summarizing overall churn performance, demographic patterns, data usage, competitor-related factors, and customer-provided churn reasons.*

## Key Findings

- **Overall churn rate:** 26.86% of customers have churned.
- **Senior customer churn:** Senior customers have a significantly higher churn rate of **38.22%**.
- **Competitive pressure:** A major driver of churn is competition, particularly competitors offering:
  - Better pricing and service offers.
  - More attractive devices and upgrade options.
  - Stronger perceived value for customers.
- **Unlimited Data plan behavior:** Customers on Unlimited Data plans who demonstrate relatively low data usage have elevated churn. This suggests that some customers may not perceive enough value from their current plans.
- **Customer segmentation:** Churn varies across age groups, service usage patterns, and plan types, emphasizing the need for targeted rather than one-size-fits-all retention campaigns.

## Data Modeling Techniques

The analysis used the following data modeling and analysis techniques:

- **Excel PivotTables**
  - Summarized churn by customer demographics, plans, usage, and churn reasons.
  - Compared churn rates across customer segments.
  - Identified patterns in customer behavior and service usage.

- **Calculated Fields**
  - Calculated overall and segment-level churn rates.
  - Compared churned and retained customer populations.
  - Derived performance metrics to support business insights.

- **Binned Age Groups**
  - Grouped customers into meaningful age categories.
  - Enabled comparison of churn behavior across different life-stage segments.
  - Helped identify senior customers as a high-risk retention segment.

## Worksheet Architecture

The `1_1_data_preparation.xlsx` workbook is organized into five worksheets. Each sheet supports a different stage of the analysis, from customer-level data preparation to executive dashboard reporting.

| Worksheet | Category | Primary Function |
|:---|:---|:---|
| `Databel - Customer` | Raw Data | Primary customer-level table containing 6,687 records, demographics, service plans, usage behavior, charges, churn status, churn categories, and churn reasons. |
| `Databel - Aggregate` | Processed Data | Grouped analysis table containing derived dimensions such as consumption tiers, demographic groupings, and averaged operational metrics used in PivotTable analysis. |
| `Churn Analysis` | Analytical Models | Collection of PivotTables and analytical matrices evaluating churn by demographics, age groups, data consumption, Unlimited Data plans, state, tenure, and contract type. |
| `Customer Pivots` | Summary Metrics | Summary worksheet containing headline KPIs and detailed competitor-related churn breakdowns. |
| `Overview` | Executive Dashboard | Presentation-ready dashboard containing KPI cards, high-risk segment summaries, state-level comparisons, and visual charts. |

### `Databel - Customer`

This worksheet is the primary customer-level source table. It contains one row per customer and provides the underlying fields used throughout the analysis, including:

- **Customer identifiers and churn status:** `Customer ID`, `Churn Label`, and the binary `Churned` field.
- **Demographics:** `Age`, `Gender`, `Under 30`, `Senior`, and `State`.
- **Plans and services:** `Contract Type`, `Payment Method`, `Intl Plan`, `Unlimited Data Plan`, and `Device Protection & Online Backup`.
- **Usage and charges:** Account length, local and international calls and minutes, average monthly GB download, monthly charge, total charges, extra international charges, and extra data charges.
- **Churn categorization:** `Churn Category` and `Churn Reason`, including reasons such as a competitor making a better offer or dissatisfaction with support.

### `Databel - Aggregate`

This worksheet contains processed and grouped data used to support segment-level analysis. It includes derived categories such as:

- **Grouped consumption:** `Less than 5GB`, `Between 5 and 10 GB`, and `10 or more GB`.
- **Demographic groupings:** Under-30, Senior, Other, and age-based groups.
- **Segment metrics:** Average monthly charges, average customer service calls, average extra international charges, average extra data charges, and average monthly GB download.

These grouped fields make it easier to compare churn patterns across meaningful customer segments.

### `Churn Analysis`

This worksheet acts as the main analytical PivotTable hub. It evaluates churn drivers across multiple business dimensions, including:

- Churn rates by demographic group and age range.
- Senior versus non-senior customer churn.
- Unlimited Data plan status compared with grouped data consumption.
- State-level churn among customers with an international plan.
- Churn by account-length or tenure bands.
- Churn comparisons across contract types, including month-to-month and longer-term contracts.

### `Customer Pivots`

This worksheet contains summary metrics and detailed behavioral breakdowns. Its main functions include:

- Reporting the headline KPIs of **6,687 total customers**, **1,796 churned customers**, and a **26.86% churn rate**.
- Ranking competitor-related churn reasons.
- Comparing customer defections associated with better competitor offers, better competitor devices, higher download speeds, and more data.

### `Overview`

This worksheet is the executive dashboard and final presentation layer of the workbook. It brings together:

- KPI cards for total customers, churned customers, and overall churn rate.
- Demographic churn comparisons, including the **38.22% senior churn rate**.
- Age-range customer counts and churn rates.
- Churn by average data consumption and Unlimited Data plan status.
- Competitor churn analysis.
- Customer-provided churn reasons.
- State-level international-plan churn comparisons.

The `Overview` worksheet is designed to communicate the most important findings quickly to business stakeholders.

## Strategic Business Recommendations

### 1. Develop a Senior Customer Retention Program

Since senior customers experience a churn rate of **38.22%**, Databel should introduce dedicated retention initiatives, including:

- Simplified plan options and billing communications.
- Personalized customer support for service and device issues.
- Loyalty discounts or long-term customer benefits.
- Proactive outreach before contract or promotional periods expire.
- Device education and upgrade assistance.

### 2. Strengthen Competitive Positioning

Competitor-driven churn indicates that customers are responding to better offers and devices elsewhere. Databel should:

- Review pricing and promotional offers against major competitors.
- Introduce targeted win-back offers for customers considering cancellation.
- Improve device upgrade programs and financing options.
- Communicate the value of Databel’s network, services, and customer support more clearly.
- Monitor competitor promotions on an ongoing basis.

### 3. Optimize Unlimited Data Plans

Customers with Unlimited Data plans but low usage may not see sufficient value in their current plans. Databel should:

- Identify customers whose usage is consistently below the plan’s value threshold.
- Offer lower-cost or right-sized plans that better match actual usage.
- Provide personalized plan reviews through customer service and digital channels.
- Use usage alerts and plan recommendations to increase transparency.
- Promote additional benefits, such as hotspot data or entertainment services, where appropriate.

### 4. Implement Proactive Churn Monitoring

Databel should create an early-warning retention process using indicators such as:

- Declining usage.
- Repeated service complaints.
- Contract or promotion expiration.
- Competitor-related dissatisfaction.
- Low engagement with plan benefits.
- Recent device or billing issues.

High-risk customers can then receive timely, personalized interventions before they churn.

### 5. Use Segment-Based Retention Campaigns

Retention strategies should be tailored to customer needs rather than applied uniformly. Databel can improve campaign effectiveness by segmenting customers based on:

- Age group.
- Current plan.
- Usage behavior.
- Tenure.
- Churn reason.
- Device ownership and upgrade eligibility.

## Project File Directory

```text
databel-customer-churn-analysis/
├── 1_1_data_preparation.xlsx
├── overview.png
└── README.md
```

## Conclusion

The analysis shows that Databel’s churn problem is driven by a combination of customer demographics, competitive offers, device expectations, and plan-value perception.

By focusing on senior customers, improving competitive offers, optimizing Unlimited Data plans, and introducing proactive, segment-based retention campaigns, Databel can reduce churn and improve long-term customer loyalty.
