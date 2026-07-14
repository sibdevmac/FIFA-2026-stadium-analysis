# ⚽ FIFA 2026 Venue Selection Analysis: Infrastructure vs Football Passion

## 📌 Project Overview

The FIFA World Cup is the largest sporting event in the world after the Olympic Games. While the tournament is celebrated for bringing nations together, the selection of host venues often raises an interesting question:

> **Does FIFA prioritize commercial infrastructure or football passion when selecting host cities?**

This project attempts to answer that question using data analytics techniques including feature engineering, correlation analysis, clustering, Principal Component Analysis (PCA), and geographic visualization.

The objective is to investigate whether FIFA's venue selection is driven primarily by tourism and infrastructure or whether football culture also plays a significant role.

---

# 📂 Dataset

Since no official dataset exists combining infrastructure indicators for FIFA host cities, a custom dataset was created containing all FIFA 2026 venues.

The dataset contains the following variables:

| Variable | Description |
|----------|-------------|
| Stadium | FIFA World Cup venue |
| City | Host city |
| Country | Host nation |
| Capacity | Stadium seating capacity |
| Annual_Tourists_Millions | Annual tourist arrivals (millions) |
| Airport_Passengers_Millions | Annual airport passenger traffic (millions) |
| Hotel_Rooms | Estimated hotel room availability |
| Metro_Population_Millions | Metropolitan population |

---

# 🏗 Infrastructure Index

To quantify the commercial readiness of each city, an **Infrastructure Index** was developed.

The index combines:

- Annual Tourists
- Airport Passenger Traffic
- Hotel Room Capacity

After normalizing the variables, the Infrastructure Index was calculated to compare cities on a common scale.

This serves as a proxy for a city's ability to accommodate international visitors during the FIFA World Cup.

---

# 📊 Infrastructure vs Stadium Capacity

The first analysis compares:

- **Infrastructure Index**
- **Stadium Capacity**

The visualization divides cities into four strategic quadrants.

### Key Findings

### High Infrastructure + High Capacity

- New York
- Los Angeles
- Atlanta
- Dallas

These cities possess:

- Major international airports
- Large tourism industries
- Extensive hotel infrastructure
- High-capacity stadiums

These appear to be FIFA's flagship commercial venues.

---

### Lower Infrastructure + High Capacity

- Mexico City
- Kansas City

These cities possess large stadiums despite comparatively lower infrastructure scores.

Their inclusion suggests that football heritage and sporting significance influence FIFA's selection process.

---

### Lower Infrastructure + Lower Capacity

- Monterrey
- Guadalajara
- Vancouver
- Toronto

These cities appear to provide regional representation while maintaining strong football traditions.

---

### Higher Infrastructure + Moderate Capacity

- Miami
- Philadelphia
- Seattle
- San Francisco Bay Area

These cities demonstrate strong logistical capability despite having relatively smaller stadiums.

---

# 🌎 Geographic Visualization

The Infrastructure Index was visualized on a North America map using a bubble plot.

Bubble size represents:

- Stadium Capacity

Bubble color represents:

- Infrastructure Index

This visualization clearly demonstrates how FIFA venues are concentrated around major transportation and tourism hubs.

---

# 🔥 Correlation Analysis

A correlation heatmap was generated to investigate relationships among the infrastructure variables.

## Major Findings

### Airport Passengers ↔ Hotel Rooms

**Correlation: 0.93**

Cities with higher airport traffic consistently have larger hotel capacities.

---

### Annual Tourists ↔ Airport Passengers

**Correlation: 0.77**

Major tourist destinations generally possess stronger international connectivity.

---

### Annual Tourists ↔ Hotel Rooms

**Correlation: 0.75**

Tourism demand is strongly associated with accommodation infrastructure.

---

### Capacity ↔ Tourism

**Correlation: 0.60**

Although larger stadiums tend to exist in tourist destinations, notable exceptions indicate that stadium size alone does not explain FIFA's selection process.

---

## Key Insight

The correlation analysis demonstrates that FIFA host cities generally possess integrated tourism and transportation infrastructure.

