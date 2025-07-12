---
id: filename-informs-about-last-data-point-timestamp
aliases:
  - Filename informs about last data point timestamp
tags: []
date: 2025-07-11T10:12:51+0200
---

# Filename informs about last data point timestamp
- Any dataset must contain timestamp in millis & datetime in ISO 8601 format.
- There _must_ be a verification that datetime column is in UTC+0 timezone.
- Time manipulation must be done in on place.
> As a result the filename of the dataset can be used to inform about the last data point timestamp. This information can be stored in the filename next to other metadata, such as the instrument name, the data source, and the date of the snapshot.

