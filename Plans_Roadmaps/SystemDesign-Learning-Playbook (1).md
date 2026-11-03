# System Design Learning Playbook

## Goal

Avoid forgetting concepts and build long-term system design intuition.

The objective is not to memorize definitions.

The objective is to:

- Recognize patterns
- Understand trade-offs
- Apply concepts to real systems
- Explain designs confidently during interviews

---

# Core Principle

System Design is not a knowledge problem.

It is a pattern recognition problem.

Most large-scale systems are combinations of a relatively small set of recurring patterns:

- Load Balancer
- Cache
- CDN
- Replication
- Sharding
- Message Queue
- Saga
- CQRS
- API Gateway
- Distributed Lock
- Circuit Breaker
- Rate Limiter

The goal is to recognize when each pattern should be applied.

---

# How To Learn Every Topic

## Step 1 – Learn
Understand:
- The problem
- The solution
- The trade-offs

## Step 2 – Draw
Create a simple diagram.

## Step 3 – Explain
Without notes, answer:
- What problem does this solve?
- Why does it exist?
- When should I use it?

## Step 4 – Relate To A Real System
Ask:
- How does Instagram use this?
- How does Netflix use this?
- How would an EHR system use this?

## Step 5 – Build (When Appropriate)
Build:
- Rate Limiter
- LRU Cache
- URL Shortener
- Pub/Sub
- Distributed Lock
- Outbox Pattern

---

# Note-Taking Template

## Topic Name

### Problem
What problem does this solve?

### Solution
One paragraph only.

### Diagram
Draw a simple architecture diagram.

### Trade-Offs

Pros:
- ...

Cons:
- ...

### Real-World Examples
- Netflix
- Amazon
- Instagram

### Interview Triggers
Mention this concept when discussing:
- ...
- ...

---

# Create A Pattern Library

| Pattern | Solves | Common Usage |
|----------|---------|-------------|
| Cache | Slow reads | High read traffic |
| CDN | Global latency | Media delivery |
| Replication | Read scaling | Read-heavy workloads |
| Sharding | Write scaling | Massive datasets |
| Queue | Async processing | Notifications |
| Saga | Distributed transactions | Microservices |
| Rate Limiter | Abuse protection | Public APIs |
| Circuit Breaker | Cascading failures | Distributed systems |
| CQRS | Read-heavy systems | Reporting systems |

---

# Create Architecture Case Studies

Maintain pages for:

1. URL Shortener
2. Chat Application
3. Instagram Feed
4. Notification System
5. Payment System
6. Inventory System
7. Appointment Scheduling System
8. Patient Management System
9. Uber Matching System
10. Multi-Tenant SaaS Platform

Continuously evolve them as you learn.

---

# Active Recall Strategy

Every Sunday:

Without looking at notes, explain:

- DNS
- Load Balancer
- Cache
- Replication
- Sharding
- Kafka
- Saga
- CAP Theorem

Anything you cannot explain becomes a revision topic.

---

# Weekly Review

Create a one-page summary of everything learned that week.

---

# Monthly Review

Create a one-page mind map showing how concepts connect.

---

# Architecture Thinking Habit

For every concept learned, answer:

How would this apply to healthcare systems?

Examples:

### Cache
- Provider lookup
- Patient demographics

### Replication
- Read-only patient searches
- Reporting systems

### Kafka
- Appointment notifications
- Audit events

### Saga
- Patient registration workflows
- Appointment booking workflows

---

# Recommended Study Ratio

- 30% Learning
- 20% Drawing Diagrams
- 20% Building Small POCs
- 30% Solving Design Problems

---

# Revision Schedule

## Same Day
- Learn topic
- Draw diagram

## Next Day
- Explain topic without notes

## End Of Week
- Review all topics

## End Of Month
- Create a one-page mind map

## Every Quarter
Re-design:
- URL Shortener
- Notification System
- Chat Application
- EHR System

---

# Success Metric

You are ready for system design interviews when you can:

- Explain concepts without notes
- Identify trade-offs quickly
- Estimate scale confidently
- Design systems on a blank whiteboard
- Defend architectural decisions
- Discuss bottlenecks and failure scenarios naturally
