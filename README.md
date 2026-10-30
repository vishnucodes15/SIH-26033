# Smart India Hackathon Workshop
# Date:30/10/2026
## Reference Number:26009605
## Name:Sre Vishnu Priyar L N

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
 1. Detailed Explanation of the Proposed Solution

My project is a decentralized, AI-powered digital marketplace and collaborative logistics network that connects individual farmers and Farmer Producer Organizations (FPOs) directly with retail consumers, Resident Welfare Associations (RWAs), and institutional bulk buyers such as hostels, restaurants, and food processors.

This project operates through three integrated pillars:

***Multimodal Farmer & FPO Onboarding Portal:** Farmers list harvested or upcoming crops using a zero-typing voice interface in regional languages via mobile app, WhatsApp bot, or Interactive Voice Response (IVR).
***Dual-Engine Direct Marketplace (B2B & B2C Group Buying):** Institutional buyers execute forward contracts and bulk spot purchases, while urban households use neighborhood group-buying pools to aggregate small orders into single bulk drops.
***Collaborative Logistics Grid:** An automated dispatch engine that aggregates local rural transport (tractors, mini-trucks, and third-party logistics fleets) into milk-run collection routes with real-time tracking.

### 2. How It Addresses the Problem

***Eliminates Multi-Tier Intermediaries:** Bypasses the traditional four to six layers of commission agents and sub-wholesalers by routing orders and escrow payments directly from buyers to farmer bank accounts.
***Prevents Distress Selling via Demand Forecasting:** Machine learning models analyze seasonal trends, weather, and regional consumption to advise FPOs on harvest timing and expected price bands.
***Cuts Transport Costs via Route Optimization:** Dynamic load-pooling combines partial loads from multiple neighboring farms along a single route, lowering per-kilogram freight costs by 25% to 35%.

### 3. Innovation and Uniqueness

***Edge-AI Computer Vision Grading at Farm Gate:** Farmers capture a smartphone photo of their produce batch to generate an instant, tamper-proof grade (Grade A, B, or C) based on size, color, and surface defects.
***Neighborhood Micro-Consolidation (RWA Pooling):** Solves the high cost of B2C last-mile delivery by turning urban apartment societies into single drop-off nodes once a minimum community weight threshold is reached.
***ONDC-Native Interoperability:** Built on the Open Network for Digital Commerce (Beckn Protocol), allowing farmer listings in this project to be discovered across external buyer apps without platform lock-in.
***Instant Split-Settlement Escrow:** Upon digital proof-of-delivery at the buyer node, smart UPI mandates instantly split and settle payments to the farmer and the logistics driver simultaneously.


## Technical Approach
### 1. Technologies to Be Used

| Layer | Technology Stack | Core Purpose |
| --- | --- | --- |
| **Frontend & Voice** | Flutter, React.js, Bhashini API | Cross-platform apps and regional voice input |
| **Backend & Protocol** | Node.js, FastAPI, Beckn Protocol | Microservices API and ONDC network integration |
| **AI & Analytics** | PyTorch, YOLOv8, Prophet, OR-Tools | Crop grading, demand forecasting, and routing |
| **Database & Storage** | PostgreSQL, PostGIS, Redis | Geospatial matching and real-time order state |
| **Payments & Cloud** | UPI Autopay, Docker, AWS | Split escrow settlements and scalable hosting |

In this project, the mobile application uses offline-first local caching so farmers in low-connectivity rural zones can record inventory and sync automatically when network coverage returns. Geospatial indexing via PostGIS maps farm coordinates against available rural transport fleets within a 15-kilometer radius.

### 2. Methodology and Process for Implementation
<img width="666" height="462" alt="image" src="https://github.com/user-attachments/assets/9bf92d33-a906-446a-aea1-2610d04d8166" />

#### Step-by-Step Implementation Process

1. **Supply Registration & AI Grading:** A farmer or FPO representative logs available produce via voice or app and uploads a sample photo, which the YOLOv8 model grades for quality verification.
2. **Predictive Pricing & Listing:** The AI engine cross-references historical Agmarknet mandi rates, regional weather data, and active buyer demand to recommend a fair floor price before publishing the lot.
3. **Demand Aggregation:** Bulk buyers place direct lot orders, while retail consumers join 24-hour neighborhood pooling windows to combine individual vegetable and grain baskets into bulk orders.
4. **Capacitated Vehicle Routing (CVRP):** Once order thresholds are met, Google OR-Tools calculates the shortest multi-stop pickup sequence across farms and assigns the nearest registered commercial vehicle.
5. **Quality Check & Escrow Payout:** The driver scans a QR code at farm pickup and buyer drop-off, triggering an automated UPI split settlement that credits the farmer and transporter immediately.


