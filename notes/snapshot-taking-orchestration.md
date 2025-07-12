---
id: snapshot-taking-orchestration
aliases:
  - Snapshot Taking Orchestration
tags:
  - process
date: 2025-07-10T07:57:22+0200
---

# Snapshot Taking Orchestration
> Orchestrating parallel snapshot taking of market data only when there is new data, for 10+ data points per instrument, and for 100+ instruments.
---
1. Can't be driven by information encapsulated in the data itself, as data would need to loaded consuming memory and time.
2. Should be driven by the information about the data, such as the time of the last snapshot taken, and the latest timestamp of any data point stored.
3. This information should be stored outside the data, and updated every time a new data point is received.
  - [[filename-informs-about-last-data-point-timestamp|Filename informs about last data point timestamp]]
  - [[centralization-of-filenames-and-its-metadada|Centralization of Filenames and its metadada]]

