# PSE Ideas
## Rationale
This repository and the corresponding process intends to support collecting ideas and track their status till potential
decision for implementation.

## Process
_Inspired by the [EIP process](https://eips.ethereum.org/EIPS/eip-1) (lighter,less formal/technical process.)_. 

```mermaid
graph TB
  reframe --> rework[Rework idea]

  open([Open Issue])--> draft[Draft]
  draft --> ready[Ready for review]
  ready -. Optional .-> pitch{{Pitch}}
  ready ---> review[Review]
  review ---> decision{Decision}
  pitch -.-> decision
  rework --> ready

  decision --> reframe([Reframe idea])
  decision --> project([Start project])
  decision --> dismiss([Do not start project])


  
  draft --> withdrawn[Withdrawn]
  ready --> withdrawn
  rework --> withdrawn
  
  style pitch stroke-dasharray: 3 3
  
  click open href "https://github.com/privacy-scaling-explorations/ideas/issues/new/choose" "Create new idea proposal"
```

- draft: idea tracked as an issue in this idea repository
- ready: once the idea author marks an idea as ready, the PSE team will review
- pitch: monthly pitch dasy will take place and can be optionally the opporunity for authors to present their ideas
- decision:
  - rework: idea needs to be refined or rescoped
  - start project: the PSE group will support the implementation of the idea
  - do not start project 
