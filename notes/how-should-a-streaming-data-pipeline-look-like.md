---
id: how-should-a-streaming-data-pipeline-look-like
aliases:
  - How should a streaming data pipeline look like?
tags:
  - question
date: 2025-07-10T05:58:33+0200
---

1. Orchestrating parallel snapshot taking of market data only when there is new data, for 10+ data points per instrument, and for 100+ instruments. [[snapshot-taking-orchestration|Snapshot Taking Orchestration]]
1. How to efficiently process and calculate new variables of market data in real-time, without recalculating everything from scratch every time a new data point arrives, and without loading history data that is not needed for new calculations.
2. How to process all the instruments fast and with the least amount of IT insfrastructure resources.
