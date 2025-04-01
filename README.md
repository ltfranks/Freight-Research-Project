# Simulating Disruption Events in the US Highway Freight Network

![image](https://github.com/user-attachments/assets/724116a5-34ca-47d7-ace5-0c9dc636a33e)


## Overview
This project simulates disruptions in the US highway freight network using data from the US Department of Transportation's Freight Analysis Framework (FAF). The goal is to analyze how disruptions impact cargo transportation and identify the most vulnerable highway segments.

## Authors
- Ananya Bishnoi
- Frank Tucci
- Luke Franks
- Miya Reese

**Advisor:** Dr. Theresa Migler

## Data Source
The simulation uses FAF data, which includes:
- Origin and destination of shipments
- Mode of transportation
- Estimated weight and value of shipments

In 2022, approximately **11.7 billion tons** of cargo, worth **$15 trillion**, were shipped via US highways.

## Methodology
### Network Construction
- FAF’s statistical metro areas serve as **nodes**.
- Directed edges represent trade corridors where **edge weights** indicate tons of cargo transported.
- The analysis focuses on corridors with **over 500,000 tons** of annual cargo flow in the **continental US**.

### Simulation Design
1. **Disruption Simulation:** A selected edge (road segment) is removed to simulate a blockage.
2. **Rerouting:** Cargo is rerouted through alternative paths via intermediate nodes.
3. **Traffic Impact Analysis:** Increased load on detour routes is computed as a percentage increase in normal throughput.
4. **Vulnerability Assessment:** The process is repeated for each edge, and the average strain on roads is recorded.

## Findings
- Highways in **California, Texas Triangle, Midwest, and the East Coast** show the highest freight density.
- **Closeness centrality** highlights the most connected nodes.
- **Small-to-medium-sized cities parallel to major trade corridors** are the most vulnerable to disruptions.
- The results can help **transportation planners and emergency response teams** prepare for highway disruptions.

## Future Work
- Develop a **realistic US highway model** instead of a point-to-point network.
- Implement **advanced route-assignment algorithms** that split shipments across multiple paths and transport modes (e.g., rail).

## Visualization
- **Figure 1:** Top 10 city pairings and commodity types.
- **Figure 2:** Network map and degree distribution.
- **Figure 3:** Rerouting example from Los Angeles to San Francisco via Fresno.
- **Figure 4:** Vulnerability heatmap (Red = High Risk, Blue = Low Risk).

## Code Repository
The simulation code is available in this Jupyter Notebook:
[Senior Project Code](https://github.com/ltfranks/Freight-Research-Project/blob/main/senior_proj.ipynb)

## References
- Bureau of Transportation Statistics. Freight Analysis Framework 5. [FAF5 Data](https://www.bts.gov/faf)
