# LLD Track (Low-Level Design)

## Objective

Master **20 LLD problems** (10 frequent + 10 unique) with ability to design clean, extensible class-level architectures.

## Weekly Target

- **Weeks 1-4**: Learn OOP fundamentals, practice 1 LLD problem/week
- **Weeks 5-8**: Practice 1-2 LLD problems/week
- **Weeks 9-12**: Practice 1-2 LLD problems/week (mock interviews)
- **Weeks 13-16**: Review and master all 20 problems

---

## LLD Fundamentals (Weeks 1-4)

### OOP Principles

1. **Encapsulation**
   - Hide internal state
   - Expose behavior through methods
   - Use access modifiers (private, protected, public)

2. **Inheritance vs Composition**
   - Prefer composition over inheritance
   - Use inheritance for "is-a" relationships
   - Use composition for "has-a" relationships

3. **Abstraction**
   - Define interfaces/abstract classes
   - Hide implementation details
   - Focus on what, not how

4. **Polymorphism**
   - Method overriding
   - Interface implementation
   - Runtime binding

---

### SOLID Principles

1. **Single Responsibility Principle (SRP)**
   - A class should have one reason to change
   - One responsibility per class

2. **Open/Closed Principle (OCP)**
   - Open for extension
   - Closed for modification
   - Use interfaces, abstract classes, strategy pattern

3. **Liskov Substitution Principle (LSP)**
   - Subtypes must be substitutable for base types
   - Don't break base class contracts

4. **Interface Segregation Principle (ISP)**
   - Many small, specific interfaces
   - Avoid fat interfaces
   - Clients shouldn't depend on unused methods

5. **Dependency Inversion Principle (DIP)**
   - Depend on abstractions, not concretions
   - Inject dependencies
   - Use interfaces for loose coupling

---

### Design Patterns

#### Creational Patterns

1. **Singleton**
   - One instance per JVM
   - Thread-safe implementation
   - Use for: configuration, logging, cache

2. **Factory / Abstract Factory**
   - Object creation encapsulation
   - Family of related objects
   - Use for: database connections, UI components

3. **Builder**
   - Complex object construction
   - Fluent API
   - Use for: SQL queries, HTTP requests

4. **Prototype**
   - Clone existing objects
   - Use for: expensive object creation

---

#### Structural Patterns

1. **Adapter**
   - Incompatible interface compatibility
   - Use for: legacy system integration

2. **Facade**
   - Simplified interface to complex subsystem
   - Use for: API gateways, service layers

3. **Decorator**
   - Add behavior dynamically
   - Use for: logging, caching, validation

4. **Proxy**
   - Control access to object
   - Use for: lazy loading, access control

5. **Composite**
   - Tree structure of objects
   - Use for: file systems, UI components

---

#### Behavioral Patterns

1. **Strategy**
   - Family of algorithms
   - Interchangeable at runtime
   - Use for: payment methods, sorting algorithms

2. **Observer**
   - One-to-many dependency
   - Automatic notification
   - Use for: event listeners, pub/sub

3. **State**
   - Object changes behavior based on state
   - Use for: order lifecycle, game states

4. **Command**
   - Encapsulate request as object
   - Use for: undo/redo, macro commands

5. **Chain of Responsibility**
   - Pass request through chain of handlers
   - Use for: approval workflows, logging

---

## 20 LLD Problems

### FREQUENT PROBLEMS (10)

#### 1. Design Parking Lot System

**Requirements:**
- Multiple floors, parking spots
- Different vehicle types (car, bike, truck)
- Spot allocation strategy
- Payment processing
- Entry/exit tracking

**Key Classes:**
- `ParkingLot` (singleton)
- `Floor`, `ParkingSpot`
- `Vehicle` (abstract), `Car`, `Bike`, `Truck`
- `Ticket`, `Payment`
- `ParkingStrategy` (interface)

**Patterns:**
- Singleton (ParkingLot)
- Strategy (parking allocation)
- Factory (vehicle creation)

**Practice:** Week 3, Week 12

---

#### 2. Design Elevator System

**Requirements:**
- Multiple elevators
- Floor requests (up/down)
- Elevator state management
- Optimal scheduling

**Key Classes:**
- `ElevatorController`
- `Elevator`, `ElevatorState`
- `Request`, `Direction`
- `ElevatorScheduler`

**Patterns:**
- State pattern (elevator states)
- Strategy (scheduling algorithm)
- Observer (request notification)

**Practice:** Week 6, Week 13

---

#### 3. Design Library Management System

**Requirements:**
- Book catalog management
- User checkout/return
- Fine calculation
- Search functionality

**Key Classes:**
- `Library`, `Book`, `BookItem`
- `User`, `Librarian`, `Member`
- `Checkout`, `Return`, `Fine`
- `SearchStrategy`

**Patterns:**
- Repository pattern (book storage)
- Strategy (search algorithms)
- Observer (overdue notifications)

