
---

## 6. SYSTEM ARCHITECTURE

```mermaid
flowchart TD
    A[Real-World Data] --> B[State Reconstruction]
    B --> C[Causal Inference]
    C --> D[Temporal World Model]
    D --> E[Simulation Engine]
    E --> F[Decision Engine]
    F --> G[Action]
    G --> H[Feedback]
    H --> B
flowchart LR
    A[Data] --> B[State]
    B --> C[Causality]
    C --> D[Simulation]
    D --> E[Decision]
    E --> F[Action]
    F --> G[Feedback]
    G --> A
flowchart LR
    A[Data] --> B[State]
    B --> C[Causality]
    C --> D[Simulation]
    D --> E[Decision]
    E --> F[Action]
    F --> G[Feedback]
    G --> A
event = {
    "timestamp": "...",
    "source": "...",
    "state": "...",
    "uncertainty": "..."
}
S(t+1) = f(S(t), A(t), ε)
π* = argmax E[Utility − Risk]
prediction → reality → update
P(S_t | D_0:t)

G* = argmax P(G | D)

S(t+1) = f(S(t), A(t), ε)

Q(s,a) = E[R_t + γ max Q(s',a')]
