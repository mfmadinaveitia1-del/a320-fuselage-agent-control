# A320 Fuselage Agent Control

Interactive dashboard prototype for an AI multi-agent system that monitors A320-family fuselage assembly KPIs:

- Quality complaints (quality notifications by defect type)
- Scrap (value and Pareto by part family)
- Assembled regions (section status S11–S19 per aircraft)
- Right first time (trend and by station)

The **Agent orchestration** section shows how the agents work together: orchestration graph, incident trace, shift timeline, source → agent → outcome flow, agents on the fuselage, agent × KPI heatmap, and load / response time.

All figures are **simulated sample data**. The assistant answers are rule-based from that data. Single static `index.html`, no build step.
