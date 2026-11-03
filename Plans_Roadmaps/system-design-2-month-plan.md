# System Design in 2 Months — Beginner to Interview-Ready

Same core philosophy as the 1-month plan, but with room to actually absorb concepts instead of racing through them, plus more topics and roughly double the practice problems. ~1-1.5 hrs/day is enough at this pace.

---

## Month 1 — Foundations + Data Layer (was crammed into 2 weeks, now gets 4)

### Week 1 — Networking & Core Building Blocks
| Day | Topic |
|---|---|
| 1 | Client-server model, DNS resolution, HTTP request/response lifecycle |
| 2 | TCP vs UDP, what a "connection" actually is, HTTPS/TLS basics |
| 3 | Latency vs Throughput, tail latency (p50/p95/p99) |
| 4 | Availability math (99.9% vs 99.99%), SLAs vs SLOs vs SLIs |
| 5 | Vertical vs Horizontal scaling, statelessness |
| 6-7 | Review, write your own one-page summary of the week (no copying notes) |

### Week 2 — Load Balancing & Caching (deeper than the 1-month version)
| Day | Topic |
|---|---|
| 8 | Load balancer types: L4 vs L7 |
| 9 | LB algorithms: round robin, least connections, weighted, consistent hashing |
| 10 | Health checks, failover, sticky sessions |
| 11 | Caching strategies: cache-aside, write-through, write-behind |
| 12 | Cache eviction (LRU/LFU), TTL, cache stampede problem + solutions |
| 13 | CDNs: push vs pull, edge caching, when a CDN doesn't help |
| 14 | Review — diagram a full request path with LB + cache for a system you use daily |

### Week 3 — Databases Part 1
| Day | Topic |
|---|---|
| 15 | SQL vs NoSQL — when each fits, ACID vs BASE |
| 16 | Indexing — B-trees, why reads speed up but writes slow down |
| 17 | Composite indexes, covering indexes, query planning basics |
| 18 | Normalization vs denormalization |
| 19 | NoSQL types: key-value, document, column-family, graph — pick the right one per use case |
| 20-21 | Review — design a schema for a simple app (e.g. a blogging platform) both ways |

### Week 4 — Databases Part 2 (Distributed Data)
| Day | Topic |
|---|---|
| 22 | Replication: leader-follower, sync vs async, replication lag |
| 23 | Sharding: range-based, hash-based, hot shard problem |
| 24 | Consistent hashing — build the concept from scratch, understand virtual nodes |
| 25 | CAP theorem, PACELC, strong vs eventual consistency |
| 26 | Transactions: ACID deep dive, 2-phase commit, saga pattern |
| 27-28 | **Checkpoint project:** design a simple distributed key-value store on paper — sharding strategy, replication, consistency tradeoffs. Explain it out loud, no notes. |

---

## Month 2 — Distributed Systems, Architecture, and Heavy Practice

### Week 5 — Messaging, APIs, and Service Design
| Day | Topic |
|---|---|
| 29 | Message queues & pub/sub (Kafka/RabbitMQ-style), delivery guarantees |
| 30 | Backpressure, dead-letter queues, event-driven architecture |
| 31 | Microservices vs monoliths — real tradeoffs, service boundaries |
| 32 | API design: REST vs gRPC vs GraphQL, idempotency, pagination |
| 33 | Rate limiting: token bucket, leaky bucket, sliding window — implement one |
| 34-35 | Review — design the messaging flow for a notification system |

### Week 6 — Reliability & Scale Patterns
| Day | Topic |
|---|---|
| 36 | Fault tolerance: circuit breakers, retries with backoff, timeouts |
| 37 | Redundancy, graceful degradation, single points of failure |
| 38 | Geo-distribution: multi-region design, data locality, latency tradeoffs |
| 39 | Search & indexing at scale (inverted indexes, Elasticsearch-style systems) |
| 40 | Monitoring & observability: metrics, logging, tracing, alerting basics |
| 41-42 | Review + mock explain of the full stack top to bottom |

### Week 7 — Interview Practice Round 1
Use the framework every time:
1. **Clarify requirements** — functional + non-functional, ask about scale
2. **Back-of-envelope estimation** — QPS, storage, bandwidth
3. **High-level design** — boxes first, keep it simple
4. **Deep dive** — pick 1-2 components, go deep
5. **Bottlenecks & tradeoffs** — what breaks at 10x scale

| Day | Practice Problem |
|---|---|
| 43 | URL Shortener |
| 44 | Rate Limiter (implement the algorithm live) |
| 45 | Design Twitter/X feed (fan-out on write vs read) |
| 46 | Design a Chat App (WhatsApp) — delivery guarantees, ordering |
| 47 | Design Instagram/YouTube — media storage, CDN, feed gen |
| 48-49 | Review your own solutions against reference designs, note gaps |

### Week 8 — Interview Practice Round 2 + Mocks
| Day | Practice Problem |
|---|---|
| 50 | Design Uber/Lyft — geo-indexing, matching algorithm |
| 51 | Design an E-commerce checkout/inventory system |
| 52 | Design a Web Crawler |
| 53 | Design a Distributed Cache (like Redis/Memcached) |
| 54 | Design a Notification System (push/email/SMS at scale) |
| 55-60 | **Mock interviews** — record yourself or practice with a peer, 40 min each, no notes. Do at least 5-6 of these in the final week. |

---

## How to Practice Each Problem (every time, no exceptions)
- 35-45 min timer, no notes, talk out loud the whole time.
- State assumptions and numbers before you start drawing.
- After each one, compare to a reference solution and write down specifically what you missed — usually it's non-functional requirements or one bottleneck, not "the whole design."

## Resources Worth Using
- **Book:** *Designing Data-Intensive Applications* (Kleppmann) — with 2 months, actually read most of it, not just skim. It's the single best conceptual foundation available.
- **Free:** "System Design Primer" (GitHub repo) for Weeks 1-6 reference.
- **Practice:** ByteByteGo's YouTube channel for visual walkthroughs of Week 7-8 problems.

## Why This Pacing Works Better Than Cramming
The extra month goes almost entirely into: (1) letting concepts like consistent hashing and CAP theorem actually sink in instead of being memorized, and (2) doubling your practice problem count and mock interview reps. In interviews, the failure mode is rarely "didn't know a term" — it's "couldn't reason under pressure" or "forgot to ask about scale before designing." That's a practice problem, not a knowledge problem, which is why Weeks 7-8 matter as much as the other six combined.
