# HLD Track (High-Level Design)

## Objective

Master **20 HLD problems** (10 frequent + 10 unique) with ability to design scalable systems under interview pressure.

## Weekly Target

- **Weeks 1-4**: Learn fundamentals, practice 1 HLD problem/week
- **Weeks 5-8**: Practice 2 HLD problems/week
- **Weeks 9-12**: Practice 2-3 HLD problems/week (mock interviews)
- **Weeks 13-16**: Review and master all 20 problems

---

## HLD Fundamentals (Weeks 1-4)

### Core Concepts

1. **Client-Server Architecture**
   - HTTP/HTTPS, REST, gRPC, WebSockets
   - Load balancers, reverse proxies, API gateways

2. **Databases**
   - SQL vs NoSQL (when to use which)
   - Indexing, replication, sharding, partitioning
   - ACID vs BASE, CAP theorem
   - Read replicas, write-through caching

3. **Caching**
   - Cache-aside, write-through, write-behind
   - LRU, LFU, FIFO eviction policies
   - Cache invalidation strategies
   - Redis, Memcached, CDN

4. **Messaging**
   - Message queues (Kafka, RabbitMQ, SQS)
   - Pub/sub pattern
   - Event sourcing, CQRS
   - At-least-once vs exactly-once delivery

5. **Scalability**
   - Horizontal vs vertical scaling
   - Microservices architecture
   - Service discovery, circuit breakers
   - Rate limiting, throttling

6. **Observability**
   - Logging, metrics, tracing
   - Health checks, dashboards
   - Alerting, SLOs, SLAs

---

## 20 HLD Problems

### FREQUENT PROBLEMS (10)

#### 1. Design URL Shortener (TinyURL)

**Requirements:**
- Generate short URLs from long URLs
- Redirect short URLs to original
- Analytics: click count, referrer, location
- Custom short URLs (optional)

**Key Components:**
- Hashing algorithm (Base62, MD5, SHA-256)
- Key-value store (Redis for cache, DB for persistence)
- Database sharding strategy
- CDN for static content

**Scale:**
- 100M+ URLs
- <10ms redirect latency
- 99.99% availability

**Practice:** Week 3, Week 12

---

#### 2. Design News Feed / Timeline (Twitter, Facebook)

**Requirements:**
- Users post tweets/posts
- Followers see posts in timeline
- Real-time updates
- Rich media support

**Key Components:**
- Fan-out on write vs fan-out on read
- Graph database for social connections
- Feed generation service
- Caching strategy (Redis)
- Pagination (cursor-based)

**Scale:**
- 500M+ users
- 10K+ posts/second
- Timeline latency <200ms

**Practice:** Week 5, Week 13

---

#### 3. Design Chat/Messaging System (WhatsApp, Slack)

**Requirements:**
- 1:1 and group messaging
- Message persistence
- Read receipts, typing indicators
- Media sharing

**Key Components:**
- WebSocket connections
- Message queue (Kafka)
- Database for message history
- Presence service (online/offline)
- End-to-end encryption (optional)

**Scale:**
- 1B+ users
- 50K+ messages/second
- <100ms message delivery

**Practice:** Week 6, Week 14

---

#### 4. Design Video Streaming Platform (YouTube, Netflix)

**Requirements:**
- Video upload and transcoding
- Adaptive bitrate streaming
- Recommendations
- Subscriptions, playlists

**Key Components:**
- Object storage (S3)
- CDN for video delivery
- Transcoding service (FFmpeg)
- Recommendation engine
- Metadata database

**Scale:**
- 100M+ videos
- Petabyte storage
- Millions of concurrent streams

**Practice:** Week 7, Week 15

---

#### 5. Design Notification System

**Requirements:**
- Email, SMS, push notifications
- Templates, personalization
- Retry logic, dead-letter handling
- Rate limiting

**Key Components:**
- Event-driven architecture (Kafka)
- Template service
- Provider integration (SendGrid, Twilio, FCM)
- Priority queue for urgent notifications

**Scale:**
- Billions of notifications/day
- <5s delivery for urgent notifications
- 99.9% delivery rate

**Practice:** Week 8, Week 16

---

#### 6. Design Ride Sharing Service (Uber, Lyft)

