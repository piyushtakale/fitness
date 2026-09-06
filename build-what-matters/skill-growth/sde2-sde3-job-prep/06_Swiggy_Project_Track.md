# Swiggy/Zepto Clone Project Track

## Objective

Build a **production-grade food delivery microservices application** with:
- 6+ microservices (Auth, Restaurant, Order, Payment, Delivery, Notification)
- React frontend + mobile app (Capacitor)
- AWS deployment (ECS/Fargate, RDS, ElastiCache, S3, CloudFront)
- Event-driven architecture (Kafka/RabbitMQ)
- Observability (logging, metrics, tracing)

## Weekly Target

- **Weeks 1-4**: Build core services (Auth, Restaurant, Order, Payment)
- **Weeks 5-8**: Add Delivery, Notification, deploy to AWS, build mobile app
- **Weeks 9-12**: Add advanced features (real-time, search, observability)
- **Weeks 13-16**: Polish, document, create demo, prepare for interviews

---

## Project Architecture

### Microservices

1. **API Gateway** (Spring Cloud Gateway)
   - Route requests to services
   - JWT validation
   - Rate limiting
   - Global error handling

2. **Auth Service**
   - User registration/login
   - JWT token generation
   - Role-based access control
   - Password hashing

3. **Restaurant Service**
   - Restaurant CRUD
   - Menu management
   - Search and filtering
   - Redis caching

4. **Order Service**
   - Cart management
   - Order creation
   - Order lifecycle
   - Event publishing

5. **Payment Service**
   - Payment intent creation
   - Webhook handling
   - Payment status tracking
   - Event publishing

6. **Delivery Service**
   - Delivery partner management
   - Order assignment
   - Delivery tracking
   - Status updates

7. **Notification Service**
   - Email/SMS/Push notifications
   - Templates
   - Retry logic
   - Dead-letter handling

---

## Technology Stack

### Backend
- Java 17/21
- Spring Boot 3
- Spring Cloud (Gateway, Config)
- Spring Security (JWT)
- Spring Data JPA
- Flyway (migrations)

### Databases
- PostgreSQL (RDS)
- Redis (ElastiCache)
- Kafka/MSK (event streaming)

### Frontend
- React 18
- TypeScript
- Vite
- Tailwind CSS / Material UI
- React Query (state management)
- Axios (API client)

### DevOps
- Docker
- GitHub Actions (CI/CD)
- AWS ECS/Fargate
- AWS RDS
- AWS ElastiCache
- AWS S3 + CloudFront
- AWS CloudWatch

### Mobile
- Capacitor
- Android Studio
- iOS (optional)

---

## Week-by-Week Plan

### Week 1: Project Setup and Auth Service

**Goals:**
- Define MVP scope
- Set up mono-repo structure
- Implement Auth service
- Deploy to Heroku/local

**Tasks:**
- [ ] Define user stories (customer, restaurant owner, delivery partner, admin)
- [ ] Draw service boundaries diagram
- [ ] Initialize GitHub mono-repo
- [ ] Set up Spring Boot 3 starter module
- [ ] Implement `User`, `Address` entities
- [ ] Flyway migrations for PostgreSQL
- [ ] Implement registration/login APIs
- [ ] JWT token generation and validation
- [ ] Deploy Auth service to Heroku

**Deliverable:** Auth service with login/register working

---

### Week 2: Restaurant Service and Frontend Setup

**Goals:**
- Implement Restaurant service
- Set up React frontend
- Deploy restaurant listing

**Tasks:**
- [ ] Design `Restaurant`, `MenuCategory`, `MenuItem`, `OperatingHours` entities
- [ ] Implement CRUD APIs for restaurants
- [ ] Add search and filtering
- [ ] Redis caching for popular restaurants
- [ ] Initialize React app (Vite + TypeScript)
- [ ] Set up routing and API client
- [ ] Build Login/Signup pages
- [ ] Build Home page with restaurant list
- [ ] Build Restaurant detail page
- [ ] CI/CD pipeline for Auth + Restaurant services

**Deliverable:** Restaurant service + React UI for browsing

---

### Week 3: Order Service and Event Streaming

**Goals:**
- Implement Order service
- Set up Kafka/RabbitMQ
- Build Cart and Checkout UI

**Tasks:**
- [ ] Design `Cart`, `CartItem`, `Order`, `OrderItem` entities
- [ ] Implement Cart APIs (add, update, remove)
- [ ] Implement Order APIs (create, get, list)
- [ ] Set up Kafka/RabbitMQ locally with Docker
- [ ] Publish `OrderCreated` events
- [ ] Build Cart page UI
- [ ] Build Checkout flow UI
- [ ] Docker Compose for local development

**Deliverable:** Order service with event streaming

---

### Week 4: Payment Service and Integration

**Goals:**
- Implement Payment service
- Integrate Razorpay/Stripe (test mode)
- Build payment UI
- Dockerize all services

**Tasks:**
- [ ] Design payment flow
- [ ] Implement payment intent creation API
- [ ] Implement webhook handling
- [ ] Signature verification
- [ ] Publish `PaymentSucceeded`/`PaymentFailed` events
- [ ] Integrate Razorpay SDK in React
- [ ] Build payment page UI
- [ ] Build order tracking page
- [ ] Dockerize all services
- [ ] Create `docker-compose.yml` for local dev

**Deliverable:** End-to-end order + payment flow

---

### Week 5: Delivery Service and Notifications

**Goals:**
- Implement Delivery service
- Implement Notification service
- Add email notifications

