# High-Level Design 

## 1. System Design Fundamentals

[1.1 What is High-Level Design (HLD)](hld-syllabus.md#11-what-is-high-level-design-hld)

[1.2 HLD vs LLD (Low-Level Design)](hld-syllabus.md#12-hld-vs-lld-low-level-design)

[1.3 Functional vs Non-Functional Requirements](hld-syllabus.md#13-functional-vs-non-functional-requirements)

[1.4 Capacity Estimation (QPS, Storage, Bandwidth)](hld-syllabus.md#14-capacity-estimation-qps-storage-bandwidth)

[1.5 Constraints and Assumptions](hld-syllabus.md#15-constraints-and-assumptions)

[1.6 Design Trade-offs Analysis](hld-syllabus.md#16-design-trade-offs-analysis)

[1.7 Stakeholder Communication](hld-syllabus.md#17-stakeholder-communication)

[1.8 Design Review Process](hld-syllabus.md#18-design-review-process)

## 2. Requirements Gathering

[2.1 Functional Requirements Elicitation](hld-syllabus.md#21-functional-requirements-elicitation)

[2.2 Non-Functional Requirements (Latency, Availability, Durability)](hld-syllabus.md#22-non-functional-requirements-latency-availability-durability)

[2.3 Scale and Growth Projections](hld-syllabus.md#23-scale-and-growth-projections)

[2.4 Security and Compliance Needs](hld-syllabus.md#24-security-and-compliance-needs)

[2.5 Operational Requirements (Monitoring, Debugging)](hld-syllabus.md#25-operational-requirements-monitoring-debugging)

[2.6 Cost Constraints and Budget](hld-syllabus.md#26-cost-constraints-and-budget)

[2.7 Time-to-Market Considerations](hld-syllabus.md#27-time-to-market-considerations)

[2.8 Technology Stack Constraints](hld-syllabus.md#28-technology-stack-constraints)

## 3. Capacity Planning

[3.1 Traffic Estimation (Daily Active Users, Peak QPS)](hld-syllabus.md#31-traffic-estimation-daily-active-users-peak-qps)

[3.2 Storage Estimation (Data Growth Rate, Retention Period)](hld-syllabus.md#32-storage-estimation-data-growth-rate-retention-period)

[3.3 Bandwidth Estimation (Ingress, Egress, Peak vs Average)](hld-syllabus.md#33-bandwidth-estimation-ingress-egress-peak-vs-average)

[3.4 Memory Estimation (Caching Layer Requirements)](hld-syllabus.md#34-memory-estimation-caching-layer-requirements)

[3.5 Compute Estimation (CPU Cores, Instance Sizing)](hld-syllabus.md#35-compute-estimation-cpu-cores-instance-sizing)

[3.6 Database Sizing (Rows, Indexes, Connections)](hld-syllabus.md#36-database-sizing-rows-indexes-connections)

[3.7 Network Capacity (Load Balancers, CDN, Regional Traffic)](hld-syllabus.md#37-network-capacity-load-balancers-cdn-regional-traffic)

[3.8 3-5 Year Growth Projections](hld-syllabus.md#38-3-5-year-growth-projections)

[3.9 Scaling Thresholds and Triggers](hld-syllabus.md#39-scaling-thresholds-and-triggers)

## 4. Database Design

[4.1 SQL vs NoSQL Selection Criteria](hld-syllabus.md#41-sql-vs-nosql-selection-criteria)

[4.2 Relational Databases (PostgreSQL, MySQL)](hld-syllabus.md#42-relational-databases-postgresql-mysql)

[4.3 Document Databases (MongoDB, DynamoDB, Firestore)](hld-syllabus.md#43-document-databases-mongodb-dynamodb-firestore)

[4.4 Key-Value Stores (Redis, Memcached, DynamoDB)](hld-syllabus.md#44-key-value-stores-redis-memcached-dynamodb)

[4.5 Wide-Column Stores (Cassandra, HBase, Bigtable)](hld-syllabus.md#45-wide-column-stores-cassandra-hbase-bigtable)

[4.6 Graph Databases (Neo4j, Amazon Neptune)](hld-syllabus.md#46-graph-databases-neo4j-amazon-neptune)

[4.7 Time-Series Databases (InfluxDB, Prometheus)](hld-syllabus.md#47-time-series-databases-influxdb-prometheus)

[4.8 Search Engines (Elasticsearch, OpenSearch)](hld-syllabus.md#48-search-engines-elasticsearch-opensearch)

[4.9 Sharding Strategies (Hash, Range, Directory-Based)](hld-syllabus.md#49-sharding-strategies-hash-range-directory-based)

[4.10 Partitioning vs Replication](hld-syllabus.md#410-partitioning-vs-replication)

[4.11 Indexing Strategies (Primary, Secondary, Composite, Covering)](hld-syllabus.md#411-indexing-strategies-primary-secondary-composite-covering)

[4.12 Denormalization Use Cases](hld-syllabus.md#412-denormalization-use-cases)

[4.13 Materialized Views](hld-syllabus.md#413-materialized-views)

[4.14 Database Migration Strategies (Zero-Downtime)](hld-syllabus.md#414-database-migration-strategies-zero-downtime)

[4.15 Multi-Region Database Replication](hld-syllabus.md#415-multi-region-database-replication)

[4.16 Database Connection Pooling](hld-syllabus.md#416-database-connection-pooling)

[4.17 Read Replicas for Read-Heavy Workloads](hld-syllabus.md#417-read-replicas-for-read-heavy-workloads)

## 5. API Design

[5.1 REST API Principles (Resources, Methods, Status Codes)](hld-syllabus.md#51-rest-api-principles-resources-methods-status-codes)

[5.2 GraphQL (Queries, Mutations, Subscriptions)](hld-syllabus.md#52-graphql-queries-mutations-subscriptions)

[5.3 gRPC (Protocol Buffers, Streaming, Performance)](hld-syllabus.md#53-grpc-protocol-buffers-streaming-performance)

[5.4 WebSocket (Bi-Directional Real-Time Communication)](hld-syllabus.md#54-websocket-bi-directional-real-time-communication)

[5.5 API Versioning Strategies (URI, Header, Content Negotiation)](hld-syllabus.md#55-api-versioning-strategies-uri-header-content-negotiation)

[5.6 API Pagination (Offset, Cursor, Keyset)](hld-syllabus.md#56-api-pagination-offset-cursor-keyset)

[5.7 API Filtering, Sorting, and Field Selection](hld-syllabus.md#57-api-filtering-sorting-and-field-selection)

[5.8 Rate Limiting (Fixed Window, Sliding Window, Token Bucket)](hld-syllabus.md#58-rate-limiting-fixed-window-sliding-window-token-bucket)

[5.9 Idempotency Keys for Safe Retries](hld-syllabus.md#59-idempotency-keys-for-safe-retries)

[5.10 API Authentication (API Keys, JWT, OAuth2)](hld-syllabus.md#510-api-authentication-api-keys-jwt-oauth2)

[5.11 API Documentation (OpenAPI, Postman)](hld-syllabus.md#511-api-documentation-openapi-postman)

[5.12 API Gateway vs Direct Exposure](hld-syllabus.md#512-api-gateway-vs-direct-exposure)

[5.13 Backward Compatibility Design](hld-syllabus.md#513-backward-compatibility-design)

## 6. Caching Strategies

[6.1 Cache Types (CDN, Client-Side, Server-Side, Database)](hld-syllabus.md#61-cache-types-cdn-client-side-server-side-database)

[6.2 Cache Patterns (Cache-Aside, Read-Through, Write-Through, Write-Behind)](hld-syllabus.md#62-cache-patterns-cache-aside-read-through-write-through-write-behind)

[6.3 Cache Eviction Policies (LRU, LFU, FIFO, TTL, Random)](hld-syllabus.md#63-cache-eviction-policies-lru-lfu-fifo-ttl-random)

[6.4 Cache Consistency Strategies (Eventual vs Strong)](hld-syllabus.md#64-cache-consistency-strategies-eventual-vs-strong)

[6.5 Cache Invalidation Techniques (Time-Based, Event-Based, Manual)](hld-syllabus.md#65-cache-invalidation-techniques-time-based-event-based-manual)

[6.6 Distributed Caching (Redis Cluster, Memcached)](hld-syllabus.md#66-distributed-caching-redis-cluster-memcached)

[6.7 Multi-Level Caching (L1 Local, L2 Distributed)](hld-syllabus.md#67-multi-level-caching-l1-local-l2-distributed)

[6.8 Cache Stampede Prevention](hld-syllabus.md#68-cache-stampede-prevention)

[6.9 Cache Warm-Up Strategies](hld-syllabus.md#69-cache-warm-up-strategies)

[6.10 Cache Sizing and Capacity Planning](hld-syllabus.md#610-cache-sizing-and-capacity-planning)

[6.11 CDN Caching for Static Assets](hld-syllabus.md#611-cdn-caching-for-static-assets)

[6.12 Browser Caching Headers](hld-syllabus.md#612-browser-caching-headers)

## 7. Load Balancing

[7.1 Layer 4 Load Balancing (IP and Port Level)](hld-syllabus.md#71-layer-4-load-balancing-ip-and-port-level)

[7.2 Layer 7 Load Balancing (HTTP/HTTPS Routing)](hld-syllabus.md#72-layer-7-load-balancing-httphttps-routing)

[7.3 Load Balancing Algorithms (Round-Robin, Least Connections, IP Hash)](hld-syllabus.md#73-load-balancing-algorithms-round-robin-least-connections-ip-hash)

[7.4 Weighted Load Balancing for Heterogeneous Servers](hld-syllabus.md#74-weighted-load-balancing-for-heterogeneous-servers)

[7.5 Health Checks (Active vs Passive)](hld-syllabus.md#75-health-checks-active-vs-passive)

[7.6 Session Persistence (Sticky Sessions) vs Stateless](hld-syllabus.md#76-session-persistence-sticky-sessions-vs-stateless)

[7.7 SSL/TLS Termination at Load Balancer](hld-syllabus.md#77-ssltls-termination-at-load-balancer)

[7.8 Global Load Balancing (GSLB, Route53)](hld-syllabus.md#78-global-load-balancing-gslb-route53)

[7.9 Load Balancer High Availability (Active-Passive, Active-Active)](hld-syllabus.md#79-load-balancer-high-availability-active-passive-active-active)

[7.10 Load Balancer vs Reverse Proxy vs API Gateway](hld-syllabus.md#710-load-balancer-vs-reverse-proxy-vs-api-gateway)

[7.11 Cloud Load Balancers (ALB, NLB, ELB, Cloud Load Balancing)](hld-syllabus.md#711-cloud-load-balancers-alb-nlb-elb-cloud-load-balancing)

## 8. Message Queues & Streaming

[8.1 Point-to-Point Messaging (Queues)](hld-syllabus.md#81-point-to-point-messaging-queues)

[8.2 Publish-Subscribe Messaging (Topics)](hld-syllabus.md#82-publish-subscribe-messaging-topics)

[8.3 Message Ordering Guarantees](hld-syllabus.md#83-message-ordering-guarantees)

[8.4 At-Least-Once, At-Most-Once, Exactly-Once Delivery](hld-syllabus.md#84-at-least-once-at-most-once-exactly-once-delivery)

[8.5 Dead Letter Queues](hld-syllabus.md#85-dead-letter-queues)

[8.6 Message Retention and TTL](hld-syllabus.md#86-message-retention-and-ttl)

[8.7 Competing Consumers Pattern](hld-syllabus.md#87-competing-consumers-pattern)

[8.8 Request-Reply Pattern](hld-syllabus.md#88-request-reply-pattern)

[8.9 Event Sourcing Architecture](hld-syllabus.md#89-event-sourcing-architecture)

[8.10 Change Data Capture (CDC)](hld-syllabus.md#810-change-data-capture-cdc)

[8.11 Message Brokers (Kafka, RabbitMQ, SQS, Pub/Sub)](hld-syllabus.md#811-message-brokers-kafka-rabbitmq-sqs-pubsub)

[8.12 Streaming vs Batch Processing](hld-syllabus.md#812-streaming-vs-batch-processing)

[8.13 Backpressure Handling](hld-syllabus.md#813-backpressure-handling)

[8.14 Message Partitioning and Rebalancing](hld-syllabus.md#814-message-partitioning-and-rebalancing)

## 9. Microservices Architecture

[9.1 Monolith vs Microservices Trade-offs](hld-syllabus.md#91-monolith-vs-microservices-trade-offs)

[9.2 Service Decomposition Strategies (By Business Capability, Subdomain)](hld-syllabus.md#92-service-decomposition-strategies-by-business-capability-subdomain)

[9.3 Database per Service Pattern](hld-syllabus.md#93-database-per-service-pattern)

[9.4 Saga Pattern for Distributed Transactions](hld-syllabus.md#94-saga-pattern-for-distributed-transactions)

[9.5 CQRS (Command Query Responsibility Segregation)](hld-syllabus.md#95-cqrs-command-query-responsibility-segregation)

[9.6 Event-Driven Architecture](hld-syllabus.md#96-event-driven-architecture)

[9.7 API Gateway Aggregation Pattern](hld-syllabus.md#97-api-gateway-aggregation-pattern)

[9.8 Backend for Frontend (BFF) Pattern](hld-syllabus.md#98-backend-for-frontend-bff-pattern)

[9.9 Service Mesh (Istio, Linkerd, Consul)](hld-syllabus.md#99-service-mesh-istio-linkerd-consul)

[9.10 Circuit Breaker Pattern (Netflix Hystrix)](hld-syllabus.md#910-circuit-breaker-pattern-netflix-hystrix)

[9.11 Retry and Timeout Policies](hld-syllabus.md#911-retry-and-timeout-policies)

[9.12 Bulkhead Pattern for Fault Isolation](hld-syllabus.md#912-bulkhead-pattern-for-fault-isolation)

[9.13 Sidecar Pattern](hld-syllabus.md#913-sidecar-pattern)

[9.14 Ambassador Pattern](hld-syllabus.md#914-ambassador-pattern)

[9.15 Service Discovery (Client-Side, Server-Side)](hld-syllabus.md#915-service-discovery-client-side-server-side)

[9.16 Distributed Tracing (Jaeger, Zipkin)](hld-syllabus.md#916-distributed-tracing-jaeger-zipkin)

[9.17 Service Versioning and Deprecation](hld-syllabus.md#917-service-versioning-and-deprecation)

## 10. Distributed Systems

[10.1 CAP Theorem (Consistency, Availability, Partition Tolerance)](hld-syllabus.md#101-cap-theorem-consistency-availability-partition-tolerance)

[10.2 PACELC Theorem](hld-syllabus.md#102-pacelc-theorem)

[10.3 Strong Consistency vs Eventual Consistency](hld-syllabus.md#103-strong-consistency-vs-eventual-consistency)

[10.4 Quorum-Based Consistency (W, R, N)](hld-syllabus.md#104-quorum-based-consistency-w-r-n)

[10.5 Leader Election Algorithms (Bully, Raft, Paxos)](hld-syllabus.md#105-leader-election-algorithms-bully-raft-paxos)

[10.6 Distributed Consensus (Raft, Paxos)](hld-syllabus.md#106-distributed-consensus-raft-paxos)

[10.7 Distributed Transactions (2PC, 3PC, Saga)](hld-syllabus.md#107-distributed-transactions-2pc-3pc-saga)

[10.8 Conflict-Free Replicated Data Types (CRDTs)](hld-syllabus.md#108-conflict-free-replicated-data-types-crdts)

[10.9 Vector Clocks for Ordering](hld-syllabus.md#109-vector-clocks-for-ordering)

[10.10 Gossip Protocol for Membership](hld-syllabus.md#1010-gossip-protocol-for-membership)

[10.11 Distributed Locking (Redlock, ZooKeeper, etcd)](hld-syllabus.md#1011-distributed-locking-redlock-zookeeper-etcd)

[10.12 Split-Brain Prevention](hld-syllabus.md#1012-split-brain-prevention)

[10.13 Clock Synchronization (NTP, Logical Clocks)](hld-syllabus.md#1013-clock-synchronization-ntp-logical-clocks)

[10.14 Idempotency in Distributed Systems](hld-syllabus.md#1014-idempotency-in-distributed-systems)

## 11. Data Replication & Sharding

[11.1 Replication Strategies (Single-Leader, Multi-Leader, Leaderless)](hld-syllabus.md#111-replication-strategies-single-leader-multi-leader-leaderless)

[11.2 Synchronous vs Asynchronous Replication](hld-syllabus.md#112-synchronous-vs-asynchronous-replication)

[11.3 Read-After-Write Consistency (Write Concerns)](hld-syllabus.md#113-read-after-write-consistency-write-concerns)

[11.4 Sharding Key Selection](hld-syllabus.md#114-sharding-key-selection)

[11.5 Consistent Hashing for Distributed Sharding](hld-syllabus.md#115-consistent-hashing-for-distributed-sharding)

[11.6 Range-Based vs Hash-Based Sharding](hld-syllabus.md#116-range-based-vs-hash-based-sharding)

[11.7 Directory-Based Sharding](hld-syllabus.md#117-directory-based-sharding)

[11.8 Shard Rebalancing Strategies](hld-syllabus.md#118-shard-rebalancing-strategies)

[11.9 Cross-Shard Queries and Joins](hld-syllabus.md#119-cross-shard-queries-and-joins)

[11.10 Global Secondary Indexes](hld-syllabus.md#1110-global-secondary-indexes)

[11.11 Hot Partition Mitigation](hld-syllabus.md#1111-hot-partition-mitigation)

[11.12 Shard Splitting and Merging](hld-syllabus.md#1112-shard-splitting-and-merging)

## 12. High Availability & Disaster Recovery

[12.1 Availability Metrics (9s: 99.9%, 99.99%, 99.999%)](hld-syllabus.md#121-availability-metrics-9s-999-9999-99999)

[12.2 Redundancy Patterns (Active-Passive, Active-Active)](hld-syllabus.md#122-redundancy-patterns-active-passive-active-active)

[12.3 Load Balancer HA Configuration](hld-syllabus.md#123-load-balancer-ha-configuration)

[12.4 Database HA (Failover, Replication, Cluster)](hld-syllabus.md#124-database-ha-failover-replication-cluster)

[12.5 Multi-AZ and Multi-Region Deployments](hld-syllabus.md#125-multi-az-and-multi-region-deployments)

[12.6 Zone-Aware Architecture](hld-syllabus.md#126-zone-aware-architecture)

[12.7 Disaster Recovery Tiers (RTO, RPO)](hld-syllabus.md#127-disaster-recovery-tiers-rto-rpo)

[12.8 Backup Strategies (Full, Incremental, Differential)](hld-syllabus.md#128-backup-strategies-full-incremental-differential)

[12.9 Warm Standby vs Hot Standby](hld-syllabus.md#129-warm-standby-vs-hot-standby)

[12.10 Pilot Light Disaster Recovery](hld-syllabus.md#1210-pilot-light-disaster-recovery)

[12.11 Chaos Engineering Practices](hld-syllabus.md#1211-chaos-engineering-practices)

[12.12 Health Checks and Auto-Healing](hld-syllabus.md#1212-health-checks-and-auto-healing)

[12.13 Graceful Degradation](hld-syllabus.md#1213-graceful-degradation)

[12.14 Rate Limiting and Load Shedding](hld-syllabus.md#1214-rate-limiting-and-load-shedding)

## 13. Security Design

[13.1 Authentication (Password, OAuth2, SSO, Biometric)](hld-syllabus.md#131-authentication-password-oauth2-sso-biometric)

[13.2 Authorization (RBAC, ABAC, ReBAC)](hld-syllabus.md#132-authorization-rbac-abac-rebac)

[13.3 Encryption at Rest (AES-256, Key Management)](hld-syllabus.md#133-encryption-at-rest-aes-256-key-management)

[13.4 Encryption in Transit (TLS 1.2+, mTLS)](hld-syllabus.md#134-encryption-in-transit-tls-12-mtls)

[13.5 API Security (Rate Limiting, CORS, Input Validation)](hld-syllabus.md#135-api-security-rate-limiting-cors-input-validation)

[13.6 Secrets Management (Vault, AWS Secrets Manager)](hld-syllabus.md#136-secrets-management-vault-aws-secrets-manager)

[13.7 DDoS Protection (Cloudflare, AWS Shield)](hld-syllabus.md#137-ddos-protection-cloudflare-aws-shield)

[13.8 Web Application Firewall (WAF)](hld-syllabus.md#138-web-application-firewall-waf)

[13.9 SQL Injection and XSS Prevention](hld-syllabus.md#139-sql-injection-and-xss-prevention)

[13.10 Compliance Requirements (GDPR, HIPAA, SOC2, PCI-DSS)](hld-syllabus.md#1310-compliance-requirements-gdpr-hipaa-soc2-pci-dss)

[13.11 Audit Logging](hld-syllabus.md#1311-audit-logging)

[13.12 Zero Trust Architecture](hld-syllabus.md#1312-zero-trust-architecture)

[13.13 Network Segmentation (VPC, Security Groups, NACLs)](hld-syllabus.md#1313-network-segmentation-vpc-security-groups-nacls)

[13.14 Threat Modeling (STRIDE Methodology)](hld-syllabus.md#1314-threat-modeling-stride-methodology)

[13.15 Penetration Testing Strategy](hld-syllabus.md#1315-penetration-testing-strategy)

[13.16 Incident Response Plan](hld-syllabus.md#1316-incident-response-plan)

## 14. Scalability Strategies

[14.1 Vertical Scaling (Scale Up)](hld-syllabus.md#141-vertical-scaling-scale-up)

[14.2 Horizontal Scaling (Scale Out)](hld-syllabus.md#142-horizontal-scaling-scale-out)

[14.3 Auto-Scaling Policies (CPU, Memory, Custom Metrics)](hld-syllabus.md#143-auto-scaling-policies-cpu-memory-custom-metrics)

[14.4 Stateless vs Stateful Scaling](hld-syllabus.md#144-stateless-vs-stateful-scaling)

[14.5 Database Read Replicas for Query Scaling](hld-syllabus.md#145-database-read-replicas-for-query-scaling)

[14.6 Connection Pooling for Scale](hld-syllabus.md#146-connection-pooling-for-scale)

[14.7 Function-as-a-Service (Serverless) Scaling](hld-syllabus.md#147-function-as-a-service-serverless-scaling)

[14.8 Asynchronous Processing for Scale](hld-syllabus.md#148-asynchronous-processing-for-scale)

[14.9 Event-Driven Scaling](hld-syllabus.md#149-event-driven-scaling)

[14.10 Caching for Read Scale](hld-syllabus.md#1410-caching-for-read-scale)

[14.12 Data Partitioning for Scale](hld-syllabus.md#1412-data-partitioning-for-scale)

[14.13 Microservice Granularity for Independent Scaling](hld-syllabus.md#1413-microservice-granularity-for-independent-scaling)

## 15. Performance Optimization

[15.1 Latency vs Throughput Trade-offs](hld-syllabus.md#151-latency-vs-throughput-trade-offs)

[15.2 Indexing for Query Performance](hld-syllabus.md#152-indexing-for-query-performance)

[15.3 Query Optimization and Execution Plans](hld-syllabus.md#153-query-optimization-and-execution-plans)

[15.4 Connection Pooling Optimization](hld-syllabus.md#154-connection-pooling-optimization)

[15.5 Pagination and Lazy Loading](hld-syllabus.md#155-pagination-and-lazy-loading)

[15.6 Database Query Batching](hld-syllabus.md#156-database-query-batching)

[15.7 Pre-computation and Materialized Views](hld-syllabus.md#157-pre-computation-and-materialized-views)

[15.8 Asynchronous Processing Patterns](hld-syllabus.md#158-asynchronous-processing-patterns)

[15.9 Data Compression for Storage and Network](hld-syllabus.md#159-data-compression-for-storage-and-network)

[15.10 Response Compression (Gzip, Brotli)](hld-syllabus.md#1510-response-compression-gzip-brotli)

[15.11 Asset Optimization (Minification, Bundling, CDN)](hld-syllabus.md#1511-asset-optimization-minification-bundling-cdn)

[15.12 HTTP/2 and HTTP/3 Benefits](hld-syllabus.md#1512-http2-and-http3-benefits)

[15.13 Performance Testing (Load, Stress, Soak, Spike)](hld-syllabus.md#1513-performance-testing-load-stress-soak-spike)

[15.14 Performance Baselining and Regression Detection](hld-syllabus.md#1514-performance-baselining-and-regression-detection)

[15.15 Lazy vs Eager Loading Strategies](hld-syllabus.md#1515-lazy-vs-eager-loading-strategies)

## 16. Monitoring & Observability

[16.1 Metrics (Counters, Gauges, Histograms, Summaries)](hld-syllabus.md#161-metrics-counters-gauges-histograms-summaries)

[16.2 Logging (Structured Logs, Log Levels, Aggregation)](hld-syllabus.md#162-logging-structured-logs-log-levels-aggregation)

[16.3 Distributed Tracing (Spans, Traces, Context Propagation)](hld-syllabus.md#163-distributed-tracing-spans-traces-context-propagation)

[16.4 SLI (Service Level Indicators) Definition](hld-syllabus.md#164-sli-service-level-indicators-definition)

[16.5 SLO (Service Level Objectives) Setting](hld-syllabus.md#165-slo-service-level-objectives-setting)

[16.6 SLA (Service Level Agreements) Compliance](hld-syllabus.md#166-sla-service-level-agreements-compliance)

[16.7 Error Budgets](hld-syllabus.md#167-error-budgets)

[16.8 Alerting Rules (Severity, Thresholds, Deduplication)](hld-syllabus.md#168-alerting-rules-severity-thresholds-deduplication)

[16.9 Dashboards for System Health](hld-syllabus.md#169-dashboards-for-system-health)

[16.10 Anomaly Detection](hld-syllabus.md#1610-anomaly-detection)

[16.11 Capacity Forecasting](hld-syllabus.md#1611-capacity-forecasting)

[16.12 Performance Profiling](hld-syllabus.md#1612-performance-profiling)

[16.13 Black-Box vs White-Box Monitoring](hld-syllabus.md#1613-black-box-vs-white-box-monitoring)

[16.14 On-Call and Incident Response](hld-syllabus.md#1614-on-call-and-incident-response)

[16.15 Post-Mortem and Root Cause Analysis](hld-syllabus.md#1615-post-mortem-and-root-cause-analysis)

[16.16 Monitoring Tools (Prometheus, Grafana, Datadog, New Relic)](hld-syllabus.md#1616-monitoring-tools-prometheus-grafana-datadog-new-relic)

## 17. Deployment Strategies

[17.1 Blue-Green Deployment](hld-syllabus.md#171-blue-green-deployment)

[17.2 Canary Deployment](hld-syllabus.md#172-canary-deployment)

[17.3 Rolling Deployment](hld-syllabus.md#173-rolling-deployment)

[17.4 Feature Flags / Toggles](hld-syllabus.md#174-feature-flags--toggles)

[17.5 A/B Testing Infrastructure](hld-syllabus.md#175-ab-testing-infrastructure)

[17.6 Dark Launches](hld-syllabus.md#176-dark-launches)

[17.7 Continuous Integration (CI) Pipeline](hld-syllabus.md#177-continuous-integration-ci-pipeline)

[17.8 Continuous Delivery (CD) Pipeline](hld-syllabus.md#178-continuous-delivery-cd-pipeline)

[17.9 Infrastructure as Code (Terraform, CloudFormation)](hld-syllabus.md#179-infrastructure-as-code-terraform-cloudformation)

[17.10 Configuration Management](hld-syllabus.md#1710-configuration-management)

[17.11 Container Orchestration (Kubernetes, ECS, Nomad)](hld-syllabus.md#1711-container-orchestration-kubernetes-ecs-nomad)

[17.12 Immutable Infrastructure](hld-syllabus.md#1712-immutable-infrastructure)

[17.13 Zero-Downtime Migrations (Schema Changes, Data Migrations)](hld-syllabus.md#1713-zero-downtime-migrations-schema-changes-data-migrations)

[17.14 Rollback and Revert Strategies](hld-syllabus.md#1714-rollback-and-revert-strategies)

## 18. Trade-off Analysis

[18.1 Consistency vs Availability](hld-syllabus.md#181-consistency-vs-availability)

[18.2 Latency vs Throughput](hld-syllabus.md#182-latency-vs-throughput)

[18.3 Read Optimization vs Write Optimization](hld-syllabus.md#183-read-optimization-vs-write-optimization)

[18.4 Normalization vs Denormalization](hld-syllabus.md#184-normalization-vs-denormalization)

[18.5 Batch vs Real-Time Processing](hld-syllabus.md#185-batch-vs-real-time-processing)

[18.6 Monolith vs Microservices Trade-offs](hld-syllabus.md#186-monolith-vs-microservices-trade-offs)

[18.7 SQL vs NoSQL for Specific Use Cases](hld-syllabus.md#187-sql-vs-nosql-for-specific-use-cases)

[18.8 Cloud vs On-Premise Decision](hld-syllabus.md#188-cloud-vs-on-premise-decision)

[18.9 Build vs Buy Decision Matrix](hld-syllabus.md#189-build-vs-buy-decision-matrix)

[18.10 Cost vs Performance Optimization](hld-syllabus.md#1810-cost-vs-performance-optimization)

[18.11 Time-to-Market vs Technical Debt](hld-syllabus.md#1811-time-to-market-vs-technical-debt)

[18.12 Vendor Lock-in vs Standardization](hld-syllabus.md#1812-vendor-lock-in-vs-standardization)

## 19. System Design Case Studies

[19.1 URL Shortener (TinyURL, bit.ly)](hld-syllabus.md#191-url-shortener-tinyurl-bitly)

[19.2 Chat System (WhatsApp, Slack, Discord)](hld-syllabus.md#192-chat-system-whatsapp-slack-discord)

[19.3 Video Streaming Platform (YouTube, Netflix, Twitch)](hld-syllabus.md#193-video-streaming-platform-youtube-netflix-twitch)

[19.4 Social Media Feed (Twitter, Instagram, Facebook)](hld-syllabus.md#194-social-media-feed-twitter-instagram-facebook)

[19.5 E-Commerce Platform (Amazon, Shopify)](hld-syllabus.md#195-e-commerce-platform-amazon-shopify)

[19.6 Ride-Sharing (Uber, Lyft)](hld-syllabus.md#196-ride-sharing-uber-lyft)

[19.7 Online Food Delivery (DoorDash, Zomato)](hld-syllabus.md#197-online-food-delivery-doordash-zomato)

[19.8 Payment System (Stripe, PayPal)](hld-syllabus.md#198-payment-system-stripe-paypal)

[19.9 Collaborative Document Editing (Google Docs)](hld-syllabus.md#199-collaborative-document-editing-google-docs)

[19.10 Real-Time Leaderboard (Gaming, Analytics)](hld-syllabus.md#1910-real-time-leaderboard-gaming-analytics)

[19.11 Key-Value Store (Redis, DynamoDB Design)](hld-syllabus.md#1911-key-value-store-redis-dynamodb-design)

[19.12 Rate Limiter (Distributed Token Bucket)](hld-syllabus.md#1912-rate-limiter-distributed-token-bucket)

[19.13 Proximity Service (Yelp, Google Maps Nearby Places)](hld-syllabus.md#1913-proximity-service-yelp-google-maps-nearby-places)

[19.14 Notification System (Push, Email, SMS)](hld-syllabus.md#1914-notification-system-push-email-sms)

[19.15 Web Crawler (Google Search)](hld-syllabus.md#1915-web-crawler-google-search)

[19.16 File Storage System (Dropbox, Google Drive)](hld-syllabus.md#1916-file-storage-system-dropbox-google-drive)

[19.17 Job Queue System](hld-syllabus.md#1917-job-queue-system)

[19.18 Metrics Aggregation System](hld-syllabus.md#1918-metrics-aggregation-system)

[19.19 Search Autocomplete (Typeahead)](hld-syllabus.md#1919-search-autocomplete-typeahead)

[19.20 Distributed ID Generator (Snowflake)](hld-syllabus.md#1920-distributed-id-generator-snowflake)

[19.21 Digital Wallet (Venmo, Google Pay)](hld-syllabus.md#1921-digital-wallet-venmo-google-pay)

[19.22 Task Scheduler (Distributed Cron)](hld-syllabus.md#1922-task-scheduler-distributed-cron)

[19.23 Online Stock Trading (Robinhood)](hld-syllabus.md#1923-online-stock-trading-robinhood)

## 20. Data Pipelines

[20.1 ETL vs ELT Patterns](hld-syllabus.md#201-etl-vs-elt-patterns)

[20.2 Batch Data Processing (Spark, Hadoop)](hld-syllabus.md#202-batch-data-processing-spark-hadoop)

[20.3 Stream Data Processing (Flink, Kafka Streams)](hld-syllabus.md#203-stream-data-processing-flink-kafka-streams)

[20.4 Lambda Architecture (Batch + Stream)](hld-syllabus.md#204-lambda-architecture-batch--stream)

[20.5 Kappa Architecture (Stream-Only)](hld-syllabus.md#205-kappa-architecture-stream-only)

[20.6 Data Lake and Data Warehouse](hld-syllabus.md#206-data-lake-and-data-warehouse)

[20.7 Schema Registry and Evolution](hld-syllabus.md#207-schema-registry-and-evolution)

[20.8 Data Quality and Validation](hld-syllabus.md#208-data-quality-and-validation)

[20.9 Data Lineage and Governance](hld-syllabus.md#209-data-lineage-and-governance)

[20.10 Slowly Changing Dimensions (SCD Type 1,2,3)](hld-syllabus.md#2010-slowly-changing-dimensions-scd-type-123)

[20.11 Event Time vs Processing Time](hld-syllabus.md#2011-event-time-vs-processing-time)

[20.12 Windowing and Watermarks](hld-syllabus.md#2012-windowing-and-watermarks)

[20.13 Exactly-Once Processing Guarantees](hld-syllabus.md#2013-exactly-once-processing-guarantees)

## 21. Idempotency & Resilience

[21.1 Idempotent API Design Principles](hld-syllabus.md#211-idempotent-api-design-principles)

[21.2 Idempotency Keys and Storage](hld-syllabus.md#212-idempotency-keys-and-storage)

[21.3 Retry with Exponential Backoff](hld-syllabus.md#213-retry-with-exponential-backoff)

[21.4 Retry Budgets (Per-Service, Per-Endpoint)](hld-syllabus.md#214-retry-budgets-per-service-per-endpoint)

[21.5 Retry Amplification Prevention](hld-syllabus.md#215-retry-amplification-prevention)

[21.6 Deadlines and Timeouts at Each Layer](hld-syllabus.md#216-deadlines-and-timeouts-at-each-layer)

[21.7 Cascading Failure Prevention](hld-syllabus.md#217-cascading-failure-prevention)

[21.8 Retry Circuit Breakers](hld-syllabus.md#218-retry-circuit-breakers)

[21.9 Retry with Jitter](hld-syllabus.md#219-retry-with-jitter)

[21.10 Transactional Outbox Pattern](hld-syllabus.md#2110-transactional-outbox-pattern)

[21.11 Message Deduplication](hld-syllabus.md#2111-message-deduplication)

[21.12 At-Least-Once Delivery with Idempotent Processing](hld-syllabus.md#2112-at-least-once-delivery-with-idempotent-processing)

[21.13 Saga Compensating Transactions](hld-syllabus.md#2113-saga-compensating-transactions)

[21.14 Retry Storms and Coordinated Omission](hld-syllabus.md#2114-retry-storms-and-coordinated-omission)

## 22. Real-Time Systems

[22.1 Low-Latency Requirements (<10ms, <100ms)](hld-syllabus.md#221-low-latency-requirements-10ms-100ms)

[22.2 In-Memory Data Structures (Redis, Memcached)](hld-syllabus.md#222-in-memory-data-structures-redis-memcached)

[22.3 Polling vs WebSocket vs Server-Sent Events (SSE)](hld-syllabus.md#223-polling-vs-websocket-vs-server-sent-events-sse)

[22.4 Long Polling vs Streaming](hld-syllabus.md#224-long-polling-vs-streaming)

[22.5 Real-Time Analytics](hld-syllabus.md#225-real-time-analytics)

[22.6 Real-Time Data Pipelines (Kafka, Flink)](hld-syllabus.md#226-real-time-data-pipelines-kafka-flink)

[22.7 Time-Series Databases (InfluxDB, TimescaleDB)](hld-syllabus.md#227-time-series-databases-influxdb-timescaledb)

[22.8 Event Sourcing & CQRS for Real-Time UIs](hld-syllabus.md#228-event-sourcing--cqrs-for-real-time-uis)

[22.9 Soft-State vs Hard-State Real-Time Systems](hld-syllabus.md#229-soft-state-vs-hard-state-real-time-systems)

[22.10 Micro-Batching](hld-syllabus.md#2210-micro-batching)

## 23. Production Operations

[23.1 Capacity Planning and Forecasting](hld-syllabus.md#231-capacity-planning-and-forecasting)

[23.2 Resource Optimization (Right-Sizing)](hld-syllabus.md#232-resource-optimization-right-sizing)

[23.3 Cost Management (FinOps)](hld-syllabus.md#233-cost-management-finops)

[23.4 Chaos Engineering in Production](hld-syllabus.md#234-chaos-engineering-in-production)

[23.5 Fault Injection Testing](hld-syllabus.md#235-fault-injection-testing)

[23.6 Deployment Windows and Blackouts](hld-syllabus.md#236-deployment-windows-and-blackouts)

[23.7 Migration Strategies](hld-syllabus.md#237-migration-strategies)

[23.8 Blue-Green for Stateful Systems](hld-syllabus.md#238-blue-green-for-stateful-systems)

[23.9 Schema Migration at Scale](hld-syllabus.md#239-schema-migration-at-scale)

[23.10 Data Backfill Pipelines](hld-syllabus.md#2310-data-backfill-pipelines)

[23.11 Feature Flags for Gradual Rollout](hld-syllabus.md#2311-feature-flags-for-gradual-rollout)

[23.12 Automated Rollback Triggers](hld-syllabus.md#2312-automated-rollback-triggers)

[23.13 Safe Experiment (A/B Testing) Infrastructure](hld-syllabus.md#2313-safe-experiment-ab-testing-infrastructure)

[23.14 Production Readiness Review](hld-syllabus.md#2314-production-readiness-review)

[23.15 Operation Runbooks](hld-syllabus.md#2315-operation-runbooks)

[23.16 On-Call Rotation and Incident Response](hld-syllabus.md#2316-on-call-rotation-and-incident-response)

[23.17 Post-Incident Review (Blameless)](hld-syllabus.md#2317-post-incident-review-blameless)