**Requirements:**
- Real-time location tracking
- Driver-rider matching
- ETA calculation
- Surge pricing
- Payment integration

**Key Components:**
- Geospatial indexing (GeoHash, R-tree)
- WebSocket for real-time updates
- Matching algorithm
- Pricing engine
- Trip management service

**Scale:**
- Million concurrent rides
- <1s matching latency
- <50ms location updates

**Practice:** Week 9, Week 13

---

#### 7. Design Food Delivery App (Swiggy, Zomato)

**Requirements:**
- Restaurant discovery
- Order placement and tracking
- Delivery partner assignment
- Payment processing
- Ratings and reviews

**Key Components:**
- Search service (Elasticsearch)
- Order management service
- Delivery assignment algorithm
- Real-time tracking (WebSocket)
- Payment gateway integration

**Scale:**
- Million orders/day
- <2s order confirmation
- <5s delivery assignment

**Practice:** Week 11, Week 16

---

#### 8. Design File Storage & Sharing (Dropbox, Google Drive)

**Requirements:**
- File upload/download
- Sync across devices
- Versioning
- Sharing and permissions

**Key Components:**
- Chunking and deduplication
- Object storage (S3)
- Metadata database
- Sync service
- CDN for downloads

**Scale:**
- Petabyte storage
- Millions of concurrent users
- <1s sync latency

**Practice:** Week 8, Week 14

---

#### 9. Design E-commerce Platform (Amazon, Flipkart)

**Requirements:**
- Product catalog and search
- Shopping cart
- Inventory management
- Order management
- Payment processing
- Recommendations

**Key Components:**
- Product search (Elasticsearch)
- Inventory service
- Order saga pattern
- Payment service
- Recommendation engine

**Scale:**
- Billion products
- Million orders/day
- <100ms search latency

**Practice:** Week 10, Week 15

---

#### 10. Design Web Crawler / Search Engine

**Requirements:**
- Crawl billions of web pages
- Respect robots.txt, politeness
- Deduplication
- Indexing for search

**Key Components:**
- URL frontier (priority queue)
- Distributed workers
- Content deduplication (MinHash)
- Indexing service
- Storage (HDFS, S3)

**Scale:**
- 10B+ pages
- 100K pages/second crawl rate
- <1s search latency

**Practice:** Week 12, Week 16

---

### UNIQUE PROBLEMS (10)

#### 11. Design Online Code Compiler (LeetCode, HackerRank)

**Requirements:**
- Code submission and execution
- Multiple language support
- Test case evaluation
- Result streaming

**Key Components:**
- Containerization (Docker)
- Code execution sandbox
- Queue for job processing
- Result caching

**Scale:**
- 10K+ concurrent executions
- <5s execution time
- Secure sandboxing

**Practice:** Week 13

---

#### 12. Design Stock Trading Platform (Zerodha, Robinhood)

**Requirements:**
- Real-time stock quotes
- Order placement (buy/sell)
- Order matching engine
- Portfolio management
- Risk management

**Key Components:**
- Order book (buy/sell queues)
- Matching engine (price-time priority)
- Real-time WebSocket for quotes
- Risk management service
- Settlement service

**Scale:**
- Million trades/day
- <1ms order matching
- <100ms quote updates

**Practice:** Week 11, Week 15

---

#### 13. Design Distributed Job Scheduler (Airflow-like)

**Requirements:**
- DAG-based job dependencies
- Cron scheduling
- Retry and failure handling
- Worker pool management

**Key Components:**
- DAG parser
- Scheduler service
- Worker pool
- Task queue (Kafka/RabbitMQ)
- State persistence

**Scale:**
- 100K+ jobs/day
- <1s scheduling latency
- 99.9% job completion rate

**Practice:** Week 14

---

#### 14. Design Live Streaming Platform (Twitch, YouTube Live)

**Requirements:**
- Live video ingestion (RTMP/WebRTC)
- Low-latency streaming
- Chat integration
- Viewer analytics

**Key Components:**
- Ingestion service
- Transcoding service
- CDN edge servers
- Real-time chat (WebSocket)
- Analytics service

**Scale:**
- 10K+ concurrent streams
- <2s end-to-end latency
- Million concurrent viewers

