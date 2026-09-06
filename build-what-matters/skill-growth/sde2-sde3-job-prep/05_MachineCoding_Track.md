# Machine Coding Track

## Objective

Master **30 machine coding problems** (20 frequent + 10 unique) with ability to write fully working, clean code under time pressure.

## Weekly Target

- **Weeks 1-4**: Practice 1 machine coding problem/week (focus on clean code)
- **Weeks 5-8**: Practice 1-2 machine coding problems/week (focus on speed)
- **Weeks 9-12**: Practice 2 machine coding problems/week (mock interviews)
- **Weeks 13-16**: Review and master all 30 problems

---

## Machine Coding Fundamentals (Weeks 1-4)

### What is Machine Coding?

Machine coding rounds test your ability to:
- Write **fully working, compilable code** under time pressure
- Design clean class structure
- Handle edge cases and errors
- Write basic tests
- Explain your design decisions

### Evaluation Criteria

1. **Code Correctness (40%)**
   - Compiles and runs
   - Handles all requirements
   - Edge cases covered

2. **Code Quality (30%)**
   - Clean, readable code
   - Good naming conventions
   - Proper separation of concerns

3. **Design (20%)**
   - Clean class structure
   - Appropriate use of patterns
   - Extensibility

4. **Testing (10%)**
   - Basic test coverage
   - Edge case testing

---

### Time Management Strategy

| Time | Activity |
|------|----------|
| 0-10 min | Understand requirements, clarify doubts |
| 10-20 min | Design class structure, write method signatures |
| 20-70 min | Implement core functionality |
| 70-80 min | Test with sample inputs, fix bugs |
| 80-90 min | Code cleanup, add comments, prepare explanation |

---

## 30 Machine Coding Problems

### FREQUENT PROBLEMS (20)

#### 1. LRU Cache Implementation

**Requirements:**
- `get(key)` → O(1)
- `put(key, value)` → O(1)
- Evict least recently used when capacity exceeded
- Thread-safe (optional)

**Key Classes:**
- `LRUCache<K, V>`
- `Node<K, V>` (doubly linked list)
- `HashMap<K, Node>`

**Time Limit:** 30-45 minutes

**Practice:** Week 2, Week 10

---

#### 2. Parking Lot System

**Requirements:**
- Multiple floors, parking spots
- Different vehicle types
- Entry/exit tracking
- Payment calculation

**Key Classes:**
- `ParkingLot`, `Floor`, `ParkingSpot`
- `Vehicle`, `Car`, `Bike`, `Truck`
- `Ticket`, `Payment`

**Time Limit:** 60-90 minutes

**Practice:** Week 3, Week 12

---

#### 3. Snake and Ladder Game

**Requirements:**
- Board with snakes and ladders
- Dice roll mechanism
- Multiple players
- Win condition

**Key Classes:**
- `Board`, `Cell`, `Snake`, `Ladder`
- `Player`, `Dice`
- `Game`, `GameStatus`

**Time Limit:** 45-60 minutes

**Practice:** Week 4, Week 8

---

#### 4. Tic-Tac-Toe Game

**Requirements:**
- 3x3 board
- Two players (X, O)
- Win condition checking
- Turn management

**Key Classes:**
- `Board`, `Cell`, `Player`
- `Game`, `GameStatus`
- `Move`

**Time Limit:** 30-45 minutes

**Practice:** Week 4, Week 12

---

#### 5. Splitwise / Expense Manager

**Requirements:**
- Add users to groups
- Add expenses with split strategies
- Calculate balances
- Settle debts

**Key Classes:**
- `User`, `Group`, `Expense`
- `Split` (abstract), `EqualSplit`, `ExactSplit`, `PercentSplit`
- `Balance`, `Transaction`

**Time Limit:** 60-75 minutes

**Practice:** Week 5, Week 9

---

#### 6. Logger Framework (Console, File, Remote)

**Requirements:**
- Multiple log levels (DEBUG, INFO, WARN, ERROR)
- Multiple appenders (console, file, remote)
- Thread-safe logging
- Configuration

**Key Classes:**
- `Logger`, `LogLevel`, `LogMessage`
- `Appender` (interface), `ConsoleAppender`, `FileAppender`
- `LogFormatter`

**Time Limit:** 45-60 minutes

**Practice:** Week 7, Week 12

---

#### 7. Rate Limiter (Token Bucket / Sliding Window)

**Requirements:**
- Token bucket algorithm
- Sliding window algorithm
- User-based rate limiting
- Thread-safe

**Key Classes:**
- `RateLimiter`, `RateLimitConfig`
- `TokenBucket`, `SlidingWindow`
- `UserQuota`, `Request`

**Time Limit:** 45-60 minutes

**Practice:** Week 8, Week 11

---

#### 8. Meeting Room Scheduler

**Requirements:**
- Book meeting rooms
- Time slot management
- Conflict detection
- Recurring meetings (optional)

