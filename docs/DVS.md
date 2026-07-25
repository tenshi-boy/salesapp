# Salesapp — Order Management System

## 1. Purpose & Core Value
Salesapp is a system that provides customers with an end-to-end order process through a single entry point. It handles all orchestration — checking product availability, reserving, capturing payment, and initiating delivery — freeing the customer from interacting with each service individually.

The system is built as a pet project to demonstrate competencies in DDD, EDA, and CQRS.

## 2. Problem Domain Focus
The central domain is `Sales` — a bounded context responsible for the customer order lifecycle and its execution orchestration. Adjacent business processes — inventory management, financial provisioning, and delivery — are externalized into separate contexts and represented by stubs.

## 3. Architectural Approach and Patterns
The project is built on the following principles:

1. **Domain Isolation (DDD):** The `Sales` domain is implemented as an independent bounded context with its own domain model, decoupled from external systems.
2. **Event-Driven Architecture (EDA):** A natural consequence of DDD — isolated contexts need an asynchronous, loosely coupled channel. The **Outbox pattern** guarantees atomicity of business changes and events.
3. **SAGA:** orchestrates distributed business operations and ensures consistency across contexts. An **ACL** at context boundaries protects the domain model from external semantics.
4. **Scalability:** isolated contexts, asynchronous coordination, and eventual consistency form the foundation for horizontal scaling and readiness for a microservices architecture.
5. **CQRS:** separating the write and read models adds another dimension for independent development and scaling.
6. **Minimalism and Clarity:** the goal of the project is to demonstrate architectural decisions, not to maximize business functionality. Each pattern is present only to the extent necessary to convey the design intent.

## 4. Business Value
Context isolation provides the freedom to develop each bounded context in parallel and at its own pace. This architecture enables the business to respond faster to market changes and introduce new scenarios without the risk of breaking existing logic.

## 5. Success Criteria
The project will be considered successful if its implementation demonstrates:

1. Skilled at decomposing complex domains into isolated bounded contexts with well-defined boundaries and clear communication rules.
2. Practical skills in applying DDD, EDA, SAGA, and CQRS.
3. Effective use of the Spring ecosystem to implement the stated architecture.

## 6. Project Slogan
**"Contexts instead of chaos. Events instead of couplings."**