**Practice:** Week 14

---

#### 15. Design Content Delivery Network (CDN)

**Requirements:**
- Global content distribution
- Cache invalidation
- Geographic routing
- Origin pull/push

**Key Components:**
- Edge servers
- DNS routing (GeoDNS)
- Cache management
- Origin servers
- Analytics and logging

**Scale:**
- Global reach
- TB/sec bandwidth
- <50ms cache hit latency

**Practice:** Week 14

---

#### 16. Design Hotel Booking Aggregator (Booking.com, Airbnb)

**Requirements:**
- Aggregation from multiple sources
- Price comparison
- Availability sync
- Booking flow

**Key Components:**
- Aggregator service (APIs to hotels)
- Search and filter
- Booking service
- Payment integration
- Cancellation handling

**Scale:**
- 100K+ hotels
- Million bookings/day
- <500ms search latency

**Practice:** Week 13

---

#### 17. Design Online Multiplayer Gaming Backend

**Requirements:**
- Game state synchronization
- Matchmaking
- Leaderboard
- Anti-cheat measures

**Key Components:**
- Game server cluster
- State synchronization (WebSocket)
- Matchmaking algorithm
- Leaderboard service (Redis sorted sets)
- Analytics service

**Scale:**
- Million concurrent players
- <100ms state updates
- <1s matchmaking

**Practice:** Week 15

---

#### 18. Design Ad Click Aggregator (Google Ads Analytics)

**Requirements:**
- Real-time click tracking
- Aggregation by campaign, advertiser
- Fraud detection
- Reporting dashboard

**Key Components:**
- Event streaming (Kafka)
- Real-time aggregation (Flink/Spark)
- Fraud detection service
- Data warehouse
- Dashboard service

**Scale:**
- Billion clicks/day
- Real-time aggregation
- <1s dashboard updates

**Practice:** Week 15

---

#### 19. Design Parking Lot Management at Scale (IoT sensors)

**Requirements:**
- Real-time occupancy tracking
- IoT sensor data ingestion
- Analytics dashboard
- Mobile app integration

**Key Components:**
- IoT gateway service
- Real-time data processing
- Occupancy database
- Analytics service
- Mobile API

**Scale:**
- 100K+ parking spots
- City-wide deployment
- <1s occupancy updates

**Practice:** Week 16

---

#### 20. Design Collaborative Code Editor (Google Docs for code)

**Requirements:**
- Real-time collaborative editing
- Conflict resolution
- Version history
- Code execution (optional)

**Key Components:**
- Operational transformation (OT) or CRDT
- WebSocket connections
- Document storage
- Version control
- Code execution sandbox

**Scale:**
- 1K+ concurrent users/doc
- <100ms sync latency
- Conflict-free merges

**Practice:** Week 16

---

## HLD Practice Methodology

### Problem-Solving Framework (45-60 minutes)

1. **Requirements (5 min)**
   - Functional requirements
   - Non-functional requirements (scale, latency, availability)

2. **Back-of-envelope estimation (5 min)**
   - Traffic, storage, bandwidth
   - Number of servers needed

3. **High-level architecture (15 min)**
   - Draw components and data flow
   - Identify bottlenecks

4. **Deep dive (20 min)**
   - Database schema
   - API design
   - Scaling strategy

5. **Wrap-up (5 min)**
   - Trade-offs
   - Future improvements

### Weekly Practice Schedule

- **Weeks 1-4**: 1 HLD problem/week (fundamentals focus)
- **Weeks 5-8**: 2 HLD problems/week (apply fundamentals)
- **Weeks 9-12**: 2-3 HLD problems/week (mock interviews)
- **Weeks 13-16**: Review all 20 problems, focus on weak areas

### Resources

- **Books**: "System Design Interview" by Alex Xu (Vol 1 & 2)
- **YouTube**: Gaurav Sen, ByteByteGo, System Design Interview
- **Practice**: LeetCode Discuss, Pramp, Interviewing.io

### Success Metrics

- **Week 4**: Comfortable with 3-4 basic HLD problems
- **Week 8**: Can design 8-10 systems from scratch
- **Week 12**: Confident with all frequent problems
- **Week 16**: Master all 20 problems, can defend trade-offs
