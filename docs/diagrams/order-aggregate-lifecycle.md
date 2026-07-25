```mermaid
stateDiagram-v2
    [*] --> PENDING : CreateOrderCommand

    PENDING --> CONFIRMED : confirm()
    PENDING --> CANCELLED : cancel()

    CONFIRMED --> COMPLETED : complete()
    CONFIRMED --> CANCELLED : cancel()
```