**Key Classes:**
- `ConferenceRoom`, `Booking`, `TimeSlot`
- `User`, `Meeting`
- `ConflictResolver`

**Time Limit:** 45-60 minutes

**Practice:** Week 9, Week 14

---

#### 9. In-Memory Key-Value Store

**Requirements:**
- `set(key, value, ttl)`
- `get(key)`
- `delete(key)`
- TTL expiry
- Thread-safe

**Key Classes:**
- `KeyValueStore<K, V>`
- `Entry<K, V>`
- `ExpiryManager`

**Time Limit:** 45-60 minutes

**Practice:** Week 10, Week 14

---

#### 10. Elevator System Simulation

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

**Time Limit:** 75-90 minutes

**Practice:** Week 6, Week 13

---

#### 11. Library Management System

**Requirements:**
- Book catalog management
- User checkout/return
- Fine calculation
- Search functionality

**Key Classes:**
- `Library`, `Book`, `BookItem`
- `User`, `Librarian`, `Member`
- `Checkout`, `Return`, `Fine`

**Time Limit:** 60-75 minutes

**Practice:** Week 6, Week 11

---

#### 12. Movie Ticket Booking System

**Requirements:**
- Show timings
- Seat selection
- Booking lifecycle
- Payment integration

**Key Classes:**
- `Movie`, `Show`, `Theater`
- `Seat`, `Booking`, `BookingStatus`
- `User`, `Payment`

**Time Limit:** 60-75 minutes

**Practice:** Week 12, Week 16

---

#### 13. Chess Game (Basic moves and checkmate)

**Requirements:**
- 8x8 board
- Piece movement rules
- Check, checkmate detection
- Turn management

**Key Classes:**
- `Board`, `Square`, `Piece` (abstract)
- `King`, `Queen`, `Rook`, `Bishop`, `Knight`, `Pawn`
- `Player`, `Game`, `Move`

**Time Limit:** 90-120 minutes

**Practice:** Week 6, Week 13

---

#### 14. Vending Machine

**Requirements:**
- Product inventory
- Coin insertion and validation
- Change calculation
- State transitions

**Key Classes:**
- `VendingMachine`, `Product`, `Inventory`
- `Coin`, `CoinDenomination`
- `VendingState`, `ChangeCalculator`

**Time Limit:** 60-75 minutes

**Practice:** Week 11, Week 14

---

#### 15. Task Scheduler / To-Do List

**Requirements:**
- Add/remove/edit tasks
- Priority management
- Due dates
- Status tracking (pending/done)

**Key Classes:**
- `Task`, `TaskStatus`, `Priority`
- `TaskManager`, `User`

**Time Limit:** 30-45 minutes

**Practice:** Week 10

---

#### 16. ATM Machine Simulation

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

**Time Limit:** 60-75 minutes

**Practice:** Week 7, Week 15

---

#### 17. Sudoku Solver

**Requirements:**
- Solve 9x9 Sudoku board
- Backtracking algorithm
- Constraint checking
- Board validation

**Key Classes:**
- `SudokuBoard`, `Cell`
- `SudokuSolver`, `Validator`

**Time Limit:** 45-60 minutes

**Practice:** Week 10

---

#### 18. Calculator (Basic + Scientific)

**Requirements:**
- Basic operations (+, -, *, /)
- Scientific functions (sin, cos, log, exp)
- Expression parsing
- Operator precedence

**Key Classes:**
- `Calculator`, `Expression`
- `Operator`, `Operand`
- `ExpressionParser`

**Time Limit:** 30-45 minutes

**Practice:** Week 9

---

#### 19. Shopping Cart System

**Requirements:**
- Add/remove items
- Quantity update
- Discount/coupon application
- Checkout flow

**Key Classes:**
- `CartItem`, `Product`, `ShoppingCart`
- `Coupon`, `DiscountStrategy`
- `Checkout`, `Payment`

**Time Limit:** 45-60 minutes

**Practice:** Week 10

---

#### 20. Snake Game (Console/GUI)

**Requirements:**
- Grid-based movement
- Food spawn mechanism
- Collision detection
- Score tracking

**Key Classes:**
- `Snake`, `Food`, `Board`
- `Game`, `GameStatus`
- `Direction`

**Time Limit:** 45-60 minutes

**Practice:** Week 8

---

### UNIQUE PROBLEMS (10)

#### 21. File System Implementation (ls, cd, mkdir, touch)

**Requirements:**
- Tree structure for directories/files
- Commands: ls, cd, mkdir, touch, rm
- Path navigation (absolute/relative)
- File metadata

**Key Classes:**
- `FileSystem`, `Directory`, `File`
- `Path`, `Command`
- `CommandExecutor`

**Time Limit:** 60-75 minutes

**Practice:** Week 13

---

#### 22. Cricket Score Tracker with Commentary

