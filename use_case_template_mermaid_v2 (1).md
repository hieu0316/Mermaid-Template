# Use cases

## Use case: XYZ


| **Actors**                       |        |
| -------------------------------- | ------ |
| Primary actors                   | User   |
| Secondary actors                 |        |
| **Preconditions**                | System is activated |
| **Postconditions**               |        |


```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

```mermaid
flowchart TD
    Start --> Stop
```
