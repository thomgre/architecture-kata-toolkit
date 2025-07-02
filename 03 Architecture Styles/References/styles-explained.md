# Architecture Styles List

## Layered

A traditional architecture pattern that organizes code into horizontal layers, where each layer has a specific responsibility and can only communicate with adjacent layers. Common layers include presentation, business logic, persistence, and database layers. This creates clear separation of concerns but can lead to performance issues due to the sequential nature of layer traversal.

## Modular Monolith

A single deployable application that is internally organized into well-defined, loosely coupled modules with clear boundaries and interfaces. Unlike a traditional monolith, it maintains good modularity and separation of concerns while avoiding the complexity of distributed systems. Each module encapsulates related functionality and can be developed by separate teams.

## Microkernel

Also known as plug-in architecture, this pattern consists of a minimal core system that provides basic functionality, with additional features implemented as plug-in components. The core system defines interfaces and manages plug-ins, while plug-ins extend the system's capabilities. Common in applications like IDEs, web browsers, and product-based software.

## Microservices

An architectural approach that structures an application as a collection of small, autonomous services that communicate over well-defined APIs. Each service is independently deployable, owns its data, and focuses on a specific business capability. This enables teams to work independently but introduces complexity in service coordination and data consistency.

## Service-based

A hybrid approach between monolithic and microservices architectures, where the application is divided into a small number of coarse-grained services (typically 4-12). Services are larger than microservices and may share databases, reducing operational complexity while still providing better modularity than a monolith.

## Service-oriented

An architectural style that structures applications as a collection of loosely coupled services that communicate through well-defined interfaces. Often implemented using enterprise service buses (ESB) and web services standards. Emphasizes service reusability, contract-based interfaces, and enterprise-wide service governance.

## Event-driven

An architecture where components communicate asynchronously through events. Event producers publish events when state changes occur, and event consumers react to relevant events. This creates loose coupling between components and enables real-time processing, but can make system behavior harder to predict and debug.

## Space-based

A distributed architecture designed to handle extreme scalability by eliminating the database as a bottleneck. It uses in-memory data grids and replicates data across multiple processing units. The architecture dynamically scales processing units based on load and is particularly suited for applications with variable and unpredictable user loads.