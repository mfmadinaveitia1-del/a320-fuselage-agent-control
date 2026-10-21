# A320 Fuselage Agent Control

## Goal

Provide a unified, real-time view of A320 fuselage assembly performance, ensuring production remains on track in terms of quality, cost, and delivery. The dashboard enables early identification of critical path deviations, elimination of non-value-added activities, and optimization of manufacturing processes through Lean principles, including Kanban, Just-in-Time (JIT), and Just-in-Sequence (JIS).

By integrating AI Agents, Edge AI, Digital Twins, Industrial Metaverse, and Cloud technologies, the solution enables proactive detection and prediction of supply chain, quality, and production disruptions. This supports faster, data-driven decision-making, minimizes downtime, reduces scrap and rework, and improves right-first-time performance, contributing to the production target of 100 aircraft per month.

The dashboard also provides end-to-end visibility into multi-agent orchestration, illustrating how specialized AI agents collaborate, exchange information, coordinate decisions, and execute complex, multi-step workflows as a unified, goal-driven system. This transparency enables stakeholders to monitor agent activities, understand automated decisions, track issue resolution, and maintain human oversight of critical manufacturing operations.

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

## Join cell twin

The **Join cell 07** section embeds the robot-cell digital twin from [ai-risk-benchmark/fuselage-join-twin](https://github.com/mfmadinaveitia1-del/ai-risk-benchmark/tree/main/fuselage-join-twin): six riveting robots, a vision gantry, two AGVs and 11 agents on the section 15/21 join. A copy lives in `join-cell/index.html`; opened with `?embed=1` it shows only the cell, the inspector and the agent list, and the dashboard sizes the frame to it. Open `join-cell/` on its own for the full twin with KRIs, CTQ capability and the event trace.

## Wall-display mode

The page keeps the screen awake with the Screen Wake Lock API (Chrome, Edge, Safari 16.4+, Firefox 126+), re-acquires it when the tab becomes visible again, and shows the status in the top bar. The simulation rolls over from shift to shift (A 06:00, B 14:00, C 22:00) so it runs indefinitely.

## A320 FAL Digital Twin

The folder [`fal-twin/`](fal-twin/) holds a second prototype: an interactive digital twin of the A320 Family final assembly line (S50 to flight line) in a "decision trace" layout. It shows the goal and key results, a 3D line view, critical path, takt margins, alerts with a rule-based assistant, rush-order planning and power load balancing. Open `fal-twin/index.html`, or the Pages site at `/fal-twin/`. All data is synthetic.
