---
id: archiver-archives-manager
aliases:
  - "Archiver: archives manager"
tags: []
date: 2025-07-25T06:30:33+0200
---

## Maxims
1. This service must be [[stateless-class|Stateless Class]], because as its names suggests is a worker which has the sole responsibility of managing the archives. A worker is not changed by the work it does. It has capabilities to inflict change on "things" but this work doesn't change itself.
2. The [[backend|Backend]] can receive multiple request from different client services at the same time. Each request will have different parameters, so they must be managed independently. But, if the `Archiver` registers parameters or results, of any given process as an state of itself, all process will share that state. Conclusion no process will be independent.
3. If some parameters or results are registered as state of the `Archiver` then to avoid any issue by the concurrent processes, it would have to be an [[stateful-class|Stateful Class]]. But this will force to spawn a new worker for each request received by the [[backend|Backend]], which is dumb.
4. It only has one entity attribute which is the binded volume path, is the location of the `gc_archives` inside the container. As an analogy, would be the address of the building where the worker works.
---
## Responsibilities decomposition
1. Is the only one that knows how files are distributed among directories of the `gc_archives`. Thus provides this directory to the specific `file manager`
