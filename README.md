# Smart India Hackathon Workshop
# Date:26\10\2026
## Reference Number:26004666
## Name: Neha S 

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
FarmBridge: A Demand-Driven Farm-to-Market Network

FarmBridge is a digital platform designed to connect farmers directly with retailers, restaurants, institutional buyers, and consumers. It reduces dependence on unnecessary intermediaries by combining demand aggregation, harvest matching, transparent pricing, and shared transportation.

The platform introduces a Demand-Pool and Harvest-Match mechanism that collects buyer requirements, combines compatible orders, and matches them with available farm produce. This enables farmers to access multiple buyers while helping consumers obtain fresh produce at competitive prices.

Key features include:

Direct farmer-to-buyer marketplace.

Farmer Producer Organization (FPO) and group-selling support.

Demand aggregation and harvest matching.

Transparent pricing with itemized transportation and service charges.

Shared delivery planning to reduce logistics costs.

Produce quality verification and batch tracking.

Digital transaction receipts and payment-status tracking.

Regional-language support and low-bandwidth access.

Farmers retain control over their minimum acceptable selling price and must approve proposed transactions before confirmation.


## Technical Approach
Technology Stack

Frontend: React Progressive Web App (PWA).

Backend: Python with FastAPI.

Database: PostgreSQL with PostGIS for geographic queries.

Matching engine: Python-based rules and weighted scoring.

Mapping: OpenStreetMap and OSRM or an equivalent routing service.

Notifications: SMS and in-app notifications.

Deployment: Docker and cloud hosting.

System Architecture and Workflow

flowchart TD
    A[Farmers and FPOs] --> B[Farmer Portal]
    C[Retailers and Consumers] --> D[Buyer Portal]
    B --> E[Backend API]
    D --> E
    E --> F[Demand Pool and Harvest Registry]
    F --> G[Matching Engine]
    G --> H[Transparent Price Calculator]
    H --> I{Both Parties Approve?}
    I -- No --> G
    I -- Yes --> J[Shared Logistics Planner]
    J --> K[Collection and Quality Check]
    K --> L[Delivery and Batch Tracking]
    L --> M[Payment and Settlement Tracking]
    M --> N[Farmer and Buyer Dashboards]
    F --> O[(PostgreSQL Database)]
    G --> O
    L --> O
    M --> O

Implementation Methodology

Register farmers, FPOs, retailers, and consumers.

Record crop type, quantity, quality grade, harvest date, and location.

Collect buyer requirements and aggregate compatible orders.

Match available farm lots using price, quantity, freshness, quality, and distance.

Display the complete price breakdown and obtain confirmation from both parties.

Group compatible orders into cost-efficient delivery routes.

Record collection weights, quality checks, delivery status, and payment information.

Evaluate performance using farmer earnings, buyer costs, delivery efficiency, and order fulfilment.

<img width="1174" height="2400" alt="sih" src="https://github.com/user-attachments/assets/5f397ae3-1f74-40bd-bed2-77b8e8eb7c1c" />


## Feasibility and Viability
FarmBridge is feasible as a student software project because it can be developed using open-source technologies such as React, Python FastAPI, and PostgreSQL. The initial prototype can focus on one agricultural region, a few selected crops, and a small group of farmers and buyers. Existing mapping services can be used for delivery planning, reducing development complexity and cost.

The platform can be implemented in phases, beginning with farmer registration, crop listings, buyer requests, and transparent pricing. Demand aggregation, harvest matching, delivery planning, and payment tracking can then be integrated.

Potential Challenges and Strategies to Overcome Them

1. Limited Digital Literacy: Some farmers may find digital platforms difficult to use. This can be addressed through a simple regional-language interface, voice guidance, and assistance from Farmer Producer Organizations (FPOs).

2. Fragmented Buyer Demand: Individual buyers may require small quantities, making direct delivery expensive. The platform will combine compatible orders and coordinate shared transportation.

3. High Transportation Costs: Long distances and partially loaded vehicles can increase delivery expenses. The shared logistics planner will group nearby deliveries and optimize collection routes.

4. Produce Quality Variations: Differences in quality and freshness can cause disputes. The platform will maintain batch records, collection weights, quality grades, and delivery confirmation.

5. Inaccurate Inventory Information: Farmers may list quantities that are no longer available. Inventory will be updated after order confirmation and verified during collection.

6. Low Internet Connectivity: Rural areas may experience unreliable internet access. A lightweight Progressive Web App (PWA), saved draft information, and SMS notifications can improve accessibility.

7. Payment Disputes and Delays: Unclear deductions can reduce trust. The platform will display itemized prices, maintain transaction records, and track payment and settlement status.

8. Financial Sustainability: Excessive platform charges could reduce farmers' earnings. FarmBridge will use transparent, reasonable service fees and may generate revenue through bulk-buyer subscriptions and logistics coordination services.

The project is technically achievable using existing software tools and can be tested through a small pilot before wider deployment. Its long-term viability will depend on farmer participation, reliable buyer demand, efficient transportation, and demonstrable improvements in farmer earnings and consumer costs.



## Impact and Benefits
Social Benefits

Provides digital market access to rural communities.

Supports Farmer Producer Organizations and local agricultural networks.

Enables participation through regional languages and simplified interfaces.

Improves trust through transparent transaction records.

Environmental Benefits

Reduces unnecessary delivery trips through order consolidation.

Helps improve vehicle utilization.

Supports faster movement of perishable produce.

Has the potential to reduce food wastage through demand-based matching.

Measurable Performance Indicators

Farmer net realization per kilogram.

Consumer savings per kilogram.

Transportation cost per completed order.

Percentage of orders delivered successfully.

Percentage of produce lost or rejected.

Average time taken for farmer settlement.

Repeat participation by farmers and buyers.

The impact should be verified through a pilot that compares results against baseline transactions involving equivalent produce, quality, and delivery conditions.
## Research and References
SIH-26033 GitHub Repository: https://github.com/selvasachein/SIH-26033.git

e-NAM — National Agriculture Market: https://www.enam.gov.in/

OpenStreetMap: https://www.openstreetmap.org/

FastAPI Documentation: https://fastapi.tiangolo.com/

PostgreSQL Documentation: https://www.postgresql.org/docs/

OSRM Routing Engine: https://project-osrm.org/
