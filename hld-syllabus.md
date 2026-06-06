# 1. SYSTEM DESIGN FUNDAMENTALS

## 1.1 What is High-Level Design (HLD)
1.1.1 Definition of High-Level Design in software architecture  
1.1.2 Role of HLD in the software development lifecycle (SDLC)  
1.1.3 Components of HLD (Architecture diagrams, modules, interfaces)  
1.1.4 Audience for HLD (Stakeholders, architects, developers)  
1.1.5 How HLD guides implementation teams  
1.1.6 Real-world examples of HLD for web applications  
1.1.7 Common misconceptions about HLD  

## 1.2 HLD vs LLD (Low-Level Design)
1.2.1 What is Low-Level Design (LLD)  
1.2.2 Level of abstraction differences between HLD and LLD  
1.2.3 HLD focus (Components, data flow) vs LLD focus (Classes, functions, algorithms)  
1.2.4 Input-output relationship (HLD feeds into LLD)  
1.2.5 Documentation differences (Block diagrams vs sequence/class diagrams)  
1.2.6 Who creates HLD vs LLD (Architects vs Senior Engineers)  
1.2.7 Transitioning from HLD to LLD in agile projects  

## 1.3 Functional vs Non-Functional Requirements
1.3.1 What are Functional Requirements (FRs)  
1.3.2 What are Non-Functional Requirements (NFRs)  
1.3.3 Examples of FRs (User login, file upload, search)  
1.3.4 Examples of NFRs (Scalability, latency, durability, security)  
1.3.5 How NFRs drive architecture decisions  
1.3.6 Trade-offs between conflicting NFRs (Consistency vs Availability)  
1.3.7 Documenting and validating requirements with stakeholders  

## 1.4 Capacity Estimation (QPS, Storage, Bandwidth)
1.4.1 Why capacity estimation is critical in system design  
1.4.2 Estimating Queries Per Second (QPS) for read/write operations  
1.4.3 Traffic patterns (Peak vs average traffic)  
1.4.4 Storage estimation for structured and unstructured data  
1.4.5 Bandwidth calculation for network planning  
1.4.6 Memory estimation for caching tiers  
1.4.7 Real-world estimation walkthrough (e.g., Twitter, YouTube)  
1.4.8 Tools and formulas for capacity planning  

## 1.5 Constraints and Assumptions
1.5.1 What are design constraints (Budget, time, technology stack)  
1.5.2 What are design assumptions (User growth rate, read/write ratio)  
1.5.3 How to identify constraints early in the design phase  
1.5.4 Documenting assumptions to align stakeholders  
1.5.5 Risk management based on invalidated assumptions  
1.5.6 Examples of constraints (GDPR compliance, cloud provider limits)  
1.5.7 Iterative refinement of assumptions  

## 1.6 Design Trade-offs Analysis
1.6.1 What is a design trade-off  
1.6.2 Consistency vs Availability (CAP Theorem implications)  
1.6.3 Read throughput vs Write throughput trade-offs  
1.6.4 Latency vs Cost trade-offs  
1.6.5 SQL vs NoSQL decision framework  
1.6.6 Strong consistency vs Eventual consistency  
1.6.7 Trade-off analysis matrices and documentation  
1.6.8 Communicating trade-offs to non-technical stakeholders  

## 1.7 Stakeholder Communication
1.7.1 Who are stakeholders in system design (Product, Eng, Ops, Security)  
1.7.2 Translating technical designs into business value  
1.7.3 Visual aids for communication (C4 models, UML, sequence diagrams)  
1.7.4 Running design review meetings  
1.7.5 Handling conflicting stakeholder priorities  
1.7.6 Documenting decisions (Architecture Decision Records - ADRs)  
1.7.7 Feedback loops and design iteration  

## 1.8 Design Review Process
1.8.1 What is a design review  
1.8.2 Pre-review preparation (Checklists, prerequisites)  
1.8.3 Roles in a design review (Reviewer, presenter, scribe)  
1.8.4 Review criteria (Scalability, security, operability)  
1.8.5 Common design review anti-patterns  
1.8.6 Incorporating feedback and versioning designs  
1.8.7 Post-review sign-off and next steps  
1.8.8 Tools for collaborative design reviews (Confluence, Miro, Google Docs)  









# 2. REQUIREMENTS GATHERING

## 2.1 Functional Requirements Elicitation
2.1.1 What is functional requirements elicitation  
2.1.2 Stakeholder identification for requirements gathering  
2.1.3 User stories and use case development  
2.1.4 Prioritization frameworks (MoSCoW, Kano model)  
2.1.5 Requirements validation techniques (prototyping, reviews)  
2.1.6 Documenting functional requirements (PRD, FRD)  
2.1.7 Common pitfalls in requirements elicitation  
2.1.8 Real-world examples of functional requirements (e.g., upload video, post comment)  

