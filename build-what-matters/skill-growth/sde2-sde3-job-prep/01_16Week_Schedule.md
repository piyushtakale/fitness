# 16-Week Detailed Schedule

## Weekly Rhythm

| Day | Main Focus | Time | Secondary Activity |
|-----|-----------|------|-------------------|
| Monday | DSA Practice | 3-4 hrs | — |
| Tuesday | Swiggy Project | 3-4 hrs | — |
| Wednesday | HLD / System Design | 3-4 hrs | Job applications (30 min after Week 4) |
| Thursday | LLD or Machine Coding | 3-4 hrs | — |
| Friday | AI / Agentic Development | 2.5-3 hrs | Job applications/profile (30 min after Week 4) |
| Saturday | Deep Work: Project or Hard DSA | 4-6 hrs | Job applications (30 min after Week 4) |
| Sunday | Review, Behavioral, Weekly Planning | 3-4 hrs | Job applications (30 min after Week 4) |

**Job-search rule after Week 4:** Check alerts every day (5-10 min), apply/tailor/profile work on alternate dates for ~30 min. Never wait for a weekly "job-search day."

---

# Phase 1: Foundation (Weeks 1-4)

## Week 1: Setup and Arrays

**Weekly goal:** Establish your environment, start Array DSA, define the Swiggy/Zepto MVP, and learn HLD/LLD basics.

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Move Zeroes, Majority Element, Remove Duplicates from Sorted Array, Best Time to Buy/Sell Stock. For each: brute force → optimal Java solution → explain complexity aloud. | 4 solved problems + notes |
| Tue | Project | Define MVP: customer, restaurant owner, delivery partner, admin. Write user journeys. Draw service boundaries: Gateway, Auth, Restaurant, Order, Payment, Delivery, Notification. Initialize mono-repo. | `docs/mvp.md`, architecture v1 |
| Wed | HLD | Learn: client-server, monolith vs microservices, HTTP, REST, API gateway, latency vs throughput, availability. Practice: draw a basic food-delivery architecture. | 1 architecture diagram |
| Thu | LLD | Learn OOP refresh: encapsulation, inheritance, composition, interfaces, SOLID (SRP/OCP/DIP). Design a simple `User`, `Address`, `Restaurant`, `MenuItem` model. | Class diagram + Java skeleton |
| Fri | AI | Set up Cursor at home. Learn composer/agent mode, context rules, terminal use, and review workflow. Ask Cursor to scaffold a Spring Boot project; review every generated file manually. | Cursor installed + notes |
| Sat | Project Deep Work | Set up Spring Boot 3, Java 21/17, PostgreSQL, Flyway, Docker Compose, shared common module. Create README and local environment instructions. | Backend boots locally |
| Sun | Review | Re-solve 2 array problems without notes. Draft STAR story #1: difficult project/problem you owned. Create an error log template. | STAR #1 + review notes |

## Week 2: Strings, Bit Manipulation, and Authentication

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Valid Palindrome, Is Subsequence, Longest Common Prefix, Reverse Words in a String, Zigzag Conversion. | 5 problems |
| Tue | Project | Auth service: `User`, `Address`, roles; Flyway migrations; registration, login, password hashing, JWT access/refresh tokens. | Auth APIs working |
| Wed | HLD | Learn database selection: SQL vs NoSQL, indexes, ACID, replication, read replicas, caching basics. Design data storage for the food-delivery MVP. | DB decision document |
| Thu | Machine Coding | Implement **LRU Cache** in Java in 45 minutes: HashMap + doubly linked list; add JUnit tests. | Runnable Git repo/module |
| Fri | AI | Learn GitHub Copilot/Cursor comparison. Use Cursor to generate tests for Auth service; inspect, correct, and improve them. Learn prompt pattern: context → constraints → task → acceptance tests. | Prompt library v1 |
| Sat | Project Deep Work | API Gateway (Spring Cloud Gateway): routes, JWT validation filter, global error format, OpenAPI setup. Deploy local stack using Docker Compose. | Gateway routing Auth |
| Sun | Review | Solve: Single Number, Number of 1 Bits, Counting Bits, Reverse Bits. Draft STAR story #2: technical decision/trade-off. | 4 bit problems + STAR #2 |