**Tasks:**
- [ ] Design `DeliveryPartner`, `DeliveryAssignment` entities
- [ ] Implement delivery assignment logic
- [ ] Implement status update APIs
- [ ] Subscribe to `OrderCreated` events
- [ ] Publish `DeliveryAssigned` events
- [ ] Build Delivery Partner UI (web)
- [ ] Set up Notification service
- [ ] Email templates for order events
- [ ] Integrate SendGrid/AWS SES
- [ ] Subscribe to order/payment/delivery events

**Deliverable:** Delivery assignment + email notifications

---

### Week 6: AWS Deployment

**Goals:**
- Deploy services to AWS
- Set up RDS, ElastiCache
- Configure ECS/Fargate

**Tasks:**
- [ ] Create AWS account and IAM users
- [ ] Set up VPC, subnets, security groups
- [ ] Create RDS PostgreSQL instance
- [ ] Migrate schema to RDS
- [ ] Set up ElastiCache Redis
- [ ] Set up MSK or EventBridge
- [ ] Create ECS cluster
- [ ] Create task definitions for each service
- [ ] Deploy services to ECS/Fargate
- [ ] Configure Application Load Balancer
- [ ] Add CloudWatch logging

**Deliverable:** All services deployed to AWS

---

### Week 7: Frontend Deployment and Mobile Setup

**Goals:**
- Deploy React app to S3 + CloudFront
- Set up Capacitor for mobile
- Build Android APK

**Tasks:**
- [ ] Build React app for production
- [ ] Create S3 bucket for static hosting
- [ ] Configure CloudFront CDN
- [ ] Set up API Gateway or ALB routing
- [ ] Add Capacitor to React project
- [ ] Configure `capacitor.config.ts`
- [ ] Add Android platform
- [ ] Build APK
- [ ] Test on Android emulator
- [ ] Optimize UI for mobile

**Deliverable:** Public frontend + mobile APK

---

### Week 8: Admin Dashboard and Documentation

**Goals:**
- Build admin dashboard
- Add load testing
- Write documentation
- Record demo video

**Tasks:**
- [ ] Build admin dashboard (restaurant management, order visibility)
- [ ] Add RBAC (role-based access control)
- [ ] Load testing with JMeter/k6
- [ ] Identify and fix bottlenecks
- [ ] Write comprehensive README
- [ ] Create API documentation (Swagger/OpenAPI)
- [ ] Write architecture documentation
- [ ] Record 5-10 minute demo video
- [ ] Upload to portfolio/YouTube

**Deliverable:** Production-ready project with documentation

---

### Week 9: Real-Time Features and Search

**Goals:**
- Add WebSocket for real-time order tracking
- Implement Elasticsearch for search
- Add geolocation features

**Tasks:**
- [ ] Add WebSocket support to Order service
- [ ] Implement real-time status updates
- [ ] Set up Elasticsearch cluster
- [ ] Implement restaurant search with filters
- [ ] Add location-based discovery
- [ ] Optimize React UI for mobile
- [ ] Add native features (push notifications, location)
- [ ] Document scaling strategy

**Deliverable:** Real-time order tracking + advanced search

---

### Week 10: Security and Resilience

**Goals:**
- Add security hardening
- Implement circuit breakers
- Add distributed tracing

**Tasks:**
- [ ] Add API rate limiting per user
- [ ] Implement request validation
- [ ] Add SQL injection prevention
- [ ] Add Resilience4j circuit breakers
- [ ] Implement retry logic with backoff
- [ ] Set up distributed tracing (Zipkin/Jaeger)
- [ ] Add correlation IDs across services
- [ ] Review AWS costs and optimize
- [ ] Add SonarQube analysis
- [ ] Improve test coverage >80%

**Deliverable:** Secure, resilient system

---

### Week 11: Advanced Features

**Goals:**
- Add order scheduling
- Implement analytics
- Add A/B testing

**Tasks:**
- [ ] Implement order scheduling (order for later)
- [ ] Add favorite restaurants
- [ ] Integrate analytics (GA4/Mixpanel)
- [ ] Track user journey funnel
- [ ] Set up feature flags (LaunchDarkly/custom)
- [ ] Implement A/B test for checkout flow
- [ ] Add i18n support
- [ ] Improve accessibility (ARIA, keyboard navigation)
- [ ] Complete regression testing

**Deliverable:** Feature-rich application

---

### Week 12: Interview Preparation

**Goals:**
- Prepare project pitch
- Practice explaining architecture
- Update resume and LinkedIn

**Tasks:**
- [ ] Practice 10-minute architecture pitch
- [ ] Prepare answers for "Why microservices?"
- [ ] Document trade-offs made
- [ ] Update resume with project metrics
- [ ] Create detailed LinkedIn post
- [ ] Clean up GitHub repo
- [ ] Add badges (build status, coverage)
- [ ] Create portfolio page
- [ ] Practice mock interviews using project

**Deliverable:** Interview-ready project presentation

---

### Weeks 13-16: Polish and Production Readiness

**Goals:**
- Final polish
- Production monitoring
- Interview mastery

**Tasks:**
- [ ] Fix remaining UI/UX issues
- [ ] Improve error messages
- [ ] Add loading states
- [ ] Set up production monitoring dashboards
- [ ] Configure alerts for critical issues
- [ ] Create runbook for common issues
- [ ] Final mock interviews
- [ ] Apply to target companies
- [ ] Network with engineers at target companies

**Deliverable:** Production-grade portfolio project

---

## Success Metrics

- **Week 4**: Core services (Auth, Restaurant, Order, Payment) working end-to-end
- **Week 8**: Full application deployed to AWS with documentation
- **Week 12**: Advanced features, security, resilience complete
- **Week 16**: Production-ready, interview-ready portfolio project

---

## Resources

- **YouTube**: Swiggy clone tutorials, Spring Boot microservices
- **GitHub**: Reference implementations for food delivery apps
- **AWS**: Free tier for learning
- **Documentation**: Spring Boot, React, Capacitor official docs
