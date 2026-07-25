# salesapp

A pet project of an order management system. Demonstrates DDD, event-driven architecture, CQRS, and orchestration of distributed processes using SAGA on Spring.

**"Contexts instead of chaos. Events instead of couplings."**

## Documentation

- [Domain Vision Statement](docs/DVS.md) ([ru](docs/DVS-ru.md))
- [Context Map](docs/diagrams/context-map.md)
- [Order Aggregate Lifecycle](docs/diagrams/order-aggregate-lifecycle.md)
- [Successful Order Flow (Happy Path)](docs/diagrams/successful-order-flow.md)
- [Order Rejection Flow (Edge Case)](docs/diagrams/order-rejection-flow.md)
- [Customer Cancellation from Confirmed](docs/diagrams/customer-cancellation-from-confirmed.md)
- [Customer Cancellation from Pending](docs/diagrams/customer-cancellation-from-pending.md)

## Requirements

- Java 21
- Gradle 8.x (wrapper included — no manual installation required)

## How to Run Tests

```bash
./gradlew test