**Practice:** Week 4, Week 14

---

#### 4. Design ATM Machine

**Requirements:**
- Card validation
- PIN verification
- Balance inquiry
- Cash withdrawal
- Transaction logging

**Key Classes:**
- `ATM`, `Card`, `Account`
- `Transaction`, `Withdrawal`, `Deposit`
- `CashDispenser`, `CardReader`
- `ATMState`

**Patterns:**
- State pattern (ATM states)
- Strategy (transaction types)
- Factory (transaction creation)

**Practice:** Week 7, Week 15

---

#### 5. Design Splitwise / Expense Sharing

**Requirements:**
- User groups
- Expense splitting (equal, exact, percentage)
- Balance calculation
- Debt simplification

**Key Classes:**
- `User`, `Group`, `Expense`
- `Split` (abstract), `EqualSplit`, `ExactSplit`, `PercentSplit`
- `Balance`, `Transaction`
- `Graph` (for debt simplification)

**Patterns:**
- Strategy (split types)
- Observer (balance updates)
- Factory (split creation)

**Practice:** Week 5, Week 11

---

#### 6. Design Tic-Tac-Toe Game

**Requirements:**
- 3x3 board
- Two players (X, O)
- Win condition checking
- Turn management

**Key Classes:**
- `Board`, `Cell`, `Player`
- `Game`, `GameStatus`
- `Move`, `WinStrategy`

**Patterns:**
- Strategy (win checking)
- State pattern (game states)

**Practice:** Week 3, Week 12

---

#### 7. Design Chess Game

**Requirements:**
- 8x8 board
- Piece movement rules
- Check, checkmate detection
- Turn management

**Key Classes:**
- `Board`, `Square`, `Piece` (abstract)
- `King`, `Queen`, `Rook`, `Bishop`, `Knight`, `Pawn`
- `Player`, `Game`, `Move`
- `MoveValidator`

**Patterns:**
- Strategy (piece movement)
- Command (move execution)
- Factory (piece creation)

**Practice:** Week 6, Week 13

---

#### 8. Design Hotel/Room Booking System

**Requirements:**
- Room inventory
- Date-based availability
- Booking lifecycle
- Cancellation policy

**Key Classes:**
- `Hotel`, `Room`, `RoomType`
- `Booking`, `BookingStatus`
- `User`, `Payment`
- `PricingStrategy`

**Patterns:**
- State pattern (booking states)
- Strategy (pricing, cancellation)
- Factory (booking creation)

**Practice:** Week 9, Week 14

---

#### 9. Design Logging System

**Requirements:**
- Multiple log levels (DEBUG, INFO, WARN, ERROR)
- Multiple appenders (console, file, remote)
- Thread-safe logging
- Log rotation

**Key Classes:**
- `Logger`, `LogLevel`, `LogMessage`
- `Appender` (interface), `ConsoleAppender`, `FileAppender`
- `LogFormatter`
- `LogManager`

**Patterns:**
- Strategy (appenders, formatters)
- Singleton (Logger, LogManager)
- Chain of Responsibility (log levels)

**Practice:** Week 4, Week 10

---

#### 10. Design Rate Limiter

**Requirements:**
- Token bucket algorithm
- Sliding window algorithm
- User-based rate limiting
- Distributed rate limiting (optional)

**Key Classes:**
- `RateLimiter`, `RateLimitConfig`
- `TokenBucket`, `SlidingWindow`
- `UserQuota`, `Request`

**Patterns:**
- Strategy (rate limiting algorithms)
- Factory (algorithm selection)

**Practice:** Week 9, Week 11

---

### UNIQUE PROBLEMS (10)

#### 11. Design Vending Machine with Coin Change

**Requirements:**
- Product inventory
- Coin insertion and validation
- Change calculation
- State transitions

**Key Classes:**
- `VendingMachine`, `Product`, `Inventory`
- `Coin`, `CoinDenomination`
- `VendingState` (Idle, HasMoney, Dispensing)
- `ChangeCalculator`

**Patterns:**
- State pattern (vending states)
- Strategy (change calculation)

**Practice:** Week 13

---

#### 12. Design Restaurant Reservation System with Waitlist

**Requirements:**
- Table management
- Time slot booking
- Waitlist with priority
- Notification on availability

**Key Classes:**
- `Restaurant`, `Table`, `Reservation`
- `TimeSlot`, `WaitlistEntry`
- `NotificationService`
- `PriorityQueue`

**Patterns:**
- Observer (waitlist notifications)
- Strategy (table allocation)

**Practice:** Week 15

---

#### 13. Design Traffic Signal System

**Requirements:**
- Multiple signals (red, yellow, green)
- Timer-based transitions
- Emergency override
- Pedestrian crossing

**Key Classes:**
- `TrafficSignal`, `SignalState`
- `Timer`, `SignalController`
- `EmergencyOverride`, `PedestrianCrossing`

