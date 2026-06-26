# aztec_simple_voting
An educational project explores two different implementations of private on-chain voting, comparing their design, security  and scalability.

## Private Voting Implementations

```mermaid
flowchart TB
    A["Private Voting"]

    A --> B["Approach 1<br/>Private bool state"]
    A --> C["Approach 2<br/>One-time UintNote"]

    %% Left
    B --> B1["State is stored in a private<br/>bool variable tied to the voter"]
    B --> B2["One vote per address<br/>is enforced by assert checks"]
    B --> B3["Minimal implementation"]
    B --> B4["Best for simple voting"]

    %% Right
    C --> C1["Vote is represented by<br/>a spendable UintNote"]
    C --> C2["The note can be spent<br/>only once"]
    C --> C3["Works independently<br/>of the voter address"]
    C --> C4["Much easier to compose<br/>into larger protocols"]
    C --> C5["Fits the ZK note/nullifier model"]
```
