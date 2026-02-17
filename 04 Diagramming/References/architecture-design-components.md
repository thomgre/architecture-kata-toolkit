# Architecture Design Components

## Examples of components in the physical architecture

**Clients & End-User Devices**
The physical endpoints where users interact with the system — desktop browsers, mobile apps, tablets, IoT devices, embedded sensors, kiosks, and CLI tools. Each implies different connectivity assumptions, screen real estate, and capability constraints.

**CDN / Edge Network**
Content delivery networks and edge PoPs (Points of Presence) that sit geographically close to users. Handles static asset delivery, TLS termination, DDoS protection, and increasingly compute (edge functions). Examples: Cloudflare, AWS CloudFront, Fastly.

**Load Balancers & API Gateways**
Traffic distribution and API management layer. Load balancers route requests across service instances. API gateways add authentication, rate limiting, request routing, protocol translation, and observability at the ingress point. Examples: NGINX, AWS ALB, Kong, Apigee.

**Web & Application Servers**
The compute tier that runs application logic — web servers serving rendered pages, application servers running business logic, and background workers processing async jobs. Can be VMs, containers, or serverless functions.

**Microservices / Service Mesh**
Individual bounded services each owning a specific domain capability, communicating over the network. A service mesh (Istio, Linkerd) adds a sidecar proxy layer for mTLS, retries, circuit breaking, and observability between services without changing application code.

**Message Brokers & Event Streams**
Asynchronous communication infrastructure. Message queues (RabbitMQ, SQS) decouple producers from consumers for task-based work. Event streaming platforms (Kafka, Kinesis) provide durable, ordered, replayable event logs for high-throughput data pipelines. The distinction matters architecturally — queues imply consumption, streams imply publication.

**Databases & Storage**
The persistence layer, which typically includes several distinct components in a real system. Relational databases (PostgreSQL, MySQL) for structured transactional data. Document stores (MongoDB) for flexible schemas. Key-value stores (Redis, DynamoDB) for low-latency lookups and caching. Time-series databases (InfluxDB, TimescaleDB) for sensor and metrics data. Object storage (S3, GCS) for blobs, files, and large binary assets. Search engines (Elasticsearch) for full-text and faceted queries.

**Cache Layer**
In-memory stores sitting in front of databases or between services to absorb read traffic and reduce latency. Can be application-level (in-process), distributed (Redis, Memcached), or query-result caches built into databases. Important to distinguish from the database itself on a diagram.

**Data Platform**
The analytical infrastructure separate from the operational (OLTP) databases. Includes data warehouses (Snowflake, BigQuery, Redshift) for structured analytics, data lakes (S3 + Iceberg, Azure Data Lake) for raw and semi-structured storage, ETL/ELT pipelines (dbt, Spark, Airflow) for transformation, and BI/reporting tools as consumers.

**Identity & Auth Services**
Authentication and authorization infrastructure. Identity providers (Okta, Azure AD, Auth0) handle SSO, MFA, and token issuance. OAuth 2.0 / OIDC authorization servers manage token lifecycles. Internal services may use a separate secrets manager (Vault, AWS Secrets Manager) for credential storage.

**Third-Party & External Services**
APIs and platforms outside your system boundary that you depend on — payment processors, mapping services, email/SMS providers, weather APIs, ERP systems, partner data feeds. These appear on a physical diagram to show external dependencies and egress points.

**Edge / On-Premises Compute**
Hardware deployed outside the cloud, at a physical location — on-prem servers, edge nodes in factories or construction sites, retail store servers, or ruggedized field devices. Important for systems with offline-first or low-latency local processing requirements. Includes the local network infrastructure (switches, routers, local LAN/WiFi mesh).

**Networking & Connectivity**
The physical and virtual network infrastructure connecting all other components — VPCs, subnets (public/private), VPNs, Direct Connect / ExpressRoute links, peering connections, firewalls, and security groups. Often invisible on high-level diagrams but critical to show when security boundaries, data residency, or hybrid cloud topology is architecturally significant.

**Observability Infrastructure**
The supporting layer that makes the system operable — log aggregation (ELK stack, Loki), metrics collection (Prometheus, Datadog), distributed tracing (Jaeger, Tempo), alerting (PagerDuty), and dashboards (Grafana). Not part of the business logic but physically present in the deployment and often a first-class architectural concern.

**CI/CD & Deployment Infrastructure**
The pipeline infrastructure that builds, tests, and ships the system — source control (GitHub, GitLab), build servers (GitHub Actions, Jenkins), container registries (ECR, Docker Hub), and deployment orchestrators (Kubernetes, ECS, Nomad). Relevant on physical diagrams when deployment architecture itself is a constraint or a deliverable.