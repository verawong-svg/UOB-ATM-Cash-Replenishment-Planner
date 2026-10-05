# UOB-ATM-Cash-Replenishment-Planner

A team hackathon prototype exploring how demand forecasting and operational planning could support UOB"s ATM cash replenishment process.

## Challenge

UOB's Operational Planning and Analytics (OPA) team manages cash replenishment planning for more than 350 ATMs across Singapore

The challenge was to determine which ATMs should be replenished and when, while balancing two competing objectives:

- Prevent ATMs from running out of cash
- Minimise unnecessary replenishment trips and operational cost

 ## Key Operational Constraints

 The proposed solution had to account for several business rules:
 - Maximum of 190 replenishment trips per day
 - ATMs falling below the 25% cash threshold should be identified as at risk
 - An ATM cannot be replenished more than once a day
 - ATMs must be replenished on Day 15 if they have not been serviced during the previous 14 days
 - Scheduled trips follows a 65% / 25% / 10% allocation across P0, P1 and P2 service windows
 - The next day's vendor schedule must be prepared by 4.30PM

## Proposed Solution

Our team developed the concept for an operational planning prototype that converts forecasted ATM cash demand into a next-day replenishment schedule.

The prototype follows this general flow:
**ATM demand patterns -> Demand forecast -> Cash-level projection -> At-risk ATM identification -> Priority scheduling -> Vendor schedule**
The prototype uses synthetic ATM data for demonstration rather than actual UOB customer or transaction data
### Demand Forecasting

The prototype uses an explainable forecasting approach based on factors including:

- Baseline ATM demand
- Weekday and weekend patterns
- Payday effects
- Public holidays
- Recent demand trends

The forecast is then used to project an ATM's cash balance and identify whether it is at risk of falling below the required threshold.

### Constraint-Based Scheduling

At-risk ATMs are prioritized according to urgency before assigned to the available replenishment windows.

The scheduling component considers the daily trip limit, mandatory replenishment rules and required P0/P1/P2 allocation. When demand exceeds available trip capacity, remaining at-risk ATMs are surfaced for follow-up rather than silently excluded.

## Prototype Features

- Interactive 350-ATM synthetic network
- Explainable cash-demand forecasting
- Projected cash-level monitoring
- At-risk ATM identification
- Priority-based replenishment scheduling
- Operational constraint validation
- P0 / P1 / P2 service-window allocation
- Vendor schedule generation and CSV export
- Interactive operational dashboard

## My Contribution
I worked as part of a four-member team and focused on understanding and presenting the scheduling and operational-constraints component of our proposed solution.

My presentation covered how at-risk ATMs were prioritised, how the 190-trip daily limit and P0/P1/P2 allocation affected scheduling, and how at-risk ATMs exceeding available trip capacity could be surfaced for operational follow-up.

This experience strengthened my understanding of translating business requirements into system logic and communicating a technical solution in a practical operational context.

## AI-Assisted Development

Claude was used as an AI-assisted development tool to generate the prototype implementation from the team's solution concept and requirements.

Our team focused on understanding the business problem, shaping the proposed solution, reviewing and understanding the generated prototype, and presenting how the solution addressed the challenge requirements.

## Technologies & Tools

- React / JavaScript
- Recharts
- Claude
- Synthetic data for prototype demonstration

## Team Project & Code Attribution

This repository documents my experience and contribution to the team hackathon project. The original prototype source code is maintained in the team's repository and is not duplicated here.

## Key Takeaways

Through this hackathon, I gained experience in:

- Breaking down a real-world operational problem into system requirements
- Understanding forecasting and constraint-based scheduling logic
- Using generative AI to rapidly prototype a technical solution
- Evaluating and explaining AI-generated implementation
- Collaborating within a four-member team
- Presenting a technical solution under hackathon time constraints
  
