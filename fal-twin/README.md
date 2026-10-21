# A320 FAL Digital Twin

Interactive concept of a digital twin for an A320 Family final assembly line (FAL), from section delivery (S50) to the flight line.

**Goal:** achieve 100 A320 aircraft per month by improving final assembly efficiency, ensuring on-time delivery, minimizing quality complaints and scrap, and reducing rework. The dashboard provides real-time production visibility, identifies bottlenecks, detects quality issues, and enables data-driven decision-making.

- **Industrial metaverse:** immersive 3D visualization and cross-functional collaboration to evaluate production processes, test improvements and accelerate decision-making.
- **Digital twin view:** simulate production scenarios to anticipate disruptions, eliminate waiting times and optimize throughput; evaluate the impact of changes on lead time, quality and resource utilization before physical implementation.
- **Edge AI:** real-time sensor data and on-site AI processing to detect anomalies, identify bottlenecks, prevent defects and reduce scrap, improving Right First Time (RFT).

**Live demo:** https://mfmadinaveitia1-del.github.io/a320-fuselage-agent-control/fal-twin/

## What it shows
- **Goal & key results:** live scorecard of delivery rate, lead time, on-time delivery, first-pass yield, rework, gliders, OEE and power peak against targets.
- **Line trace and isometric 3D line view** (three.js) with physical, digital-twin, metaverse and heat views.
- **Now reading:** guided tour, aircraft/AGV inspector with station-by-station journey, and a rule-based twin assistant.
- **Relation graph, takt margin field, station drop and signals over sweeps,** in a "decision trace" layout.
- **Alerts & predictive maintenance:** bottlenecks, engine shortage, late aircraft, robot vibration, paint-booth humidity and power-peak forecasts.
- **Orders and rush-order planning,** fleet search, line balancing (yamazumi), critical path (CPM) and an impact report that re-simulates 200 days × 3 seeds.

## How it is built
A single self-contained `index.html`: a discrete-event simulation, CPM and the assistant's rules run in the browser. No build step and no backend; three.js is loaded from a CDN.

## Data
All layouts, cycle times, rates, defect rates, costs, customers and power figures are **synthetic**, invented for this concept. They do not represent any manufacturer's data. The assistant is rule-based on the twin's model, not a language model.

A one-page summary is in [`A320_FAL_Twin_OnePager.pdf`](A320_FAL_Twin_OnePager.pdf).

Author: Miguel Figueroa