## Week 3: Hashing, Restaurant Service, and LLD

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Group Anagrams, Contains Duplicate II, Isomorphic Strings, Ransom Note, Longest Consecutive Sequence. | 5 problems |
| Tue | Project | Restaurant service: schema for Restaurant, MenuCategory, MenuItem, OperatingHours; APIs for list, detail, create, menu management. | Restaurant APIs |
| Wed | HLD | Learn load balancing, CDN, caching (cache-aside/write-through), Redis, cache invalidation. Design **URL Shortener** for 45-60 minutes. | HLD write-up #1 |
| Thu | LLD | Design **Parking Lot**: requirements, entities, class diagram, spot allocation strategy, payment abstraction, extensibility. Implement key classes. | Parking Lot design |
| Fri | AI | Build a small "Code Review Assistant" CLI: paste diff → LLM returns review checklist/findings. Use an API or mock initially; focus on prompt/versioning/logging. | Mini AI tool #1 |
| Sat | Project Deep Work | Add Redis cache for popular restaurant queries. Add React + TypeScript/Vite: routing, API client, login, restaurant listing/detail pages. | Restaurant UI + caching |
| Sun | Review | Re-solve one hashing and one string problem. Record a 5-minute explanation of the project’s current architecture. | Video/self-review notes |

## Week 4: Two Pointers, Orders, and Payment Flow

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Two Sum II, Container With Most Water, 3Sum, Merge Sorted Array, Trapping Rain Water. | 5 problems |
| Tue | Project | Order service: Cart, CartItem, Order, OrderItem, order-state model. Implement cart APIs and order creation API. | Cart + order APIs |
| Wed | HLD | Learn CAP, consistency, message queues, pub/sub, idempotency, eventual consistency. Design **Notification System** or **Food Delivery App** at HLD. | HLD write-up #2 |
| Thu | Machine Coding | Implement **Tic-Tac-Toe** in 45 minutes. Separate board, player, game, and win strategy. Add tests. | Runnable solution |
| Fri | AI | Learn RAG fundamentals: embeddings, chunking, vector store, retrieval, context-window limitations, evaluation. Build a small local document Q&A proof-of-concept. | Mini AI tool #2 |
| Sat | Project Deep Work | Configure Kafka/RabbitMQ locally. Publish `OrderCreated`; implement consumer skeletons. Add React Cart and Checkout UI. | Event-driven order flow |
| Sun | Review | Month-1 review: re-solve 3 weak DSA problems, review 2 HLD designs, refine STAR stories. Define resume content inventory: achievements, metrics, projects. | Month-1 assessment |

---

# Phase 2: Depth and Deployment (Weeks 5-8)

## Week 5: Linked Lists, Payment, and Public Profile

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Reverse Linked List, Palindrome Linked List, Remove Nth Node From End, Copy List with Random Pointer, Add Two Numbers. | 5 problems |
| Tue | Project | Payment service: payment intent/create API, mock provider first, webhook verification, idempotency key, `PaymentSucceeded`/`PaymentFailed` events. | Payment flow |
| Wed | HLD | Design **News Feed / Timeline**. Cover fan-out on write vs read, celebrity problem, feeds, caching, ranking, pagination. | HLD write-up #3 + job applications |
| Thu | LLD | Design **Splitwise**: users/groups/expenses, equal/exact/percentage split strategies, balance calculation, debt simplification. | Splitwise design |
| Fri | AI + Job | Create final one-page resume in a single focused session. Update LinkedIn headline/about/experience, turn on job alerts. Apply to relevant openings found in last 48 hours. | Resume v1 + LinkedIn updated |
| Sat | Project Deep Work | Integrate payment service with Order service through events. Implement checkout/payment UI and order confirmation. | End-to-end order/payment |
| Sun | Review + Job | Write STAR story #3 (conflict/influence) and #4 (failure/learning). Apply/tailor for fresh jobs for 30 min. | 4 STAR stories |

## Week 6: Trees, Delivery, and AWS Basics

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Binary Tree Level Order Traversal, Validate BST, Kth Smallest in BST, Path Sum III, Serialize/Deserialize Binary Tree. | 5 problems |
| Tue | Project | Delivery service: DeliveryPartner, delivery assignment/status APIs. Implement simple allocation: available partner + lowest active orders; document limitation. | Delivery APIs |
| Wed | HLD | Design **Chat System / WhatsApp**. Cover WebSockets, online presence, message persistence, groups, ordering, delivery/read receipts. Apply to fresh jobs. | HLD write-up #4 |
| Thu | Machine Coding | Implement **Snake and Ladder** in 60 minutes with board configuration, dice abstraction, multiple players, win condition. | Runnable solution |
| Fri | AI + Job | Learn LangChain/LangGraph concepts: chains, tools, agents, state, memory, guardrails. Build a simple tool-calling agent that reads local project docs and answers architecture questions. | Mini AI tool #3 |
| Sat | Project Deep Work | Dockerize all services. Use Docker Compose for Gateway, services, PostgreSQL, Redis, Kafka. Add health checks. | Full local stack |
| Sun | Review + Job | Review tree templates. Practice 10-minute project architecture pitch. Apply to jobs posted within 48 hours. | Pitch recording |

