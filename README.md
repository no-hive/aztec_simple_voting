# aztec_simple_voting
An educational project explores two different implementations of private on-chain voting, comparing their design, security  and scalability.

## Private Voting Implementations

```mermaid
flowchart TB

    A["Private Voting"]

    A --> L
    A --> R

    subgraph L["APPROACH 1: PRIVATE BOOL STATE"]
        direction TB
        L1["Private bool variable"]
        L2["State tied to voter address"]
        L3["One vote enforced by assert checks"]
        L4["Minimal implementation"]
        L5["Best for simple voting"]

        L1 --> L2 --> L3 --> L4 --> L5
    end

    subgraph R["APPROACH 2: UINTNOTE"]
        direction TB
        R1["Spendable UintNote"]
        R2["Can be spent only once"]
        R3["Independent of voter address"]
        R4["Composable with larger protocols"]
        R5["Aligned with the ZK note/nullifier model"]

        R1 --> R2 --> R3 --> R4 --> R5
    end
```
