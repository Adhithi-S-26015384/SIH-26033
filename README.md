# Smart India Hackathon Workshop
## Date: 25-11-2026
## Reference Number: 26015384
## Name: Adhithi S

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

### Benefits:

• Better prices for farmers.

• Lower prices for consumers.

• Reduced supply chain inefficiencies.

## Proposed Solution:
### 1. Detailed explanation of the proposed solution

KrishiSetu is a mobile app and website where farmers and FPOs sell their crops straight to buyers. It also arranges delivery and uses AI to make selling smarter.
It has four parts:

Farmer and FPO app: The farmer lists a crop by speaking in their own language, then adds a photo, the amount and the price they want. It works on low-end phones, and SMS and WhatsApp work as a backup.
Buyer marketplace: Families can order fresh produce or take a weekly subscription. Shops, hostels, canteens and other bulk buyers post what they need and bid directly to FPOs.
Delivery help: One truck picks up from many nearby farms and delivers to the buyer. Trucks from partners and cold-storage vehicles handle produce that spoils quickly.
AI engine: It guesses how much people will buy, suggests a fair price and plans the fastest route for each delivery. Every order makes its guesses better.

Payment goes through UPI. The money is held safely and released to the farmer only after the buyer confirms delivery.

2. How it addresses the problem

Today a crop passes through many hands before it reaches the buyer: farmer, collector, mandi agent, wholesaler, retailer, then consumer. Each one takes a cut, so the farmer gets less and the buyer pays more.

With KrishiSetu the crop goes from the farmer or FPO to KrishiSetu to the buyer, so the extra steps disappear.

Farmers earn more: the money that went to middlemen is shared between farmer and buyer.
Buyers pay less: there are fewer steps, and shared trucks cost less per farmer.
Less food is wasted: AI forecasts and faster delivery mean fewer unsold or spoiled loads.

3. Innovation and uniqueness of the solution

Shared trucks for small farmers: orders from many small farms are pooled onto one route, so each farmer pays less for transport.
Open prices: every order shows the market price, the price paid and how much of the buyer's money reached the farmer.
Easy to use: voice in local languages, SMS and WhatsApp backup, and FPO staff who help new farmers start.
Plan-ahead selling: the AI tells farmers when and where to sell, and tells buyers how much supply to expect, so crops do not rot unsold.

## Technical Approach

1. Technologies to be used

Phone app: React Native for Android, plus a simple website (PWA)
Voice and language: speech-to-text and text-to-speech in local languages, so farmers can talk instead of type
Server: Python (FastAPI), PostgreSQL with PostGIS for locations, Redis for speed
AI forecasting: Prophet, XGBoost and LSTM to guess demand and prices
Route planning: Google OR-Tools to plan the shortest pickup and delivery routes
Data sources: Agmarknet and e-NAM prices, weather data, our own order history
Payments: UPI, with money held safely until delivery is confirmed
Messages: SMS and WhatsApp gateways as a backup for farmers with basic phones
Hosting: Docker containers on a cloud server
Hardware: no special hardware. Farmers use their own Android phones, and delivery drivers use phone GPS

2. Methodology and process for implementation

Flow of one order:

Farmer lists crop → AI suggests price and finds a buyer → Buyer orders and pays by UPI (money held) → Orders are pooled and routed → One truck picks up and delivers → Buyer confirms → Farmer is paid → Data goes back to improve the AI

Steps:

List crops: the farmer adds the crop, photo and amount by voice or form.
Find a buyer: AI checks market prices and nearby demand, then suggests a fair price and a buyer.
Order and pay: the buyer pays by UPI, and the money is held safely.
Pick up: the route planner groups nearby orders onto one truck and picks the shortest route.
Deliver and pay: the buyer confirms the goods, and the money is released to the farmer.
Learn: delivery times, prices and ratings are saved so forecasts and routes improve.

How we will build it:

Weeks 1–2: build the farmer app, the buyer screens and UPI payment with held money.
Weeks 3–4: add price data, the forecasting model and the route planner.
Weeks 5–6: test with a few FPOs and buyers in one district, then fix problems.
After that: add more districts, crops and partner trucks.