**Patterns:**
- State pattern (signal states)
- Observer (state change notifications)

**Practice:** Week 11, Week 16

---

#### 14. Design Conference Room Scheduler with Conflict Resolution

**Requirements:**
- Room booking
- Recurring meetings
- Conflict detection
- Calendar integration

**Key Classes:**
- `ConferenceRoom`, `Booking`, `TimeSlot`
- `User`, `Meeting`
- `ConflictResolver`, `Calendar`

**Patterns:**
- Strategy (conflict resolution)
- Observer (booking notifications)

**Practice:** Week 14

---

#### 15. Design Online Auction System (eBay-like)

**Requirements:**
- Product listing
- Bidding mechanism
- Time-based closure
- Winner selection

**Key Classes:**
- `Auction`, `Product`, `Bid`
- `User`, `AuctionStatus`
- `BidStrategy`, `WinnerSelector`

**Patterns:**
- Observer (bid notifications)
- Strategy (bidding strategies)

**Practice:** Week 12, Week 16

---

#### 16. Design Music Streaming Library (Spotify-like)

**Requirements:**
- Song/album/artist management
- Playlist creation
- Search and filtering
- User preferences

**Key Classes:**
- `Song`, `Album`, `Artist`, `Playlist`
- `User`, `MusicLibrary`
- `SearchStrategy`, `RecommendationEngine`

**Patterns:**
- Strategy (search, recommendations)
- Observer (playlist updates)

**Practice:** Week 15

---

#### 17. Design Cricket Scoreboard

**Requirements:**
- Match types (T20, ODI, Test)
- Live score updates
- Player statistics
- Commentary engine

**Key Classes:**
- `Match`, `Team`, `Player`
- `Innings`, `Over`, `Ball`
- `Scorecard`, `Commentary`

**Patterns:**
- Strategy (match types)
- Observer (score updates)

**Practice:** Week 13

---

#### 18. Design Stock Exchange Order Matching System

**Requirements:**
- Buy/sell orders
- Price-time priority matching
- Partial fills
- Trade execution

**Key Classes:**
- `Order`, `OrderType` (BUY, SELL)
- `OrderBook`, `MatchingEngine`
- `Trade`, `Stock`

**Patterns:**
- Strategy (matching algorithms)
- Observer (trade notifications)

**Practice:** Week 11, Week 16

---

#### 19. Design Airline Reservation with Seat Selection

**Requirements:**
- Flight inventory
- Seat map and selection
- Class types (economy, business)
- Meal preferences

**Key Classes:**
- `Flight`, `Seat`, `SeatMap`
- `Reservation`, `Passenger`
- `PricingStrategy`, `MealPreference`

**Patterns:**
- Strategy (pricing, seat allocation)
- State pattern (reservation states)

**Practice:** Week 14

---

#### 20. Design Movie Ticket Booking with Dynamic Pricing

**Requirements:**
- Show timings
- Seat selection
- Dynamic pricing (demand-based)
- Cancellation and refund

**Key Classes:**
- `Movie`, `Show`, `Theater`
- `Seat`, `Booking`, `BookingStatus`
- `PricingStrategy`, `RefundPolicy`

**Patterns:**
- Strategy (pricing, refund)
- State pattern (booking lifecycle)

**Practice:** Week 12, Week 16

---

## LLD Practice Methodology

### Problem-Solving Framework (60-90 minutes)

1. **Requirements clarification (5-10 min)**
   - Functional requirements
   - Non-functional requirements (extensibility, testability)

2. **Identify entities and relationships (10-15 min)**
   - Core classes
   - Relationships (inheritance, composition, association)

3. **Draw class diagram (10-15 min)**
   - Classes, attributes, methods
   - Interfaces, abstract classes
   - Relationships (UML notation)

4. **Implement key classes (30-40 min)**
   - Core business logic
   - Design patterns
   - Clean code principles

5. **Discuss extensions (5-10 min)**
   - Future requirements
   - Trade-offs
   - Testing strategy

### Weekly Practice Schedule

- **Weeks 1-4**: 1 LLD problem/week (OOP fundamentals focus)
- **Weeks 5-8**: 1-2 LLD problems/week (design patterns focus)
- **Weeks 9-12**: 1-2 LLD problems/week (mock interviews)
- **Weeks 13-16**: Review all 20 problems, focus on weak areas

### Resources

- **Books**: "Head First Design Patterns", "Clean Code"
- **YouTube**: Gaurav Sen LLD, System Design Interview LLD
- **Practice**: LeetCode Discuss, GitHub LLD repositories

### Success Metrics

- **Week 4**: Comfortable with 3-4 basic LLD problems
- **Week 8**: Can design 8-10 systems with clean class diagrams
- **Week 12**: Confident with all frequent problems
- **Week 16**: Master all 20 problems, can explain patterns and trade-offs
