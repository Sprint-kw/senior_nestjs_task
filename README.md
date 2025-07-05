
# Senior NestJS Developer Task

## 1. Product Overview

You are building a **real-time question-and-answer platform** for mobile and web users using NestJS. Users can ask questions, provide answers, and interact in real-time.

### Core User Interactions

1. **Post Questions** with:
    - Title
    - Description
    - Tags (e.g., `technology`, `health`, `education`, etc.)

2. **Provide Answers** to posted questions.
3. **Vote** (upvote/downvote) on answers.
4. **Mark answers as "Accepted"** (only question poster).
5. **Real-time Notifications**: Users are notified when their questions receive answers or votes.

### System Scale & Performance

- High concurrency and real-time interactions.
- Efficient handling of large volumes of questions, answers, and interactions.
- Fast query performance.

---

## 2. Core Requirements

Implement the following endpoints, optimized for scale and concurrency:

### 2.1 Create a Question

- **Endpoint**: `POST /questions`
- **Body**:
```json
{
    "title": "How to implement WebSockets in NestJS?",
    "description": "I need guidance on best practices for WebSockets.",
    "tags": ["nestjs", "websockets"]
}
```

---

### 2.2 Retrieve Questions

- **Endpoint**: `GET /questions`
- **Query Parameters**:
  - `tag` (optional)
  - `page`, `limit` (pagination)

---

### 2.3 Answer a Question

- **Endpoint**: `POST /questions/{id}/answers`
- **Body**:
```json
{
    "userId": 999,
    "content": "You can use the @nestjs/websockets package and Gateway."
}
```

---

### 2.4 Vote on an Answer

- **Endpoint**: `POST /answers/{id}/vote`
- **Body**:
```json
{
    "userId": 999,
    "voteType": "upvote"
}
```

---

### 2.5 Mark Answer as Accepted

- **Endpoint**: `POST /answers/{id}/accept`
- **Body**:
```json
{
    "userId": 999
}
```

---

### 2.6 Real-time Notifications

- Integrate WebSockets to notify users of new answers, votes, or accepted answers instantly.

---

## 3. Additional Technical Requirements

### 3.1 Database & Scalability
- Use PostgreSQL with TypeORM or Prisma.

### 3.2 Caching
- Use Redis for caching popular queries.

### 3.3 Real-time Features
- Implement WebSocket Gateway for notifications using NestJS WebSockets.

### 3.4 Rate Limiting & Security
- Rate limit critical endpoints (e.g., posting questions and answers).
- Implement JWT-based authentication.

### 3.5 Observability
- Expose system metrics (`/metrics`) compatible with Prometheus.

### 3.6 Testing
- Unit tests for core logic.
- Integration tests covering the entire flow (posting questions, answers, notifications).

### 3.7 Dockerization
- Provide a complete `docker-compose.yml` to deploy:
  - NestJS service
  - PostgreSQL database
  - Redis cache
  - Prometheus

### 3.8 Documentation
- Include detailed API docs and architectural explanations.
- Performance considerations and trade-offs documented.

### 3.9 Future Growth
- Describe strategies for scaling the platform to handle millions of users.
- Outline potential refactoring points or technical debt.

---

## 4. Bonus
- Implement an event-driven architecture with message queues (RabbitMQ or Kafka) for analytics or notifications.

---

## 5. Prioritization & Evaluation
You are evaluated on:
- Architectural clarity and scalability.
- Real-time implementation correctness.
- Efficient database and caching strategy.
- Testing robustness.
- Quality of documentation and technical reasoning.

---

# Deliverables

- Source code in a GitHub repository (NestJS, TypeScript).
- Database schema (migration scripts).
- Docker Compose file.
- Testing suite (unit and integration tests).
- Documentation (`README.md`).
