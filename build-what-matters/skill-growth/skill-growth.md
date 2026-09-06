# Career Transition Plan (SDE-2/SDE-3 Role)

**Purpose:** This document is your structured reference for moving into a stronger SDE-2/SDE-3 role with better compensation, healthier work-life balance, modern engineering exposure, and a Pune location or workable relocation path. It is not a rigid contract. It is a compass to keep you from drifting, over-preparing without shipping, or applying randomly without focus.

---

## Why This Goal Matters

This is not just about a higher salary. It is about:

- **Financial leverage for your family home:** A stronger role makes the ₹70–80 lakh Pune home goal realistic instead of stressful.
- **Professional confidence:** Rebuilding your sense of competence and enjoyment in engineering after a period of grief and stagnation.
- **Long-term career trajectory:** Positioning yourself for senior, staff, or principal tracks rather than remaining stuck in a mid-level plateau.
- **Work-life sustainability:** A role that supports your health, relationships, and creative life instead of draining them.

> **Reminder:** Your career is a tool for a meaningful life, not the only measure of your worth.

---

## Target Profile

| Parameter | Target |
|---|---|
| Role level | SDE-2 or SDE-3 (Senior Software Engineer) |
| Location | Pune-based or Pune-flexible (remote/hybrid acceptable) |
| Compensation | ₹35–50 LPA total (stretch: ₹45–60+ LPA for strong product roles) |
| Tech stack | Modern backend (Java/Spring Boot or similar), cloud-native (AWS/GCP/Azure), distributed systems, CI/CD, observability |
| Work-life balance | Sustainable hours, reasonable on-call, supportive culture |
| Growth path | Clear technical progression, mentorship opportunities, modern engineering practices |

---

## Market Context (2026)

### Salary Benchmarks

- **Senior Software Engineer (5–9 years):** ₹18–35 LPA average; top-tier product companies and GCCs can reach ₹40–75 LPA or higher. [web:53][web:57]
- **Pune-specific ranges:**
  - Mid-level (3–5 years): ₹15–25 LPA
  - Senior (6–9 years): ₹28–45 LPA
  - Lead/Staff: ₹40–65+ LPA [web:52]
- **SDE-3 (7–10 years):**
  - IT Services: ₹22–35 LPA
  - Product companies: ₹50–90 LPA
  - FAANG: ₹1–1.5 Cr+ [web:61]

### Interview Focus Areas

Senior roles test more than coding speed. They evaluate:

- **Technical judgement & system design:** Trade-offs, scalability, reliability, cost, and operational complexity. [web:55][web:62]
- **Code quality & review:** Clean, maintainable, testable code with clear reasoning. [web:62]
- **Production operations:** Incident response, debugging, monitoring, and ownership of failures. [web:56][web:62]
- **Cross-team influence:** Ability to collaborate, mentor, and drive decisions without formal authority. [web:62]
- **Behavioural & values alignment:** Ownership, feedback, growth mindset, and team impact. [web:62]

---

## Preparation Pillars

| Pillar | What to Build | Why It Matters |
|---|---|---|
| DSA | Patterns, timed medium-level problems, explanation of trade-offs, periodic hard problems | Tests coding fluency and problem-solving under interview conditions |
| HLD | Requirements, estimations, APIs, data models, storage choices, caching, queues, scaling, reliability, observability | Central for senior backend/system-design interviews |
| LLD | SOLID, object modelling, design patterns, concurrency where relevant, clean extensible Java | Shows that you can turn designs into maintainable production code |
| Java / Spring Boot | REST APIs, JPA/Hibernate, validation, security, testing, exception handling, async processing, caching | Makes your backend experience concrete and credible |
| React | Components, state, hooks, routing, forms, API integration, testing basics | Gives you practical full-stack range without making frontend your main focus |
| Cloud and delivery | AWS fundamentals, Docker, CI/CD, deployment, logging, metrics, secrets and environment configuration | Demonstrates that you can ship and operate a service, not merely write local code |
| Behavioural | Leadership, ownership, conflict, failure, ambiguity, impact, mentoring | Often decides SDE-3 outcomes when technical candidates are comparable |

---

## Project: Swiggy-Style Food Ordering Platform