## 2.2 Non-Functional Requirements (Latency, Availability, Durability)
2.2.1 What are non-functional requirements (NFRs) in system design  
2.2.2 Latency requirements (p99, p95, p50) and SLAs  
2.2.3 Availability requirements (99.9%, 99.99%, 99.999%)  
2.2.4 Durability and data persistence guarantees (e.g., 11 9's)  
2.2.5 Throughput requirements (requests per second, data processed)  
2.2.6 Consistency requirements (strong vs eventual)  
2.2.7 Recoverability and RTO/RPO objectives  
2.2.8 Documentation and validation of NFRs  

## 2.3 Scale and Growth Projections
2.3.1 Why scale projections are critical for architecture  
2.3.2 User growth estimation (DAU, MAU) over 1, 3, 5 years  
2.3.3 Data growth projections (storage, archival needs)  
2.3.4 Traffic growth projections (peak vs average)  
2.3.5 Feature-driven scale considerations  
2.3.6 Seasonal and event-driven traffic spikes  
2.3.7 Building slack and buffer into projections  
2.3.8 Revisiting projections during system evolution  

## 2.4 Security and Compliance Needs
2.4.1 What are security requirements in system design  
2.4.2 Authentication requirements (SSO, MFA, OIDC)  
2.4.3 Authorization and access control requirements (RBAC, ABAC)  
2.4.4 Data privacy requirements (PII, GDPR, CCPA, HIPAA)  
2.4.5 Encryption requirements (at rest, in transit)  
2.4.6 Audit logging and compliance trail needs  
2.4.7 Network security requirements (WAF, DDoS protection)  
2.4.8 Third-party security assessments and penetration testing  

## 2.5 Operational Requirements (Monitoring, Debugging)
2.5.1 What are operational requirements  
2.5.2 Monitoring and alerting requirements (metrics, logs, traces)  
2.5.3 Debugging and observability needs (distributed tracing)  
2.5.4 Deployment requirements (CI/CD, rollback capabilities)  
2.5.5 Backup and disaster recovery requirements  
2.5.6 Incident response and on-call requirements  
2.5.7 Capacity management and auto-scaling needs  
2.5.8 Documentation and runbook requirements  

## 2.6 Cost Constraints and Budget
2.6.1 Why cost constraints shape architecture decisions  
2.6.2 Infrastructure budget allocation (compute, storage, network)  
2.6.3 Cloud provider pricing models (on-demand, reserved, spot)  
2.6.4 Operational cost projections (staffing, licenses, support)  
2.6.5 Cost optimization trade-offs vs performance/reliability  
2.6.6 Total Cost of Ownership (TCO) vs cloud vs on-premise  
2.6.7 Budget approval and governance processes  
2.6.8 Cost monitoring and chargeback/showback models  

## 2.7 Time-to-Market Considerations
2.7.1 What are time-to-market (TTM) requirements  
2.7.2 MVP vs full-featured system trade-offs  
2.7.3 Parallel development vs sequential design phases  
2.7.4 Leveraging managed services vs building in-house  
2.7.5 Technical debt acceptance for faster delivery  
2.7.6 Feature release cadence and milestones  
2.7.7 Competitive pressure and market window considerations  
2.7.8 Balancing speed with quality and security  

## 2.8 Technology Stack Constraints
2.8.1 What are technology stack constraints  
2.8.2 Organizational skill set and expertise limitations  
2.8.3 Existing legacy system integration requirements  
2.8.4 Programming language and framework preferences  
2.8.5 Database and storage technology restrictions  
2.8.6 Cloud provider or data center lock-in considerations  
2.8.7 Open source vs commercial software policies  
2.8.8 Version compatibility and upgrade constraints  














# 3. CAPACITY PLANNING

## 3.1 Traffic Estimation (Daily Active Users, Peak QPS)
3.1.1 What is traffic estimation in capacity planning  
3.1.2 Daily Active Users (DAU) and Monthly Active Users (MAU) calculation  
3.1.3 Peak QPS (Queries Per Second) estimation methodology  
3.1.4 Read vs write ratio determination  
3.1.5 Traffic patterns (diurnal, weekly, seasonal variations)  
3.1.6 User behavior assumptions and their impact  
3.1.7 Conversion rates and feature adoption projections  
3.1.8 Real-world traffic estimation examples (e-commerce, social media)  

## 3.2 Storage Estimation (Data Growth Rate, Retention Period)
3.2.1 Why storage estimation is critical for system design  
3.2.2 Structured data storage calculation (rows, columns, size per record)  
3.2.3 Unstructured data storage calculation (images, videos, documents)  
3.2.4 Data growth rate projections (daily, monthly, yearly)  
3.2.5 Retention period requirements (hot, warm, cold storage tiers)  
3.2.6 Index and metadata storage overhead  
3.2.7 Backup and archival storage needs  
3.2.8 Storage estimation walkthrough (e.g., messaging app, video platform)  

## 3.3 Bandwidth Estimation (Ingress, Egress, Peak vs Average)
3.3.1 What is bandwidth estimation in capacity planning  
3.3.2 Ingress bandwidth calculation (incoming data to system)  
3.3.3 Egress bandwidth calculation (outgoing data to users)  
3.3.4 Peak bandwidth vs average bandwidth requirements  
3.3.5 Request size and response size assumptions  
3.3.6 Media and file transfer bandwidth considerations  
3.3.7 CDN bandwidth offloading strategy  
3.3.8 Regional and cross-region bandwidth costs  

## 3.4 Memory Estimation (Caching Layer Requirements)
3.4.1 Why memory estimation is important for performance  
3.4.2 Cache hit ratio targets and their impact  
3.4.3 Hot data set size estimation (e.g., frequent access patterns)  
3.4.4 Cache eviction policies and memory overhead  
3.4.5 In-memory database sizing (Redis, Memcached)  
3.4.6 Application tier memory requirements  
3.4.7 Session storage and stateful memory needs  
3.4.8 Memory estimation walkthrough for typical workloads  

## 3.5 Compute Estimation (CPU Cores, Instance Sizing)
3.5.1 What is compute estimation in capacity planning  
3.5.2 CPU core requirements per request/operation  
3.5.3 CPU-bound vs I/O-bound workload differentiation  
3.5.4 Instance sizing strategies (many small vs few large)  
3.5.5 Compute overhead for framework and runtime  
3.5.6 Autoscaling headroom and buffer capacity  
3.5.7 Compute estimation for batch vs real-time workloads  
3.5.8 Real-world compute estimation examples  

## 3.6 Database Sizing (Rows, Indexes, Connections)
3.6.1 Why database sizing requires special attention  
3.6.2 Row count estimation per table over time  
3.6.3 Row size calculation (columns, data types, overhead)  
3.6.4 Index storage overhead and maintenance impact  
3.6.5 Database connection pool sizing (max connections, idle connections)  
3.6.6 Write throughput vs read throughput capacity  
3.6.7 Replica lag and replication capacity needs  
3.6.8 Database sizing walkthrough (e.g., user table, orders table)  

## 3.7 Network Capacity (Load Balancers, CDN, Regional Traffic)
3.7.1 What is network capacity planning  
3.7.2 Load balancer throughput and connection limits  
3.7.3 CDN capacity and edge cache sizing  
3.7.4 Regional and multi-region traffic distribution  
3.7.5 Network latency and jitter requirements  
3.7.6 Firewall and DDoS mitigation capacity  
3.7.7 Service mesh and proxy overhead  
3.7.8 Network capacity monitoring and alerting thresholds  

## 3.8 3-5 Year Growth Projections
3.8.1 Why long-term projections matter in system design  
3.8.2 Extrapolating growth from current or estimated metrics  
3.8.3 Business roadmap impact on infrastructure needs  
3.8.4 Technology obsolescence and refresh cycles  
3.8.5 Vendor lock-in and cloud exit considerations  
3.8.6 Build vs buy decisions based on projected scale  
3.8.7 Greenfield vs brownfield planning differences  
3.8.8 Presenting projections to leadership for funding  

## 3.9 Scaling Thresholds and Triggers
3.9.1 What are scaling thresholds and triggers  
3.9.2 CPU utilization thresholds (e.g., 70% scale up, 30% scale down)  
3.9.3 Memory utilization thresholds  
3.9.4 Queue depth and request backlog triggers  
3.9.5 Connection pool exhaustion thresholds  
3.9.6 Database connection and replica lag triggers  
3.9.7 Custom metric-based triggers (business KPIs)  
3.9.8 Cooldown periods and hysteresis to prevent flapping  















# 4. DATABASE DESIGN

## 4.1 SQL vs NoSQL Selection Criteria
4.1.1 What is the SQL vs NoSQL decision in system design  
4.1.2 Data structure requirements (structured vs semi-structured vs unstructured)  
4.1.3 Schema flexibility needs (fixed vs evolving schema)  
4.1.4 ACID compliance and transaction requirements  
4.1.5 Scalability model (vertical vs horizontal)  
4.1.6 Query complexity and join requirements  
4.1.7 Consistency vs availability trade-offs (CAP theorem)  
4.1.8 Real-world decision framework for SQL vs NoSQL  

## 4.2 Relational Databases (PostgreSQL, MySQL)
4.2.1 What are relational databases (RDBMS) in system design  
4.2.2 PostgreSQL architecture and use cases  
4.2.3 MySQL architecture and use cases  
4.2.4 ACID compliance and transaction support  
4.2.5 SQL query language and join capabilities  
4.2.6 Indexing in relational databases (B-Tree, Hash, GIN)  
4.2.7 Foreign keys and referential integrity  
4.2.8 When to choose relational databases over NoSQL  

## 4.3 Document Databases (MongoDB, DynamoDB, Firestore)
4.3.1 What are document databases  
4.3.2 MongoDB architecture (document model, sharding, replication)  
4.3.3 DynamoDB architecture (partition key, sort key, DAX)  
4.3.4 Firestore architecture (real-time, serverless)  
4.3.5 Schema-less design and flexible document structures  
4.3.6 Embedded documents vs referencing patterns  
4.3.7 Query capabilities and limitations of document stores  
4.3.8 Use cases (content management, catalogs, user profiles)  

## 4.4 Key-Value Stores (Redis, Memcached, DynamoDB)
4.4.1 What are key-value stores  
4.4.2 Redis architecture (in-memory, persistence, data structures)  
4.4.3 Memcached architecture (simple cache, distributed hashing)  
4.4.4 DynamoDB as a key-value store (low-latency access)  
4.4.5 Simple get/put operations and O(1) access patterns  
4.4.6 TTL and expiration policies  
4.4.7 Use cases (session storage, caching, leaderboards)  
4.4.8 Limitations (no secondary indexes, limited querying)  

## 4.5 Wide-Column Stores (Cassandra, HBase, Bigtable)
4.5.1 What are wide-column stores  
4.5.2 Cassandra architecture (ring topology, gossip protocol, tunable consistency)  
4.5.3 HBase architecture (HDFS-based, column families)  
4.5.4 Bigtable architecture (Google's petabyte-scale store)  
4.5.5 Partition key and clustering column design  
4.5.6 High write throughput and linear scalability  
4.5.7 Eventual consistency and write patterns  
4.5.8 Use cases (time-series, IoT, messaging, real-time analytics)  

## 4.6 Graph Databases (Neo4j, Amazon Neptune)
4.6.1 What are graph databases  
4.6.2 Neo4j architecture (Cypher query language, property graph model)  
4.6.3 Amazon Neptune architecture (W3C standards, RDF, Gremlin)  
4.6.4 Nodes, edges, and properties concepts  
4.6.5 Traversal-based querying for relationship-heavy data  
4.6.6 ACID compliance in graph databases  
4.6.7 Use cases (social networks, fraud detection, recommendation engines)  
4.6.8 When graph databases are the right choice  

## 4.7 Time-Series Databases (InfluxDB, Prometheus)
4.7.1 What are time-series databases (TSDB)  
4.7.2 InfluxDB architecture (continuous queries, retention policies)  
4.7.3 Prometheus architecture (pull model, TSDB, recording rules)  
4.7.4 Timestamp-based indexing and downsampling  
4.7.5 High write throughput for metrics data  
4.7.6 Retention and compaction strategies  
4.7.7 Query patterns (aggregations over time windows)  
4.7.8 Use cases (monitoring metrics, IoT sensor data, financial tick data)  

## 4.8 Search Engines (Elasticsearch, OpenSearch)
4.8.1 What are search engines in database design  
4.8.2 Elasticsearch architecture (inverted index, sharding, replication)  
4.8.3 OpenSearch architecture (fork of Elasticsearch)  
4.8.4 Full-text search and relevance scoring (BM25, TF-IDF)  
4.8.5 Indexing and near real-time search capabilities  
4.8.6 Aggregations and analytics features  
4.8.7 Logging and observability use cases (ELK stack)  
4.8.8 Limitations (consistency, write latency, operational complexity)  

## 4.9 Sharding Strategies (Hash, Range, Directory-Based)
4.9.1 What is database sharding  
4.9.2 Hash-based sharding (consistent hashing, virtual nodes)  
4.9.3 Range-based sharding (dynamic splitting, hot partition risk)  
4.9.4 Directory-based sharding (lookup service, flexible rebalancing)  
4.9.5 Shard key selection criteria and trade-offs  
4.9.6 Cross-shard query challenges (scatter-gather)  
4.9.7 Rebalancing and resharding strategies  
4.9.8 Real-world sharding examples (user_id, geo-region, tenant_id)  

## 4.10 Partitioning vs Replication
4.10.1 What is data partitioning (sharding)  
4.10.2 What is data replication  
4.10.3 Partitioning for scalability (horizontal scaling)  
4.10.4 Replication for availability and read throughput  
4.10.5 Partitioning and replication together (combined architecture)  
4.10.6 Single leader vs multi-leader vs leaderless replication  
4.10.7 Synchronous vs asynchronous replication  
4.10.8 Failure handling in partitioned and replicated systems  

## 4.11 Indexing Strategies (Primary, Secondary, Composite, Covering)
4.11.1 What are database indexes  
4.11.2 Primary index (clustered index) design  
4.11.3 Secondary index (non-clustered) design  
4.11.4 Composite index (multiple columns) ordering strategy  
4.11.5 Covering index to eliminate table access  
4.11.6 Unique index vs non-unique index  
4.11.7 Index maintenance overhead (write amplification)  
4.11.8 Real-world indexing patterns for common queries  

## 4.12 Denormalization Use Cases
4.12.1 What is denormalization in database design  
4.12.2 Denormalization vs normalization trade-offs  
4.12.3 Reducing join requirements for read-heavy workloads  
4.12.4 Pre-joining related data into single documents  
4.12.5 Duplicating data across tables (controlled redundancy)  
4.12.6 Denormalization in NoSQL databases as standard practice  
4.12.7 Consistency challenges with denormalized data  
4.12.8 Real-world denormalization examples (dashboard aggregates, user profiles)  

## 4.13 Materialized Views
4.13.1 What are materialized views  
4.13.2 Materialized views vs standard views (stored vs virtual)  
4.13.3 Precomputed aggregates for query performance  
4.13.4 Refresh strategies (synchronous, asynchronous, periodic)  
4.13.5 Use cases (reporting, analytics dashboards, rollups)  
4.13.6 Materialized views in different databases (PostgreSQL, Oracle, Cassandra)  
4.13.7 Storage overhead and maintenance costs  
4.13.8 Alternatives to materialized views (ETL pipelines, caching)  

## 4.14 Database Migration Strategies (Zero-Downtime)
4.14.1 What are database migrations  
4.14.2 Schema migration challenges in production  
4.14.3 Dual-write pattern for migration  
4.14.4 Blue-green database migration  
4.14.5 Online schema change tools (gh-ost, pt-online-schema-change)  
4.14.6 Backward-compatible schema changes  
4.14.7 Data backfill and consistency validation  
4.14.8 Rollback strategies for failed migrations  

## 4.15 Multi-Region Database Replication
4.15.1 What is multi-region database replication  
4.15.2 Cross-region replication for disaster recovery  
4.15.3 Active-passive multi-region setup  
4.15.4 Active-active multi-region challenges (conflict resolution)  
4.15.5 Replication lag across geographic distances  
4.15.6 Multi-region database offerings (Aurora Global, Cosmos DB, Spanner)  
4.15.7 Write conflict resolution strategies (last-write-wins, CRDTs)  
4.15.8 Use cases (global user base, compliance, low-latency reads)  

## 4.16 Database Connection Pooling
4.16.1 What is database connection pooling  
4.16.2 Connection establishment overhead and pooling benefits  
4.16.3 Connection pool sizing (max connections, min idle)  
4.16.4 Connection pool libraries (HikariCP, PgBouncer, ProxySQL)  
4.16.5 Connection leak detection and prevention  
4.16.6 Timeout configuration (connection, idle, wait)  
4.16.7 Connection pooling in serverless environments  
4.16.8 Common connection pool misconfigurations  

## 4.17 Read Replicas for Read-Heavy Workloads
4.17.1 What are read replicas  
4.17.2 Primary-replica replication architecture  
4.17.3 Read scaling using read replicas (horizontal read scaling)  
4.17.4 Replica lag and stale read trade-offs  
4.17.5 Load balancing read queries across replicas  
4.17.6 Promoting a replica to primary for failover  
4.17.7 Read replica placement (same AZ, cross AZ, cross region)  
4.17.8 Use cases (analytics queries, reporting, dashboard reads)  















# 5. API DESIGN

## 5.1 REST API Principles (Resources, Methods, Status Codes)
5.1.1 What is REST API design  
5.1.2 Resources and resource naming conventions (nouns vs verbs)  
5.1.3 HTTP methods mapping (GET, POST, PUT, PATCH, DELETE)  
5.1.4 GET (idempotent, safe, cacheable) usage patterns  
5.1.5 POST (non-idempotent, resource creation) usage patterns  
5.1.6 PUT (idempotent, full replacement) vs PATCH (partial update)  
5.1.7 DELETE (idempotent) usage patterns  
5.1.8 HTTP status codes (2xx success, 3xx redirect, 4xx client error, 5xx server error)  
5.1.9 RESTful API design best practices  

## 5.2 GraphQL (Queries, Mutations, Subscriptions)
5.2.1 What is GraphQL in API design  
5.2.2 GraphQL vs REST comparison (over-fetching, under-fetching)  
5.2.3 Queries (request specific fields, nested data)  
5.2.4 Mutations (create, update, delete operations)  
5.2.5 Subscriptions (real-time events, WebSocket-based)  
5.2.6 Schema definition language (SDL) and types  
5.2.7 Resolvers (field-level data fetching logic)  
5.2.8 N+1 query problem and batching solutions (DataLoader)  
5.2.9 GraphQL API gateway and federation  
5.2.10 Use cases (mobile APIs, complex data fetching, product catalogs)  

## 5.3 gRPC (Protocol Buffers, Streaming, Performance)
5.3.1 What is gRPC in API design  
5.3.2 Protocol Buffers (protobuf) message definition  
5.3.3 Strong typing and code generation benefits  
5.3.4 Unary RPC (request-response pattern)  
5.3.5 Server streaming (single request, stream of responses)  
5.3.6 Client streaming (stream of requests, single response)  
5.3.7 Bidirectional streaming (real-time two-way communication)  
5.3.8 HTTP/2 transport and performance advantages  
5.3.9 gRPC vs REST vs GraphQL comparison  
5.3.10 Use cases (microservices, low-latency systems, polyglot environments)  

## 5.4 WebSocket (Bi-Directional Real-Time Communication)
5.4.1 What is WebSocket in API design  
5.4.2 WebSocket vs HTTP (persistent connection vs request-response)  
5.4.3 WebSocket handshake (HTTP upgrade mechanism)  
5.4.4 Full-duplex bi-directional messaging  
5.4.5 Message framing (text vs binary frames)  
5.4.6 Keep-alive and ping-pong mechanisms  
5.4.7 Connection lifecycle management (open, message, close, error)  
5.4.8 Scaling WebSocket connections (sticky sessions, pub/sub backends)  
5.4.9 Use cases (chat, live updates, gaming, collaborative editing, financial tickers)  

## 5.5 API Versioning Strategies (URI, Header, Content Negotiation)
5.5.1 What is API versioning  
5.5.2 URI path versioning (/v1/resource, /v2/resource)  
5.5.3 Custom header versioning (Accept-Version, X-API-Version)  
5.5.4 Content negotiation versioning (Accept header with custom MIME type)  
5.5.5 Query parameter versioning (?version=1)  
5.5.6 Breaking vs non-breaking changes classification  
5.5.7 Deprecation lifecycle and sunset policies  
5.5.8 Supporting multiple versions simultaneously  
5.5.9 Version removal and migration strategies  
5.5.10 Real-world versioning examples (Stripe, GitHub, Twilio)  

## 5.6 API Pagination (Offset, Cursor, Keyset)
5.6.1 What is API pagination  
5.6.2 Offset-based pagination (limit, offset, page) mechanics  
5.6.3 Offset pagination problems (performance, inconsistent results)  
5.6.4 Cursor-based pagination (after, before, next_page_token) mechanics  
5.6.5 Keyset pagination (seek method using indexed columns)  
5.6.6 Time-based pagination (filters on created_at)  
5.6.7 Pagination metadata (total_count, next_url, previous_url)  
5.6.8 UI pagination patterns (infinite scroll, load more, page selector)  
5.6.9 Real-world pagination examples (Twitter, Facebook, GitHub GraphQL)  

## 5.7 API Filtering, Sorting, and Field Selection
5.7.1 What are API filtering, sorting, and field selection  
5.7.2 Filtering syntax (field=value, field=value1,value2, field_range)  
5.7.3 Complex filtering (AND, OR, nested conditions, operators like gt, lt, in)  
5.7.4 Sorting syntax (sort=field,-field for ascending/descending)  
5.7.5 Multi-field sorting (sort=field1,-field2,field3)  
5.7.6 Field selection (fields=id,name,email) to reduce payload size  
5.7.7 GraphQL as the ultimate filtering/selection solution  
5.7.8 Security considerations (preventing large response DDoS)  
5.7.9 Performance implications (database query optimization)  

## 5.8 Rate Limiting (Fixed Window, Sliding Window, Token Bucket)
5.8.1 What is rate limiting in API design  
5.8.2 Fixed window counter algorithm (reset at fixed intervals)  
5.8.3 Sliding window log algorithm (timestamp tracking)  
5.8.4 Sliding window counter algorithm (hybrid approach)  
5.8.5 Token bucket algorithm (steady rate with bursts)  
5.8.6 Leaky bucket algorithm (smoothing traffic spikes)  
5.8.7 Rate limiting by user, IP, API key, or custom dimension  
5.8.8 Rate limit headers (X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Reset)  
5.8.9 Rate limit exceeded response (HTTP 429)  
5.8.10 Distributed rate limiting (Redis, centralized counters)  

## 5.9 Idempotency Keys for Safe Retries
5.9.1 What is idempotency in API design  
5.9.2 Idempotent operations (GET, PUT, DELETE) vs non-idempotent (POST)  
5.9.3 Idempotency key concept (client-generated unique identifier)  
5.9.4 Idempotency key request header (Idempotency-Key)  
5.9.5 Storing idempotency keys (database TTL, Redis)  
5.9.6 Successful and failed request deduplication  
5.9.7 Idempotency key expiration and cleanup  
5.9.8 Use cases (payment processing, order creation, form submissions)  
5.9.9 Real-world examples (Stripe, PayPal, Square APIs)  

## 5.10 API Authentication (API Keys, JWT, OAuth2)
5.10.1 What is API authentication in design  
5.10.2 API Key authentication (simple, revocation challenges)  
5.10.3 Basic Authentication (username/password, base64 encoding)  
5.10.4 JWT (JSON Web Tokens) structure (header, payload, signature)  
5.10.5 JWT validation and stateless authentication  
5.10.6 OAuth2 framework (resource owner, client, authorization server, resource server)  
5.10.7 OAuth2 grant types (authorization code, client credentials, implicit, password)  
5.10.8 OIDC (OpenID Connect) for identity layer  
5.10.9 Mutual TLS (mTLS) for service-to-service authentication  
5.10.10 API authentication selection criteria for different scenarios  

## 5.11 API Documentation (OpenAPI, Postman)
5.11.1 What is API documentation  
5.11.2 OpenAPI Specification (formerly Swagger) structure  
5.11.3 Defining paths, parameters, request bodies, responses in OpenAPI  
5.11.4 OpenAPI tools (Swagger UI, ReDoc, Swagger Editor)  
5.11.5 Postman Collections for API documentation and testing  
5.11.6 API documentation automation (code-first vs design-first)  
5.11.7 Interactive API documentation benefits  
5.11.8 API changelog and version documentation  
5.11.9 Developer portal and API onboarding experience  

## 5.12 API Gateway vs Direct Exposure
5.12.1 What is an API gateway  
5.12.2 API gateway as reverse proxy architecture  
5.12.3 API gateway vs direct API exposure comparison  
5.12.4 API gateway features (rate limiting, authentication, logging, caching, transformation)  
5.12.5 Request aggregation and backend routing  
5.12.6 API gateway for microservices (single entry point)  
5.12.7 API gateway overhead (latency, complexity, cost)  
5.12.8 API gateway offerings (Kong, AWS API Gateway, Nginx, Envoy, Traefik)  
5.12.9 When to use API gateway vs load balancer vs direct exposure  
5.12.10 API gateway failure domain considerations  

## 5.13 Backward Compatibility Design
5.13.1 What is backward compatibility in API design  
5.13.2 Adding optional fields (clients ignore unknown fields)  
5.13.3 Never removing or renaming existing fields  
5.13.4 Changing field types (widening vs narrowing, compatibility risks)  
5.13.5 Adding new endpoints (no impact on existing clients)  
5.13.6 Changing default values (versioning requirement)  
5.13.7 Changing business logic (expected behavior changes)  
5.13.8 Deprecation headers and sunset announcements  
5.13.9 Testing backward compatibility (consumer contract tests)  
5.13.10 GraphQL and gRPC backward compatibility strategies  















# 6. CACHING STRATEGIES

## 6.1 Cache Types (CDN, Client-Side, Server-Side, Database)
6.1.1 What is caching in system design  
6.1.2 CDN (Content Delivery Network) cache for static assets  
6.1.3 Client-side caching (browser cache, mobile app cache, HTTP cache headers)  
6.1.4 Server-side cache (application memory, in-memory data stores)  
6.1.5 Database cache (buffer pool, query cache, materialized views)  
6.1.6 DNS caching (resolver caches, TTL-based)  
6.1.7 Web proxy and reverse proxy caching (Squid, Varnish, Nginx)  
6.1.8 Cache hierarchy and multi-tier caching architectures  

## 6.2 Cache Patterns (Cache-Aside, Read-Through, Write-Through, Write-Behind)
6.2.1 What are cache access patterns  
6.2.2 Cache-Aside (Lazy Loading) pattern (application manages cache)  
6.2.3 Cache-Aside flow (read miss → load from DB → write to cache)  
6.2.4 Read-Through pattern (cache library loads missing data automatically)  
6.2.5 Write-Through pattern (write to cache and DB synchronously)  
6.2.6 Write-Behind (Write-Back) pattern (write to cache, async write to DB)  
6.2.7 Write-Around pattern (write directly to DB, avoid cache on write)  
6.2.8 Pattern selection criteria for different workloads  
6.2.9 Real-world examples of each pattern  

## 6.3 Cache Eviction Policies (LRU, LFU, FIFO, TTL, Random)
6.3.1 What are cache eviction policies  
6.3.2 LRU (Least Recently Used) algorithm and implementation  
6.3.3 LFU (Least Frequently Used) algorithm and use cases  
6.3.4 FIFO (First In First Out) algorithm (simplest, ignores access patterns)  
6.3.5 TTL (Time To Live) based eviction (absolute expiry, sliding expiry)  
6.3.6 Random eviction (good enough for many workloads)  
6.3.7 MRU (Most Recently Used) for specific access patterns  
6.3.8 ARC (Adaptive Replacement Cache) hybrid approach  
6.3.9 Policy selection based on access pattern characteristics  

## 6.4 Cache Consistency Strategies (Eventual vs Strong)
6.4.1 What is cache consistency in system design  
6.4.2 Strong consistency (cache and DB always match)  
6.4.3 Eventual consistency (cache may be stale temporarily)  
6.4.4 Write-through for strong consistency (slower writes)  
6.4.5 Write-behind for eventual consistency (higher write throughput)  
6.4.6 Cache invalidation on write (delete or update cache)  
6.4.7 Lease and lock-based consistency (distributed locks)  
6.4.8 Versioning and vector clocks for cache consistency  
6.4.9 Consistency vs performance trade-offs  

## 6.5 Cache Invalidation Techniques (Time-Based, Event-Based, Manual)
6.5.1 What is cache invalidation  
6.5.2 Time-based invalidation (TTL expiry) simplicity and predictability  
6.5.3 Event-based invalidation (data change triggers cache update)  
6.5.4 Manual invalidation (admin or API triggered purge)  
6.5.5 Purge vs ban vs refresh invalidation methods  
6.5.6 Stale-while-revalidate strategy (serve stale, refresh async)  
6.5.7 Stale-if-error strategy (serve stale on backend error)  
6.5.8 Cache invalidation as a hard problem (cache invalidation is hard)  
6.5.9 Real-world invalidation strategies (CDN purges, webhooks)  

## 6.6 Distributed Caching (Redis Cluster, Memcached)
6.6.1 What is distributed caching  
6.6.2 Consistent hashing for cache node distribution  
6.6.3 Redis Cluster architecture (hash slots, master-replica)  
6.6.4 Memcached architecture (simple, fast, no persistence)  
6.6.5 Gossip protocol for cluster membership  
6.6.6 Replication and failover in distributed caches  
6.6.7 Write and read quorum configurations  
6.6.8 Client-side sharding vs proxy-based sharding  
6.6.9 Redis vs Memcached comparison for distributed caching  
6.6.10 Use cases (session stores, rate limiting, leaderboards)  

## 6.7 Multi-Level Caching (L1 Local, L2 Distributed)
6.7.1 What is multi-level caching (L1/L2 architecture)  
6.7.2 L1 cache (local to application process, ultra-low latency)  
6.7.3 L2 cache (distributed, shared across applications)  
6.7.4 L1 cache population from L2 or database  
6.7.5 Cache coherency between L1 and L2  
6.7.6 Tuning L1 and L2 size ratios  
6.7.7 Use case (hot key offload from L2, reducing network hops)  
6.7.8 Multi-level caching in cloud providers (CloudFront → origin → database)  
6.7.9 Real-world multi-level caching architecture examples  

## 6.8 Cache Stampede Prevention
6.8.1 What is cache stampede (thundering herd) problem  
6.8.2 Cache expiration stampede (many simultaneous recomputations)  
6.8.3 Cache miss stampede (concurrent misses on cold cache)  
6.8.4 Request coalescing (single request recomputes, others wait)  
6.8.5 Probabilistic early expiration (recompute before TTL ends)  
6.8.6 Distributed mutex/lock for recomputation (setnx, redlock)  
6.8.7 Leaky bucket and rate limiting for recomputation  
6.8.8 Stale-while-revalidate as stampede prevention  
6.8.9 Real-world stampede prevention in large-scale systems  

## 6.9 Cache Warm-Up Strategies
6.9.1 What is cache warm-up  
6.9.2 Preloading popular data on application startup  
6.9.3 Scheduled cache warm-up for known traffic patterns  
6.9.4 Cache warming via traffic replay or shadow testing  
6.9.5 On-demand vs precomputed warm-up strategies  
6.9.6 Warm-up for deployment and autoscaling events  
6.9.7 Batch vs single key warm-up approaches  
6.9.8 Warm-up impact on database during preload  
6.9.9 Real-world warm-up strategies (e-commerce product catalogs, news feeds)  

## 6.10 Cache Sizing and Capacity Planning
6.10.1 Why cache sizing is critical for performance  
6.10.2 Working set size estimation (active data only, not all data)  
6.10.3 Memory per key overhead estimation  
6.10.4 Hit ratio as function of cache size (diminishing returns)  
6.10.5 Peak vs average cache usage planning  
6.10.6 Growth projections for cache capacity  
6.10.7 Memory fragmentation and overhead (Redis, Memcached)  
6.10.8 Monitoring cache metrics (hit rate, miss rate, eviction rate)  
6.10.9 Right-sizing cache clusters for cost optimization  

## 6.11 CDN Caching for Static Assets
6.11.1 What is CDN caching  
6.11.2 CDN edge locations and POP architecture  
6.11.3 Static assets for CDN (images, CSS, JS, videos, downloads)  
6.11.4 Cache-Control headers for CDN (public, max-age, s-maxage)  
6.11.5 CDN cache invalidation (purge, versioned URLs, fingerprinting)  
6.11.6 CDN TTL strategies (long TTL with versioned assets)  
6.11.7 CDN cache key customization (query parameters, cookies)  
6.11.8 CDN warming (pre-fetching content before traffic)  
6.11.9 CDN offerings (CloudFront, Cloudflare, Fastly, Akamai)  
6.11.10 CDN caching best practices for performance  

## 6.12 Browser Caching Headers
6.12.1 What are browser caching headers  
6.12.2 Cache-Control directive (max-age, no-cache, no-store, must-revalidate)  
6.12.3 Expires header (HTTP 1.0 legacy, absolute expiry)  
6.12.4 ETag (entity tag) for conditional requests  
6.12.5 Last-Modified header for conditional requests  
6.12.6 If-None-Match and If-Modified-Since validation  
6.12.7 Public vs private cache directives  
6.12.8 Service worker caching for progressive web apps  
6.12.9 Cache busting via versioned URLs or query parameters  
6.12.10 Browser cache best practices for web applications  















# 7. LOAD BALANCING

## 7.1 Layer 4 Load Balancing (IP and Port Level)
7.1.1 What is Layer 4 load balancing  
7.1.2 Operating at transport layer (TCP/UDP, IP, ports)  
7.1.3 No inspection of HTTP headers or application data  
7.1.4 Connection-based routing (forwards raw TCP/UDP connections)  
7.1.5 Low latency and high throughput characteristics  
7.1.6 Minimal processing overhead per packet  
7.1.7 Use cases (database load balancing, gaming, VoIP, any TCP/UDP service)  
7.1.8 Layer 4 load balancing implementations (NLB, HAProxy in TCP mode, IPVS)  

## 7.2 Layer 7 Load Balancing (HTTP/HTTPS Routing)
7.2.1 What is Layer 7 load balancing  
7.2.2 Operating at application layer (HTTP/HTTPS, WebSocket, gRPC)  
7.2.3 HTTP header inspection and routing decisions  
7.2.4 Path-based routing (/api vs /static vs /admin)  
7.2.5 Host-based routing (different domains to different backends)  
7.2.6 Header-based and cookie-based routing  
7.2.7 SSL/TLS termination and inspection capabilities  
7.2.8 Use cases (microservices gateways, API routing, content-based routing)  
7.2.9 Layer 7 load balancing implementations (ALB, Nginx, HAProxy, Traefik, Envoy)  

## 7.3 Load Balancing Algorithms (Round-Robin, Least Connections, IP Hash)
7.3.1 What are load balancing algorithms  
7.3.2 Round-Robin algorithm (sequential distribution, simple, equal share)  
7.3.3 Weighted Round-Robin (different capacities per server)  
7.3.4 Least Connections algorithm (send to server with fewest active connections)  
7.3.5 Weighted Least Connections (capacity-aware least connections)  
7.3.6 Least Response Time algorithm (combines connections + response time)  
7.3.7 IP Hash (consistent hashing for client affinity)  
7.3.8 Random algorithm with two choices (power of two choices)  
7.3.9 Algorithm selection criteria for different workload patterns  

## 7.4 Weighted Load Balancing for Heterogeneous Servers
7.4.1 What is weighted load balancing  
7.4.2 Heterogeneous server environments (different CPU, memory, capacity)  
7.4.3 Assigning weights based on server capacity (CPU cores, RAM, network)  
7.4.4 Weighted Round-Robin algorithm mechanics  
7.4.5 Weighted Least Connections mechanics  
7.4.6 Dynamic weight adjustment (based on real-time metrics)  
7.4.7 Slow start weights for newly added servers  
7.4.8 Use cases (mixed instance types, gradual rollout of new hardware)  
7.4.9 Weight configuration best practices  

## 7.5 Health Checks (Active vs Passive)
7.5.1 What are load balancer health checks  
7.5.2 Active health checks (load balancer probes backend servers)  
7.5.3 Active check types (TCP connection, HTTP request, HTTPS, gRPC, custom)  
7.5.4 Active check parameters (interval, timeout, healthy/unhealthy thresholds)  
7.5.5 Passive health checks (observe real traffic for failures)  
7.5.6 Passive failure detection (connection errors, HTTP 5xx, timeouts)  
7.5.7 Combining active and passive health checks  
7.5.8 Slow start after health check recovery (avoid overwhelming recovering server)  
7.5.9 Health check endpoint design best practices (/health, /ready, /live)  

## 7.6 Session Persistence (Sticky Sessions) vs Stateless
7.6.1 What is session persistence (sticky sessions)  
7.6.2 Sticky sessions via cookie insertion (application cookie, load balancer cookie)  
7.6.3 Sticky sessions via client IP hash (simple but affected by NAT/proxies)  
7.6.4 Sticky sessions use cases (shopping cart, in-memory session data)  
7.6.5 Problems with sticky sessions (uneven load, failover issues)  
7.6.6 Stateless architecture benefits (any server can handle any request)  
7.6.7 Moving session state to external store (Redis, database) for statelessness  
7.6.8 Trade-offs: session persistence vs horizontal scalability  
7.6.9 Real-world patterns (Spring Session, Express session stores)  

## 7.7 SSL/TLS Termination at Load Balancer
7.7.1 What is SSL/TLS termination  
7.7.2 Load balancer decrypts HTTPS traffic, forwards plain HTTP to backends  
7.7.3 Certificate management at load balancer (single certificate location)  
7.7.4 Performance benefits (offloading crypto work from application servers)  
7.7.5 SSL passthrough (encrypted traffic passed to backend without decryption)  
7.7.6 End-to-end encryption (re-encrypt from load balancer to backend)  
7.7.7 Mutual TLS (mTLS) termination at load balancer  
7.7.8 TLS version and cipher suite configuration  
7.7.9 Certificate renewal automation (Let's Encrypt, AWS ACM)  
7.7.10 Security trade-offs of SSL termination vs passthrough  

## 7.8 Global Load Balancing (GSLB, Route53)
7.8.1 What is global load balancing (GSLB)  
7.8.2 DNS-based global load balancing (Route53, CloudFlare, Akamai)  
7.8.3 GeoDNS (geographic routing to nearest region)  
7.8.4 Latency-based routing (route to lowest latency region)  
7.8.5 Weighted DNS (traffic distribution across regions)  
7.8.6 Failover routing (active-passive region failover)  
7.8.7 DNS caching limitations and TTL tuning  
7.8.8 Anycast routing for global load balancing (CloudFlare, Fastly)  
7.8.9 Global load balancer health checks across regions  
7.8.10 Use cases (multi-region active-active, disaster recovery, compliance routing)  

## 7.9 Load Balancer High Availability (Active-Passive, Active-Active)
7.9.1 What is load balancer high availability  
7.9.2 Active-Passive failover model (standby takes over on failure)  
7.9.3 VRRP and keepalived for active-passive HA  
7.9.4 Virtual IP (VIP) floating between load balancers  
7.9.5 Active-Active model (both load balancers handling traffic)  
7.9.6 ECMP (Equal Cost Multi-Path) routing for active-active  
7.9.7 Anycast for active-active load balancer HA  
7.9.8 Cloud-native load balancer HA (AWS NLB/ALB, Azure Load Balancer)  
7.9.9 Failure detection and failover time considerations  
7.9.10 Split-brain prevention in HA load balancer setups  

## 7.10 Load Balancer vs Reverse Proxy vs API Gateway
7.10.1 What is a reverse proxy  
7.10.2 What is an API gateway  
7.10.3 Load balancer (L4, simple distribution) vs reverse proxy (L7, advanced routing)  
7.10.4 Reverse proxy features (SSL termination, caching, compression, rewriting)  
7.10.5 API gateway features (rate limiting, authentication, transformation, aggregation)  
7.10.6 Overlap and differences between the three concepts  
7.10.7 Single component handling all roles (Nginx, HAProxy, Envoy, Traefik)  
7.10.8 Microservices pattern (API gateway → load balancers → services)  
7.10.9 Selection criteria for different architecture needs  

## 7.11 Cloud Load Balancers (ALB, NLB, ELB, Cloud Load Balancing)
7.11.1 What are cloud load balancers  
7.11.2 AWS ALB (Application Load Balancer) - Layer 7, HTTP/HTTPS, path/host routing  
7.11.3 AWS NLB (Network Load Balancer) - Layer 4, TCP/UDP/TLS, high throughput, static IP  
7.11.4 AWS GWLB (Gateway Load Balancer) - for third-party virtual appliances  
7.11.5 AWS CLB (Classic Load Balancer) - legacy, both L4 and basic L7  
7.11.6 Azure Load Balancer (External and Internal) - Layer 4, HA, outbound NAT  
7.11.7 Azure Application Gateway - Layer 7, WAF, SSL termination, path routing  
7.11.8 GCP Cloud Load Balancing - global, cross-region, anycast, integrated CDN  
7.11.9 Cloud load balancer comparison (features, pricing, scale limits)  
7.11.10 Cloud load balancer integration with autoscaling and managed instance groups  

















# 8. MESSAGE QUEUES & STREAMING

## 8.1 Point-to-Point Messaging (Queues)
8.1.1 What is point-to-point messaging  
8.1.2 Queue-based messaging model (one producer, one consumer per message)  
8.1.3 Message consumption and removal from queue after delivery  
8.1.4 Load balancing across multiple consumers of same queue  
8.1.5 Queue message ordering (FIFO queues vs standard queues)  
8.1.6 Use cases (task distribution, work queues, background processing)  
8.1.7 Point-to-point implementations (SQS, RabbitMQ queues, Azure Queue)  
8.1.8 Point-to-point vs publish-subscribe comparison  

## 8.2 Publish-Subscribe Messaging (Topics)
8.2.1 What is publish-subscribe messaging  
8.2.2 Topic-based messaging model (one message, many subscribers)  
8.2.3 Publishers and subscribers decoupling via topics  
8.2.4 Fan-out pattern for parallel processing  
8.2.5 Subscription types (push vs pull, durable vs non-durable)  
8.2.6 Topic filtering (key-based, header-based, SQL-based)  
8.2.7 Wildcard and pattern-based subscriptions  
8.2.8 Use cases (event broadcasting, notifications, real-time updates)  
8.2.9 Publish-subscribe implementations (SNS, Kafka topics, Pub/Sub, RabbitMQ exchanges)  

## 8.3 Message Ordering Guarantees
8.3.1 What are message ordering guarantees  
8.3.2 Strict ordering requirements (event sourcing, financial transactions)  
8.3.3 FIFO queues (first-in-first-out with exactly-once processing)  
8.3.4 Partition-based ordering (order guaranteed within partition, not across)  
8.3.5 Sequence numbers and sequence IDs for client-side ordering  
8.3.6 Total order vs partial order trade-offs  
8.3.7 Ordering overhead on throughput and latency  
8.3.8 Reordering scenarios (retries, failures, network issues)  
8.3.9 Real-world ordering strategies (Kafka partitions, SQS FIFO, RabbitMQ with single consumer)  

## 8.4 At-Least-Once, At-Most-Once, Exactly-Once Delivery
8.4.1 What are message delivery semantics  
8.4.2 At-most-once delivery (fire-and-forget, possible message loss)  
8.4.3 At-most-once use cases (real-time telemetry, transient logs)  
8.4.4 At-least-once delivery (retries, possible duplicates)  
8.4.5 At-least-once implementation (consumer offsets, message acknowledgment)  
8.4.6 Exactly-once delivery (no duplicates, no loss, highest complexity)  
8.4.7 Exactly-once implementation (idempotent consumers, transactional boundaries)  
8.4.8 Distributed transactions and two-phase commit for exactly-once  
8.4.9 Kafka exactly-once semantics (transactions, idempotent producers)  
8.4.10 Delivery semantics trade-offs (throughput vs correctness)  

## 8.5 Dead Letter Queues
8.5.1 What is a dead letter queue (DLQ)  
8.5.2 Handling unprocessable messages (poison pills, schema errors, format issues)  
8.5.3 DLQ trigger conditions (max delivery attempts exceeded, TTL expiry)  
8.5.4 DLQ message retention and inspection  
8.5.5 Reprocessing DLQ messages (manual or automated)  
8.5.6 Alerting on DLQ message arrival  
8.5.7 DLQ for debugging and root cause analysis  
8.5.8 Real-world DLQ configuration (SQS Dead-Letter Queue, RabbitMQ DLX)  
8.5.9 Best practices for DLQ monitoring and cleanup  

## 8.6 Message Retention and TTL
8.6.1 What are message retention and TTL  
8.6.2 Message retention policies (time-based, size-based)  
8.6.3 Message TTL (Time To Live) from enqueue time  
8.6.4 Queue-level vs message-level TTL configuration  
8.6.5 Dead letter queue TTL for failed messages  
8.6.6 Retention for replayability (event sourcing, Kafka retention)  
8.6.7 Storage implications of long retention periods  
8.6.8 Log compaction for key-based retention  
8.6.9 Retention monitoring and capacity planning  

## 8.7 Competing Consumers Pattern
8.7.1 What is the competing consumers pattern  
8.7.2 Multiple consumers processing messages from same queue  
8.7.3 Horizontal scaling for message processing  
8.7.4 Load distribution across consumer instances  
8.7.5 Message prefetch and consumer capacity control  
8.7.6 Consumer failure and message re-queue behavior  
8.7.7 Partitioned queues for ordered competing consumers  
8.7.8 Use cases (parallel processing, worker pools, batch processing)  
8.7.9 Implementation in message brokers (SQS, RabbitMQ, Kafka Consumer Groups)  

## 8.8 Request-Reply Pattern
8.8.1 What is the request-reply pattern in messaging  
8.8.2 Temporary reply queue for synchronous response over async messaging  
8.8.3 Correlation ID for matching request and response  
8.8.4 Reply queue timeout and timeout handling  
8.8.5 Direct reply-to optimization (skip intermediate queue)  
8.8.6 Use cases (RPC over message queues, service orchestration)  
8.8.7 Request-reply vs pure async fire-and-forget  
8.8.8 Implementation patterns (RabbitMQ direct reply-to, SQS temporary queues)  
8.8.9 Request-reply latency and throughput considerations  

## 8.9 Event Sourcing Architecture
8.9.1 What is event sourcing  
8.9.2 State derived from immutable event log (not stored directly)  
8.9.3 Event store as source of truth (append-only, immutable events)  
8.9.4 Replaying events to rebuild application state  
8.9.5 Auditability and debugging benefits of event sourcing  
8.9.6 Event versioning and schema evolution  
8.9.7 Snapshots for performance optimization  
8.9.8 Event sourcing vs CRUD architecture comparison  
8.9.9 Use cases (banking ledgers, version control systems, shopping carts)  
8.9.10 Event sourcing implementations (EventStoreDB, Kafka as event store)  

## 8.10 Change Data Capture (CDC)
8.10.1 What is Change Data Capture (CDC)  
8.10.2 Capturing database changes as event streams (INSERT, UPDATE, DELETE)  
8.10.3 CDC architecture (source database → capture → message queue)  
8.10.4 Log-based CDC (reading transaction logs, minimal database impact)  
8.10.5 Trigger-based CDC (database triggers, higher overhead)  
8.10.6 Query-based CDC (polling for changes, simple but inefficient)  
8.10.7 Use cases (real-time analytics, cache invalidation, search indexing)  
8.10.8 CDC tools (Debezium, AWS DMS, GoldenGate, Maxwell, Canal)  
8.10.9 Outbox pattern for reliable CDC in microservices  

## 8.11 Message Brokers (Kafka, RabbitMQ, SQS, Pub/Sub)
8.11.1 What are message brokers  
8.11.2 Apache Kafka architecture (partitions, topics, brokers, Zookeeper/KRaft)  
8.11.3 Kafka use cases (streaming, log aggregation, event sourcing)  
8.11.4 RabbitMQ architecture (exchanges, queues, bindings, AMQP)  
8.11.5 RabbitMQ use cases (task distribution, RPC, complex routing)  
8.11.6 AWS SQS (fully managed, simple queue, high throughput, SQS FIFO for ordering)  
8.11.7 Google Cloud Pub/Sub (global topics, push/pull, exactly-once)  
8.11.8 Kafka vs RabbitMQ vs SQS vs Pub/Sub comparison  
8.11.9 Selection criteria (throughput, ordering, retention, latency, operational overhead)  

## 8.12 Streaming vs Batch Processing
8.12.1 What is batch processing  
8.12.2 What is stream processing  
8.12.3 Batch processing characteristics (finite data, scheduled, high throughput)  
8.12.4 Stream processing characteristics (infinite data, continuous, low latency)  
8.12.5 Micro-batching as hybrid approach (Spark Streaming, Flink)  
8.12.6 Lambda architecture (batch + stream combined)  
8.12.7 Kappa architecture (stream only, batch as special case)  
8.12.8 Use cases (real-time dashboards vs nightly reports)  
8.12.9 Batch vs stream processing trade-offs (complexity, latency, cost)  

## 8.13 Backpressure Handling
8.13.1 What is backpressure in messaging systems  
8.13.2 Producer outpacing consumer scenario  
8.13.3 Consumer-side backpressure (slow consumer problem)  
8.13.4 Message broker-based backpressure (queue depth limits, flow control)  
8.13.5 Prefetch limit for consumer backpressure  
8.13.6 Reactive streams and non-blocking backpressure  
8.13.7 TCP backpressure at transport layer  
8.13.8 Backpressure strategies (block, drop, buffer, throttle)  
8.13.9 Monitoring consumer lag for backpressure detection  
8.13.10 Real-world backpressure handling (Kafka consumer lag, RabbitMQ credit flow)  

## 8.14 Message Partitioning and Rebalancing
8.14.1 What is message partitioning  
8.14.2 Partition as unit of parallelism (each partition consumed by one consumer)  
8.14.3 Partition key for message placement (consistent hashing)  
8.14.4 Partition count and ordering guarantees  
8.14.5 Consumer group rebalancing (partition redistribution on consumer change)  
8.14.6 Rebalancing strategies (eager rebalancing, cooperative rebalancing)  
8.14.7 Partition rebalancing impact on processing latency  
8.14.8 Static partition assignment vs dynamic rebalancing  
8.14.9 Partition leadership and high availability  
8.14.10 Kafka partition rebalancing deep dive  
















# 9. MICROSERVICES ARCHITECTURE

## 9.1 Monolith vs Microservices Trade-offs
9.1.1 What is monolithic architecture  
9.1.2 What is microservices architecture  
9.1.3 Monolith advantages (simplicity, single codebase, easier transactions, lower latency)  
9.1.4 Monolith disadvantages (slow deployment, scaling limitations, technology lock-in)  
9.1.5 Microservices advantages (independent deployment, team autonomy, technology diversity)  
9.1.6 Microservices disadvantages (distributed system complexity, network latency, data consistency)  
9.1.7 Development velocity comparison between monolith and microservices  
9.1.8 Operational overhead differences (more services, more monitoring, more DevOps)  
9.1.9 Monolith-first strategy (start monolith, extract microservices when needed)  
9.1.10 Decision framework for monolith vs microservices  

## 9.2 Service Decomposition Strategies (By Business Capability, Subdomain)
9.2.1 What is service decomposition in microservices  
9.2.2 Decomposition by business capability (user service, payment service, inventory service)  
9.2.3 Decomposition by subdomain (domain-driven design bounded contexts)  
9.2.4 Decomposition by verb or use case (order service, shipping service)  
9.2.5 Decomposition by noun or resource (customer service, product service)  
9.2.6 Decomposition by data ownership (each service owns its data)  
9.2.7 Strangler fig pattern for incremental decomposition  
9.2.8 Identifying service boundaries using DDD aggregates  
9.2.9 Common decomposition anti-patterns (chatty services, distributed monolith)  

## 9.3 Database per Service Pattern
9.3.1 What is database per service pattern  
9.3.2 Service autonomy via private database ownership  
9.3.3 No direct database access between services (only via APIs)  
9.3.4 Polyglot persistence (different database types per service)  
9.3.5 Database per service challenges (cross-service queries, distributed transactions)  
9.3.6 Cross-service query strategies (API composition, CQRS, materialized views)  
9.3.7 Shared database anti-pattern (couples services, defeats microservices purpose)  
9.3.8 Database per service in different domains (SQL, NoSQL, event store)  
9.3.9 Migration strategies from shared database to database per service  

## 9.4 Saga Pattern for Distributed Transactions
9.4.1 What is the saga pattern  
9.4.2 Distributed transaction problem across multiple services  
9.4.3 Saga as sequence of local transactions with compensation  
9.4.4 Choreography-based saga (event-driven, decentralized coordination)  
9.4.5 Orchestration-based saga (centralized coordinator/saga orchestrator)  
9.4.6 Compensating transactions for rollback (undo operations)  
9.4.7 Saga ACID trade-offs (no isolation, eventual consistency)  
9.4.8 Handling partial failures and retries in sagas  
9.4.9 Monitoring and observability for saga executions  
9.4.10 Real-world saga examples (order fulfillment, travel booking)  

## 9.5 CQRS (Command Query Responsibility Segregation)
9.5.1 What is CQRS pattern  
9.5.2 Separating command (write) and query (read) responsibilities  
9.5.3 Command model (optimized for writes, business logic, validation)  
9.5.4 Query model (optimized for reads, denormalized, multiple views)  
9.5.5 Separate databases for command and query models  
9.5.6 Synchronous vs asynchronous update propagation from command to query  
9.5.7 CQRS with event sourcing combination  
9.5.8 CQRS benefits (independent scaling, separate security, optimized queries)  
9.5.9 CQRS complexity trade-offs (eventual consistency, more moving parts)  
9.5.10 When to use CQRS (complex domains, high read-write ratio, different read models)  

## 9.6 Event-Driven Architecture
9.6.1 What is event-driven architecture (EDA)  
9.6.2 Events as first-class citizens (event producers, event consumers)  
9.6.3 Event brokers for asynchronous communication (Kafka, RabbitMQ, Pub/Sub)  
9.6.4 Loose coupling via event-based communication  
9.6.5 Event-driven vs request-driven (synchronous) communication  
9.6.6 Event schemas and versioning for compatibility  
9.6.7 Event processing patterns (simple, windowed, stateful, streaming)  
9.6.8 Use cases (real-time notifications, analytics pipelines, microservices choreography)  
9.6.9 Event-driven challenges (eventual consistency, debugging complexity, message ordering)  

## 9.7 API Gateway Aggregation Pattern
9.7.1 What is API gateway aggregation pattern  
9.7.2 API gateway as facade for multiple backend services  
9.7.3 Fan-out aggregation (single request to gateway → multiple backend calls)  
9.7.4 Reducing client-side complexity and network round trips  
9.7.5 Aggregation for mobile and UI-specific responses  
9.7.6 Parallel vs sequential aggregation strategies  
9.7.7 Timeout and partial response handling for aggregated calls  
9.7.8 API gateway aggregation vs GraphQL federation  
9.7.9 Performance considerations for aggregation (latency accumulation)  
9.7.10 Use cases (dashboard APIs, mobile-friendly APIs, microservice UI composition)  

## 9.8 Backend for Frontend (BFF) Pattern
9.8.1 What is Backend for Frontend (BFF) pattern  
9.8.2 Per-client-type backend (web BFF, mobile BFF, third-party BFF)  
9.8.3 BFF tailored to specific client needs (screen size, network, latency)  
9.8.4 BFF aggregation and transformation for optimal client payloads  
9.8.5 Independent BFF evolution per platform  
9.8.6 BFF vs single API gateway for all clients  
9.8.7 BFF ownership (frontend team owns their BFF)  
9.8.8 BFF implementation frameworks (GraphQL BFF, REST BFF)  
9.8.9 Real-world BFF examples (Netflix, Spotify, SoundCloud)  

## 9.9 Service Mesh (Istio, Linkerd, Consul)
9.9.1 What is service mesh in microservices  
9.9.2 Service mesh architecture (data plane + control plane)  
9.9.3 Sidecar proxy deployment pattern (Envoy, Linkerd proxy)  
9.9.4 Service mesh features (service discovery, traffic management, observability, security)  
9.9.5 Istio architecture (Istiod, ingress gateway, Envoy sidecars)  
9.9.6 Linkerd architecture (lightweight, Rust/Go proxies, simplicity focus)  
9.9.7 Consul service mesh (HashiCorp ecosystem integration)  
9.9.8 mTLS and zero-trust security with service mesh  
9.9.9 Service mesh vs API gateway (different layers, can be complementary)  
9.9.10 Service mesh overhead (latency, resource consumption, operational complexity)  

## 9.10 Circuit Breaker Pattern (Netflix Hystrix)
9.10.1 What is circuit breaker pattern  
9.10.2 Three circuit states (closed, open, half-open)  
9.10.3 Closed state (normal operation, failures counted)  
9.10.4 Open state (fail fast, no requests to failing service)  
9.10.5 Half-open state (probing for recovery, limited requests)  
9.10.6 Failure threshold and timeout configuration  
9.10.7 Cascading failure prevention with circuit breakers  
9.10.8 Circuit breaker in code (Resilience4j, Hystrix, Polly)  
9.10.9 Circuit breaker with service mesh (Envoy outlier detection)  
9.10.10 Monitoring circuit breaker state changes  

## 9.11 Retry and Timeout Policies
9.11.1 What are retry and timeout policies in microservices  
9.11.2 Timeout configuration (connection timeout, read timeout, request timeout)  
9.11.3 Retry strategies (immediate retry, exponential backoff, jitter)  
9.11.4 Retry for transient failures (network blips, service restarts)  
9.11.5 Maximum retry attempts and retry budgets  
9.11.6 Idempotency requirement for retry safety  
9.11.7 Retry storms and retry amplification prevention  
9.11.8 Timeout and retry interaction (timeout → retry → timeout)  
9.11.9 Retry and timeout in service mesh and API gateway  
9.11.10 Real-world retry policies (AWS SDK, gRPC retry, Kafka consumer retry)  

## 9.12 Bulkhead Pattern for Fault Isolation
9.12.1 What is bulkhead pattern  
9.12.2 Bulkhead concept from ship design (watertight compartments)  
9.12.3 Thread pool isolation (separate pools for different services/customers)  
9.12.4 Connection pool isolation (separate pools per downstream)  
9.12.5 Process/machine level bulkheads (service instances on separate nodes)  
9.12.6 Queue-based bulkheads (separate queues for different workloads)  
9.12.7 Bulkhead in code (Resilience4j bulkhead, Hystrix thread pools)  
9.12.8 Bulkhead vs circuit breaker vs rate limiter comparison  
9.12.9 Use cases (multi-tenant systems, critical vs non-critical operations)  

## 9.13 Sidecar Pattern
9.13.1 What is sidecar pattern  
9.13.2 Sidecar container alongside main application container  
9.13.3 Shared network namespace and filesystem access  
9.13.4 Sidecar responsibilities (logging, monitoring, configuration, service mesh proxy)  
9.13.5 Sidecar example (Envoy sidecar for service mesh)  
9.13.6 Sidecar benefits (separate concerns, language-agnostic, upgrade independently)  
9.13.7 Sidecar in Kubernetes (multi-container pods)  
9.13.8 Sidecar configuration with Istio (automatic injection)  
9.13.9 Sidecar pattern vs daemon set pattern  
9.13.10 Use cases (log shipping, metrics collection, request routing)  

## 9.14 Ambassador Pattern
9.14.1 What is ambassador pattern  
9.14.2 Ambassador as proxy for external service communication  
9.14.3 Ambassador running alongside application (sidecar)  
9.14.4 Ambassador responsibilities (retries, circuit breaking, monitoring, auth)  
9.14.5 Offloading client-side service discovery to ambassador  
9.14.6 Ambassador for legacy systems (shim for modern protocols)  
9.14.7 Ambassador for multi-region database access  
9.14.8 Ambassador vs service mesh sidecar differences  
9.14.9 Implementation examples (Envoy, HAProxy, Nginx as ambassador)  
9.14.10 Use cases (database proxy, external API gateway, legacy system modernization)  

## 9.15 Service Discovery (Client-Side, Server-Side)
9.15.1 What is service discovery in microservices  
9.15.2 Service registry as central source of truth (Consul, Eureka, etcd, Zookeeper)  
9.15.3 Service registration (self-registration vs third-party registration)  
9.15.4 Client-side discovery (client queries registry for service location)  
9.15.5 Client-side discovery implementations (Netflix OSS, Eureka + Ribbon)  
9.15.6 Server-side discovery (load balancer/router queries registry)  
9.15.7 Server-side discovery implementations (AWS ALB/NLB, Kubernetes Services)  
9.15.8 DNS-based discovery (Kubernetes DNS, Consul DNS)  
9.15.9 Service mesh discovery (Pilot/control plane pushes to sidecars)  
9.15.10 Health checking and service deregistration on failure  

## 9.16 Distributed Tracing (Jaeger, Zipkin)
9.16.1 What is distributed tracing in microservices  
9.16.2 Trace, span, and context propagation concepts  
9.16.3 Trace ID and span ID for request correlation  
9.16.4 OpenTelemetry standard for tracing instrumentation  
9.16.5 Jaeger architecture (agent, collector, query, UI)  
9.16.6 Zipkin architecture (collector, storage, API, UI)  
9.16.7 Sampling strategies (head-based, tail-based, probabilistic)  
9.16.8 Context propagation across services (HTTP headers, gRPC metadata)  
9.16.9 Tracing vs logging vs metrics (three pillars of observability)  
9.16.10 Use cases (latency analysis, error diagnosis, dependency mapping)  

## 9.17 Service Versioning and Deprecation
9.17.1 What is service versioning in microservices  
9.17.2 Semantic versioning (major.minor.patch) for services  
9.17.3 API versioning strategies (URL path, header, content negotiation)  
9.17.4 Contract testing for version compatibility (Pact, Spring Cloud Contract)  
9.17.5 Multiple version coexistence in production  
9.17.6 Deprecation policy and sunset headers  
9.17.7 Client notification for deprecated endpoints  
9.17.8 Blue-green and canary for version rollout  
9.17.9 API version lifecycle (alpha → beta → stable → deprecated → removed)  
9.17.10 Breaking vs non-breaking change detection automation  















# 10. DISTRIBUTED SYSTEMS

## 10.1 CAP Theorem (Consistency, Availability, Partition Tolerance)
10.1.1 What is the CAP theorem in distributed systems  
10.1.2 Consistency definition (all nodes see same data at same time)  
10.1.3 Availability definition (every request receives a response)  
10.1.4 Partition tolerance definition (system continues despite network partitions)  
10.1.5 CAP theorem proof (only two of three can be achieved simultaneously)  
10.1.6 CP systems (consistency + partition tolerance, e.g., HBase, MongoDB)  
10.1.7 AP systems (availability + partition tolerance, e.g., Cassandra, DynamoDB)  
10.1.8 CA systems (consistency + availability, impossible in distributed systems)  
10.1.9 CAP theorem misconceptions and practical interpretations  
10.1.10 Choosing CAP trade-offs based on application requirements  

## 10.2 PACELC Theorem
10.2.1 What is PACELC theorem (extension of CAP)  
10.2.2 PACELC structure (if Partition, then Availability vs Consistency; else Latency vs Consistency)  
10.2.3 PA/EC systems (partition → availability, else → consistency, e.g., Cassandra, DynamoDB)  
10.2.4 PC/EC systems (partition → consistency, else → consistency, e.g., HBase, MongoDB)  
10.2.5 PA/EL systems (partition → availability, else → low latency, e.g., Riak, CouchDB)  
10.2.6 PC/EL systems (partition → consistency, else → low latency)  
10.2.7 PACELC vs CAP theorem comparison  
10.2.8 Real-world database classification using PACELC  
10.2.9 Using PACELC for distributed system design decisions  

## 10.3 Strong Consistency vs Eventual Consistency
10.3.1 What is strong (linearizable) consistency  
10.3.2 Strong consistency guarantees (reads see latest write, total order)  
10.3.3 Strong consistency costs (higher latency, lower availability during partitions)  
10.3.4 Strong consistency implementations (Paxos, Raft, quorum reads/writes)  
10.3.5 What is eventual consistency  
10.3.6 Eventual consistency guarantees (all replicas converge eventually, no stale read bound)  
10.3.7 Eventual consistency benefits (high availability, low latency, partition tolerance)  
10.3.8 Tunable consistency (read/write consistency levels in Cassandra, DynamoDB)  
10.3.9 Causal consistency (happens-before relationships) as middle ground  
10.3.10 Use cases for strong vs eventual consistency  

## 10.4 Quorum-Based Consistency (W, R, N)
10.4.1 What is quorum-based consistency  
10.4.2 N (replication factor) total number of replicas  
10.4.3 W (write quorum) number of replicas for successful write  
10.4.4 R (read quorum) number of replicas for successful read  
10.4.5 Strong consistency condition (W + R > N)  
10.4.6 Write-all-read-one consistency (W = N, R = 1)  
10.4.7 Write-one-read-all consistency (W = 1, R = N)  
10.4.8 Quorum configuration trade-offs (latency vs consistency)  
10.4.9 Hinted handoff and read repair for consistency maintenance  
10.4.10 Real-world quorum configurations in DynamoDB, Cassandra, Riak  

## 10.5 Leader Election Algorithms (Bully, Raft, Paxos)
10.5.1 What is leader election in distributed systems  
10.5.2 Bully algorithm (highest node ID becomes leader)  
10.5.3 Bully algorithm message flow (election, victory, coordinator)  
10.5.4 Bully algorithm pros (simple) and cons (node ID not correlated with capability)  
10.5.5 Raft leader election (randomized timeouts, term numbers, votes)  
10.5.6 Raft election states (follower, candidate, leader)  
10.5.7 Raft election safety (at most one leader per term)  
10.5.8 Paxos leader election (distinct from consensus, distinguished proposer)  
10.5.9 Leader election in ZooKeeper (fast leader election algorithm)  
10.5.10 Use cases (database primary selection, cluster coordination)  

## 10.6 Distributed Consensus (Raft, Paxos)
10.6.1 What is distributed consensus problem  
10.6.2 Consensus requirements (agreement, validity, termination, integrity)  
10.6.3 Paxos algorithm overview (proposers, acceptors, learners)  
10.6.4 Paxos phases (prepare, promise, accept, accepted)  
10.6.5 Multi-Paxos for multiple consensus instances  
10.6.6 Paxos complexity challenges (difficult to understand and implement)  
10.6.7 Raft algorithm overview (designed for understandability)  
10.6.8 Raft components (leader election, log replication, safety)  
10.6.9 Raft log replication and commitment  
10.6.10 Consensus implementations (etcd Raft, ZooKeeper ZAB, Consul Raft)  

## 10.7 Distributed Transactions (2PC, 3PC, Saga)
10.7.1 What are distributed transactions  
10.7.2 Two-Phase Commit (2PC) protocol overview  
10.7.3 2PC phase 1 (prepare/voting phase)  
10.7.4 2PC phase 2 (commit/abort phase)  
10.7.5 2PC blocking problem (coordinator failure blocks participants)  
10.7.6 2PC limitations (single point of failure, blocking, performance)  
10.7.7 Three-Phase Commit (3PC) overview (non-blocking but complex)  
10.7.8 Saga pattern as alternative to distributed transactions  
10.7.9 Saga choreography vs orchestration for long-running transactions  
10.7.10 Use cases and trade-offs (2PC for short, critical; Saga for long-running)  

## 10.8 Conflict-Free Replicated Data Types (CRDTs)
10.8.1 What are CRDTs (Conflict-Free Replicated Data Types)  
10.8.2 CRDTs for optimistic replication without coordination  
10.8.3 State-based CRDTs (CvRDTs) with merge operation  
10.8.4 Operation-based CRDTs (CmRDTs) with causal delivery  
10.8.5 Commutative, associative, idempotent merge operations  
10.8.6 Counter CRDT (increment/decrement without coordination)  
10.8.7 Set CRDTs (G-Set, 2P-Set, OR-Set, LWW-Element-Set)  
10.8.8 Register CRDTs (LWW-Register, MV-Register)  
10.8.9 Map CRDT (composition of other CRDTs)  
10.8.10 CRDT implementations (Redis CRDTs, Riak DT, Automerge, Yjs)  

## 10.9 Vector Clocks for Ordering
10.9.1 What are vector clocks for event ordering  
10.9.2 Vector clock structure (node → counter mapping)  
10.9.3 Vector clock update rules (increment on own events, merge incoming)  
10.9.4 Happens-before relationship using vector clocks  
10.9.5 Concurrent event detection via vector clocks  
10.9.6 Vector clock size growth problem and bounded versions  
10.9.7 Vector clocks vs Lamport timestamps (detecting concurrency vs total order)  
10.9.8 Version vectors for detecting data conflicts (DynamoDB, Cassandra)  
10.9.9 Dotted version vectors (compact representation)  
10.9.10 Use cases (distributed conflict detection, causal consistency)  

## 10.10 Gossip Protocol for Membership
10.10.1 What is gossip protocol (epidemic protocol)  
10.10.2 Gossip for cluster membership and failure detection  
10.10.3 Periodic random peer selection for message propagation  
10.10.4 Gossip message types (sync, ack, ack2 for SWIM)  
10.10.5 SWIM (Scalable Weakly-consistent Infection-style Membership) protocol  
10.10.6 Gossip-based failure detection (suspicion, confirmation, timeout)  
10.10.7 Gossip convergence time and bandwidth trade-offs  
10.10.8 Gossip in Cassandra (gossip for node state and schema)  
10.10.9 Gossip in Consul (Serf for membership)  
10.10.10 Gossip vs heartbeat vs consistent hashing for cluster management  

## 10.11 Distributed Locking (Redlock, ZooKeeper, etcd)
10.11.1 What is distributed locking  
10.11.2 Distributed lock requirements (safety, liveness, fault tolerance)  
10.11.3 Redis Redlock algorithm overview  
10.11.4 Redlock steps (get time, lock N instances, offset, validity)  
10.11.5 Redlock criticisms (clock drift, GC pauses, network delays)  
10.11.6 ZooKeeper for distributed locking (ephemeral sequential nodes)  
10.11.7 ZooKeeper lock implementation (create sequential, watch predecessor)  
10.11.8 etcd for distributed locking (lease-based, revision numbers)  
10.11.9 Lease and TTL for lock safety during client failure  
10.11.10 Distributed lock use cases (leader election, cron job coordination)  

## 10.12 Split-Brain Prevention
10.12.1 What is split-brain in distributed systems  
10.12.2 Split-brain causes (network partition, connectivity loss)  
10.12.3 Split-brain consequences (data corruption, inconsistent state)  
10.12.4 Quorum-based split-brain prevention (majority rule)  
10.12.5 Fencing tokens for write safety (unique monotonically increasing tokens)  
10.12.6 STONITH (Shoot The Other Node In The Head) for physical fencing  
10.12.7 Lease and heartbeat expiration for node timeout  
10.12.8 Split-brain detection and recovery strategies  
10.12.9 Split-brain prevention in consensus algorithms (Raft, Paxos)  
10.12.10 Real-world split-brain incidents (database clusters, leader elections)  

## 10.13 Clock Synchronization (NTP, Logical Clocks)
10.13.1 Why clock synchronization matters in distributed systems  
10.13.2 Physical clocks problems (clock drift, monotonicity violations)  
10.13.3 NTP (Network Time Protocol) for clock synchronization  
10.13.4 NTP limitations (network latency, leap second, precision)  
10.13.5 Google TrueTime (GPS + atomic clocks) for Spanner  
10.13.6 Logical clocks alternative to physical clocks  
10.13.7 Lamport timestamps (happens-before, total order)  
10.13.8 Vector clocks for causal order  
10.13.9 Hybrid Logical Clocks (HLCs) combining physical and logical  
10.13.10 Use cases (distributed transactions, causality tracking)  

## 10.14 Idempotency in Distributed Systems
10.14.1 What is idempotency in distributed systems  
10.14.2 Idempotent operation definition (same result on multiple executions)  
10.14.3 HTTP idempotent methods (GET, PUT, DELETE) vs non-idempotent (POST)  
10.14.4 Idempotency key pattern (client-generated unique key)  
10.14.5 Idempotency key storage and deduplication  
10.14.6 Retry safety using idempotency (network failures, timeouts)  
10.14.7 At-least-once delivery with idempotent processing = exactly-once effect  
10.14.8 Natural idempotency (deduplication by business key)  
10.14.9 Idempotent API design best practices  
10.14.10 Real-world idempotency examples (payment processing, order creation)  


















# 11. DATA REPLICATION & SHARDING

## 11.1 Replication Strategies (Single-Leader, Multi-Leader, Leaderless)
11.1.1 What is data replication in distributed databases  
11.1.2 Single-leader (primary-secondary) replication architecture  
11.1.3 Single-leader use cases (high read throughput, simple consistency)  
11.1.4 Single-leader limitations (write bottleneck, leader failover complexity)  
11.1.5 Multi-leader replication architecture (multiple writable nodes)  
11.1.6 Multi-leader use cases (multi-datacenter, offline-first apps, collaborative editing)  
11.1.7 Multi-leader challenges (write conflicts, conflict resolution)  
11.1.8 Leaderless replication architecture (any node accepts writes)  
11.1.9 Leaderless use cases (high availability, write-heavy workloads)  
11.1.10 Leaderless implementations (Cassandra, DynamoDB, Riak)  

## 11.2 Synchronous vs Asynchronous Replication
11.2.1 What is synchronous replication  
11.2.2 Synchronous replication guarantees (no data loss, strong consistency)  
11.2.3 Synchronous replication latency impact (wait for replica acknowledgment)  
11.2.4 Synchronous replication availability trade-off (replica failure blocks write)  
11.2.5 What is asynchronous replication  
11.2.6 Asynchronous replication performance (writes complete immediately)  
11.2.7 Asynchronous replication risk (data loss on leader failure)  
11.2.8 Semi-synchronous replication (one sync replica, others async)  
11.2.9 Quorum-based replication (W > N/2 for sync behavior)  
11.2.10 Real-world replication configurations (MySQL semi-sync, PostgreSQL sync rep)  

## 11.3 Read-After-Write Consistency (Write Concerns)
11.3.1 What is read-after-write consistency  
11.3.2 Write concern definition (number of replicas for write acknowledgment)  
11.3.3 Read concern definition (consistency level for reads)  
11.3.4 Strong read-after-write (W + R > N for quorum)  
11.3.5 Write concerns in MongoDB (w:1, w:majority, w:all)  
11.3.6 Read concerns in MongoDB (local, available, majority, linearizable)  
11.3.7 Consistency levels in Cassandra (ONE, QUORUM, ALL, EACH_QUORUM)  
11.3.8 Consistency levels in DynamoDB (eventual, strong)  
11.3.9 Tunable consistency trade-offs (latency vs correctness)  
11.3.10 Use cases for different write/read concern combinations  

## 11.4 Sharding Key Selection
11.4.1 What is a sharding key (partition key) in distributed databases  
11.4.2 Sharding key role in data distribution across nodes  
11.4.3 High cardinality requirement for sharding keys  
11.4.4 Even distribution requirement for sharding keys (avoid hot spots)  
11.4.5 Query pattern alignment with sharding key (include partition key in queries)  
11.4.6 Composite sharding keys (multiple attributes for distribution)  
11.4.7 Sharding key immutability (changing key requires data movement)  
11.4.8 Common sharding key examples (user_id, customer_id, geo_hash)  
11.4.9 Sharding key selection anti-patterns (low cardinality, monotonically increasing)  
11.4.10 Testing and validating sharding key choices  

## 11.5 Consistent Hashing for Distributed Sharding
11.5.1 What is consistent hashing for distributed systems  
11.5.2 Consistent hashing hash ring concept  
11.5.3 Hash ring with virtual nodes for load balancing  
11.5.4 Consistent hashing node addition (minimal key movement)  
11.5.5 Consistent hashing node removal (keys redistributed only from removed node)  
11.5.6 Consistent hashing vs modulo hashing (scalability difference)  
11.5.7 Consistent hashing implementations (DynamoDB, Cassandra, Riak)  
11.5.8 Jump consistent hashing (simpler, faster, limited use cases)  
11.5.9 Consistent hashing with bounded loads (capacity-aware distribution)  
11.5.10 Use cases (distributed caches, database sharding, load balancers)  

## 11.6 Range-Based vs Hash-Based Sharding
11.6.1 What is range-based sharding  
11.6.2 Range-based sharding mechanics (key ranges assigned to shards)  
11.6.3 Range-based sharding advantages (efficient range queries, dynamic splitting)  
11.6.4 Range-based sharding disadvantages (hot spots, uneven distribution)  
11.6.5 Range-based sharding implementations (HBase, Bigtable, ScyllaDB)  
11.6.6 What is hash-based sharding  
11.6.7 Hash-based sharding mechanics (hash(key) % N → shard)  
11.6.8 Hash-based sharding advantages (even distribution, simple)  
11.6.9 Hash-based sharding disadvantages (no range queries, resharding costly)  
11.6.10 Hash-based sharding implementations (Cassandra, DynamoDB, MongoDB hashed sharding)  

## 11.7 Directory-Based Sharding
11.7.1 What is directory-based sharding  
11.7.2 Directory service as lookup table for key-to-shard mapping  
11.7.3 Directory-based sharding flexibility (arbitrary mapping, easy rebalancing)  
11.7.4 Directory service as single point of failure and bottleneck  
11.7.5 Directory service caching and replication for performance  
11.7.6 Directory-based sharding in Vitess (keyspaces, tablets, vschema)  
11.7.7 Directory-based sharding in Elasticsearch (routing table)  
11.7.8 Directory-based vs hash-based vs range-based comparison  
11.7.9 Use cases (multi-tenant systems with custom partitioning, legacy migration)  
11.7.10 Directory service implementations (ZooKeeper, etcd, Consul)  

## 11.8 Shard Rebalancing Strategies
11.8.1 What is shard rebalancing (resharding)  
11.8.2 Why rebalancing is needed (node addition, removal, uneven growth)  
11.8.3 Fixed number of shards with node reassignment (Elasticsearch)  
11.8.4 Dynamic splitting of hot shards (HBase, Bigtable)  
11.8.5 Consistent hashing with virtual node redistribution  
11.8.6 Directory-based mapping updates for rebalancing  
11.8.7 Online rebalancing vs offline rebalancing  
11.8.8 Data movement during rebalancing (streaming vs bulk copy)  
11.8.9 Rebalancing impact on query performance and availability  
11.8.10 Rebalancing automation and monitoring strategies  

## 11.9 Cross-Shard Queries and Joins
11.9.1 What are cross-shard queries in sharded databases  
11.9.2 Scatter-gather execution model (query all shards, aggregate results)  
11.9.3 Cross-shard query performance (slowest shard determines latency)  
11.9.4 Cross-shard join challenges (data from multiple shards)  
11.9.5 Broadcast join strategy (send small table to all shards)  
11.9.6 Shard-aware join strategy (co-locate related data on same shard)  
11.9.7 Intermediate aggregation at query coordinator  
11.9.8 Application-level joins as alternative (multiple queries)  
11.9.9 Denormalization to avoid cross-shard queries  
11.9.10 Use cases where cross-shard queries are unavoidable (reporting, admin)  

## 11.10 Global Secondary Indexes
11.10.1 What are global secondary indexes (GSI) in sharded databases  
11.10.2 Global index vs local index (cross-shard vs per-shard)  
11.10.3 Global index architecture (separate sharded index table)  
11.10.4 Global index write propagation (update main table + index asynchronously)  
11.10.5 Global index consistency (typically eventual, update propagation delay)  
11.10.6 Global index in DynamoDB (partition key + sort key)  
11.10.7 Global secondary index vs local secondary index in DynamoDB  
11.10.8 Global index in Cassandra (materialized views)  
11.10.9 Global index performance trade-offs (faster reads, slower writes)  
11.10.10 Global index use cases (querying by non-primary key attributes)  

## 11.11 Hot Partition Mitigation
11.11.1 What is hot partition problem in sharded databases  
11.11.2 Hot partition causes (popular keys, skewed data, time-series patterns)  
11.11.3 Shard key suffix with random number (add randomness for distribution)  
11.11.4 Shard key prefix with timestamp + suffix with random (balanced time-series)  
11.11.5 Write sharding (accept writes any shard, move to correct shard later)  
11.11.6 Read replica for hot read partition  
11.11.7 Caching layer for hot data offload from database  
11.11.8 Shard splitting to isolate hot key  
11.11.9 Application-level partitioning (multiple writes per logical entity)  
11.11.10 Monitoring and detecting hot partitions (latency spikes, throttling)  

## 11.12 Shard Splitting and Merging
11.12.1 What is shard splitting and merging  
11.12.2 Shard splitting for growing data (one shard → multiple smaller shards)  
11.12.3 Splitting trigger conditions (size threshold, load threshold)  
11.12.4 Online shard splitting process (split point, redirect writes, background move)  
11.12.5 Shard merging for underutilized shards  
11.12.6 Merging trigger conditions (size below threshold, low QPS)  
11.12.7 Automatic vs manual shard splitting/merging  
11.12.8 Split and merge in range-based sharding (HBase, Bigtable)  
11.12.9 Split and merge in consistent hashing (virtual node adjustment)  
11.12.10 Operational considerations (monitoring, backpressure during splits)  
















# 12. HIGH AVAILABILITY & DISASTER RECOVERY

## 12.1 Availability Metrics (9s: 99.9%, 99.99%, 99.999%)
12.1.1 What is availability in system design  
12.1.2 Availability formula (uptime / (uptime + downtime))  
12.1.3 99.9% (three nines) availability (8.77 hours downtime per year)  
12.1.4 99.99% (four nines) availability (52.6 minutes downtime per year)  
12.1.5 99.999% (five nines) availability (5.26 minutes downtime per year)  
12.1.6 99.9999% (six nines) availability (31.6 seconds downtime per year)  
12.1.7 Availability vs reliability vs durability distinctions  
12.1.8 Mean Time Between Failures (MTBF) and Mean Time To Recover (MTTR)  
12.1.9 Availability calculation for distributed systems (product of component availabilities)  
12.1.10 Setting realistic availability targets based on business requirements  

## 12.2 Redundancy Patterns (Active-Passive, Active-Active)
12.2.1 What are redundancy patterns in HA design  
12.2.2 Active-Passive (primary-secondary) architecture  
12.2.3 Active-Passive failover mechanism (standby takes over on failure)  
12.2.4 Active-Passive failover time (warm-up, DNS propagation, health detection)  
12.2.5 Active-Passive resource utilization (standby idle, cost inefficiency)  
12.2.6 Active-Active architecture (multiple nodes handling traffic simultaneously)  
12.2.7 Active-Active load distribution (load balancer distributes across all nodes)  
12.2.8 Active-Active data consistency challenges (shared state, conflict resolution)  
12.2.9 Active-Active failure handling (remaining nodes absorb traffic)  
12.2.10 Selection criteria for active-passive vs active-active  

## 12.3 Load Balancer HA Configuration
12.3.1 What is load balancer high availability  
12.3.2 Load balancer as single point of failure (must be HA)  
12.3.3 Active-Passive load balancer HA (VRRP, keepalived, floating VIP)  
12.3.4 VRRP (Virtual Router Redundancy Protocol) operation  
12.3.5 Floating Virtual IP (VIP) failover mechanism  
12.3.6 Active-Active load balancer HA (ECMP routing, anycast)  
12.3.7 ECMP (Equal Cost Multi-Path) for load balancer cluster  
12.3.8 Anycast load balancer HA (global IP, BGP routing)  
12.3.9 Cloud load balancer HA (AWS NLB/ALB, Azure LB, GCP CLB are inherently HA)  
12.3.10 Health checking between load balancers for failover trigger  

## 12.4 Database HA (Failover, Replication, Cluster)
12.4.1 What is database high availability  
12.4.2 Database replication for HA (primary to standby)  
12.4.3 Automatic failover vs manual failover for databases  
12.4.4 Leader election for database primary failover  
12.4.5 Database cluster HA (multiple nodes with consensus)  
12.4.6 MySQL HA (Group Replication, InnoDB Cluster, Galera Cluster)  
12.4.7 PostgreSQL HA (Patroni, repmgr, streaming replication + automatic failover)  
12.4.8 MongoDB HA (replica sets with automatic failover)  
12.4.9 Cassandra HA (leaderless, any node can handle writes/reads)  
12.4.10 Split-brain prevention in database HA (fencing, quorum)  

## 12.5 Multi-AZ and Multi-Region Deployments
12.5.1 What are Multi-AZ and Multi-Region deployments  
12.5.2 Availability Zone (AZ) definition (isolated data center within region)  
12.5.3 Multi-AZ deployment for within-region HA  
12.5.4 Multi-AZ benefits (protection from AZ power, network, cooling failures)  
12.5.5 Multi-AZ inter-AZ latency and bandwidth considerations  
12.5.6 Multi-Region deployment for disaster recovery and global presence  
12.5.7 Multi-Region replication patterns (active-passive, active-active)  
12.5.8 Multi-Region consistency challenges (high latency, partitioned deployments)  
12.5.9 Multi-Region cost implications (data transfer, infrastructure replication)  
12.5.10 Use cases for Multi-AZ vs Multi-Region deployments  

## 12.6 Zone-Aware Architecture
12.6.1 What is zone-aware architecture  
12.6.2 Designing workloads to survive entire AZ failure  
12.6.3 Stateless workload distribution across multiple AZs  
12.6.4 Stateful workload replication across AZs (database replicas in each AZ)  
12.6.5 Load balancer zone awareness (distribute traffic across AZs)  
12.6.6 Persistent volume AZ affinity and constraints  
12.6.7 Kubernetes zone-aware scheduling (topology spread constraints, pod anti-affinity)  
12.6.8 Quorum placement for consensus systems (odd number of AZs)  
12.6.9 Cross-AZ data transfer costs and optimization  
12.6.10 Testing AZ failure scenarios (chaos engineering)  

## 12.7 Disaster Recovery Tiers (RTO, RPO)
12.7.1 What are RTO and RPO in disaster recovery  
12.7.2 RTO (Recovery Time Objective) definition (maximum acceptable downtime)  
12.7.3 RPO (Recovery Point Objective) definition (maximum acceptable data loss)  
12.7.4 RTO and RPO trade-offs (lower RTO/RPO → higher cost and complexity)  
12.7.5 Disaster Recovery Tier 0 (no DR, RTO/RPO undefined)  
12.7.6 Disaster Recovery Tier 1 (backup and restore, high RTO/RPO)  
12.7.7 Disaster Recovery Tier 2 (pilot light, moderate RTO/RPO)  
12.7.8 Disaster Recovery Tier 3 (warm standby, lower RTO/RPO)  
12.7.9 Disaster Recovery Tier 4 (hot standby/multi-site active-active, minimal RTO/RPO)  
12.7.10 Business requirements alignment with DR tiers  

## 12.8 Backup Strategies (Full, Incremental, Differential)
12.8.1 What are backup strategies in disaster recovery  
12.8.2 Full backup (complete data copy, longest time, largest storage)  
12.8.3 Full backup restore process (fastest, single backup file)  
12.8.4 Incremental backup (only changes since last backup, fastest backup, smallest storage)  
12.8.5 Incremental restore process (full + all incrementals, slower)  
12.8.6 Differential backup (changes since last full backup)  
12.8.7 Differential restore process (full + latest differential, simpler than incremental)  
12.8.8 Backup retention policies (daily, weekly, monthly, yearly)  
12.8.9 Backup storage tiers (hot, cold, archive, glacier)  
12.8.10 Backup encryption and integrity verification  

## 12.9 Warm Standby vs Hot Standby
12.9.1 What are standby systems in disaster recovery  
12.9.2 Cold standby (off, no resources provisioned, slowest failover)  
12.9.3 Warm standby (provisioned but not fully running services, moderate failover)  
12.9.4 Warm standby characteristics (powered on, software installed, not processing traffic)  
12.9.5 Warm standby failover steps (start services, update DNS, redirect traffic)  
12.9.6 Warm standby RTO (minutes to hours)  
12.9.7 Hot standby (fully running, ready to take traffic immediately)  
12.9.8 Hot standby characteristics (all services running, often small traffic or shadow mode)  
12.9.9 Hot standby failover (instant or seconds, DNS/policy change only)  
12.9.10 Hot standby cost (near full production cost) vs warm standby (reduced cost)  

## 12.10 Pilot Light Disaster Recovery
12.10.1 What is pilot light disaster recovery  
12.10.2 Pilot light concept (from AWS, minimal core services running in DR region)  
12.10.3 Pilot light components (database replicated, essential services running)  
12.10.4 Pilot light failover (scale up additional resources on demand)  
12.10.5 Pilot light RTO (minutes to tens of minutes)  
12.10.6 Pilot light cost (small fraction of full production)  
12.10.7 Pilot light vs warm standby vs hot standby comparison  
12.10.8 Pilot light implementation steps (replication, minimal compute, automation)  
12.10.9 Pilot light testing (failover drills without full scaling)  
12.10.10 Use cases (cost-sensitive enterprises, moderate RTO requirements)  

## 12.11 Chaos Engineering Practices
12.11.1 What is chaos engineering  
12.11.2 Chaos engineering principles (build confidence in system resilience)  
12.11.3 Chaos engineering vs traditional testing differences  
12.11.4 Steady state hypothesis definition (normal system behavior)  
12.11.5 Controlled experimentation in production environment  
12.11.6 Blast radius minimization (limit experiment impact)  
12.11.7 Chaos engineering tools (Chaos Monkey, Gremlin, LitmusChaos, Chaos Mesh)  
12.11.8 Chaos experiments types (pod kill, latency injection, network partition, AZ failure)  
12.11.9 Game days for chaos engineering (scheduled, announced experiments)  
12.11.10 Automation and rollback mechanisms for chaos experiments  

## 12.12 Health Checks and Auto-Healing
12.12.1 What are health checks and auto-healing  
12.12.2 Health check types (liveness, readiness, startup)  
12.12.3 Liveness check (is the application still running?)  
12.12.4 Readiness check (is the application ready to receive traffic?)  
12.12.5 Health check endpoints design (/health, /live, /ready)  
12.12.6 Health check parameters (interval, timeout, failure threshold, success threshold)  
12.12.7 Auto-healing mechanisms (restart unhealthy instances, replace failed nodes)  
12.12.8 Orchestrator-based healing (Kubernetes, Nomad, Docker Swarm)  
12.12.9 Load balancer health check integration (remove unhealthy backends)  
12.12.10 Self-healing vs manual intervention guidelines  

## 12.13 Graceful Degradation
12.13.1 What is graceful degradation in system design  
12.13.2 Graceful degradation vs failover vs fallback  
12.13.3 Partial functionality on component failure (feature degradation)  
12.13.4 Quality of service degradation (lower resolution, reduced accuracy)  
12.13.5 Capacity degradation (throttling non-critical operations)  
12.13.6 Graceful degradation examples (shopping cart when recommendations fail, cached data when DB down)  
12.13.7 Circuit breakers for graceful degradation (fail fast, default responses)  
12.13.8 Static fallback content for dynamic features  
12.13.9 User communication during degradation (toast messages, maintenance pages)  
12.13.10 Graceful degradation vs maintaining core user journey  

## 12.14 Rate Limiting and Load Shedding
12.14.1 What are rate limiting and load shedding for HA  
12.14.2 Rate limiting to prevent system overload  
12.14.3 Rate limiting algorithms (token bucket, leaky bucket, sliding window)  
12.14.4 Rate limiting levels (per user, per IP, per endpoint, global)  
12.14.5 Rate limiting response (HTTP 429 Too Many Requests)  
12.14.6 Load shedding definition (dropping excess load proactively)  
12.14.7 Load shedding strategies (drop low-priority requests, random dropping)  
12.14.8 Priority-based load shedding (critical traffic preserved, non-critical dropped)  
12.14.9 Backpressure propagation for overload protection  
12.14.10 Load shedding vs rate limiting vs throttling comparison  
















# 13. SECURITY DESIGN

## 13.1 Authentication (Password, OAuth2, SSO, Biometric)
13.1.1 What is authentication in system security  
13.1.2 Password-based authentication (hashing, salting, bcrypt/Argon2)  
13.1.3 Password storage best practices (never store plaintext, pepper, key derivation)  
13.1.4 Multi-Factor Authentication (MFA) (SMS, TOTP, hardware tokens, biometric)  
13.1.5 OAuth2 framework for delegated authorization  
13.1.6 OAuth2 grant types (authorization code, PKCE, client credentials)  
13.1.7 OpenID Connect (OIDC) for identity layer on OAuth2  
13.1.8 Single Sign-On (SSO) using SAML, OIDC, or LDAP  
13.1.9 Biometric authentication (fingerprint, face recognition, hardware security keys)  
13.1.10 Authentication method selection for different applications  

## 13.2 Authorization (RBAC, ABAC, ReBAC)
13.2.1 What is authorization in system security  
13.2.2 Authentication vs authorization differences  
13.2.3 RBAC (Role-Based Access Control) model  
13.2.4 RBAC components (users, roles, permissions, sessions)  
13.2.5 RBAC role hierarchy and separation of duties  
13.2.6 ABAC (Attribute-Based Access Control) model  
13.2.7 ABAC attributes (user attributes, resource attributes, environment attributes)  
13.2.8 ABAC policy language (XACML, ALFA) for complex rules  
13.2.9 ReBAC (Relationship-Based Access Control) (Google Zanzibar)  
13.2.10 ReBAC for friend/follower relationships (social networks, collaboration tools)  
13.2.11 Authorization frameworks (Casbin, OPA, Cerbos, AuthZed)  

## 13.3 Encryption at Rest (AES-256, Key Management)
13.3.1 What is encryption at rest  
13.3.2 AES-256 encryption standard for data at rest  
13.3.3 Database encryption (TDE - Transparent Data Encryption)  
13.3.4 Disk-level encryption (full disk encryption, LUKS, BitLocker)  
13.3.5 File-level and object-level encryption (S3 server-side encryption)  
13.3.6 Key Management Service (KMS) for encryption keys (AWS KMS, Azure Key Vault, GCP KMS)  
13.3.7 Bring Your Own Key (BYOK) vs Cloud Provider Key  
13.3.8 Key rotation strategy (periodic, on compromise, compliance-driven)  
13.3.9 Envelope encryption (data key + master key) for performance  
13.3.10 Hardware Security Module (HSM) for highest security key storage  

## 13.4 Encryption in Transit (TLS 1.2+, mTLS)
13.4.1 What is encryption in transit  
13.4.2 TLS (Transport Layer Security) protocol overview  
13.4.3 TLS 1.2 vs TLS 1.3 features and security improvements  
13.4.4 X.509 certificates and Certificate Authorities (CA)  
13.4.5 TLS handshake process (client hello, server hello, certificate exchange)  
13.4.6 Perfect Forward Secrecy (PFS) with ephemeral key exchange  
13.4.7 mTLS (Mutual TLS) for two-way authentication  
13.4.8 mTLS use cases (service-to-service, API gateways, zero trust networks)  
13.4.9 Certificate lifecycle management (generation, renewal, revocation)  
13.4.10 Automating TLS certificates (Let's Encrypt, cert-manager, AWS ACM)  

## 13.5 API Security (Rate Limiting, CORS, Input Validation)
13.5.1 What is API security in system design  
13.5.2 API authentication (API keys, JWT, OAuth2 tokens)  
13.5.3 Rate limiting for API protection (prevent abuse, DoS attacks)  
13.5.4 Rate limiting headers (X-RateLimit-Limit, X-RateLimit-Remaining, Retry-After)  
13.5.5 CORS (Cross-Origin Resource Sharing) configuration  
13.5.6 CORS headers (Access-Control-Allow-Origin, Access-Control-Allow-Methods)  
13.5.7 Input validation (whitelist vs blacklist, type checking, length limits)  
13.5.8 SQL injection prevention via parameterized queries  
13.5.9 XSS (Cross-Site Scripting) prevention (output encoding, Content Security Policy)  
13.5.10 API request signing (HMAC, AWS Signature V4) for integrity  

## 13.6 Secrets Management (Vault, AWS Secrets Manager)
13.6.1 What is secrets management in system security  
13.6.2 Types of secrets (database passwords, API keys, TLS certificates, encryption keys)  
13.6.3 Environment variables anti-pattern for secrets (leakage risk)  
13.6.4 HashiCorp Vault architecture (seal/unseal, storage backend, dynamic secrets)  
13.6.5 Vault secret engines (KV, database, AWS, PKI, Transit)  
13.6.6 Vault authentication methods (token, Kubernetes, LDAP, OIDC, AWS IAM)  
13.6.7 AWS Secrets Manager (automatic rotation, RDS integration)  
13.6.8 Azure Key Vault and GCP Secret Manager  
13.6.9 Secrets rotation strategies (versioned secrets, dynamic credentials)  
13.6.10 Secrets injection into applications (sidecars, init containers, CSI drivers)  

## 13.7 DDoS Protection (Cloudflare, AWS Shield)
13.7.1 What is DDoS (Distributed Denial of Service) attack  
13.7.2 DDoS attack types (volumetric, protocol, application layer)  
13.7.3 Volumetric attacks (UDP flood, ICMP flood, amplification attacks)  
13.7.4 Protocol attacks (SYN flood, ping of death, Smurf attack)  
13.7.5 Application layer attacks (HTTP flood, Slowloris, RUDY)  
13.7.6 Cloudflare DDoS protection (Anycast network, rate limiting, WAF integration)  
13.7.7 AWS Shield (Standard free, Advanced paid with cost protection)  
13.7.8 AWS Shield Advanced features (DDoS response team, real-time metrics)  
13.7.9 Azure DDoS Protection and GCP Cloud Armor  
13.7.10 DDoS mitigation strategies (traffic scrubbing, blackholing, rate limiting)  

## 13.8 Web Application Firewall (WAF)
13.8.1 What is a Web Application Firewall (WAF)  
13.8.2 WAF vs traditional firewall differences (application layer awareness)  
13.8.3 WAF deployment modes (inline, reverse proxy, plugin/module)  
13.8.4 OWASP Core Rule Set (CRS) for WAF rules  
13.8.5 WAF protection against OWASP Top 10 (SQL injection, XSS, CSRF, etc.)  
13.8.6 Cloud WAF offerings (AWS WAF, Cloudflare WAF, Azure WAF, Google Cloud Armor)  
13.8.7 Bot mitigation with WAF (bot detection, CAPTCHA, rate limiting)  
13.8.8 WAF false positives management (tuning, whitelist, rule exclusions)  
13.8.9 WAF logging and alerting for security events  
13.8.10 WAF integration with CDN and load balancers  

## 13.9 SQL Injection and XSS Prevention
13.9.1 What is SQL injection attack  
13.9.2 SQL injection types (union-based, error-based, blind boolean, blind time-based)  
13.9.3 Parameterized queries (prepared statements) as primary defense  
13.9.4 Stored procedure security (still vulnerable if not parameterized)  
13.9.5 ORM frameworks and SQL injection (SQLAlchemy, Hibernate, Entity Framework)  
13.9.6 Input validation and allowlist for SQL injection prevention  
13.9.7 What is XSS (Cross-Site Scripting) attack  
13.9.8 XSS types (stored/persistent, reflected, DOM-based)  
13.9.9 Output encoding for XSS prevention (HTML escape, JavaScript escape)  
13.9.10 Content Security Policy (CSP) headers for XSS mitigation  

## 13.10 Compliance Requirements (GDPR, HIPAA, SOC2, PCI-DSS)
13.10.1 What are compliance requirements in system design  
13.10.2 GDPR (General Data Protection Regulation) overview  
13.10.3 GDPR requirements (right to delete, data portability, breach notification)  
13.10.4 HIPAA (Health Insurance Portability and Accountability Act) for healthcare data  
13.10.5 HIPAA safeguards (administrative, physical, technical)  
13.10.6 SOC2 (Service Organization Control 2) trust principles  
13.10.7 SOC2 Type I vs Type II (point in time vs over period)  
13.10.8 PCI-DSS (Payment Card Industry Data Security Standard)  
13.10.9 PCI-DSS requirements (protect cardholder data, vulnerability management)  
13.10.10 Compliance documentation and audit readiness strategies  

## 13.11 Audit Logging
13.11.1 What is audit logging in security design  
13.11.2 Audit log vs application log differences (immutability, retention, security)  
13.11.3 What events to audit (logins, permission changes, data access, configuration changes)  
13.11.4 Audit log integrity protection (write-once storage, digital signatures, blockchain)  
13.11.5 Audit log retention requirements (regulatory, operational, legal)  
13.11.6 Audit log security (access controls, encryption at rest, tamper detection)  
13.11.7 Audit log collection and aggregation (Splunk, ELK, AWS CloudTrail, Azure Monitor)  
13.11.8 User identification in audit logs (correlation IDs, impersonation tracking)  
13.11.9 Automated audit log review and alerting  
13.11.10 Audit log use cases (incident investigation, compliance reporting, forensic analysis)  

## 13.12 Zero Trust Architecture
13.12.1 What is zero trust architecture (ZTA)  
13.12.2 Zero trust principle (never trust, always verify)  
13.12.3 Traditional perimeter security vs zero trust security  
13.12.4 Zero trust components (identity, devices, networks, workloads, data)  
13.12.5 Micro-segmentation for zero trust networks  
13.12.6 mTLS for service-to-service authentication and encryption  
13.12.7 Continuous verification and monitoring (no implicit trust)  
13.12.8 Zero trust for remote access (beyond VPN)  
13.12.9 Zero trust in cloud and hybrid environments  
13.12.10 Zero trust implementation frameworks (NIST SP 800-207, BeyondCorp)  

## 13.13 Network Segmentation (VPC, Security Groups, NACLs)
13.13.1 What is network segmentation in security design  
13.13.2 VPC (Virtual Private Cloud) for cloud network isolation  
13.13.3 Public vs private subnets separation  
13.13.4 Security Groups (stateful, instance-level firewall rules)  
13.13.5 NACLs (Network Access Control Lists, stateless, subnet-level rules)  
13.13.6 Segmentation tiers (web tier, application tier, database tier)  
13.13.7 Jump boxes and bastion hosts for administrative access  
13.13.8 Service mesh for workload-level segmentation  
13.13.9 Kubernetes Network Policies for pod-level segmentation  
13.13.10 Defense in depth through layered network segmentation  

## 13.14 Threat Modeling (STRIDE Methodology)
13.14.1 What is threat modeling in security design  
13.14.2 STRIDE threat categorization (Spoofing, Tampering, Repudiation, Information Disclosure, DoS, Elevation)  
13.14.3 Spoofing threats (identity, IP, DNS, biometric)  
13.14.4 Tampering threats (data modification, code injection, MITM)  
13.14.5 Repudiation threats (denying actions, lack of audit trails)  
13.14.6 Information Disclosure threats (data leakage, exfiltration, side channels)  
13.14.7 Denial of Service threats (resource exhaustion, flooding, application crashes)  
13.14.8 Elevation of Privilege threats (unauthorized access, privilege escalation)  
13.14.9 Threat modeling process (decompose application, identify threats, document mitigations)  
13.14.10 Threat modeling tools (Microsoft Threat Modeling Tool, OWASP Threat Dragon)  

## 13.15 Penetration Testing Strategy
13.15.1 What is penetration testing in security  
13.15.2 Penetration testing vs vulnerability scanning differences  
13.15.3 Black box testing (no internal knowledge, external attacker perspective)  
13.15.4 White box testing (full knowledge, source code access)  
13.15.5 Grey box testing (limited internal knowledge)  
13.15.6 External vs internal penetration testing scopes  
13.15.7 Web application penetration testing methodology  
13.15.8 Infrastructure and network penetration testing  
13.15.9 Social engineering in penetration testing  
13.15.10 Remediation tracking and retesting cycles  

## 13.16 Incident Response Plan
13.16.1 What is an incident response plan (IRP)  
13.16.2 Incident response lifecycle phases (NIST SP 800-61)  
13.16.3 Preparation phase (tools, runbooks, training, communication trees)  
13.16.4 Detection and Analysis phase (alert triage, verification, severity classification)  
13.16.5 Containment phase (isolate affected systems, block malicious activity)  
13.16.6 Eradication phase (remove root cause, patch vulnerabilities)  
13.16.7 Recovery phase (restore systems from clean backups, validate functionality)  
13.16.8 Post-incident activity (lessons learned, documentation improvement)  
13.16.9 Incident severity levels (SEV1, SEV2, SEV3, SEV4) and SLAs  
13.16.10 Tabletop exercises and incident response drills  

















# 14. SCALABILITY STRATEGIES

## 14.1 Vertical Scaling (Scale Up)
14.1.1 What is vertical scaling (scale up)  
14.1.2 Increasing CPU, RAM, or storage on existing server  
14.1.3 Vertical scaling implementation (upgrade instance type, add resources)  
14.1.4 Vertical scaling advantages (simplicity, no application changes)  
14.1.5 Vertical scaling limitations (hardware caps, downtime during upgrade)  
14.1.6 Maximum vertical scale limits per cloud provider  
14.1.7 Vertical scaling cost characteristics (diminishing returns at high end)  
14.1.8 Use cases for vertical scaling (monoliths, legacy apps, single-node databases)  
14.1.9 Vertical scaling with zero downtime (live migration, hot add)  
14.1.10 Vertical vs horizontal scaling comparison  

## 14.2 Horizontal Scaling (Scale Out)
14.2.1 What is horizontal scaling (scale out)  
14.2.2 Adding more servers/nodes to distribute load  
14.2.3 Horizontal scaling advantages (theoretically infinite, commodity hardware)  
14.2.4 Horizontal scaling challenges (load balancing, state management, data distribution)  
14.2.5 Stateless services as ideal candidates for horizontal scaling  
14.2.6 Stateful service scaling complexity (sharding, replication, consistency)  
14.2.7 Horizontal scaling cost characteristics (linear cost growth)  
14.2.8 Cloud auto-scaling groups for horizontal scaling  
14.2.9 Kubernetes Horizontal Pod Autoscaler (HPA) for container scaling  
14.2.10 Use cases (web servers, APIs, stateless microservices)  

## 14.3 Auto-Scaling Policies (CPU, Memory, Custom Metrics)
14.3.1 What are auto-scaling policies  
14.3.2 CPU utilization-based scaling (target 50-70% utilization)  
14.3.3 CPU scaling thresholds (scale up above X%, scale down below Y%)  
14.3.4 Memory utilization-based scaling (memory pressure, garbage collection)  
14.3.5 Request-based scaling (requests per second, concurrent connections)  
14.3.6 Queue depth-based scaling (SQS queue length, Kafka consumer lag)  
14.3.7 Custom metrics for auto-scaling (business KPIs, custom application metrics)  
14.3.8 Scheduled auto-scaling (known traffic patterns, peak hours)  
14.3.9 Predictive auto-scaling (ML-based forecast of future load)  
14.3.10 Cooldown periods and stabilization windows to prevent flapping  

## 14.4 Stateless vs Stateful Scaling
14.4.1 What is stateless service scaling  
14.4.2 Stateless scaling characteristics (any instance handles any request)  
14.4.3 Stateless scaling simplicity (just add more instances, load balance)  
14.4.4 Stateless external state (session data in Redis, user state in database)  
14.4.5 What is stateful service scaling  
14.4.6 Stateful scaling challenges (data distribution, consistency, rebalancing)  
14.4.7 Stateful scaling with consistent hashing (minimize data movement)  
14.4.8 StatefulSet for stateful workloads in Kubernetes  
14.4.9 Stateful vs stateless trade-offs (simplicity vs performance/locality)  
14.4.10 Hybrid approach (stateless compute + external state store)  

## 14.5 Database Read Replicas for Query Scaling
14.5.1 What are database read replicas for scaling  
14.5.2 Primary-replica replication architecture for read scaling  
14.5.3 Read replicas offload SELECT queries from primary  
14.5.4 Read replica consistency trade-offs (replication lag, stale reads)  
14.5.5 Read replica load balancing strategies (round-robin, least connections)  
14.5.6 Read replica failure handling (remove from load balancer pool)  
14.5.7 Adding and removing read replicas dynamically  
14.5.8 Read replicas for analytics and reporting workloads  
14.5.9 Cross-region read replicas for global read scaling  
14.5.10 Read replica implementations (RDS read replicas, Aurora replicas, Cloud Spanner)  

## 14.6 Connection Pooling for Scale
14.6.1 What is connection pooling for scalability  
14.6.2 Database connection overhead (TCP handshake, authentication, resource allocation)  
14.6.3 Connection pool mechanics (pre-established connections, reuse)  
14.6.4 Connection pool sizing (max connections, min idle, overflow)  
14.6.5 Application-level connection pools (HikariCP, DBCP, pgpool)  
14.6.6 Sidecar connection pool (PGBouncer, ProxySQL, RDS Proxy)  
14.6.7 Connection pooling for serverless (RDS Proxy, Data API)  
14.6.8 HTTP connection pooling for API calls  
14.6.9 Connection pool monitoring (leaks, wait times, active connections)  
14.6.10 Connection pool sizing formulas and capacity planning  

## 14.7 Function-as-a-Service (Serverless) Scaling
14.7.1 What is Function-as-a-Service (FaaS) scaling  
14.7.2 FaaS scaling model (per-request scaling, zero to thousands instantly)  
14.7.3 Concurrency limits and per-function scaling (AWS Lambda, Azure Functions, Cloud Functions)  
14.7.4 Provisioned concurrency for latency-sensitive serverless workloads  
14.7.5 FaaS scaling advantages (no infrastructure management, pay-per-use)  
14.7.6 FaaS scaling limitations (cold starts, execution timeout, state management)  
14.7.7 Cold start mitigation strategies (keep-warm, provisioned concurrency, smaller deployment packages)  
14.7.8 FaaS and event-driven scaling (queue-based, streaming-based)  
14.7.9 Serverless containers (AWS Fargate, Google Cloud Run) scaling  
14.7.10 Use cases (spiky workloads, event processing, APIs, background jobs)  

## 14.8 Asynchronous Processing for Scale
14.8.1 What is asynchronous processing for scalability  
14.8.2 Decoupling request initiation from request completion  
14.8.3 Message queue as buffer between producers and consumers  
14.8.4 Asynchronous processing benefits (smoothing load spikes, decoupling)  
14.8.5 Async patterns (fire-and-forget, request-ack, callback/webhook)  
14.8.6 Consumer scaling (add more consumers to queue)  
14.8.7 Backpressure handling with async queues  
14.8.8 Async processing challenges (delivery semantics, idempotency, monitoring)  
14.8.9 Use cases (email sending, video processing, order fulfillment)  
14.8.10 Async processing with serverless functions (SQS + Lambda)  

## 14.9 Event-Driven Scaling
14.9.1 What is event-driven scaling  
14.9.2 Event-driven architecture (EDA) for elastic scaling  
14.9.3 Event source triggers scale (messages in queue, files in S3, webhooks)  
14.9.4 Scale from zero with event-driven design  
14.9.5 Event-driven scaling in Kubernetes (KEDA - Kubernetes Event-Driven Autoscaling)  
14.9.6 KEDA scalers (RabbitMQ, Kafka, SQS, Redis, Prometheus, Cron)  
14.9.7 Event-driven scaling vs metric-driven scaling  
14.9.8 Batch processing scaling (process more events when available)  
14.9.9 Streaming processing with autoscaling (Kafka Streams, Flink)  
14.9.10 Use cases (IoT data processing, file transformation, chat applications)  

## 14.10 Caching for Read Scale
14.10.1 What is caching for read scalability  
14.10.2 Read-heavy workloads benefit most from caching  
14.10.3 Cache-aside pattern for scaling reads (cache miss loads from database)  
14.10.4 Cache-aside scaling characteristics (scale cache nodes independently)  
14.10.5 Distributed cache scaling (Redis Cluster, Memcached)  
14.10.6 Cache hit ratio and scaling efficiency  
14.10.7 CDN for edge caching (scale static content delivery globally)  
14.10.8 Application-level caching (in-memory caches, local caches)  
14.10.9 Cache sizing for read scale (working set estimation)  
14.10.10 Cache invalidation impact on read scalability  

## 14.12 Data Partitioning for Scale
14.12.1 What is data partitioning for scalability (sharding)  
14.12.2 Splitting dataset across multiple servers horizontally  
14.12.3 Partitioning eliminates single-server bottlenecks  
14.12.4 Partitioning key selection for balanced scale  
14.12.5 Hash partitioning for even scale-out  
14.12.6 Range partitioning for ordered data and range queries  
14.12.7 Directory-based partitioning for flexible scale  
14.12.8 Partition rebalancing during scale-out  
14.12.9 Partitioning challenges (cross-partition queries, joins, transactions)  
14.12.10 Partitioning implementations (Cassandra, HBase, Vitess, DynamoDB)  

## 14.13 Microservice Granularity for Independent Scaling
14.13.1 What is microservice granularity for scaling  
14.13.2 Independent scaling of services (scale only what needs scaling)  
14.13.3 Fine-grained services (scale individual features independently)  
14.13.4 Coarse-grained services (larger services, fewer scaling knobs)  
14.13.5 Identifying scaling boundaries by traffic patterns  
14.13.6 Hot-path vs cold-path separation for efficient scaling  
14.13.7 Strangler pattern for incremental granularity improvement  
14.13.8 Domain-Driven Design (DDD) for bounded context identification  
14.13.9 Over-granularity risks (network overhead, operational complexity)  
14.13.10 Balancing granularity for optimal independent scaling  



















# 15. PERFORMANCE OPTIMIZATION

## 15.1 Latency vs Throughput Trade-offs
15.1.1 What is latency in system performance  
15.1.2 What is throughput in system performance  
15.1.3 Latency definition (time to complete single operation)  
15.1.4 Throughput definition (operations completed per time unit)  
15.1.5 Latency vs throughput trade-off relationship  
15.1.6 Batching to increase throughput (increases latency for some operations)  
15.1.7 Queuing theory and Little's Law (Latency = Queue Length / Throughput)  
15.1.8 Tail latency (p99, p999) vs average latency  
15.1.9 Optimizing for latency vs throughput based on use case  
15.1.10 Real-world trade-off examples (video encoding, database batch writes)  

## 15.2 Indexing for Query Performance
15.2.1 What are database indexes for query performance  
15.2.2 B-Tree indexes (balanced tree, good for equality and range queries)  
15.2.3 Hash indexes (O(1) lookups, equality only, no range queries)  
15.2.4 Bitmap indexes (efficient for low-cardinality columns)  
15.2.5 Inverted indexes for full-text search  
15.2.6 Composite index column ordering (most selective first)  
15.2.7 Covering index (includes all query columns, avoids table access)  
15.2.8 Index scan vs table scan performance difference  
15.2.9 Index maintenance overhead on writes (insert, update, delete)  
15.2.10 Index selection for access patterns (query profiling, slow query log)  

## 15.3 Query Optimization and Execution Plans
15.3.1 What are query optimization and execution plans  
15.3.2 EXPLAIN and ANALYZE commands for execution plan analysis  
15.3.3 Table scan vs index scan vs index seek operations  
15.3.4 Nested loop join vs hash join vs merge join  
15.3.5 Predicate pushdown for early filtering  
15.3.6 Query rewrite techniques (subquery to join, avoid functions on indexed columns)  
15.3.7 Common query optimization mistakes (SELECT *, missing WHERE, OR over IN)  
15.3.8 Partition pruning for partitioned tables  
15.3.9 Query plan caching and parameterization  
15.3.10 Database-specific optimization features (PostgreSQL, MySQL, SQL Server)  

## 15.4 Connection Pooling Optimization
15.4.1 What is connection pooling optimization  
15.4.2 Connection pool sizing formula (connections = (core_count * 2) + effective_spindle_count)  
15.4.3 Too few connections (request queuing, increased latency)  
15.4.4 Too many connections (context switching, database memory pressure)  
15.4.5 Connection pool tuning parameters (maxPoolSize, minIdle, connectionTimeout, idleTimeout)  
15.4.6 Validate connection on borrow (evict broken connections)  
15.4.7 Connection leak detection and auto-reclamation  
15.4.8 Statement caching within connection pool  
15.4.9 PgBouncer connection pooler for PostgreSQL  
15.4.10 Database-side connection limits and pooling alignment  

## 15.5 Pagination and Lazy Loading
15.5.1 What are pagination and lazy loading for performance  
15.5.2 Offset pagination (LIMIT, OFFSET) and performance issues at high offsets  
15.5.3 Cursor-based pagination (keyset, seek method) for consistent performance  
15.5.4 Keyset pagination example (WHERE id > last_id ORDER BY id LIMIT N)  
15.5.5 Lazy loading definition (load data only when needed)  
15.5.6 N+1 query problem in lazy loading (each item triggers separate query)  
15.5.7 Batch loading to solve N+1 problem (DataLoader pattern)  
15.5.8 Eager loading vs lazy loading trade-offs  
15.5.9 UI pagination patterns (infinite scroll, load more button, page selector)  
15.5.10 API pagination best practices (limit default, max limit, pagination metadata)  

## 15.6 Database Query Batching
15.6.1 What is database query batching for performance  
15.6.2 Batch inserts (multiple rows in single INSERT) for write throughput  
15.6.3 Batch size tuning (smaller batches vs larger batches trade-offs)  
15.6.4 Bulk update and delete operations  
15.6.5 JDBC batching (addBatch, executeBatch)  
15.6.6 ORM batching (Hibernate batch_size, Entity Framework batching)  
15.6.7 Batch API for microservices (submit batch, process in one request)  
15.6.8 Batching with message queues (consume in batches)  
15.6.9 Batch vs real-time processing trade-offs  
15.6.10 Use cases (data migration, ETL, bulk imports)  

## 15.7 Pre-computation and Materialized Views
15.7.1 What are pre-computation and materialized views  
15.7.2 Pre-computation definition (compute results before query time)  
15.7.3 Materialized view definition (pre-computed query result stored as table)  
15.7.4 Materialized view refresh strategies (on-commit, on-demand, periodic)  
15.7.5 Materialized view use cases (aggregation, reporting, expensive joins)  
15.7.6 Materialized view in PostgreSQL (REFRESH MATERIALIZED VIEW)  
15.7.7 Materialized view in Oracle, SQL Server (indexed views)  
15.7.8 Rollup and cube tables for OLAP pre-computation  
15.7.9 Pre-computation in data warehouses (ETL to aggregated tables)  
15.7.10 Caching as real-time pre-computation (Redis, Memcached)  

## 15.8 Asynchronous Processing Patterns
15.8.1 What are asynchronous processing patterns for performance  
15.8.2 Fire-and-forget pattern (no response needed, highest throughput)  
15.8.3 Request-ack pattern (acknowledge receipt, process async)  
15.8.4 Callback/webhook pattern (notify when complete)  
15.8.5 Polling pattern (client checks for completion)  
15.8.6 Promise/future pattern in application code  
15.8.7 Async processing benefits (reduced blocking, better resource utilization)  
15.8.8 Async processing challenges (error handling, monitoring, debugging)  
15.8.9 Async frameworks (Celery, Sidekiq, Bull, Hangfire)  
15.8.10 Use cases (email sending, report generation, video transcoding)  

## 15.9 Data Compression for Storage and Network
15.9.1 What is data compression for performance  
15.9.2 Storage compression benefits (less disk I/O, more data in cache)  
15.9.3 Network compression benefits (reduced bandwidth, faster transmission)  
15.9.4 Compression algorithms (gzip, Snappy, LZ4, Zstandard, Brotli)  
15.9.5 Snappy and LZ4 for low CPU, high speed compression  
15.9.6 Zstandard for balanced compression ratio and speed  
15.9.7 Gzip for better compression ratio with higher CPU cost  
15.9.8 Database compression (InnoDB page compression, PostgreSQL TOAST)  
15.9.9 Columnar storage compression (Parquet, ORC, ClickHouse)  
15.9.10 Message compression in Kafka, gRPC, HTTP  

## 15.10 Response Compression (Gzip, Brotli)
15.10.1 What is response compression for web performance  
15.10.2 Content-Encoding header for compressed responses  
15.10.3 Accept-Encoding request header for negotiation  
15.10.4 Gzip compression (widely supported, good compression)  
15.10.5 Brotli compression (better compression ratio, modern browsers)  
15.10.6 Brotli vs Gzip comparison (compression ratio, speed, support)  
15.10.7 Dynamic compression vs static pre-compression  
15.10.8 Compression level tuning (speed vs size trade-offs)  
15.10.9 CDN edge compression (compress once, cache, serve many)  
15.10.10 When to skip compression (already compressed assets like images, videos)  

## 15.11 Asset Optimization (Minification, Bundling, CDN)
15.11.1 What is asset optimization for web performance  
15.11.2 JavaScript minification (remove whitespace, shorten variable names)  
15.11.3 CSS minification (remove comments, whitespace)  
15.11.4 HTML minification (remove comments, whitespace)  
15.11.5 Bundling (combine multiple files into fewer requests)  
15.11.6 Code splitting (load only what's needed for current page)  
15.11.7 Tree shaking (remove unused code from bundles)  
15.11.8 Image optimization (WebP, AVIF, responsive images, lazy loading)  
15.11.9 Font optimization (subsetting, variable fonts, system fonts)  
15.11.10 CDN for asset delivery (edge caching, reduced latency, global distribution)  

## 15.12 HTTP/2 and HTTP/3 Benefits
15.12.1 What are HTTP/2 and HTTP/3 performance benefits  
15.12.2 HTTP/2 multiplexing (multiple requests over single TCP connection)  
15.12.3 HTTP/2 server push (send resources before client requests)  
15.12.4 HTTP/2 header compression (HPACK, reduces overhead)  
15.12.5 HTTP/2 request prioritization (critical resources first)  
15.12.6 HTTP/3 over QUIC (UDP-based, no head-of-line blocking)  
15.12.7 HTTP/3 faster connection establishment (0-RTT for repeat visits)  
15.12.8 HTTP/3 improved handling of packet loss  
15.12.9 HTTP/2 vs HTTP/3 comparison  
15.12.10 Enabling HTTP/2 and HTTP/3 in CDN, load balancers, web servers  

## 15.13 Performance Testing (Load, Stress, Soak, Spike)
15.13.1 What is performance testing in system design  
15.13.2 Load testing (expected normal load, verify SLAs)  
15.13.3 Stress testing (beyond breaking point, find failure threshold)  
15.13.4 Soak testing (extended duration, detect memory leaks, resource exhaustion)  
15.13.5 Spike testing (sudden traffic surge, auto-scaling validation)  
15.13.6 Endurance testing (long-term stability under sustained load)  
15.13.7 Performance testing tools (JMeter, Gatling, k6, Locust)  
15.13.8 Key metrics measured (latency, throughput, error rate, resource utilization)  
15.13.9 Performance test environment considerations (production-like, data volume)  
15.13.10 Performance test automation in CI/CD pipelines  

## 15.14 Performance Baselining and Regression Detection
15.14.1 What are performance baselining and regression detection  
15.14.2 Performance baseline definition (reference performance metrics)  
15.14.3 Establishing baseline under controlled conditions  
15.14.4 Performance regression definition (performance degradation from baseline)  
15.14.5 Automatic performance regression detection in CI/CD  
15.14.6 Statistical methods for regression detection (t-test, Mann-Whitney, threshold-based)  
15.14.7 Performance regression alerting and thresholds  
15.14.8 Comparing across versions (same environment, same data)  
15.14.9 Canary deployment with performance comparison  
15.14.10 Performance regression root cause analysis (profiling, flamegraphs)  

## 15.15 Lazy vs Eager Loading Strategies
15.15.1 What are lazy and eager loading strategies  
15.15.2 Lazy loading (load data on demand, defer until needed)  
15.15.3 Eager loading (load all related data upfront)  
15.15.4 N+1 query problem with lazy loading  
15.15.5 Lazy loading use cases (deep object graphs, optional relationships)  
15.15.6 Eager loading use cases (small datasets, always-needed relationships)  
15.15.7 Hybrid strategies (lazy with batch loading)  
15.15.8 ORM lazy/eager configuration (Hibernate fetch types, Entity Framework includes)  
15.15.9 GraphQL field-level lazy vs eager (resolver per field)  
15.15.10 Front-end lazy loading (images below fold, infinite scroll)  



















# 16. MONITORING & OBSERVABILITY

## 16.1 Metrics (Counters, Gauges, Histograms, Summaries)
16.1.1 What are metrics in observability  
16.1.2 Counter metric (monotonically increasing, e.g., request count, errors)  
16.1.3 Counter usage (rate(), increase() functions for querying)  
16.1.4 Gauge metric (goes up and down, e.g., active connections, memory usage)  
16.1.5 Gauge usage (current value, min, max, delta over time)  
16.1.6 Histogram metric (bucketed observations, e.g., request latency)  
16.1.7 Histogram quantiles (p50, p95, p99 from buckets)  
16.1.8 Summary metric (quantiles computed on client side)  
16.1.9 Histogram vs Summary trade-offs (accuracy, overhead, aggregability)  
16.1.10 Metric naming conventions and label best practices  

## 16.2 Logging (Structured Logs, Log Levels, Aggregation)
16.2.1 What is logging in observability  
16.2.2 Structured logging (JSON format, key-value pairs, searchable)  
16.2.3 Unstructured logging (plain text, human-readable, harder to query)  
16.2.4 Log levels (DEBUG, INFO, WARN, ERROR, FATAL) usage guidelines  
16.2.5 Log level in production (INFO/WARN typically, DEBUG under request)  
16.2.6 Log aggregation architecture (log shippers → buffer → storage → query)  
16.2.7 Log aggregation tools (ELK Stack, Loki, Splunk, Datadog)  
16.2.8 Log sampling for high-volume logs (head-based, tail-based, rate-limiting)  
16.2.9 Log retention policies (hot, warm, cold storage tiers)  
16.2.10 Correlation ID in logs for request tracing across services  

## 16.3 Distributed Tracing (Spans, Traces, Context Propagation)
16.3.1 What is distributed tracing in observability  
16.3.2 Trace definition (end-to-end request path across services)  
16.3.3 Span definition (single operation within a trace)  
16.3.4 Trace ID and Span ID for request correlation  
16.3.5 Parent-child span relationships (causal tree structure)  
16.3.6 Context propagation (HTTP headers, gRPC metadata, message headers)  
16.3.7 W3C Trace Context standard for interoperability  
16.3.8 OpenTelemetry for vendor-neutral instrumentation  
16.3.9 Tracing backends (Jaeger, Zipkin, Tempo, Honeycomb)  
16.3.10 Sampling strategies (head-based, tail-based, probabilistic, rate-limiting)  

## 16.4 SLI (Service Level Indicators) Definition
16.4.1 What are Service Level Indicators (SLIs)  
16.4.2 SLI as quantifiable measure of service performance  
16.4.3 Common SLI types (latency, availability, throughput, error rate, durability)  
16.4.4 Latency SLI (time to complete request, typically p50, p95, p99)  
16.4.5 Availability SLI (proportion of successful requests, uptime percentage)  
16.4.6 Error rate SLI (proportion of failed requests, 5xx errors)  
16.4.7 Throughput SLI (requests processed per second)  
16.4.8 SLI measurement window (rolling window, calendar month)  
16.4.9 SLI aggregation (average vs percentiles, time-based)  
16.4.10 Selecting meaningful SLIs for different service types  

## 16.5 SLO (Service Level Objectives) Setting
16.5.1 What are Service Level Objectives (SLOs)  
16.5.2 SLO as target value for SLI (e.g., p99 latency < 100ms)  
16.5.3 Realistic SLO setting based on historical performance  
16.5.4 SLO setting based on business requirements and user expectations  
16.5.5 Multi-tier SLOs (different targets for different customers/tiers)  
16.5.6 SLO compliance period (rolling 30 days, calendar month)  
16.5.7 SLO burn rate for error budget consumption tracking  
16.5.8 SLO for external vs internal services differences  
16.5.9 SLO documentation and stakeholder alignment  
16.5.10 SLO evolution over time (tighten as system matures)  

## 16.6 SLA (Service Level Agreements) Compliance
16.6.1 What are Service Level Agreements (SLAs)  
16.6.2 SLA as legal/business contract with consequences for breach  
16.6.3 SLA vs SLO vs SLI relationship  
16.6.4 SLA common targets (99.9%, 99.99%, 99.999% availability)  
16.6.5 SLA financial penalties (service credits, refunds) for breach  
16.6.6 SLA exclusions (scheduled maintenance, force majeure, third-party dependencies)  
16.6.7 SLA measurement and reporting to customers  
16.6.8 SLA compliance auditing and verification  
16.6.9 SLA breach incident communication  
16.6.10 SLOs typically stricter than SLAs (safety margin)  

## 16.7 Error Budgets
16.7.1 What are error budgets in SRE practice  
16.7.2 Error budget formula (100% - SLO target)  
16.7.3 Error budget example (99.9% SLO = 0.1% error budget)  
16.7.4 Error budget consumption tracking (burn rate per hour/day)  
16.7.5 Error budget decision framework (release gate, feature freeze)  
16.7.6 Error budget policies (stop releases at 50%, full freeze at 100%)  
16.7.7 Error budget reset period (typically aligned with SLO window)  
16.7.8 Error budget vs toil budget balance  
16.7.9 Blameless post-mortem for error budget exhaustion  
16.7.10 Error budget for internal vs external services  

## 16.8 Alerting Rules (Severity, Thresholds, Deduplication)
16.8.1 What are alerting rules in monitoring  
16.8.2 Alert severity levels (P0/P1/SEV1 critical, P2 high, P3 medium, P4 low)  
16.8.3 Static thresholds (CPU > 80%, latency > 500ms)  
16.8.4 Dynamic thresholds (baseline deviation, anomaly detection)  
16.8.5 Rate-based alerts (error rate > 1% over 5 minutes)  
16.8.6 Alert deduplication (group similar alerts, prevent alert storms)  
16.8.7 Alert suppression during maintenance windows  
16.8.8 Alert dependencies (don't alert on dependent services if upstream down)  
16.8.9 Alert routing (team assignment via service ownership)  
16.8.10 Alert escalation policies (unacknowledged → page → call)  

## 16.9 Dashboards for System Health
16.9.1 What are dashboards for system monitoring  
16.9.2 Dashboard types (operational, business, capacity, SLO)  
16.9.3 Golden signals on dashboards (latency, traffic, errors, saturation)  
16.9.4 USE method dashboards (Utilization, Saturation, Errors) for resources  
16.9.5 RED method dashboards (Rate, Errors, Duration) for services  
16.9.6 Dashboard layout best practices (overview → drill-down)  
16.9.7 Dashboard variables and templating (dynamic filtering)  
16.9.8 Dashboard alert integration (show active alerts, annotations)  
16.9.9 Dashboard tools (Grafana, Datadog dashboards, Tableau)  
16.9.10 Dashboard anti-patterns (chart junk, too many panels, missing context)  

## 16.10 Anomaly Detection
16.10.1 What is anomaly detection in monitoring  
16.10.2 Static threshold limitations (seasonal patterns, gradual baseline shifts)  
16.10.3 Moving average anomaly detection (deviations from rolling average)  
16.10.4 Seasonal decomposition (daily, weekly, monthly patterns)  
16.10.5 Z-score and standard deviation based anomaly detection  
16.10.6 Machine learning for anomaly detection (Prophet, Isolation Forest)  
16.10.7 Adaptive thresholding (automatic threshold adjustment)  
16.10.8 Anomaly detection on multiple dimensions (multivariate)  
16.10.9 Reducing false positives with anomaly validation  
16.10.10 Anomaly detection tools (Prometheus + mtail, Datadog anomaly, AWS Lookout)  

## 16.11 Capacity Forecasting
16.11.1 What is capacity forecasting in monitoring  
16.11.2 Historical trend analysis for resource growth prediction  
16.11.3 Time-series forecasting methods (linear regression, ARIMA, exponential smoothing)  
16.11.4 Business driver-based forecasting (user growth, feature launch impact)  
16.11.5 Seasonal capacity planning (holiday peaks, end-of-month)  
16.11.6 Leading indicators for capacity (queue depth, connection pool usage)  
16.11.7 Automatic provisioning based on forecasts  
16.11.8 Lead time for capacity procurement (cloud vs on-premise differences)  
16.11.9 Safety margin in capacity planning (buffer above forecast)  
16.11.10 Capacity planning dashboards and reporting  

## 16.12 Performance Profiling
16.12.1 What is performance profiling in observability  
16.12.2 CPU profiling (where CPU time is spent, hot methods)  
16.12.3 Memory profiling (heap allocations, memory leaks, garbage collection)  
16.12.4 I/O profiling (disk read/write, network latency)  
16.12.5 Flame graphs for visualizing profiling data  
16.12.6 Continuous profiling (always-on production profiling)  
16.12.7 Profiling overhead considerations (sampling vs instrumentation)  
16.12.8 Profiling tools (pprof, async-profiler, Pyroscope, Datadog Continuous Profiler)  
16.12.9 On-demand vs always-on profiling trade-offs  
16.12.10 Profiling for performance regression debugging  

## 16.13 Black-Box vs White-Box Monitoring
16.13.1 What are black-box and white-box monitoring  
16.13.2 Black-box monitoring (external view, user perspective)  
16.13.3 Black-box examples (synthetic tests, uptime checks, API endpoint monitoring)  
16.13.4 Black-box advantages (catches real user issues, simple)  
16.13.5 Black-box limitations (cannot see internal state, limited root cause)  
16.13.6 White-box monitoring (internal view, system metrics, application metrics)  
16.13.7 White-box examples (CPU, memory, request latency, error rate)  
16.13.8 White-box advantages (rich context, early warning, root cause analysis)  
16.13.9 White-box overhead concerns (metric collection, tracing instrumentation)  
16.13.10 Combining black-box and white-box for comprehensive observability  

## 16.14 On-Call and Incident Response
16.14.1 What is on-call in incident response  
16.14.2 On-call rotation design (follow-the-sun, primary/secondary)  
16.14.3 On-call schedule and handoff processes  
16.14.4 Incident severity levels and response expectations  
16.14.5 Incident response roles (incident commander, operations lead, communications lead)  
16.14.6 Incident triage (acknowledge, assess severity, engage responders)  
16.14.7 Runbooks and playbooks for common scenarios  
16.14.8 ChatOps and incident collaboration tools (PagerDuty, Opsgenie, Slack)  
16.14.9 On-call burnout prevention (fair rotation, no-blame culture, post-incident follow-up)  
16.14.10 On-call compensation and fatigue management  

## 16.15 Post-Mortem and Root Cause Analysis
16.15.1 What are post-mortems and root cause analysis  
16.15.2 Blameless post-mortem culture (focus on process, not people)  
16.15.3 Post-mortem timeline (immediate after incident resolution)  
16.15.4 Post-mortem structure (what happened, impact, timeline, root cause, action items)  
16.15.5 5 Whys technique for root cause analysis  
16.15.6 Fishbone diagram (Ishikawa) for complex root causes  
16.15.7 Action item assignment and tracking (prevent recurrence)  
16.15.8 Post-mortem reading and knowledge sharing  
16.15.9 Post-mortem reviews for near-misses (no customer impact)  
16.15.10 Incident metrics and trend analysis  

## 16.16 Monitoring Tools (Prometheus, Grafana, Datadog, New Relic)
16.16.1 What are monitoring and observability tools  
16.16.2 Prometheus architecture (pull model, TSDB, PromQL)  
16.16.3 Prometheus exporters and service discovery  
16.16.4 Grafana for visualization (dashboards, data sources, alerting)  
16.16.5 LGTM stack (Loki, Grafana, Tempo, Mimir) for complete observability  
16.16.6 Datadog (SaaS, unified platform, APM, logs, infrastructure)  
16.16.7 Datadog features (distributed tracing, profiling, security monitoring)  
16.16.8 New Relic (APM-focused, telemetry data platform, NRQL)  
16.16.9 OpenTelemetry as vendor-neutral standard  
16.16.10 Tool selection criteria (open source vs SaaS, cost, features, team expertise)  
















# 17. DEPLOYMENT STRATEGIES

## 17.1 Blue-Green Deployment
17.1.1 What is blue-green deployment  
17.1.2 Blue environment (current production, live traffic)  
17.1.3 Green environment (new version, staged for cutover)  
17.1.4 Traffic switch mechanism (load balancer, DNS, router)  
17.1.5 Instant rollback by switching back to blue  
17.1.6 Blue-green deployment advantages (rapid rollback, reduced risk)  
17.1.7 Blue-green challenges (double infrastructure cost, database migration)  
17.1.8 Database migration in blue-green (backward-compatible changes only)  
17.1.9 Blue-green with stateless vs stateful applications  
17.1.10 Real-world blue-green implementation (AWS, Kubernetes Services, Cloud Foundry)  

## 17.2 Canary Deployment
17.2.1 What is canary deployment  
17.2.2 Gradual traffic shifting to new version (1%, 5%, 10%, 50%, 100%)  
17.2.3 Canary deployment automation (metrics-based progression)  
17.2.4 Canary analysis (error rate, latency, throughput comparison)  
17.2.5 Automatic rollback on canary metric degradation  
17.2.6 Canary deployment advantages (risk mitigation, real production validation)  
17.2.7 Canary deployment challenges (request routing, session consistency)  
17.2.8 Canary vs blue-green comparison  
17.2.9 Canary deployment tools (Argo Rollouts, Flagger, Spinnaker, Istio)  
17.2.10 Use cases (high-risk changes, performance-sensitive features)  

## 17.3 Rolling Deployment
17.3.1 What is rolling deployment  
17.3.2 Incremental replacement of old instances with new version  
17.3.3 Rolling update parameters (maxSurge, maxUnavailable in Kubernetes)  
17.3.4 Rolling deployment batch size and interval configuration  
17.3.5 Health checking during rolling deployment  
17.3.6 Rolling deployment advantages (no additional infrastructure, gradual)  
17.3.7 Rolling deployment challenges (slower than blue-green, partial rollout state)  
17.3.8 Rolling back a rolling deployment (reverse incremental process)  
17.3.9 Rolling deployment for stateful workloads (StatefulSet ordered updates)  
17.3.10 Rolling deployment in cloud providers (AWS ECS rolling update, GKE rolling update)  

## 17.4 Feature Flags / Toggles
17.4.1 What are feature flags (feature toggles)  
17.4.2 Feature flag types (release toggle, experiment toggle, ops toggle, permission toggle)  
17.4.3 Decoupling deployment from feature release  
17.4.4 Feature flag evaluation at runtime (if/else in code)  
17.4.5 Feature flag configuration sources (config files, environment variables, remote service)  
17.4.6 Feature flag targeting (percentage rollout, user segments, whitelist)  
17.4.7 Kill switch feature flag for emergency disabling  
17.4.8 Feature flag lifecycle (add → test → release → stabilize → remove)  
17.4.9 Feature flag technical debt (old flag cleanup, conditional complexity)  
17.4.10 Feature flag management tools (LaunchDarkly, Split.io, Flagsmith, ConfigCat)  

## 17.5 A/B Testing Infrastructure
17.5.1 What is A/B testing infrastructure  
17.5.2 A/B testing definition (comparing two or more variants)  
17.5.3 Hypothesis definition (expected improvement from variant)  
17.5.4 User assignment and bucketing (consistent, deterministic)  
17.5.5 Bucketing algorithms (hash-based, consistent hashing)  
17.5.6 Experiment control vs treatment groups  
17.5.7 Metrics collection per experiment variant  
17.5.8 Statistical significance calculation (p-value, confidence intervals)  
17.5.9 A/B testing with canary deployment (variant = canary)  
17.5.10 A/B testing platforms (Optimizely, Google Optimize, custom solutions)  

## 17.6 Dark Launches
17.6.1 What is dark launch (shadow launch)  
17.6.2 Running new version alongside production without user traffic  
17.6.3 Shadow traffic (duplicate real traffic to new version)  
17.6.4 Dark launch for performance validation under real load  
17.6.5 Dark launch for correctness verification (compare outputs)  
17.6.6 Dark launch without user impact or awareness  
17.6.7 Shadow traffic implementation (proxy duplicates requests, async comparison)  
17.6.8 Dark launch tools (Apache APISIX shadow traffic, Envoy shadowing)  
17.6.9 Dark launch vs canary vs blue-green comparison  
17.6.10 Use cases (performance testing, ML model validation, database migration)  

## 17.7 Continuous Integration (CI) Pipeline
17.7.1 What is Continuous Integration (CI) pipeline  
17.7.2 CI pipeline stages (commit → build → test → package)  
17.7.3 CI trigger mechanisms (push, pull request, merge)  
17.7.4 Code compilation and dependency management  
17.7.5 Unit test execution (fast feedback, high coverage)  
17.7.6 Static code analysis (linting, security scanning, style checks)  
17.7.7 Integration testing (API tests, database tests, contract tests)  
17.7.8 Artifact and package generation (JAR, Docker image, NPM package)  
17.7.9 Artifact storage and versioning (registry, repository)  
17.7.10 CI tools (Jenkins, GitHub Actions, GitLab CI, CircleCI, Buildkite)  

## 17.8 Continuous Delivery (CD) Pipeline
17.8.1 What is Continuous Delivery (CD) pipeline  
17.8.2 CD vs Continuous Deployment (automated vs manual release trigger)  
17.8.3 CD pipeline stages (deploy to dev → test → staging → production)  
17.8.4 Infrastructure provisioning in CD pipeline  
17.8.5 Environment promotion (dev → test → staging → prod)  
17.8.6 Automated deployment strategies (blue-green, canary, rolling)  
17.8.7 Approval gates for production promotion  
17.8.8 Database migration integration in CD pipeline  
17.8.9 Smoke tests and post-deployment verification  
17.8.10 CD tools (ArgoCD, Flux, Spinnaker, Octopus Deploy)  

## 17.9 Infrastructure as Code (Terraform, CloudFormation)
17.9.1 What is Infrastructure as Code (IaC)  
17.9.2 Declarative infrastructure definition (desired state)  
17.9.3 Terraform architecture (providers, resources, state, HCL)  
17.9.4 Terraform workflow (init, plan, apply, destroy)  
17.9.5 Terraform remote state and state locking  
17.9.6 AWS CloudFormation (YAML/JSON templates, CloudFormation Designer)  
17.9.7 CloudFormation stacks and change sets  
17.9.8 IaC version control and peer review  
17.9.9 Drift detection and remediation  
17.9.10 IaC tools comparison (Terraform vs CloudFormation vs Pulumi vs CDK)  

## 17.10 Configuration Management
17.10.1 What is configuration management in deployment  
17.10.2 Configuration drift prevention (desired state enforcement)  
17.10.3 Configuration as code (config in version control)  
17.10.4 Push vs pull configuration models  
17.10.5 Configuration management tools (Ansible, Chef, Puppet, Salt)  
17.10.6 Ansible architecture (agentless, SSH-based, YAML playbooks)  
17.10.7 Chef architecture (client-server, Ruby DSL)  
17.10.8 Puppet architecture (master-agent, declarative, Ruby DSL)  
17.10.9 Environment-specific configuration (dev, staging, production)  
17.10.10 Configuration management vs orchestration vs IaC  

## 17.11 Container Orchestration (Kubernetes, ECS, Nomad)
17.11.1 What is container orchestration in deployment  
17.11.2 Kubernetes architecture (control plane, worker nodes, pods, services)  
17.11.3 Kubernetes deployment strategies (rolling, recreate, blue-green via service)  
17.11.4 AWS ECS (Elastic Container Service) architecture (tasks, services, Fargate)  
17.11.5 ECS deployment strategies (rolling update, blue-green via CodeDeploy)  
17.11.6 HashiCorp Nomad architecture (client-server, job specifications)  
17.11.7 Nomad deployment strategies (rolling canary, blue-green)  
17.11.8 Kubernetes vs ECS vs Nomad comparison  
17.11.9 Orchestration for stateless vs stateful deployments  
17.11.10 Container orchestration and CD integration  

## 17.12 Immutable Infrastructure
17.12.1 What is immutable infrastructure pattern  
17.12.2 Immutable vs mutable infrastructure comparison  
17.12.3 Immutable infrastructure principle (never modify, always replace)  
17.12.4 Immutable artifacts (pre-built images, versioned)  
17.12.5 Immutable deployment process (deploy new image, destroy old)  
17.12.6 Immutable infrastructure advantages (consistency, reproducibility, easy rollback)  
17.12.7 Immutable infrastructure challenges (build time, storage, state management)  
17.12.8 Immutable infrastructure in cloud (AMI, container images, VM snapshots)  
17.12.9 Immutable infrastructure with Kubernetes (replace pods, not exec)  
17.12.10 Immutable infrastructure and configuration management overlap  

## 17.13 Zero-Downtime Migrations (Schema Changes, Data Migrations)
17.13.1 What are zero-downtime migrations  
17.13.2 Database schema migration without application downtime  
17.13.3 Expand and contract pattern (add new schema, migrate, remove old)  
17.13.4 Backward-compatible schema changes requirements  
17.13.5 Non-breaking changes (add column, add table, add index)  
17.13.6 Breaking changes handling (rename column, change type, delete column)  
17.13.7 Online schema change tools (gh-ost, pt-online-schema-change)  
17.13.8 Dual-write pattern for data migration  
17.13.9 Data backfill strategies (batch processing, low-impact windows)  
17.13.10 Blue-green database migration (keeping old schema for rollback)  

## 17.14 Rollback and Revert Strategies
17.14.1 What are rollback and revert strategies  
17.14.2 Immediate rollback (revert to previous working version)  
17.14.3 Rollback vs revert vs undo differences  
17.14.4 Deployment rollback mechanisms (blue-green switch, canary abort, rolling reverse)  
17.14.5 Database rollback challenges (schema changes, irreversible data migration)  
17.14.6 Feature flag based rollback (disable broken feature, no redeploy)  
17.14.7 Partial rollback (only broken component, keep rest)  
17.14.8 Rollback time and MTTR considerations  
17.14.9 Rollback testing (ensure rollback actually works)  
17.14.10 Post-rollback analysis (root cause, prevention, process improvement)  















# 18. TRADE-OFF ANALYSIS

## 18.1 Consistency vs Availability
18.1.1 What is consistency vs availability trade-off (CAP theorem)  
18.1.2 Strong consistency characteristics (linearizable reads/writes, unified state view)  
18.1.3 Strong consistency use cases (financial transactions, inventory management, user settings)  
18.1.4 Strong consistency costs (higher latency, lower availability during partitions)  
18.1.5 Eventual consistency characteristics (data converges over time, stale reads possible)  
18.1.6 Eventual consistency use cases (social media feeds, analytics, reviews, product catalog)  
18.1.7 Tunable consistency trade-offs (quorum settings in Cassandra, DynamoDB)  
18.1.8 Consistency level decision framework (read vs write sensitivity)  
18.1.9 Real-world examples (banking chooses consistency, e-commerce product views choose availability)  
18.1.10 Hybrid approaches (strong for critical data, eventual for non-critical)  

## 18.2 Latency vs Throughput
18.2.1 What is latency vs throughput trade-off  
18.2.2 Low latency focus (fast individual requests, cost of batching)  
18.2.3 High throughput focus (maximize operations per second, request batching)  
18.2.4 Batching trade-off (higher throughput, increased latency for early items)  
18.2.5 Queuing theory impact (higher throughput increases queue depth and latency)  
18.2.6 Latency-sensitive workloads (user-facing APIs, real-time applications, gaming)  
18.2.7 Throughput-sensitive workloads (batch processing, ETL, data warehousing, analytics)  
18.2.8 Compression trade-off (reduces bandwidth/throughput, adds CPU latency)  
18.2.9 Caching trade-off (reduces latency for cache hits, adds check overhead)  
18.2.10 Adaptive strategies (prioritize latency for premium/real-time users, throughput for background)  

## 18.3 Read Optimization vs Write Optimization
18.3.1 What is read optimization vs write optimization trade-off  
18.3.2 Read-optimized design (pre-computed aggregates, denormalization, materialized views, indexes)  
18.3.3 Read-optimized costs (slower writes, more storage, index maintenance overhead)  
18.3.4 Write-optimized design (append-only, minimal indexes, no denormalization)  
18.3.5 Write-optimized costs (slower reads, aggregation at read time, post-processing)  
18.3.6 CQRS pattern for separate read and write optimization paths  
18.3.7 Read-heavy workload examples (content delivery, dashboards, search, reporting)  
18.3.8 Write-heavy workload examples (logging, event sourcing, IoT ingestion, clickstream)  
18.3.9 Replication for read scaling (writes to primary, reads to replicas)  
18.3.10 Decision framework based on read-to-write ratio (10:1 vs 1:10)  

## 18.4 Normalization vs Denormalization
18.4.1 What is normalization vs denormalization trade-off  
18.4.2 Normalization benefits (data integrity, reduced redundancy, smaller storage)  
18.4.3 Normalization costs (JOIN operations, slower complex queries, more locking)  
18.4.4 Denormalization benefits (faster reads, reduced JOINs, simpler queries)  
18.4.5 Denormalization costs (data duplication, update anomalies, larger storage)  
18.4.6 Third normal form (3NF) vs star schema (dimensional modeling)  
18.4.7 Denormalization in NoSQL as standard practice (embedding documents)  
18.4.8 Hybrid approach (normalized for writes, denormalized read replicas)  
18.4.9 Materialized views as controlled denormalization  
18.4.10 Decision framework (write-heavy → normalized, read-heavy analytics → denormalized)  

## 18.5 Batch vs Real-Time Processing
18.5.1 What is batch vs real-time processing trade-off  
18.5.2 Batch processing characteristics (high latency, high throughput, scheduled, bounded data)  
18.5.3 Batch processing use cases (nightly reports, payroll, ETL, billing, data warehousing)  
18.5.4 Real-time processing characteristics (low latency, continuous, unbounded data)  
18.5.5 Real-time use cases (fraud detection, recommendation, monitoring alerts, live dashboards)  
18.5.6 Micro-batching (compromise like Spark Streaming, Flink with short windows)  
18.5.7 Lambda architecture (batch and real-time pipelines together)  
18.5.8 Kappa architecture (stream processing only, batch as special case)  
18.5.9 Batch vs real-time cost comparison (batch cheaper, real-time more resource intensive)  
18.5.10 Decision framework (latency requirement > seconds → real-time; hours/days → batch)  

## 18.6 Monolith vs Microservices Trade-offs
18.6.1 What is monolith vs microservices trade-off  
18.6.2 Monolith advantages (simplicity, single codebase, easier transactions, lower latency, lower overhead)  
18.6.3 Monolith disadvantages (tight coupling, scaling limitations, slow deployment, technology lock-in)  
18.6.4 Microservices advantages (independent scaling, team autonomy, technology diversity, faster deployments)  
18.6.5 Microservices disadvantages (distributed complexity, network latency, data consistency, operational overhead)  
18.6.6 Monolith-first strategy (start monolith, extract microservices when needed)  
18.6.7 Modular monolith (middle ground with bounded contexts in single deployment)  
18.6.8 Team size and structure alignment with architecture  
18.6.9 When microservices are overkill (small teams, simple domains, early-stage startups)  
18.6.10 Gradual migration from monolith to microservices (strangler pattern)  

## 18.7 SQL vs NoSQL for Specific Use Cases
18.7.1 What is SQL vs NoSQL trade-off  
18.7.2 SQL use cases (complex queries, JOINS, ACID transactions, reporting, structured data)  
18.7.3 NoSQL use cases (high write throughput, flexible schema, horizontal scaling, large volumes)  
18.7.4 Document database use case (content management, catalogs, user profiles, event logging)  
18.7.5 Key-value store use case (session storage, caching, leaderboards, shopping carts)  
18.7.6 Wide-column store use case (time-series IoT, messaging, real-time analytics, weather data)  
18.7.7 Graph database use case (social networks, fraud detection, recommendation engines)  
18.7.8 Polyglot persistence (multiple databases for different workloads within same application)  
18.7.9 Transaction requirement (strong ACID → SQL; eventual consistency acceptable → NoSQL)  
18.7.10 Schema evolution requirement (frequent changes, varying fields → NoSQL; stable schema → SQL)  

## 18.8 Cloud vs On-Premise Decision
18.8.1 What is cloud vs on-premise trade-off  
18.8.2 Cloud advantages (low upfront cost, elastic scaling, managed services, global reach, reduced operational burden)  
18.8.3 Cloud disadvantages (ongoing operational expense, data egress costs, less control, vendor lock-in)  
18.8.4 On-premise advantages (full control, predictable costs, data sovereignty, compliance for sensitive data)  
18.8.5 On-premise disadvantages (high upfront capital expenditure, capacity planning, maintenance, scaling lag)  
18.8.6 Hybrid cloud model (sensitive data on-premise, burst to cloud)  
18.8.7 Multi-cloud strategy (avoid single vendor lock-in, but adds complexity)  
18.8.8 Total Cost of Ownership (TCO) comparison over 3-5 years  
18.8.9 Compliance and regulatory considerations (GDPR, HIPAA, data residency)  
18.8.10 Decision framework (variable/uncertain workload → cloud; predictable high volume → on-premise)  

## 18.9 Build vs Buy Decision Matrix
18.9.1 What is build vs buy trade-off  
18.9.2 Build option (custom development, owned solution, tailored exactly to needs)  
18.9.3 Buy option (commercial off-the-shelf SaaS, vendor-managed software)  
18.9.4 Build advantages (full control, no vendor dependency, exact fit, competitive advantage)  
18.9.5 Build disadvantages (time to market, maintenance cost, bugs and security, distraction from core business)  
18.9.6 Buy advantages (faster deployment, vendor responsibility for maintenance/updates, proven solution)  
18.9.7 Buy disadvantages (vendor lock-in, limited customization, recurring cost, integration challenges)  
18.9.8 Build vs buy decision matrix factors (strategic value, differentiation, cost, time, expertise)  
18.9.9 Build for core differentiators (competitive advantage, unique business logic)  
18.9.10 Buy for commodity capabilities (email sending, authentication, payment processing, monitoring)  

## 18.10 Cost vs Performance Optimization
18.10.1 What is cost vs performance trade-off  
18.10.2 Higher cost for better performance (faster hardware, more memory, SSD vs HDD, global CDN)  
18.10.3 Cost-saving measures that impact performance (smaller instances, slower storage, reduced replication)  
18.10.4 Provisioning for peak vs average load (peak → higher cost, better performance; average → lower cost, risk of degradation)  
18.10.5 Spot/preemptible instances for non-critical workloads (lower cost, lower reliability)  
18.10.6 Caching as performance improvement with cost trade-off (additional infrastructure)  
18.10.7 CDN cost vs latency reduction for global users  
18.10.8 Reserved instances vs on-demand (pre-pay discount for long-term, less flexibility)  
18.10.9 Right-sizing (avoid over-provisioning, use cost monitoring tools)  
18.10.10 Cost-performance optimization framework (set SLOs, find cheapest way to meet them)  

## 18.11 Time-to-Market vs Technical Debt
18.11.1 What is time-to-market vs technical debt trade-off  
18.11.2 Speed focus (rapid development, minimal documentation, skip tests, lower initial quality)  
18.11.3 Speed advantages (competitive advantage, user feedback validation, market opportunity capture)  
18.11.4 Speed disadvantages (accumulating technical debt, harder changes later, bugs and incidents)  
18.11.5 Technical debt definition (shortcuts, suboptimal design, missing tests, outdated documentation)  
18.11.6 Technical debt types (intentional for speed, unintentional from inexperience, bit rot)  
18.11.7 Planned technical debt (documented, tracked, scheduled for repayment)  
18.11.8 Technical debt repayment (refactoring, adding tests, improving architecture)  
18.11.9 Startup vs enterprise trade-offs (startups prioritize speed, enterprises prioritize quality)  
18.11.10 MVP approach (minimal features to validate, technical debt acceptable, repay after validation)  

## 18.12 Vendor Lock-in vs Standardization
18.12.1 What is vendor lock-in vs standardization trade-off  
18.12.2 Vendor lock-in definition (dependent on proprietary APIs, tools, data formats, services)  
18.12.3 Vendor lock-in advantages (faster development, integrated ecosystem, vendor support)  
18.12.4 Vendor lock-in disadvantages (difficult migration, pricing power, limited negotiation)  
18.12.5 Standardization definition (open standards, open source, portable across providers)  
18.12.6 Standardization advantages (portability, avoid single point of failure, competitive pricing)  
18.12.7 Standardization disadvantages (integration effort, feature lag behind proprietary, community support)  
18.12.8 Lock-in risk levels (database query language low, cloud-specific API high, data formats medium)  
18.12.9 Abstraction layers for lock-in reduction (Terraform, Kubernetes, OpenTelemetry, CDK)  
18.12.10 Decision framework (short-term project tolerate lock-in, long-term strategic prefer standardization)  



















# 19. SYSTEM DESIGN CASE STUDIES

## 19.1 URL Shortener (TinyURL, bit.ly)
19.1.1 What is URL shortener system design  
19.1.2 Functional requirements (create short URL, redirect to original, custom alias, analytics)  
19.1.3 Non-functional requirements (low latency redirect, high availability, durability)  
19.1.4 Capacity estimation (billions of writes, trillions of reads, QPS calculations)  
19.1.5 URL shortening algorithm (base62 encoding, hash functions, collision handling)  
19.1.6 Redirect flow (HTTP 301 vs 302 permanent vs temporary redirect)  
19.1.7 Database schema (original_url, short_code, user_id, created_at, expiration)  
19.1.8 Cache design (cache frequently accessed URLs, CDN for redirects)  
19.1.9 Analytics pipeline (click tracking, referrer, geolocation, device type)  
19.1.10 API design (POST /shorten, GET /:short_code, DELETE /:short_code)  

## 19.2 Chat System (WhatsApp, Slack, Discord)
19.2.1 What is chat system design  
19.2.2 Functional requirements (1-1 chat, group chat, presence indicator, message history, delivery status)  
19.2.3 Non-functional requirements (low latency, high availability, strong consistency for messages)  
19.2.4 Capacity estimation (billions of users, millions of concurrent connections, message throughput)  
19.2.5 Message flow (sender → chat server → message queue → receiver)  
19.2.6 Real-time delivery (WebSocket long-lived connections, HTTP long polling fallback)  
19.2.7 Database schema (messages table, conversations, participants, user presence)  
19.2.8 Message ordering (timestamp with sequence numbers, vector clocks)  
19.2.9 Media handling (CDN for images, files, videos; separate storage)  
19.2.10 Offline messages (store in database, deliver on reconnection)  

## 19.3 Video Streaming Platform (YouTube, Netflix, Twitch)
19.3.1 What is video streaming platform design  
19.3.2 Functional requirements (upload video, stream video, search, recommendations, comments)  
19.3.3 Non-functional requirements (low buffer time, high availability, global low latency)  
19.3.4 Video upload flow (upload to blob storage, trigger async processing pipeline)  
19.3.5 Video processing pipeline (transcoding to multiple bitrates, resolutions, adaptive bitrate streaming)  
19.3.6 Video storage architecture (hot storage for popular, cold storage for archive)  
19.3.7 CDN delivery (edge caching for popular content, origin fetch for cache miss)  
19.3.8 DASH vs HLS streaming protocols (adaptive bitrate, segment-based)  
19.3.9 Live streaming challenges (sub-second latency, rewind, DVR)  
19.3.10 Recommendation system (collaborative filtering, user watch history, trending)  

## 19.4 Social Media Feed (Twitter, Instagram, Facebook)
19.4.1 What is social media feed design  
19.4.2 Functional requirements (post content, follow/unfollow, generate feed, like/share/comment)  
19.4.3 Non-functional requirements (fast feed generation, high throughput writes, availability)  
19.4.4 Feed generation approaches (pull-based vs push-based fanout)  
19.4.5 Push-based fanout for active users (write-time distribution to followers' inboxes)  
19.4.6 Pull-based for inactive users and celebrities (read-time aggregation)  
19.4.7 Hybrid fanout strategy (push for small follower counts, pull for large)  
19.4.8 Feed ranking and scoring (relevance, recency, engagement signals)  
19.4.9 Database schema (posts table, user graph, feed metadata)  
19.4.10 Caching strategy (pre-computed feeds in Redis, CDN for media)  

## 19.5 E-Commerce Platform (Amazon, Shopify)
19.5.1 What is e-commerce platform design  
19.5.2 Functional requirements (product catalog, search, cart, checkout, orders, inventory, payments)  
19.5.3 Non-functional requirements (consistency for inventory, high availability, security)  
19.5.4 Product catalog design (search indexing, faceted filters, categories, attributes)  
19.5.5 Shopping cart (temporary storage, Redis or session-based, merge across devices)  
19.5.6 Inventory management (reservation during checkout, decrement on payment)  
19.5.7 Order processing state machine (pending → paid → shipped → delivered → completed)  
19.5.8 Checkout flow (address validation, shipping calculation, payment processing)  
19.5.9 Idempotency for payment and order creation  
19.5.10 Database sharding (by user_id, order_id, product_id based on access pattern)  

## 19.6 Ride-Sharing (Uber, Lyft)
19.6.1 What is ride-sharing system design  
19.6.2 Functional requirements (rider request ride, driver location updates, matchmaking, fare calculation)  
19.6.3 Non-functional requirements (low latency matching, high availability, geo-distributed)  
19.6.4 Driver location tracking (periodic updates, WebSocket for real-time)  
19.6.5 Ride request flow (user request → find nearby drivers → match → notify)  
19.6.6 Geospatial indexing (quadtree, geohash, Google S2 cells for nearby driver queries)  
19.6.7 Matching algorithm (nearest driver, ETA calculation, driver acceptance)  
19.6.8 Ride state management (requested → accepted → arrived → started → completed)  
19.6.9 Fare calculation (distance, time, surge pricing, promotions)  
19.6.10 Surge pricing (demand-supply imbalance, real-time price adjustment)  

## 19.7 Online Food Delivery (DoorDash, Zomato)
19.7.1 What is online food delivery system design  
19.7.2 Functional requirements (restaurant discovery, menu browsing, order placement, delivery tracking)  
19.7.3 Non-functional requirements (real-time order tracking, low latency, high consistency)  
19.7.4 Restaurant and menu data model (restaurants, items, prices, availability)  
19.7.5 Cart and order management (item selection, special instructions, order aggregation)  
19.7.6 Order assignment (nearest available delivery partner, ETA calculation)  
19.7.7 Real-time order tracking (location updates every few seconds)  
19.7.8 Estimated delivery time (preparation time + travel time calculations)  
19.7.9 Payment and split bill functionality  
19.7.10 Delivery partner dispatch and optimization (batch orders, route optimization)  

## 19.8 Payment System (Stripe, PayPal)
19.8.1 What is payment system design  
19.8.2 Functional requirements (payment processing, refunds, dispute handling, payout to merchants)  
19.8.3 Non-functional requirements (strong consistency, durability, security, compliance)  
19.8.4 Payment flow (user → merchant → payment processor → bank network)  
19.8.5 Idempotency keys for payment operations (prevent double charging)  
19.8.6 Two-phase commit for payment authorization and capture  
19.8.7 Payment state machine (authorized → captured → settled → completed)  
19.8.8 PCI-DSS compliance requirements (tokenization, encryption, isolation)  
19.8.9 Fraud detection (rules engine, ML models, velocity checks)  
19.8.10 Reconciliation (matching payments with bank statements, dispute resolution)  

## 19.9 Collaborative Document Editing (Google Docs)
19.9.1 What is collaborative document editing design  
19.9.2 Functional requirements (real-time editing, cursor tracking, version history, comments)  
19.9.3 Non-functional requirements (low latency updates, conflict-free merging, high availability)  
19.9.4 Operational Transform (OT) algorithm for conflict resolution  
19.9.5 CRDTs (Conflict-Free Replicated Data Types) for collaborative editing  
19.9.6 OT vs CRDT comparison for collaborative editing  
19.9.7 Document change propagation (delta updates via WebSocket)  
19.9.8 Cursor and presence tracking (user position in document)  
19.9.9 Version history and time travel (checkpoint snapshots + change logs)  
19.9.10 Locking for section-based editing (optional for structured documents)  

## 19.10 Real-Time Leaderboard (Gaming, Analytics)
19.10.1 What is real-time leaderboard design  
19.10.2 Functional requirements (submit score, view top N, view rank, real-time updates)  
19.10.3 Non-functional requirements (low latency updates, high write throughput, strong consistency)  
19.10.4 Redis sorted sets for leaderboard implementation (ZADD, ZRANK, ZREVRANGE)  
19.10.5 Sorted set complexity (O(log N) for inserts and queries)  
19.10.6 Sharding leaderboard by game or region  
19.10.7 Periodic archiving of historical leaderboard snapshots  
19.10.8 Handling millions of users (tiered leaderboards, buckets)  
19.10.9 Real-time scoring with anti-cheat verification  
19.10.10 Alternatives (DynamoDB with GSIs, Cassandra, PostgreSQL with proper indexing)  

## 19.11 Key-Value Store (Redis, DynamoDB Design)
19.11.1 What is key-value store system design  
19.11.2 Functional requirements (GET, PUT, DELETE, SCAN, TTL)  
19.11.3 Non-functional requirements (high throughput, low latency, scalability, durability)  
19.11.4 Consistent hashing for sharding and load distribution  
19.11.5 Replication for durability and read scaling (leaderless, quorum-based)  
19.11.6 Hinted handoff and read repair for consistency  
19.11.7 Merkle trees for anti-entropy and replica synchronization  
19.11.8 In-memory vs persistent storage trade-offs  
19.11.9 TTL and lazy expiration implementation  
19.11.10 DynamoDB architecture vs Redis architecture comparison  

## 19.12 Rate Limiter (Distributed Token Bucket)
19.12.1 What is rate limiter system design  
19.12.2 Functional requirements (limit requests per time window, per user/IP/API, configurable limits)  
19.12.3 Non-functional requirements (low latency, accuracy, fault tolerance)  
19.12.4 Token bucket algorithm for rate limiting (bucket capacity, refill rate)  
19.12.5 Leaky bucket algorithm for smoothing bursts  
19.12.6 Fixed window counter (simple but has edge effects at boundaries)  
19.12.7 Sliding window log (accurate but memory intensive)  
19.12.8 Sliding window counter (hybrid of fixed window and log)  
19.12.9 Distributed rate limiting with Redis (atomic operations, Lua scripts)  
19.12.10 Rate limiting response headers (X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Reset)  

## 19.13 Proximity Service (Yelp, Google Maps Nearby Places)
19.13.1 What is proximity service system design  
19.13.2 Functional requirements (find nearby places, radius search, update location, place details)  
19.13.3 Non-functional requirements (low query latency, high write throughput, geo-distribution)  
19.13.4 Geospatial indexing with geohash (grid-based, prefix search for neighbors)  
19.13.5 Quadtree indexing (hierarchical subdivision of space)  
19.13.6 Google S2 cells (spherical geometry for Earth-scale indexing)  
19.13.7 MongoDB geospatial indexes (2dsphere, GeoJSON support)  
19.13.8 PostGIS for spatial queries on relational databases  
19.13.9 Elasticsearch geo queries for proximity search  
19.13.10 Caching strategy for frequently queried areas and popular places  

## 19.14 Notification System (Push, Email, SMS)
19.14.1 What is notification system design  
19.14.2 Functional requirements (send notifications to users, multiple channels, templating, delivery status)  
19.14.3 Non-functional requirements (high throughput, low latency, deliverability, idempotency)  
19.14.4 Notification types (push notifications, email, SMS, in-app, webhook)  
19.14.5 Notification pipeline (producer → queue → processor → channel provider)  
19.14.6 Template management (variable substitution, multi-language support)  
19.14.7 User preference store (opt-in/out per channel, quiet hours)  
19.14.8 Rate limiting per user/channel (prevent spam, carrier limits)  
19.14.9 Delivery retry and dead letter queue for failed notifications  
19.14.10 Batching and aggregation for similar notifications (e.g., "you have 5 new messages")  

## 19.15 Web Crawler (Google Search)
19.15.1 What is web crawler system design  
19.15.2 Functional requirements (fetch pages, extract links, avoid duplicates, respect robots.txt, politeness)  
19.15.3 Non-functional requirements (scalability to billions of pages, freshness, efficiency)  
19.15.4 URL frontier (scheduler for prioritized crawling, politeness policies, deduplication)  
19.15.5 DNS resolver caching and performance optimizations  
19.15.6 Fetching infrastructure (distributed downloaders, timeout handling, retries)  
19.15.7 Link extraction and relative URL resolution  
19.15.8 URL deduplication using bloom filter (memory-efficient)  
19.15.9 Content hashing for duplicate page detection (shingles, SimHash)  
19.15.10 Crawl freshness and recrawl scheduling based on page change frequency  

## 19.16 File Storage System (Dropbox, Google Drive)
19.16.1 What is file storage system design  
19.16.2 Functional requirements (upload/download files, sync across devices, file versioning, sharing)  
19.16.3 Non-functional requirements (durability, availability, low latency, strong consistency)  
19.16.4 File chunking (split large files into fixed-size or variable-size blocks)  
19.16.5 Deduplication at block level to reduce storage  
19.16.6 Sync protocol (client changes → server → update other clients)  
19.16.7 Delta sync (only upload changed portions of file, not entire file)  
19.16.8 Conflict resolution for concurrent edits (last-write-wins, versioning, manual merge)  
19.16.9 Blob storage for actual file data, metadata in relational database  
19.16.10 File sharing permissions (ACLs, link sharing, expiration)  

## 19.17 Job Queue System
19.17.1 What is job queue system design  
19.17.2 Functional requirements (submit job, schedule job, execute job, retry failed jobs, monitor status)  
19.17.3 Non-functional requirements (durability, at-least-once/at-most-once delivery, scalability)  
19.17.4 Queue as buffer between producers and consumers  
19.17.5 Job states (queued → processing → completed/failed → retry → dead letter)  
19.17.6 Job prioritization (priority queues for urgent jobs)  
19.17.7 Scheduling for delayed and recurring jobs (cron-based, delayed execution)  
19.17.8 Consumer scaling (add more consumers for parallel processing)  
19.17.9 Job persistence and replayability (store job data in database)  
19.17.10 Job queue implementations (Redis Queue, RabbitMQ, SQS, Celery, Sidekiq)  

## 19.18 Metrics Aggregation System
19.18.1 What is metrics aggregation system design  
19.18.2 Functional requirements (ingest time-series metrics, query and aggregate, alerting, visualization)  
19.18.3 Non-functional requirements (high write throughput, low query latency, data retention)  
19.18.4 Metrics data model (timestamp, metric name, tags/labels, value)  
19.18.5 Push vs pull ingestion models (Prometheus pull, StatsD push, OpenTelemetry)  
19.18.6 Time-series database requirements (high compaction, downsampling, retention policies)  
19.18.7 Aggregation and rollups (pre-compute 1min, 5min, 1hr aggregates from raw data)  
19.18.8 Label indexing and cardinality management (avoid high cardinality explosions)  
19.18.9 Distributed query handling (query splitting, parallel execution, merging)  
19.18.10 Metrics aggregation systems (Prometheus, InfluxDB, M3, VictoriaMetrics, Thanos)  


## 19.19 Search Autocomplete (Typeahead)
19.19.1 What is search autocomplete system design
19.19.2 Functional requirements (real-time suggestions, personalization, trending queries)
19.19.3 Non-functional requirements (sub-50ms latency, high throughput)
19.19.4 Trie data structure for prefix matching
19.19.5 Trie compression (radix tree, Patricia trie) for memory efficiency
19.19.6 Ranking suggestions (frequency, recency, personalization)
19.19.7 Geospatial and language-specific autocomplete
19.19.8 Real-time update of trending queries
19.19.9 Caching strategy (CDN, Redis for popular prefixes)
19.19.10 Sharding the trie (prefix-based distribution)

## 19.20 Distributed ID Generator (Snowflake)
19.20.1 What is distributed ID generator design
19.20.2 Functional requirements (unique, sortable, 64-bit, high throughput)
19.20.3 Non-functional requirements (low latency, no single point of failure)
19.20.4 Twitter Snowflake ID structure (timestamp + datacenter ID + worker ID + sequence)
19.20.5 Timestamp bits for time-sortable IDs (41 bits, 69 years)
19.20.6 Worker ID allocation (ZooKeeper, etcd, or manual)
19.20.7 Sequence number per millisecond (12 bits, 4096 IDs per ms)
19.20.8 Clock synchronization and drift handling
19.20.9 Leaf (美团) and Sonyflake alternatives
19.20.10 Database vs Redis vs Snowflake comparison

## 19.21 Digital Wallet (Venmo, Google Pay)
19.21.1 What is digital wallet system design
19.21.2 Functional requirements (send/receive money, transaction history, social feed)
19.21.3 Non-functional requirements (consistency, durability, security)
19.21.4 Account and balance management
19.21.5 Transaction state machine (pending → completed → failed → reversed)
19.21.6 Double-entry bookkeeping for auditability
19.21.7 Social feed of transactions (privacy settings, friend-only)
19.21.8 Fraud detection and transaction limits
19.21.9 Integration with payment rails (ACH, cards, instant transfer)
19.21.10 Idempotency for transaction submission

## 19.22 Task Scheduler (Distributed Cron)
19.22.1 What is task scheduler system design
19.22.2 Functional requirements (schedule jobs, cron expressions, retries, monitoring)
19.22.3 Non-functional requirements (reliability, scalability, fault tolerance)
19.22.4 Leader election for single scheduler (Raft, ZooKeeper)
19.22.5 Job store (database table with next_run_time, status, retry count)
19.22.6 Scheduler loop (poll database for jobs due to run)
19.22.7 Worker pool for job execution (distributed workers)
19.22.8 Missed schedule handling (catchup vs skip)
19.22.9 Job deduplication and idempotent execution
19.22.10 Implementations (Airflow scheduler, Quartz, Cron as a service)

## 19.23 Online Stock Trading (Robinhood)
19.23.1 What is stock trading system design
19.23.2 Functional requirements (view prices, place orders, order book, portfolio)
19.23.3 Non-functional requirements (low latency, consistency, high availability)
19.23.4 Market data feed processing (WebSocket real-time price updates)
19.23.5 Order types (market, limit, stop-loss, stop-limit)
19.23.6 Order book management (bid/ask queues, price-time priority)
19.23.7 Order matching engine (simplified for interview)
19.23.8 Portfolio and position management
19.23.9 Idempotency for order submission
19.23.10 Trade settlement and reconciliation














# 20. DATA PIPELINES

## 20.1 ETL vs ELT Patterns
20.1.1 What is ETL (Extract, Transform, Load) pattern  
20.1.2 ETL process (extract from source, transform before load, load to target)  
20.1.3 ETL use cases (data warehousing, sensitive data masking, complex transformations)  
20.1.4 What is ELT (Extract, Load, Transform) pattern  
20.1.5 ELT process (extract from source, load raw to target, transform in target)  
20.1.6 ELT use cases (big data, cloud data warehouses, schema flexibility)  
20.1.7 ETL vs ELT trade-offs (processing location, performance, storage costs)  
20.1.8 ETL tools (Informatica, Talend, AWS Glue, Azure Data Factory)  
20.1.9 ELT platforms (Snowflake, BigQuery, Redshift, Databricks)  
20.1.10 Selection criteria (data volume, transformation complexity, latency requirements)  

## 20.2 Batch Data Processing (Spark, Hadoop)
20.2.1 What is batch data processing  
20.2.2 Batch processing characteristics (high throughput, high latency, scheduled, bounded data)  
20.2.3 Hadoop ecosystem (HDFS storage, MapReduce processing, YARN scheduling)  
20.2.4 Hadoop limitations (disk I/O heavy, complex programming, MapReduce verbosity)  
20.2.5 Apache Spark architecture (driver, executors, in-memory processing, DAG execution)  
20.2.6 Spark transformations (narrow vs wide, lazy evaluation)  
20.2.7 Spark actions (trigger computation, collect, count, save)  
20.2.8 Spark optimizations (partitioning, bucketing, broadcast joins)  
20.2.9 Batch processing use cases (nightly reports, ETL, data warehousing, analytics)  
20.2.10 Spark vs Hadoop MapReduce comparison (performance, ease of use, ecosystem)  

## 20.3 Stream Data Processing (Flink, Kafka Streams)
20.3.1 What is stream data processing  
20.3.2 Stream processing characteristics (low latency, continuous, unbounded data)  
20.3.3 Apache Flink architecture (job manager, task managers, checkpointing)  
20.3.4 Flink features (event time processing, exactly-once, state management, windowing)  
20.3.5 Kafka Streams architecture (embedded library, no separate cluster, Kafka as source/sink)  
20.3.6 Kafka Streams features (exactly-once, state stores, interactive queries)  
20.3.7 Flink vs Kafka Streams comparison (capabilities, operational complexity, latency)  
20.3.8 Apache Spark Streaming (micro-batching, structured streaming)  
20.3.9 Stream processing use cases (fraud detection, real-time dashboards, anomaly detection)  
20.3.10 Stream processing challenges (state management, exactly-once, backpressure)  

## 20.4 Lambda Architecture (Batch + Stream)
20.4.1 What is Lambda architecture  
20.4.2 Lambda architecture layers (batch layer, speed layer, serving layer)  
20.4.3 Batch layer (master dataset, pre-compute batch views, high latency)  
20.4.4 Speed layer (real-time processing, incremental updates, low latency)  
20.4.5 Serving layer (merge batch and real-time views, query API)  
20.4.6 Lambda architecture query flow (batch view + speed view = final result)  
20.4.7 Lambda architecture advantages (fault tolerance, comprehensive results)  
20.4.8 Lambda architecture disadvantages (code duplication, operational complexity)  
20.4.9 Lambda architecture tools (Spark batch + Kafka Streams speed)  
20.4.10 When Lambda is appropriate (need both accuracy and low latency)  

## 20.5 Kappa Architecture (Stream-Only)
20.5.1 What is Kappa architecture  
20.5.2 Kappa principle (unified stream processing, batch as special case)  
20.5.3 Kappa architecture components (stream source, stream processor, serving layer)  
20.5.4 Reprocessing in Kappa (replay stream from checkpoint or new topic)  
20.5.5 Kappa advantages (single codebase, simpler operations, easier maintenance)  
20.5.6 Kappa disadvantages (storage costs for replay, stream reprocessing time)  
20.5.7 Kappa vs Lambda architecture comparison  
20.5.8 Kappa implementation (Kafka + Kafka Streams, Flink, Kinesis Analytics)  
20.5.9 When Kappa is appropriate (infinite retention, reasonable reprocessing window)  
20.5.10 Real-world Kappa adoption (LinkedIn, Netflix, Uber)  

## 20.6 Data Lake and Data Warehouse
20.6.1 What is a data warehouse  
20.6.2 Data warehouse characteristics (structured data, schema-on-write, high performance queries)  
20.6.3 Data warehouse use cases (BI reporting, dashboards, business analytics)  
20.6.4 What is a data lake  
20.6.5 Data lake characteristics (raw data, schema-on-read, schema flexibility, low-cost storage)  
20.6.6 Data lake use cases (data science, machine learning, exploratory analytics)  
20.6.7 Data lakehouse (combining data lake + data warehouse features)  
20.6.8 Data lakehouse platforms (Databricks, Iceberg, Hudi, Delta Lake)  
20.6.9 Data warehouse vs data lake vs lakehouse comparison  
20.6.10 Data mesh (decentralized data ownership, domain-oriented data products)  

## 20.7 Schema Registry and Evolution
20.7.1 What is schema registry in data pipelines  
20.7.2 Schema registry role (store and manage schemas, versioning, compatibility checks)  
20.7.3 Confluent Schema Registry for Kafka (Avro, Protobuf, JSON Schema)  
20.7.4 Schema ID in message header (reduce payload size, schema lookup)  
20.7.4 Schema evolution compatibility rules (backward, forward, full, none)  
20.7.5 Backward compatibility (new schema reads old data)  
20.7.6 Forward compatibility (old schema reads new data)  
20.7.7 Full compatibility (both backward and forward)  
20.7.8 Schema evolution examples (adding optional fields, removing fields, renaming)  
20.7.9 Breaking vs non-breaking schema changes  
20.7.10 Schema registry tools (Confluent Schema Registry, AWS Glue Schema Registry, Apicurio)  

## 20.8 Data Quality and Validation
20.8.1 What is data quality in data pipelines  
20.8.2 Data quality dimensions (accuracy, completeness, consistency, timeliness, uniqueness)  
20.8.3 Data validation types (schema validation, constraint checks, referential integrity)  
20.8.4 Null checks and default value handling  
20.8.5 Data quality checks (range checks, format validation, uniqueness checks)  
20.8.6 Expectation testing framework (Great Expectations, dbt tests, Deequ)  
20.8.7 Data quality metrics (pass rate, row count, null percentage, distribution shifts)  
20.8.8 Data quality monitoring and alerting  
20.8.9 Dead letter queue for invalid records  
20.8.10 Data quality in batch vs streaming pipelines  

## 20.9 Data Lineage and Governance
20.9.1 What is data lineage  
20.9.2 Data lineage types (column-level, table-level, end-to-end)  
20.9.3 Data lineage use cases (impact analysis, debugging, compliance)  
20.9.4 Data lineage collection (parsing SQL, scanning execution plans, instrumentation)  
20.9.5 Data governance components (metadata management, data catalog, access control)  
20.9.6 Data catalog (search, discovery, documentation, ownership)  
20.9.7 Data governance tools (Amundsen, DataHub, Marquez, OpenMetadata)  
20.9.8 Data classification (PII, sensitive, public, internal)  
20.9.9 GDPR compliance with data lineage and governance  
20.9.10 Data retention and deletion policies  

## 20.10 Slowly Changing Dimensions (SCD Type 1,2,3)
20.10.1 What are Slowly Changing Dimensions (SCD)  
20.10.2 SCD Type 1 (overwrite old values, no history kept)  
20.10.3 SCD Type 1 use cases (fix data errors, non-historical attributes)  
20.10.4 SCD Type 2 (add new row with effective dates, keep full history)  
20.10.5 SCD Type 2 columns (start_date, end_date, current_flag, version number)  
20.10.6 SCD Type 2 use cases (audit tracking, historical reporting)  
20.10.7 SCD Type 3 (add previous value column, limited history)  
20.10.8 SCD Type 3 use cases (track previous value only)  
20.10.9 SCD Type 0 (never change, fixed dimension)  
20.10.10 SCD selection criteria (business requirements, storage costs, query complexity)  

## 20.11 Event Time vs Processing Time
20.11.1 What is event time in data processing  
20.11.2 Event time definition (timestamp when event actually occurred)  
20.11.3 What is processing time in data processing  
20.11.4 Processing time definition (timestamp when event processed by system)  
20.11.5 Event time vs processing time differences (late data, out-of-order data)  
20.11.6 Challenges with event time processing (clock skew, late arrivals)  
20.11.7 Challenges with processing time (depends on system health, non-deterministic)  
20.11.8 Using event time in stream processing (Flink, Kafka Streams, Spark Structured Streaming)  
20.11.9 Out-of-order data handling (allowed lateness, watermarks)  
20.11.10 Selecting event time vs processing time for different use cases  

## 20.12 Windowing and Watermarks
20.12.1 What are windowing and watermarks in stream processing  
20.12.2 Tumbling window (fixed-size, non-overlapping, aligned)  
20.12.3 Hopping window (fixed-size, overlapping, can be unaligned)  
20.12.4 Sliding window (event-driven, based on event timestamps)  
20.12.5 Session window (activity-based, gap between events)  
20.12.6 What is watermark (progress indicator, all events before watermark processed)  
20.12.7 Watermark generation strategies (periodic, punctuated, idle sources)  
20.12.8 Allowed lateness (how late events are still accepted)  
20.12.9 Late event handling (update results, side output, drop)  
20.12.10 Windowing in Flink and Kafka Streams implementations  

## 20.13 Exactly-Once Processing Guarantees
20.13.1 What is exactly-once processing guarantee  
20.13.2 Exactly-once definition (each event processed exactly once, no duplicates, no data loss)  
20.13.3 At-least-once with idempotent sinks (achieves exactly-once effect)  
20.13.4 Transactional writes for exactly-once (commit only once, rollback failures)  
20.13.5 Exactly-once in Kafka (transactions, idempotent producers, consumer offsets as transaction)  
20.13.6 Exactly-once in Flink (checkpointing, two-phase commit sink)  
20.13.7 Exactly-once in Spark Structured Streaming (write-ahead logs, idempotent sinks)  
20.13.8 Exactly-once vs exactly-once effect (true exactly-once is rare)  
20.13.9 Exactly-once costs (throughput impact, latency increase, complexity)  
20.13.10 At-least-once vs at-most-once vs exactly-once trade-offs  















# 21. IDEMPOTENCY & RESILIENCE

## 21.1 Idempotent API Design Principles
21.1.1 What is idempotency in API design  
21.1.2 Idempotent operation definition (same result after multiple identical requests)  
21.1.3 HTTP idempotent methods (GET, PUT, DELETE) vs non-idempotent (POST)  
21.1.4 Natural idempotency in PUT (same resource, same data, same result)  
21.1.5 Natural idempotency in DELETE (already deleted, still success)  
21.1.6 POST non-idempotent problem (multiple submissions create multiple resources)  
21.1.7 Making POST idempotent using idempotency key  
21.1.8 State-based idempotency (check state before performing action)  
11.1.9 Functional idempotency (same mathematical function, same output)  
21.1.10 Idempotency in event-driven systems (message deduplication)  

## 21.2 Idempotency Keys and Storage
21.2.1 What are idempotency keys for API design  
21.2.2 Idempotency key definition (unique client-generated identifier per request)  
21.2.3 Idempotency key request header (Idempotency-Key, idempotency-key)  
21.2.4 Idempotency key format (UUID, client-side generated, deterministic)  
21.2.5 Server-side idempotency storage (store key + response on first request)  
21.2.6 Idempotency storage TTL (time to live, cleanup old keys)  
21.2.7 Idempotency key response (cache response for duplicate keys)  
21.2.8 Idempotency key collision handling (different requests same key)  
21.2.9 Idempotency storage options (Redis, database, distributed cache)  
21.2.10 Real-world implementations (Stripe, PayPal, Square idempotency keys)  

## 21.3 Retry with Exponential Backoff
21.3.1 What is exponential backoff for retries  
21.3.2 Simple retry problem (immediate retry on failure, worsens congestion)  
21.3.3 Exponential backoff formula (delay = base * (2 ^ attempt))  
21.3.4 Base delay selection (100ms, 1s, depends on service latency)  
21.3.5 Maximum delay cap (don't grow indefinitely, e.g., 30s or 60s)  
21.3.6 Maximum retry attempts (3-5 typical, prevents infinite retries)  
21.3.7 Exponential backoff example (100ms, 200ms, 400ms, 800ms, 1.6s)  
21.3.8 Exponential backoff for different failure types (transient vs permanent)  
21.3.9 Backoff reset on success (reset to base delay)  
21.3.10 Implementation in clients (AWS SDK, gRPC, custom retry policies)  

## 21.4 Retry Budgets (Per-Service, Per-Endpoint)
21.4.1 What is retry budget in distributed systems  
21.4.2 Retry budget definition (limit on total retries over time window)  
21.4.3 Retry budget per service (prevent retry storms from single client)  
21.4.4 Retry budget per endpoint (different limits for different APIs)  
21.4.5 Retry budget per client (client-specific limits, fair sharing)  
21.4.6 Retry budget replenishment (time-based or request-based)  
21.4.7 Retry budget exhaustion handling (fail fast, don't retry)  
21.4.8 Retry budget for downstream services (protect dependencies)  
21.4.9 Retry budget vs rate limiting differences  
21.4.10 Real-world retry budget implementations (Google, Netflix, Uber)  

## 21.5 Retry Amplification Prevention
21.5.1 What is retry amplification in distributed systems  
21.5.2 Retry amplification definition (one failure triggers many cascading retries)  
21.5.3 Retry amplification example (client retry × service retry × downstream retry)  
21.5.4 Retry amplification impact (load multiplier, system collapse)  
21.5.5 Prevention strategy (upper bound on retry attempts across layers)  
21.5.6 Prevention strategy (retry only at one layer, preferably client or edge)  
21.5.7 Prevention strategy (use circuit breakers to stop retry cascades)  
21.5.8 Prevention strategy (exponential backoff jitter, desynchronize retries)  
21.5.9 Prevention strategy (retry budget per client, per endpoint)  
21.5.10 Detection and monitoring of retry amplification (metrics, logging, traces)  

## 21.6 Deadlines and Timeouts at Each Layer
21.6.1 What are deadlines and timeouts in distributed systems  
21.6.2 Timeout vs deadline difference (relative vs absolute)  
21.6.3 Timeout per operation (maximum wait time for single request)  
21.6.4 Deadline per request chain (absolute timestamp, no exceeding)  
21.6.5 Connection timeout (time to establish TCP/TLS connection)  
21.6.6 Read timeout (time waiting for response after sending)  
21.6.7 Write timeout (time to send full request)  
21.6.8 Timeouts at each layer (client, load balancer, application, database)  
21.6.9 Stricter timeouts rule (each layer timeout < parent timeout)  
21.6.10 Context propagation for deadlines (gRPC deadline, HTTP timeout headers)  

## 21.7 Cascading Failure Prevention
21.7.1 What is cascading failure in distributed systems  
21.7.2 Cascading failure definition (one failure triggers chain of failures)  
21.7.3 Cascading failure example (database slow → app threads blocked → health check fail → instance removed)  
21.7.4 Cascading failure from resource exhaustion (thread pool, connection pool, memory)  
21.7.5 Circuit breaker pattern for cascading failure prevention  
21.7.6 Bulkhead pattern for resource isolation  
21.7.7 Timeout and deadline for resource release  
21.7.8 Load shedding and graceful degradation  
21.7.9 Retry budget for failure isolation  
21.7.10 Prevention through incremental deployment and canary analysis  

## 21.8 Retry Circuit Breakers
21.8.1 What is circuit breaker for retries  
21.8.2 Circuit breaker states (closed, open, half-open) for retries  
21.8.3 Retry circuit breaker closed state (retries allowed normally)  
21.8.4 Retry circuit breaker open state (skip retries, fail fast)  
21.8.5 Retry circuit breaker open trigger (error rate threshold, consecutive failures)  
21.8.6 Retry circuit breaker half-open state (probing for recovery)  
21.8.7 Retry circuit breaker vs retry budget integration  
21.8.8 Retry circuit breaker configuration (failure threshold, timeout, success threshold)  
21.8.9 Retry circuit breaker without request circuit breaker (separate concerns)  
21.8.10 Circuit breaker implementations (Resilience4j, Hystrix, Polly, Envoy)  

## 21.9 Retry with Jitter
21.9.1 What is jitter in retry strategies  
21.9.2 Jitter definition (adding randomness to retry intervals)  
21.9.3 Retry without jitter problem (thundering herd, synchronized retries)  
21.9.4 Full jitter (random between 0 and calculated backoff)  
21.9.5 Equal jitter (random between base and backoff value)  
21.9.6 Decorrelated jitter (random between base and previous_interval * 3)  
21.9.7 Full jitter vs equal jitter comparison (distribution, congestion avoidance)  
21.9.8 Jitter formula examples (max(0, random(0, backoff)))  
21.9.9 Jitter use cases (large-scale distributed systems, many clients)  
21.9.10 Jitter implementation in retry libraries (retry-jitter, exponential backoff with jitter)  

## 21.10 Transactional Outbox Pattern
21.10.1 What is transactional outbox pattern  
21.10.2 Transactional outbox problem (database write + message queue inconsistency)  
21.10.3 Transactional outbox solution (store message in database as part of transaction)  
21.10.4 Outbox table schema (id, aggregate_type, aggregate_id, event_type, payload, created_at, status)  
21.10.5 Message publisher (poll outbox table, publish to message broker)  
21.10.6 Outbox publisher idempotency (at-least-once delivery to broker)  
21.10.7 Outbox publisher offset tracking (last published ID, checkpoint)  
21.10.8 Outbox pattern with CDC (change data capture to message broker)  
21.10.9 Outbox pattern vs 2PC vs Saga for consistency  
21.10.10 Outbox pattern implementations (Debezium outbox, transactional outbox with Kafka)  

## 21.11 Message Deduplication
21.11.1 What is message deduplication in distributed systems  
21.11.2 Message duplication causes (retries, network issues, broker failures)  
21.11.3 At-least-once delivery requires deduplication for exactly-once effect  
21.11.4 Consumer-side deduplication using idempotency key  
21.11.5 Deduplication storage (Redis, database, in-memory cache with TTL)  
21.11.6 Deduplication key as message_id or event_id  
21.11.7 Deduplication TTL (time window for duplicate detection)  
21.11.8 Partition-based deduplication (dedupe within partition only)  
21.11.9 Deduplication limitations (state size, TTL trade-offs, high throughput)  
21.11.10 Deduplication implementations (Kafka Transactions, AWS SQS FIFO, Redis SETNX)  

## 21.12 At-Least-Once Delivery with Idempotent Processing
21.12.1 What is at-least-once delivery with idempotent processing  
21.12.2 At-least-once delivery definition (message delivered 1+ times, no loss)  
21.12.3 At-least-once delivery challenges (duplicates guaranteed)  
21.12.4 Idempotent processing definition (process same message multiple times safely)  
21.12.5 Idempotent processing + at-least-once = exactly-once effect  
21.12.6 Idempotent processing using business key (order_id, transaction_id)  
21.12.7 Idempotent processing using idempotency key in message  
21.12.8 Idempotent processing using state checks (check before apply)  
21.12.9 At-least-once sources (SQS standard, Kafka with retries, RabbitMQ with auto-ack off)  
21.12.10 Trade-offs (at-least-once simpler than exactly-once, requires idempotent consumers)  

## 21.13 Saga Compensating Transactions
21.13.1 What are Saga compensating transactions for resilience  
21.13.2 Saga definition (distributed transaction as sequence of local transactions)  
21.13.3 Compensating transaction definition (undo previous transaction)  
21.13.4 Saga compensation example (book hotel → book flight → cancel hotel if flight fails)  
21.13.5 Choreography-based Saga (event-driven, decentralized compensation)  
21.13.6 Orchestration-based Saga (central coordinator, explicit compensation)  
21.13.7 Forward recovery vs backward recovery (retry vs compensate)  
21.13.8 Idempotent compensating transactions (compensate once, safe to repeat)  
21.13.9 Compensation for non-idempotent operations (idempotency key required)  
21.13.10 Real-world Saga examples (order processing, travel booking, money transfer)  

## 21.14 Retry Storms and Coordinated Omission
21.14.1 What are retry storms and coordinated omission  
21.14.2 Retry storm definition (many clients retrying simultaneously causing overload)  
21.14.3 Retry storm causes (service degradation + client retry policy + synchronized retries)  
21.14.4 Coordinated omission definition (not measuring time spent in retry and queue)  
21.14.5 Coordinated omission problem (latency metrics look fine while users wait long)  
21.14.6 Retry storm prevention (jitter, retry budgets, circuit breakers)  
21.14.7 Retry storm prevention (client-side backpressure, randomized retries)  
21.14.8 Coordinated omission detection (end-to-end latency measurement including retries)  
21.14.9 Coordinated omission example (load test ignores retry time, reports false low latency)  
21.14.10 Real-world incidents (retry storms causing cascading failures in large outages)  



















# 22. REAL-TIME SYSTEMS

## 22.1 Low-Latency Requirements (<10ms, <100ms)
22.1.1 What are low-latency requirements in real-time systems  
22.1.2 Sub-10ms latency use cases (high-frequency trading, gaming input, VR/AR)  
22.1.3 Sub-100ms latency use cases (video calls, live sports, real-time collaboration)  
22.1.4 Sub-1 second latency use cases (chat messages, notifications, live dashboards)  
22.1.5 Tail latency importance (p99, p99.9 vs average latency)  
22.1.6 Latency budget allocation across system components  
22.1.7 Factors affecting latency (network RTT, GC pauses, queueing, context switching)  
22.1.8 Achieving sub-10ms (in-memory processing, no disk I/O, pre-warmed caches)  
22.1.9 Measuring and monitoring low latency (OpenTelemetry, eBPF, kernel bypass)  
22.1.10 Trade-offs for low latency (higher cost, reduced throughput, complexity)  

## 22.2 In-Memory Data Structures (Redis, Memcached)
22.2.1 What are in-memory data structures for real-time systems  
22.2.2 Redis data structures (strings, hashes, lists, sets, sorted sets, streams, hyperloglog)  
22.2.3 Redis sorted sets for leaderboards (ZADD, ZRANK, ZREVRANGE)  
22.2.4 Redis streams for message queuing (XADD, XREAD, consumer groups)  
22.2.5 Redis pub/sub for real-time messaging (publish, subscribe, pattern matching)  
22.2.6 Redis Lua scripting for atomic operations  
22.2.7 Memcached simple key-value (hash table, LRU eviction, no persistence)  
22.2.8 Memcached vs Redis performance comparison  
22.2.9 In-memory vs on-disk performance difference (microseconds vs milliseconds)  
22.2.10 Persistence options for in-memory stores (RDB snapshots, AOF logs)  

## 22.3 Polling vs WebSocket vs Server-Sent Events (SSE)
22.3.1 What are polling, WebSocket, and SSE for real-time communication  
22.3.2 Short polling (client repeatedly asks server for updates)  
22.3.3 Short polling overhead (many empty responses, high latency)  
22.3.4 Long polling (server holds connection until data available)  
22.3.5 WebSocket protocol (full-duplex, persistent, low overhead)  
22.3.6 WebSocket message types (text, binary, ping/pong, close)  
22.3.7 Server-Sent Events (SSE) (server to client only, HTTP-based)  
22.3.8 WebSocket vs SSE comparison (bi-directional vs one-way, protocol complexity)  
22.3.9 Polling vs WebSocket vs SSE selection criteria  
22.3.10 Scaling WebSocket connections (sticky sessions, shared pub/sub backend)  

## 22.4 Long Polling vs Streaming
22.4.1 What is long polling vs streaming in real-time systems  
22.4.2 Long polling mechanism (request, hold, respond, client re-requests)  
22.4.3 Long polling advantages (wide browser support, no new protocol)  
22.4.4 Long polling disadvantages (overhead of repeated requests, timeout management)  
22.4.5 HTTP/1.1 streaming (chunked transfer encoding, indefinite response)  
22.4.6 HTTP/2 streaming (multiplexed, server push, more efficient)  
22.4.7 Streaming advantages (single connection, real-time push, no polling overhead)  
22.4.8 Streaming disadvantages (connection management, reconnection logic)  
22.4.9 Long polling vs streaming vs WebSocket comparison table  
22.4.10 Use cases for each (chat: WebSocket, stock ticker: SSE, IoT: MQTT)  

## 22.5 Real-Time Analytics
22.5.1 What is real-time analytics in system design  
22.5.2 Real-time analytics definition (sub-second to sub-minute insights from streaming data)  
22.5.3 Real-time analytics vs batch analytics comparison  
22.5.4 Real-time analytics architecture (stream ingestion → processing → serving)  
22.5.5 Aggregation types (tumbling windows, sliding windows, session windows)  
22.5.6 Real-time dashboard requirements (sub-second refresh, high throughput)  
22.5.7 Pre-aggregation for low-latency queries (rollups, materialized views)  
22.5.8 Lambda architecture for real-time analytics (batch + stream)  
22.5.9 Use cases (fraud detection, operational dashboards, ad bidding)  
22.5.10 Real-time analytics platforms (Pinot, Druid, ClickHouse, Rockset)  

## 22.6 Real-Time Data Pipelines (Kafka, Flink)
22.6.1 What are real-time data pipelines  
22.6.2 Real-time pipeline components (source → stream processor → sink)  
22.6.3 Kafka as distributed streaming platform (topics, partitions, brokers)  
22.6.4 Kafka producer and consumer APIs (acks, batching, compression)  
22.6.5 Kafka exactly-once semantics (idempotent producers, transactions)  
22.6.6 Apache Flink for stream processing (event time, state, checkpointing)  
22.6.7 Flink operations (map, filter, flatMap, keyBy, window, aggregate)  
22.6.8 Flink exactly-once via checkpointing and two-phase commit  
22.6.9 Kafka Streams lightweight alternative (embedded library, no separate cluster)  
22.6.10 Real-time pipeline use cases (clickstream analysis, real-time ETL, anomaly detection)  

## 22.7 Time-Series Databases (InfluxDB, TimescaleDB)
22.7.1 What are time-series databases (TSDB) for real-time systems  
22.7.2 Time-series data characteristics (timestamped, append-only, high write throughput)  
22.7.3 InfluxDB architecture (TSM storage engine, retention policies, continuous queries)  
22.7.4 InfluxDB schema design (measurement, tags, fields, timestamp)  
22.7.5 InfluxQL and Flux query languages for time-series  
22.7.6 TimescaleDB as PostgreSQL extension (hybrid row-columnar, hypertables)  
22.7.7 TimescaleDB features (continuous aggregates, data retention, compression)  
22.7.8 TSDB vs relational database for time-series (write throughput, compression, query patterns)  
22.7.9 TSDB use cases (IoT sensor data, metrics monitoring, financial tick data)  
22.7.10 TSDB selection (InfluxDB vs TimescaleDB vs Prometheus vs ClickHouse)  

## 22.8 Event Sourcing & CQRS for Real-Time UIs
22.8.1 What is event sourcing and CQRS for real-time UIs  
22.8.2 Event sourcing as source of truth (immutable event log)  
22.8.3 Real-time UI requirements (instant updates, optimistic updates, conflict resolution)  
22.8.4 Projection from event store to read model for UI  
22.8.5 CQRS pattern for separate read and write models  
22.8.6 Real-time UI event sourcing example (collaborative document editing)  
22.8.7 Optimistic UI (update UI immediately, reconcile with server events)  
22.8.8 WebSocket for pushing event stream to UI  
22.8.9 Client-side event store for offline support and replay  
22.8.10 Use cases (real-time dashboards, collaborative apps, activity feeds)  

## 22.9 Soft-State vs Hard-State Real-Time Systems
22.9.1 What are soft-state and hard-state real-time systems  
22.9.2 Hard real-time definition (deadline must be met, failure is system failure)  
22.9.3 Hard real-time examples (airbag deployment, pacemakers, industrial control)  
22.9.4 Hard real-time requirements (deterministic scheduling, bounded operations)  
22.9.5 Soft real-time definition (deadline desirable but occasional miss acceptable)  
22.9.6 Soft real-time examples (video streaming, gaming, live dashboards)  
22.9.7 Firm real-time definition (late results have no value but not catastrophic)  
22.9.8 Real-time operating systems (RTOS) for hard real-time (VxWorks, QNX, FreeRTOS)  
22.9.9 Linux for soft real-time (PREEMPT_RT patch, CPU isolation, real-time scheduling)  
22.9.10 Soft vs hard vs firm real-time trade-offs (complexity, cost, determinism)  

## 22.10 Micro-Batching
22.10.1 What is micro-batching for real-time systems  
22.10.2 Micro-batching definition (batch small groups of events at very short intervals)  
22.10.3 Micro-batching vs pure streaming vs pure batch comparison  
22.10.4 Micro-batching advantages (batch optimizations, exactly-once easier)  
22.10.5 Micro-batching disadvantages (added latency from batch wait)  
22.10.6 Spark Streaming micro-batching (batch intervals 500ms to 5 seconds)  
22.10.7 Spark Structured Streaming (micro-batching with incremental execution)  
22.10.8 Micro-batch size tuning (lower latency with smaller batches)  
22.10.9 Micro-batching with compaction (combine small batches for efficiency)  
22.10.10 Use cases (clickstream analytics, log processing, metrics aggregation)  

















# 23. PRODUCTION OPERATIONS

## 23.1 Capacity Planning and Forecasting
23.1.1 What is capacity planning in production operations  
23.1.2 Historical trend analysis for resource usage prediction  
23.1.3 Leading indicators for capacity (user growth, feature adoption, traffic patterns)  
23.1.4 Seasonal capacity planning (holiday peaks, end-of-month, Black Friday)  
23.1.5 Cloud capacity planning (on-demand vs reserved instances vs spot)  
23.1.6 On-premise capacity planning (lead time for hardware procurement)  
23.1.7 Capacity buffer and safety margin recommendations  
23.1.8 Automated capacity forecasting tools  
23.1.9 Capacity review cadence (weekly, monthly, quarterly)  
23.1.10 Capacity planning dashboards and reporting  

## 23.2 Resource Optimization (Right-Sizing)
23.2.1 What is resource optimization (right-sizing) in production  
23.2.2 Over-provisioning waste (idle resources, unnecessary cost)  
23.2.3 Under-provisioning risks (performance degradation, outages)  
23.2.4 CPU right-sizing (utilization targets 40-60%, burst tolerance)  
23.2.5 Memory right-sizing (heap usage, cache hit rates, GC overhead)  
23.2.6 Storage right-sizing (IOPS, throughput, capacity tiers)  
23.2.7 Container resource optimization (requests, limits, actual usage)  
23.2.8 Rightsizing tools (AWS Compute Optimizer, CloudWatch, Prometheus metrics)  
23.2.9 Continuous rightsizing vs periodic review  
23.2.10 Right-sizing for auto-scaling groups (min/max based on historical peak)  

## 23.3 Cost Management (FinOps)
23.3.1 What is FinOps (Financial Operations) in cloud production  
23.3.2 FinOps principles (collaboration between finance, engineering, operations)  
23.3.3 Cloud cost allocation by team, service, environment (tagging strategy)  
23.3.4 Showback vs Chargeback models for cloud costs  
23.3.5 Budget setting and alerting for cloud spend  
23.3.6 Reserved Instance and Savings Plan optimization  
23.3.7 Spot instance usage for non-critical workloads  
23.3.8 Data transfer cost optimization (within AZ, cross AZ, cross region)  
23.3.9 Storage tiering (hot, cool, cold, archive) for cost savings  
23.3.10 FinOps tools (AWS Cost Explorer, CloudHealth, Vantage, Kubecost)  

## 23.4 Chaos Engineering in Production
23.4.1 What is chaos engineering in production operations  
23.4.2 Chaos engineering principles (experiment in production, minimize blast radius)  
23.4.3 Steady state hypothesis definition before chaos experiment  
23.4.4 Blast radius control (limit to single instance, AZ, percentage of traffic)  
23.4.5 Chaos experiment types (pod kill, latency injection, network partition, AZ failure)  
23.4.6 Chaos experiment automation (scheduled, event-triggered)  
23.4.7 Rollback and halt mechanisms for experiments  
23.4.8 Chaos engineering vs traditional testing differences  
23.4.9 Chaos engineering tools (Chaos Monkey, Gremlin, LitmusChaos, Chaos Mesh)  
23.4.10 Game Days (scheduled, announced chaos experiments for team training)  

## 23.5 Fault Injection Testing
23.5.1 What is fault injection testing in production  
23.5.2 Fault injection vs chaos engineering (targeted vs exploratory)  
23.5.3 Fault injection types (API errors, latency, resource exhaustion, network issues)  
23.5.4 Database fault injection (connection failures, replication lag, deadlocks)  
23.5.5 Network fault injection (packet loss, high latency, DNS failures)  
23.5.6 Service fault injection (throw exceptions, timeout, return error codes)  
23.5.7 Fault injection in CI/CD pipeline (pre-production testing)  
23.5.8 Fault injection safety (canary only, no production impact without controls)  
23.5.9 Fault injection tools (AWS Fault Injection Simulator, Chaos Mesh, Toxiproxy)  
23.5.10 Testing system resilience with fault injection scenarios  

## 23.6 Deployment Windows and Blackouts
23.6.1 What are deployment windows and blackouts  
23.6.2 Deployment window definition (authorized time period for changes)  
23.6.3 Traditional deployment windows (weekend, off-peak hours, maintenance windows)  
23.6.4 Deployment window challenges (slow recovery, limited testing, reduced velocity)  
23.6.5 Blackout period definition (no deployments allowed)  
23.6.6 Blackout period use cases (holidays, peak sales events, earnings releases)  
23.6.7 Modern continuous deployment with no blackouts (canary, blue-green)  
23.6.8 Automated rollback as alternative to blackouts  
23.6.9 Read-only periods for compliance (financial reporting periods)  
23.6.10 Balancing deployment velocity with risk during sensitive periods  

## 23.7 Migration Strategies
23.7.1 What are migration strategies in production operations  
23.7.2 Lift and shift (rehost) migration (move as-is to new infrastructure)  
23.7.3 Lift and shift advantages (fast, minimal changes, predictable)  
23.7.4 Lift and shift disadvantages (miss optimization, legacy baggage)  
23.7.5 Replatform migration (move with moderate optimizations)  
23.7.6 Refactor (re-architect) migration (significant changes, long timeline)  
23.7.7 Strangler fig pattern (gradual replacement of monolith)  
23.7.8 Phased migration (migrate user cohorts or traffic percentages)  
23.7.9 Parallel run (both old and new systems, compare outputs)  
23.7.10 Migration rollback planning and cutover strategies  

## 23.8 Blue-Green for Stateful Systems
23.8.1 What is blue-green deployment for stateful systems  
23.8.2 Stateful systems challenge (data cannot be duplicated like stateless)  
23.8.3 Database blue-green challenge (schema changes, data consistency)  
23.8.4 Blue-green with read replicas (promote replica to primary for green)  
23.8.5 Blue-green with dual-write pattern (write to both environments)  
23.8.6 Blue-green with logical replication (CDC from blue to green)  
23.8.7 Blue-green with data copy (copy data offline, cutover during low traffic)  
23.8.8 Blue-green with feature flags (enable new code paths gradually)  
23.8.9 Blue-green rollback for stateful (data reconciliation, revert schema)  
23.8.10 Stateful blue-green trade-offs (complexity, data consistency risk)  

## 23.9 Schema Migration at Scale
23.9.1 What is schema migration at scale in production  
23.9.2 Online schema migration tools (gh-ost, pt-online-schema-change)  
23.9.3 gh-ost architecture (shadow table, binlog replay, cut-over)  
23.9.4 Backward-compatible schema changes required for zero downtime  
23.9.5 Expand and contract pattern (add new, migrate, drop old)  
23.9.6 Adding nullable columns with defaults (non-breaking)  
23.9.7 Renaming columns (needs dual writes or app compatibility)  
23.9.8 Changing column types (usually breaking, need new column + backfill)  
23.9.9 Large table migration strategies (chunking, throttling, low-impact window)  
23.9.10 Schema migration rollback (revert app first, then schema)  

## 23.10 Data Backfill Pipelines
23.10.1 What are data backfill pipelines in production  
23.10.2 Backfill definition (populate missing or corrected data historically)  
23.10.3 Backfill triggers (schema change, bug fix, new feature, data correction)  
23.10.4 Batch backfill pipeline design (read old, transform, write new)  
23.10.5 Backfill job idempotency (safe to rerun, no duplicate data)  
23.10.6 Backfill throttling (rate limits, resource usage, database impact)  
23.10.7 Backfill checkpointing (track progress, resume from failure)  
23.10.8 Online backfill while serving live traffic  
23.10.9 Dual-read and dual-write during backfill for consistency  
23.10.10 Backfill validation and comparison of old vs new  

## 23.11 Feature Flags for Gradual Rollout
23.11.1 What are feature flags for gradual rollout in production  
23.11.2 Feature flag as conditional logic in code (if feature_enabled)  
23.11.3 Percentage-based rollout (x% of users get feature)  
23.11.4 User segment rollout (internal users, beta users, specific geographies)  
23.11.5 Canary release via feature flags (enable for small traffic, monitor, expand)  
23.11.6 Kill switch feature flag (emergency disable without redeploy)  
23.11.7 Feature flag evaluation latency (sub-millisecond, remote config)  
23.11.8 Feature flag storage (config file, database, remote service)  
23.11.9 Feature flag cleanup technical debt (remove old flags)  
23.11.10 Feature flag platforms (LaunchDarkly, Split.io, Flagsmith)  

## 23.12 Automated Rollback Triggers
23.12.1 What are automated rollback triggers in production  
23.12.2 Rollback trigger definition (automatic revert on negative conditions)  
23.12.3 Error rate trigger (5xx errors exceed threshold, e.g., >1% for 2 minutes)  
23.12.4 Latency trigger (p99 latency exceeds SLO, e.g., >500ms)  
23.12.5 SLO breach trigger (error budget consumption too fast)  
23.12.6 Health check failure trigger (critical health endpoints failing)  
23.12.7 Custom metric triggers (business KPIs, user engagement drops)  
23.12.8 Canary analysis with automatic rollback (compare canary vs baseline)  
23.12.9 Rollback trigger cooldown (prevent rollback loops)  
23.12.10 Rollback trigger tools (Argo Rollouts, Flagger, Spinnaker, custom)  

## 23.13 Safe Experiment (A/B Testing) Infrastructure
23.13.1 What is safe experiment infrastructure for production  
23.13.2 Experiment infrastructure components (assignment, metrics, analysis)  
23.13.3 User bucketing for experiments (consistent, deterministic, hash-based)  
23.13.4 Experiment sample size calculation (statistical significance)  
23.13.5 Experiment metrics (primary, guardrail, secondary)  
23.13.6 Real-time experiment monitoring (detect anomalies early)  
23.13.7 Experiment auto-stop on negative guardrail (user harm detection)  
23.13.8 Experiment ramp-up (1% → 5% → 25% → 50% → 100%)  
23.13.9 Experiment analysis (p-values, confidence intervals, Bayesian methods)  
23.13.10 Experiment platforms (Optimizely, LaunchDarkly, in-house)  

## 23.14 Production Readiness Review
23.14.1 What is production readiness review (PRR)  
23.14.2 PRR goals (identify risks, ensure operational maturity, prevent incidents)  
23.14.3 Observability checklist (metrics, logs, traces, dashboards, alerts)  
23.14.4 Scalability checklist (capacity planning, auto-scaling, load testing)  
23.14.5 Resilience checklist (retries, timeouts, circuit breakers, graceful degradation)  
23.14.6 Security checklist (auth, encryption, secrets, compliance)  
23.14.7 Deployment checklist (rollback, canary, feature flags)  
23.14.8 Documentation checklist (runbooks, architecture, on-call guides)  
23.14.9 PRR approval gates before production access  
23.14.10 PRR for new services vs major changes vs minor updates  

## 23.15 Operation Runbooks
23.15.1 What are operation runbooks in production  
23.15.2 Runbook definition (step-by-step procedure for common operations)  
23.15.3 Runbook types (incident response, deployment, backup/restore, scaling)  
23.15.4 Runbook format (title, severity, prerequisites, steps, verification, rollback)  
23.15.5 Incident runbook structure (detection, triage, mitigation, resolution)  
23.15.6 Runbook automation (scripts, playbooks, ChatOps commands)  
23.15.7 Runbook testing and validation (practice drills, tabletop exercises)  
23.15.8 Runbook version control and review process  
23.15.9 Runbook vs playbook vs checklist differences  
23.15.10 Runbook examples (database failover, certificate renewal, node replacement)  

## 23.16 On-Call Rotation and Incident Response
23.16.1 What is on-call rotation in production operations  
23.16.2 On-call rotation models (primary/secondary, follow-the-sun, weekday/weekend)  
23.16.3 On-call handoff process (shift change, status update, outstanding issues)  
23.16.4 On-call expectations (response time, escalation, secondary backup)  
23.16.5 Incident severity levels (SEV1 critical, SEV2 high, SEV3 medium, SEV4 low)  
23.16.6 Incident response roles (incident commander, operations lead, communications)  
23.16.7 Incident response timeline (acknowledge → engage → mitigate → resolve)  
23.16.8 On-call tools (PagerDuty, Opsgenie, xMatters)  
23.16.9 On-call load balancing and fairness  
23.16.10 On-call compensation and burnout prevention  

## 23.17 Post-Incident Review (Blameless)
23.17.1 What is blameless post-incident review  
23.17.2 Blameless culture principle (focus on system and process, not people)  
23.17.3 Post-incident review timing (within days, while details fresh)  
23.17.4 Post-incident attendees (responders, stakeholders, SREs, management)  
23.17.5 Post-incident structure (timeline, impact, root cause, action items)  
23.17.6 Root cause analysis techniques (5 Whys, fault tree analysis)  
23.17.7 Action item types (prevent recurrence, improve detection, reduce MTTR)  
23.17.8 Action item ownership and tracking (SLAs for completion)  
23.17.9 Post-incident review distribution (learnings across organization)  
23.17.10 Incident metrics tracking (MTTD, MTTA, MTTR, incident frequency)  