However, infrastructure alone cannot explain venue selection.

Cities such as Mexico City and Kansas City suggest that football heritage also contributes to FIFA's decision-making process.

---

# 🤖 K-Means Clustering

To identify natural groups among FIFA host cities, K-Means clustering was performed after applying StandardScaler.

Three clusters emerged.

---

## Cluster 2 — Global Commercial Hubs

Cities:

- New York
- Dallas
- Los Angeles
- Atlanta

Characteristics:

- Highest tourism
- Largest airports
- Largest hotel inventory
- High-capacity stadiums

These cities maximize:

- Sponsorship opportunities
- Broadcasting reach
- International tourism revenue

---

## Cluster 1 — Regional / Football-Culture Cities

Cities:

- Monterrey
- Guadalajara
- Vancouver
- Toronto

Characteristics:

- Smaller infrastructure footprint
- Lower tourism
- Smaller stadiums

Despite comparatively modest infrastructure, Monterrey and Guadalajara remain among North America's strongest football cities.

---

## Cluster 0 — Balanced Infrastructure + Football Markets

Cities:

- Miami
- Houston
- Seattle
- Boston
- Philadelphia
- Kansas City
- Mexico City
- San Francisco Bay Area

These cities combine respectable infrastructure with significant football relevance.

---

# 📈 Principal Component Analysis (PCA)

Principal Component Analysis was performed to reduce five infrastructure variables into two principal components.

Variables included:

- Capacity
- Annual Tourists
- Airport Passengers
- Hotel Rooms
- Metro Population

The PCA visualization revealed clear separation among host cities.

---

## Principal Component 1 (PC1)

PC1 primarily represents:

> **Infrastructure / Commercial Attractiveness**

Cities with high PC1 scores include:

- New York
- Los Angeles
- Atlanta
- Dallas

These cities combine:

- High tourism
- Major airports
- Extensive hotel capacity
- Large stadiums

The farther right a city appears, the more commercially attractive it becomes as a global sporting destination.

---

## Principal Component 2 (PC2)

PC2 captures characteristics not fully explained by infrastructure.

Mexico City appears as a significant outlier because of:

- Exceptional football heritage
- Massive metropolitan population
- Iconic stadium
- Strong football culture

This separates Mexico City from the commercially oriented U.S. cities.

---

## PCA Cluster Interpretation

### Cluster 2 (Yellow)

Global Commercial Hubs

- New York
- Dallas
- Los Angeles
- Atlanta

These cities maximize commercial value through tourism, broadcasting, sponsorship, and transportation infrastructure.

---

### Cluster 1 (Green)

Regional Gateway Cities

- Monterrey
- Guadalajara
- Vancouver
- Toronto

These cities demonstrate that football culture and regional representation remain important despite comparatively smaller infrastructure.

---

### Cluster 0 (Purple)

Balanced Host Cities

- Miami
- Houston
- Boston
- Philadelphia
- Seattle
- Kansas City
- Mexico City
- San Francisco Bay Area

These cities represent a balance between infrastructure development and football significance.

---

## Major Finding

The PCA confirms that FIFA's host cities are **not homogeneous**.

Instead, they naturally separate into three strategic categories:

- Global commercial hubs
- Balanced football markets
- Regional football cities

Mexico City stands out as the strongest example of football heritage outweighing purely commercial considerations.

Similarly, Monterrey and Guadalajara demonstrate that football culture remains an important factor in venue selection despite comparatively lower tourism infrastructure.

---

# 📌 Conclusion

This analysis suggests that FIFA's venue selection process cannot be explained solely by commercial infrastructure.

While many host cities possess world-class tourism, transportation, and hospitality infrastructure, several venues with comparatively lower commercial indicators continue to be selected because of their football heritage, iconic stadiums, and regional importance.

The results indicate that FIFA balances:

- Commercial profitability
- Tourism potential
- Transportation infrastructure
- Football tradition
- Geographic representation

rather than optimizing a single objective.

---
# Author
Sibankar Saha

This project is intended for educational and portfolio purposes.

---