**Requirements:**
- Live score updates
- Overs/balls tracking
- Wickets, runs
- Commentary engine

**Key Classes:**
- `Match`, `Team`, `Player`
- `Innings`, `Over`, `Ball`
- `Scorecard`, `Commentary`

**Time Limit:** 60-75 minutes

**Practice:** Week 13

---

#### 23. Traffic Signal Controller Simulation

**Requirements:**
- Multiple signals (red, yellow, green)
- Timer-based transitions
- Emergency override
- Pedestrian crossing

**Key Classes:**
- `TrafficSignal`, `SignalState`
- `Timer`, `SignalController`
- `EmergencyOverride`, `PedestrianCrossing`

**Time Limit:** 45-60 minutes

**Practice:** Week 11, Week 16

---

#### 24. Car Rental System with Pricing

**Requirements:**
- Car inventory
- Hourly/daily pricing
- Booking/return workflow
- Damage charges

**Key Classes:**
- `Car`, `CarType`, `RentalCompany`
- `Booking`, `RentalStatus`
- `PricingStrategy`, `DamageCharge`

**Time Limit:** 60-75 minutes

**Practice:** Week 14

---

#### 25. Restaurant Table Reservation System

**Requirements:**
- Table availability
- Time slot booking
- Wait queue management
- Party size handling

**Key Classes:**
- `Restaurant`, `Table`, `Reservation`
- `TimeSlot`, `WaitlistEntry`
- `NotificationService`

**Time Limit:** 60-75 minutes

**Practice:** Week 15

---

#### 26. Notification Service with Multiple Channels

**Requirements:**
- Multiple channels (Email, SMS, Push)
- Templates
- Retry/failure handling
- Priority queue

**Key Classes:**
- `Notification`, `NotificationChannel`
- `EmailNotification`, `SMSNotification`, `PushNotification`
- `NotificationService`, `Template`

**Time Limit:** 60-75 minutes

**Practice:** Week 11

---

#### 27. Leaderboard System (Top K scores)

**Requirements:**
- Add user scores
- Get top K scores
- Get user rank
- Real-time updates

**Key Classes:**
- `Leaderboard`, `UserScore`
- `MinHeap`, `RankCalculator`

**Time Limit:** 45-60 minutes

**Practice:** Week 11

---

#### 28. Autocomplete / Typeahead System (Trie-based)

**Requirements:**
- Trie data structure
- Prefix search
- Ranking by frequency
- Efficient insert/delete

**Key Classes:**
- `Trie`, `TrieNode`
- `Autocomplete`, `SearchResult`
- `FrequencyRanker`

**Time Limit:** 45-60 minutes

**Practice:** Week 12

---

#### 29. Distributed Lock Manager

**Requirements:**
- Lock acquire/release
- Timeout handling
- Deadlock prevention
- Distributed coordination

**Key Classes:**
- `LockManager`, `Lock`
- `LockRequest`, `LockStatus`
- `DeadlockDetector`

**Time Limit:** 75-90 minutes

**Practice:** Week 15

---

#### 30. Workflow Engine (State machine execution)

**Requirements:**
- State machine definition
- Transitions with guards
- Actions on transitions
- Workflow execution engine

**Key Classes:**
- `Workflow`, `State`, `Transition`
- `Guard`, `Action`
- `WorkflowEngine`, `ExecutionContext`

**Time Limit:** 75-90 minutes

**Practice:** Week 16

---

## Machine Coding Practice Methodology

### Problem-Solving Framework (90 minutes)

1. **Understand requirements (10 min)**
   - Read problem statement twice
   - Clarify doubts (if interviewer present)
   - Write down key requirements

2. **Design class structure (15 min)**
   - Identify core classes
   - Define method signatures
   - Plan relationships

3. **Implement core functionality (50 min)**
   - Start with simplest working solution
   - Add features incrementally
   - Keep code clean and readable

4. **Test and debug (10 min)**
   - Write test cases
   - Test with sample inputs
   - Fix bugs

5. **Code cleanup (5 min)**
   - Add comments
   - Improve naming
   - Prepare explanation

### Weekly Practice Schedule

- **Weeks 1-4**: 1 machine coding problem/week (focus on clean code)
- **Weeks 5-8**: 1-2 machine coding problems/week (focus on speed)
- **Weeks 9-12**: 2 machine coding problems/week (mock interviews)
- **Weeks 13-16**: Review all 30 problems, focus on weak areas

### Resources

- **GitHub**: machine-coding-problems, awesome-low-level-design
- **Practice**: LeetCode Discuss, Pramp, Interviewing.io
- **Books**: "Cracking the Coding Interview"

### Success Metrics

- **Week 4**: Can solve 3-4 basic problems in 60-90 minutes
- **Week 8**: Can solve 8-10 problems with clean code
- **Week 12**: Confident with all frequent problems
- **Week 16**: Master all 30 problems, can solve most in <60 minutes