Build a backend-heavy food-ordering system with React as a functional frontend. This project should be a credible production-style case study—not an endless attempt to recreate every Swiggy feature.

### Recommended Scope

- **Customer flows:** Browse restaurants/menu, cart, checkout, place and track an order
- **Restaurant flows:** Manage menu and accept or reject orders
- **Delivery simulation:** Assignment and order-status progression; no real maps or live driver tracking required
- **Backend:** Spring Boot, PostgreSQL, REST APIs, authentication/authorization, input validation, global error handling, migrations, unit and integration tests
- **Engineering:** Docker Compose for local setup, GitHub Actions for tests/build, deployment, structured logs, health endpoint, and a concise architecture document
- **Optional (after core is complete):** Redis cache, async notifications/queue, rate limiting, search, or a separate worker service

### AI-Assisted Development

Use Cursor, Copilot, or Claude Code to accelerate the work, but treat every generated module as something you must be able to explain in an interview.

For each nontrivial feature, keep a short decision record:

```text
Feature:
Chosen approach:
Alternatives considered:
Why this approach fits:
Failure modes / trade-offs:
How it is tested:
```

This turns AI assistance into evidence of engineering judgment rather than a dependency.

---

## Two-Track Strategy

### Track 1: Capability Building (Months 1–4)

Focus on consistent preparation and project completion.

1. **DSA:** 4–5 sessions/week, 60–90 minutes each. Focus on patterns (arrays, strings, linked lists, trees, graphs, DP, sliding window, two pointers).
2. **System Design:** 2 sessions/week, 90 minutes each. Study one HLD topic and apply it to a mini-design (URL shortener, rate limiter, notification system).
3. **Project:** 2–3 sessions/week, 2–3 hours each. Build the Swiggy-style platform incrementally.
4. **Behavioural:** 1 session/week, 60 minutes. Write and refine 6–8 STAR stories (Situation, Task, Action, Result).

### Track 2: Job Search & Interviews (Months 3–6+)

Begin applying while still improving.

1. **CV refinement:** Create two versions (backend-focused and full-stack-leaning).
2. **Referrals:** Reach out to ex-colleagues, alumni, and LinkedIn connections in target companies.
3. **Applications:** Apply to 5–10 roles/week, focusing on Pune or Pune-flexible positions.
4. **Mock interviews:** 1–2 mocks/week (coding, system design, behavioural).
5. **Iterate:** Use feedback from each interview to adjust preparation.

---

## Target Companies & Roles

| Company Type | Examples | Compensation Range | Notes |
|---|---|---|---|
| Product (India) | Rippling, Atlassian, Salesforce, Adobe, Intuit | ₹35–60 LPA | Strong engineering culture, modern tech |
| GCCs | Walmart, Target, Barclays, Wells Fargo, Mastercard | ₹25–45 LPA | Pune presence, stable work, good WLB |
| Startups (Series B–D) | Razorpay, Cred, Zepto, Blinkit, PharmEasy | ₹30–55 LPA | High growth, modern stack, variable WLB |
| FAANG / Big Tech | Google, Amazon, Microsoft, Netflix | ₹45 LPA–1.5 Cr+ | High bar, long process, strong brand |
| Remote (US/EU) | Various via AngelList, RemoteOK, LinkedIn | $80k–$150k+ | Pune location possible, tax complexity |

---

## Location Strategy

### Pune Advantages

- Close to family (Ulhasnagar ~3–4 hours) and sister (studying in Pune).
- Lower cost of living than Bengaluru; easier to buy a home.
- Strong IT corridors: Hinjewadi, Wakad, Baner, Kharadi, Hadapsar, PCMC.
- Growing product and GCC presence.

### Trade-offs

- Slightly lower average compensation than Bengaluru/Hyderabad for similar roles.
- Fewer ultra-high-paying startups compared to Bengaluru.
- Some roles may require hybrid or occasional travel.

> **Decision rule:** Prioritize roles that improve compensation, growth, and Pune feasibility rather than accepting the first escape route.

---

## Financial Planning

### Current Baseline

- **Current CTC:** ₹26 LPA
- **Monthly savings:** ~₹50,000 (invested in mutual funds)
- **Target CTC:** ₹35–50 LPA (stretch: ₹45–60+ LPA)