<img width="452" height="678" alt="images" src="https://github.com/user-attachments/assets/9ceec8e1-4e96-4998-b24b-013444813f58" />

<img width="678" height="452" alt="images (1)" src="https://github.com/user-attachments/assets/67345c4c-97e7-4103-a7eb-338b68f7cad7" />


## Feasibility and Viability
1. Analysis of the feasibility of the idea

Technical: the main parts already exist. UPI handles payments, Agmarknet and e-NAM give public price data, and tools like OR-Tools plan routes. We connect them rather than invent them, so a working first version can be built in a few weeks.
Economic: we earn a small fee on each order, a fee for delivery, and a subscription from big buyers. The total is kept below what middlemen take today, so farmers still earn more and buyers still pay less.
Operational: FPOs already gather crops from many farmers. They can act as local pickup points, check quality and train farmers to use the app.
Where to start: one district, a few FPOs, and buyers who order regularly, such as hostels, canteens and shops. Once this works, we add more districts.

2. Potential challenges and risks

Many farmers find apps hard to use.
Buyers and farmers may argue about crop quality.
Fresh crops can spoil on the way.
A marketplace needs both buyers and sellers, and it is hard to get both at the start.
Farmers fear they will not get paid, and buyers fear they will not get what they ordered.
At the start there is little data, so the AI's guesses on demand and price may be off.

3. Strategies for overcoming these challenges

Apps are hard: use a voice app in local languages, SMS and WhatsApp as a backup, and FPO staff who help farmers list crops.
Quality arguments: use photos and grades at listing, buyer ratings, and a short window after delivery to accept or reject goods.
Spoilage: plan short routes, pick up the same day, and use cold-storage trucks from partners for crops that spoil fast.
Getting both sides: start with FPOs and a few regular big buyers in one district, so there are orders from day one.
Trust in payment: hold the buyer's UPI payment safely and release it to the farmer only after the buyer confirms delivery.
Little data: start with old mandi prices from Agmarknet and e-NAM, then let the AI learn from every real order.

## Impact and Benefits
1. Potential impact on the target audience

Farmers and FPOs: they keep a bigger share of the final price because fewer middlemen take a cut. They get paid faster, and the AI shows them what to grow, when to sell and where demand is. Small farmers pay less for transport because they share trucks.
Consumers (families): they get fresher produce at lower prices, and they can see where it came from and what the farmer was paid.
Bulk buyers (shops, hostels, canteens): they get steady supply from one place, direct deals with FPOs, and one app for ordering, paying and delivery.
Government and policy makers: they get clear data on prices, supply and demand, which helps in tracking food prices and planning.

2. Benefits of the solution

Social: small and marginal farmers get fair deals. FPOs become stronger, and drivers, pickup staff and field helpers get new rural jobs. Voice and local-language access brings farmers who are not comfortable with apps into digital markets.
Economic: less money is lost in the supply chain, so more income stays in villages. Farmers earn more, buyers pay less and the extra steps disappear.
Environmental: less food is thrown away because forecasts and faster delivery reduce spoilage. Shared trucks and planned routes mean fewer trips and fewer empty return journeys, so fuel use and emissions are lower.

## Research and References

1. Details / links of the reference and research work

e-NAM (National Agriculture Market): India's online market for crops. We studied how it connects farmers to buyers and where it falls short on delivery. enam.gov.in
Agmarknet: daily mandi prices and arrivals, which we use as the starting data for price guesses and for the open price display. agmarknet.gov.in
ONDC (Open Network for Digital Commerce): an open network for online shopping. We looked at it as a way to reach more buyers later. ondc.org
SFAC (Small Farmers' Agribusiness Consortium): supports FPOs. We used it to understand how FPOs work and how they can act as local hubs. sfacindia.com
NABARD: promotes and funds FPOs. nabard.org
Department of Consumer Affairs: monitors prices of essential food items, which shows the price gap between farm and shop. consumeraffairs.nic.in
Google OR-Tools: the free tool we use to plan the shortest delivery routes. developers.google.com/optimization
Prophet: the free forecasting tool we use to guess demand and prices. facebook.github.io/prophet