## Week 7: Binary Search, AWS Deployment, and Observability

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Search in Rotated Sorted Array, Find Minimum in Rotated Array, Koko Eating Bananas, Find Peak Element, Median of Two Sorted Arrays. | 5 problems |
| Tue | Project | AWS foundation: IAM least privilege, VPC basics, security groups, RDS PostgreSQL. Migrate one service to RDS. | RDS connected |
| Wed | HLD | Design **Video Streaming (YouTube/Netflix)**. Cover upload, transcoding, object storage, CDN, adaptive bitrate, metadata and recommendations. Apply to fresh jobs. | HLD write-up #5 |
| Thu | LLD | Design **Elevator System**: states, requests, scheduler/dispatch strategy, multiple elevators, concurrent events. | Elevator class design |
| Fri | AI + Job | Learn LLM application architecture: UI → backend → orchestration → retrieval/tools → model → observability. Explore LangSmith/OpenTelemetry concepts. Improve GitHub profile README. | AI architecture notes |
| Sat | Project Deep Work | Deploy services on AWS ECS/Fargate or a deliberately simpler EC2/Docker setup. Use ECR images, ALB routing, CloudWatch logs. Document deploy architecture. | First cloud deployment |
| Sun | Review + Job | Review binary-search invariants. Apply/tailor to fresh jobs. Audit application tracker and follow up on earlier applications. | Application tracker updated |

## Week 8: Graphs, Notifications, Mobile Readiness

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Number of Islands, Clone Graph, Rotting Oranges, Course Schedule, Word Ladder. | 5 problems |
| Tue | Project | Notification service: templates, event consumption, email provider mock/SES, retry policy, dead-letter handling design. | Notification flow |
| Wed | HLD | Design **File Storage / Dropbox**. Cover chunking, sync, versioning, conflict handling, metadata vs blob storage. Apply to fresh jobs. | HLD write-up #6 |
| Thu | Machine Coding | Implement **Meeting Room Scheduler** in 60 minutes: rooms, time intervals, conflict detection, booking/cancellation, recurring extension discussion. | Runnable solution |
| Fri | AI + Job | Build a RAG assistant for your project documentation: ingest README/design docs, retrieve citations, answer architecture questions. Add evaluation questions. Apply to jobs. | Mini AI tool #4 |
| Sat | Project Deep Work | Deploy React frontend to S3 + CloudFront. Add Capacitor; make UI responsive; build/test Android app shell. | Public frontend + APK shell |
| Sun | Review + Job | Month-2 review: DSA weak-pattern list, architecture gaps, project demo rehearsal. Apply/follow up. | Midpoint scorecard |

---

# Phase 3: Interview Readiness (Weeks 9-12)

## Week 9: Dynamic Programming and Real-Time Features

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Climbing Stairs, House Robber, House Robber II, Coin Change, Partition Equal Subset Sum. | 5 problems |
| Tue | Project | Add WebSocket/SSE-based order status updates. Add delivery-partner status update flow. | Live order tracking |
| Wed | HLD | Design **Ride Sharing (Uber/Ola)**. Cover geospatial indexing, location updates, matching, ETA, surge pricing, reliability. Apply to fresh jobs. | HLD write-up #7 |
| Thu | LLD | Design **Rate Limiter**: interfaces, token bucket/fixed/sliding window strategies, in-memory vs distributed boundaries. | Rate limiter design |
| Fri | AI + Job | Learn AI evaluation: golden dataset, groundedness, relevance, hallucination checks, latency/cost metrics. Add basic RAG evaluation to your project-doc assistant. Apply/follow up. | Evaluation report |
| Sat | Deep Work | First full coding mock (60 min) + 30 min debrief. Then fix one major project issue from your backlog. | Mock #1 scorecard |
| Sun | Review + Job | Prepare STAR #5 (leadership) and #6 (ambiguity). Apply to fresh positions. | 6 STAR stories |