### Impact of Job Switch

| Scenario | CTC | Monthly Take-Home (approx.) | Monthly Savings Potential |
|---|---|---|---|
| Current | ₹26 LPA | ₹1.6–1.7 Lakh | ₹50,000 |
| Target (low) | ₹35 LPA | ₹2.1–2.2 Lakh | ₹80,000–1 Lakh |
| Target (high) | ₹50 LPA | ₹2.8–3.0 Lakh | ₹1.2–1.5 Lakh |

> **Note:** These are rough estimates. Actual take-home depends on tax regime, deductions, and variable pay structure.

---

## Interview Readiness Checklist

Use this checklist before applying or interviewing.

### Technical

- [ ] DSA: Comfortable with medium-level problems in 20–30 minutes
- [ ] HLD: Can design a scalable system (e.g., food delivery, URL shortener, rate limiter) with clear trade-offs
- [ ] LLD: Can model objects, apply design patterns, and write clean, testable Java code
- [ ] Spring Boot: Comfortable with REST APIs, JPA, validation, security, testing
- [ ] Cloud: Can deploy a service on AWS (or similar) with CI/CD, logging, and monitoring
- [ ] Project: Swiggy-style platform is deployed, documented, and ready to discuss

### Behavioural

- [ ] 6–8 STAR stories prepared (ownership, conflict, failure, impact, mentoring, ambiguity)
- [ ] Can articulate why you want to leave current role and what you seek next
- [ ] Can discuss strengths, weaknesses, and growth areas honestly

### Practical

- [ ] CV refined (backend and full-stack versions)
- [ ] LinkedIn profile updated with key achievements
- [ ] Referral network activated (ex-colleagues, alumni, LinkedIn)
- [ ] Mock interviews completed (coding, system design, behavioural)

---

## Open Questions to Answer Over Time

These are questions you will answer gradually as you research, network, and interview.

1. Which companies in Pune align best with my tech stack and work-life goals?
2. Am I ready for SDE-3, or should I target SDE-2 roles first?
3. What is my non-negotiable minimum compensation for a switch?
4. How much variable pay vs. fixed pay am I comfortable with?
5. Do I prefer a product company, GCC, or startup environment?
6. What is my notice period, and how can I manage it during interviews?
7. Should I consider remote roles with US/EU companies for higher compensation?
8. What specific skills (e.g., Kubernetes, Kafka, GraphQL) would make me more competitive?
9. How do I explain my career gap or slower growth due to personal circumstances?
10. What is my long-term career vision (5–10 years), and how does this role fit?

---

## First Milestones

| Time horizon | Outcome to aim for |
|---|---|
| Next 30 days | Reopen DSA and system-design practice; initialize project repository; build one small end-to-end vertical slice |
| Next 90 days | Complete project MVP; cover core DSA patterns; practise HLD/LLD consistently; add AWS/Docker/CI-CD; prepare 6–8 behavioural stories |
| Next 6 months | Run timed DSA rounds, system-design mocks, project walkthroughs, CV refinement, referrals, and applications |
| Next 6–12 months | Secure a stronger role with better compensation, growth, and Pune feasibility |

---

## Guardrails

- **Do not wait to feel "fully ready" before applying.** Apply continuously while improving.
- **Do not accept the first offer out of fear.** Evaluate fit, compensation, growth, and culture.
- **Do not let preparation become another form of avoidance.** Shipping code and interviewing are part of the goal.
- **Do not compare your timeline to others.** Your path includes grief, recovery, and rebuilding; that is valid and real.

> **Reminder:** You are not trying to prove you are "back to normal." You are building a career that supports the life you want now.

---

## Next Actions

1. **This week:** Reopen your DSA tracker and system-design notes. Commit to one 60-minute session.
2. **This month:** Initialize the Swiggy-style project repository and build one small feature end-to-end.
3. **Next quarter:** Complete the project MVP, run 2–3 mock interviews, and begin applying to 5–10 roles/week.
4. **Ongoing:** Keep this document open whenever you feel directionless, overwhelmed, or impulsive about the career goal.

---

**Last updated:** September 2, 2026