## Feasibility and Viability
### 1. Analysis of the Feasibility of the Idea

* **Technical Feasibility:** High, as this project combines mature, open-source frameworks (YOLOv8, OR-Tools, PostGIS) with existing India Stack public digital infrastructure (Bhashini, UPI, and ONDC).
* **Operational Feasibility:** By anchoring rural collection around existing FPOs and Village Level Entrepreneurs (VLEs), my project avoids heavy capital expenditure on private warehouses.
* **Financial Viability:** The system sustains operations via a lean 2% to 3% transaction fee on B2B bulk orders and premium analytics subscriptions for institutional food processors.

### 2. Potential Challenges and Risks

* **Digital Literacy & Rural Connectivity Gaps:** Smallholder farmers may struggle with complex smartphone interfaces or intermittent mobile data at the farm gate.
* **Quality Disputes Upon Delivery:** Bulk buyers may reject or discount produce on arrival if physical quality deviates from the listed grade.
* **Last-Mile Logistics Fragmentation:** Empty return trips (deadheading) and uncoordinated rural drivers can inflate transportation costs on low-volume days.

### 3. Strategies for Overcoming These Challenges

* **Voice-First & Assisted Onboarding:** Deploy Bhashini-powered voice bots alongside trained FPO coordinators who batch-upload inventory on behalf of non-smartphone farmers.
* **Two-Stage Verification & Transit Insurance:** Pair smartphone AI grading at pickup with rapid physical verification by the logistics partner, backed by micro-insurance for transit spoilage.
* **Backhaul Load Matching:** Partner with rural agri-input suppliers (fertilizers, seeds, and FMCG distributors) so delivery trucks carry farm inputs on their return leg to villages.


## Impact and Benefits
### 1. Potential Impact on the Target Audience

* **Farmers & FPOs:** Increases net price realization by 25% to 40% while eliminating delayed payments and arbitrary mandi commission deductions.
* **Retail Consumers & RWAs:** Reduces household expenditure on fresh produce by 15% to 25% with farm-traceable freshness delivered within 18 to 24 hours of harvest.
* **Bulk Buyers & Retailers:** Guarantees predictable supply volumes, standardized quality grading, and transparent procurement pricing without daily wholesale market visits.

### 2. Benefits of the Solution

* **Economic Benefits:** Retains rural wealth within farming communities, creates steady income for local commercial vehicle owners, and stabilizes retail food inflation.
* **Social Benefits:** Empowers smallholder farmers with transparent market data, strengthens collective bargaining through FPOs, and reduces rural debt traps.
* **Environmental Benefits:** Cuts post-harvest perishable food wastage by up to 30% through harvest-to-order matching and reduces carbon emissions via optimized truck load factors.


## Research and References
1. **Ministry of Agriculture & Farmers Welfare (e-NAM & Agmarknet Portal):** Historical wholesale price indices and mandi arrival datasets — [https://agmarknet.gov.in](https://www.google.com/search?q=https://agmarknet.gov.in)
2. **NITI Aayog Task Force Report on Agriculture Development:** Analysis of supply chain fragmentation, post-harvest losses, and farmer share in consumer rupee — [https://www.niti.gov.in](https://www.google.com/search?q=https://www.niti.gov.in)
3. **NABARD FPO Status Report & Guidelines:** Operational frameworks for integrating Farmer Producer Organizations into digital value chains — [https://www.nabard.org](https://www.google.com/search?q=https://www.nabard.org)
4. **Open Network for Digital Commerce (ONDC) Agri-Domain Whitepaper:** Technical standards for decentralized agricultural e-commerce and Beckn protocol schemas — [https://ondc.org](https://www.google.com/search?q=https://ondc.org)
5. **Digital India Bhashini Mission:** Open APIs for multilingual voice translation and speech-to-text for rural inclusion — [https://bhashini.gov.in](https://www.google.com/search?q=https://bhashini.gov.in)