## Week 10: Backtracking, Search, and Reliability

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Generate Parentheses, Permutations, Subsets, Combination Sum, N-Queens. | 5 problems |
| Tue | Project | Add Resilience4j circuit breaker, retries with exponential backoff, timeout policy, idempotent consumers. Create failure scenarios. | Resilience demo |
| Wed | HLD | Design **E-commerce / Amazon**. Cover catalog, search, cart, inventory, checkout, payments, order workflow. Apply to fresh jobs. | HLD write-up #8 |
| Thu | Machine Coding | Implement **In-Memory Key-Value Store**: set/get/delete, TTL, expiration cleanup, thread-safety discussion. | Runnable solution |
| Fri | AI + Job | Build a small tool-using agent: "Project Task Assistant" that reads your GitHub issues/docs and returns a prioritized work plan. Add explicit allowed tools and guardrails. Apply/tailor. | Mini AI tool #5 |
| Sat | Deep Work | System-design mock: Food Delivery App / Swiggy. Use your own project as evidence; record 60-minute session and critique it. | Mock #2 scorecard |
| Sun | Review + Job | Review backtracking templates and API failure scenarios. Follow up on applications/referral requests. | Follow-up log |

## Week 11: Heaps, Intervals, and Scale

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Top K Frequent Elements, K Closest Points, Merge Intervals, Insert Interval, Meeting Rooms II. | 5 problems |
| Tue | Project | Add observability: structured logs, correlation IDs, metrics, tracing (OpenTelemetry/Zipkin optional), dashboards and alarms. | Observability dashboard |
| Wed | HLD | Design **Food Delivery at Scale (Swiggy/Zepto)**. Cover restaurant discovery, order saga, assignment, event bus, geo, monitoring, payments. Apply to fresh jobs. | HLD write-up #9 |
| Thu | LLD | Design **Movie Ticket Booking**: seat holds, booking lifecycle, concurrency/oversell prevention, pricing strategy, payment abstraction. | Booking design |
| Fri | AI + Job | Learn AI security and production concerns: prompt injection, data leakage, PII, cost caps, fallback models, rate limits. Add safe logging/redaction notes to mini projects. Apply. | AI security checklist |
| Sat | Deep Work | Full machine coding mock: **Parking Lot** or **Splitwise**, 90 minutes in Java with tests. 30 min code review. | Mock #3 code repo |
| Sun | Review + Job | Refine resume using project progress and measurable achievements. Apply/follow up. | Resume v2 |

## Week 12: Greedy, DP, and Interview Loops

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Solve: Jump Game II, Gas Station, Task Scheduler, Longest Common Subsequence, Edit Distance. | 5 problems |
| Tue | Project | Add admin dashboard essentials: restaurant management, order visibility, health summary. Add RBAC. | Admin MVP |
| Wed | HLD | Design **Web Crawler / Search**. Cover URL frontier, politeness, deduplication, distributed workers, indexing basics. Apply to fresh jobs. | HLD write-up #10 |
| Thu | Machine Coding | Implement **Logger Framework**: levels, appenders (console/file), configuration, thread-safe behavior; use Strategy pattern. | Runnable solution |
| Fri | AI + Job | Explore modern agentic coding workflow: plan mode, issue-to-PR workflow, automated test generation, code review agent. Run it on a small project feature and document what AI did vs what you verified. Apply. | Agent workflow case study |
| Sat | Deep Work | Mock loop: one DSA round + one behavioral round. Review recordings/notes. | Mock #4 scorecard |
| Sun | Review + Job | Phase-3 review: determine top 3 DSA gaps, top 3 design gaps, top 3 project gaps. Apply/follow up. | Gap-remediation list |

---

# Phase 4: Conversion and Polish (Weeks 13-16)

## Week 13: Hard Problems and Project Documentation

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Timed hard set: Trapping Rain Water, Serialize/Deserialize Binary Tree, Word Ladder, Minimum Window Substring. Review all failures. | 4 hard problems |
| Tue | Project | Write complete architecture documentation: requirements, service ownership, APIs, schema, sequence diagrams, event flow, deployment, scaling trade-offs. | `docs/architecture.md` |
| Wed | HLD | Design **Stock Trading Platform** or **Online Code Compiler**. Focus on latency, ordering, sandboxing/risk controls as appropriate. Apply. | HLD write-up #11 |
| Thu | LLD | Design **Vending Machine** or **Traffic Signal Controller**. Focus on state transitions, extensibility and testability. | LLD design |
| Fri | AI + Job | Build a basic AI feature for the Swiggy project: restaurant-menu Q&A / meal recommendation assistant using RAG or tool calling. Keep it scoped and document limitations. Apply. | AI feature MVP |
| Sat | Deep Work | Coding mock + HLD mock on same day; simulate an interview loop. | Mock #5 scorecard |
| Sun | Review + Job | Practice 10-minute project pitch and 2-minute resume walk-through. Applications and follow-ups. | Recorded pitch |

