# A320 Fuselage Agent Control

## Goal

Give the A320 fuselage line one place to see whether assembly is on track for quality, cost and delivery, and why it is not when it slips. The four KPIs that decide this are quality complaints, scrap, assembled regions against plan, and right first time. A team of AI agents watches them around the clock, spots deviations as they happen, finds likely causes and routes each issue to the right person, so the line reacts within minutes instead of at the next shift meeting.

**Who it is for:** shift and line leads, quality engineers, production planners and the project team responsible for fuselage assembly.

**What the agents do:** read SAP QM, SAP MM, MES confirmations, inspection records and torque logs; classify quality notifications and assign owners; keep the scrap Pareto and section status current; compute right first time per station; open an 8D and escalate to the shift lead when a limit is crossed; draft the shift handover.

**What it should achieve:** faster reaction to quality and scrap events, fewer repeat defects through early root-cause work, less manual KPI reporting, and one shared picture of the line across shifts.

## What is on the page

Interactive dashboard prototype for an AI multi-agent system that monitors A320-family fuselage assembly KPIs:

- Quality complaints (quality notifications by defect type)
- Scrap (value and Pareto by part family)
- Assembled regions (section status S11–S19 per aircraft)
- Right first time (trend and by station)

The **Agent orchestration** section shows how the agents work together: orchestration graph, incident trace, shift timeline, source → agent → outcome flow, agents on the fuselage, agent × KPI heatmap, and load / response time.

All figures are **simulated sample data**. The assistant answers are rule-based from that data. Single static `index.html`, no build step.

## Wall-display mode

The page keeps the screen awake with the Screen Wake Lock API (Chrome, Edge, Safari 16.4+, Firefox 126+), re-acquires it when the tab becomes visible again, and shows the status in the top bar. The simulation rolls over from shift to shift (A 06:00, B 14:00, C 22:00) so it runs indefinitely.