## Week 14: Company-Agnostic Interview Mastery

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Timed mixed set from weakest patterns. Do 3 medium + 1 hard in 2 hours; spend 1 hour on review. | Weakness report |
| Tue | Project | Performance/load test using k6/JMeter. Define metrics, run baseline, identify one bottleneck, optimize and re-run. | Load-test report |
| Wed | HLD | Design **CDN** or **Distributed Job Scheduler**. Discuss partitions, retries, monitoring, failure recovery. Apply. | HLD write-up #12 |
| Thu | Machine Coding | Implement **Shopping Cart / Inventory Reservation** in 60-90 minutes. Include clear APIs, validation, test cases. | Runnable solution |
| Fri | AI + Job | Learn model/tool selection: hosted API vs local model, structured outputs, function calling, embeddings models, vector DB trade-offs. Update portfolio/LinkedIn with AI project learnings. Apply. | AI decision matrix |
| Sat | Deep Work | Full mock loop: DSA, LLD/machine coding, behavioral. Get peer/AI feedback. | Mock #6 scorecard |
| Sun | Review + Job | Revisit weak mock areas; application follow-up and recruiter outreach. | Improvement plan |

## Week 15: Application Acceleration and Interview Simulation

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | LeetCode-style mock contest: 4 problems in 90 minutes; complete post-contest editorial analysis. | Contest review |
| Tue | Project | Production polish: error states, loading states, validation, security scan, dependency cleanup, responsive/mobile QA. | Release candidate |
| Wed | HLD | Design **Collaborative Editor** or **Live Streaming Platform**. Explain conflict resolution/WebSocket/data partitioning. Apply. | HLD write-up #13 |
| Thu | LLD | Design **Restaurant Reservation with Waitlist** or **Airline Booking**. Handle time overlap, status transitions, cancellation, concurrency. | LLD design |
| Fri | AI + Job | Create a personal job-search assistant: use structured data to track jobs, generate tailored accomplishment bullets, and draft outreach—verify all claims manually. Apply to fresh openings. | Mini AI tool #6 |
| Sat | Deep Work | Mock loop #7 (SDE2-focused) and mock loop #8 (SDE3-focused): compare depth, ownership, and communication. | Two scorecards |
| Sun | Review + Job | Finalize tailored resume variants: backend, full-stack, platform/microservices. Follow up/referral outreach. | Resume variants |

## Week 16: Final Readiness and Interview Pipeline

| Day | Focus | Detailed Tasks | Deliverable |
|-----|-------|----------------|-------------|
| Mon | DSA | Final DSA revision: templates for arrays, trees, graphs, DP, binary search, intervals, heaps. Solve 3 random medium/hard problems. | One-page DSA template sheet |
| Tue | Project | Final demo: verify live URL, repository setup, README, architecture diagrams, demo data, API docs, mobile build. Record 8-10 minute demo. | Portfolio-ready project |
| Wed | HLD | Final HLD mock: Design Food Delivery System; defend trade-offs at SDE3 depth. Apply to fresh roles. | Mock #9 scorecard |
| Thu | Machine Coding | Final machine coding mock: choose unknown problem from list, 90 minutes, Java + tests + clean README. | Mock #10 repo |
| Fri | AI + Job | Final AI/agentic portfolio cleanup. Publish a concise technical post about what you built and learned. Apply/follow up. | Portfolio + post |
| Sat | Deep Work | Full interview simulation: DSA + HLD + behavioral + project deep dive. Debrief and make final notes. | Final readiness report |
| Sun | Review + Job | Retrospective. Build next 4-week maintenance plan: 3 DSA sessions, 1 design mock, 1 project/AI improvement, continuous applications. | Maintenance plan |

---

## Important Adjustments

- If you miss a weekday, **do not cram two full days together**. Move the task to Saturday/Sunday or skip the lowest-value task.
- On design-problem days, reduce DSA; the day’s stream is the priority.
- Job applications are **time-sensitive**: check alerts daily and apply to a strong opening within 24-48 hours.
- Every completed HLD/LLD/machine-coding task should leave an artifact: diagram, markdown write-up, Java repo, tests, or recording.
