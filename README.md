# NestJS Developer Task

## Overview
Create a basic question-and-answer (Q&A) platform using NestJS with mocked backend data.

## Features
- **Questions**:
  - Users can create questions with a title, description, and tags.
  - Retrieve a list of questions with pagination.
  - Optional filtering of questions by tags.

- **Answers**:
  - Users can post answers to questions.
  - Users can vote (upvote/downvote) on answers.
  - Question creators can mark answers as accepted.

## Technical Requirements
- Use NestJS framework with TypeScript.
- Set up a PostgreSQL database using Prisma or TypeORM.
- Implement basic rate limiting on critical API endpoints (creating questions, posting answers).
- Optionally implement basic caching with Redis.
- Dockerize the NestJS application for easy deployment.
- Provide a Docker-compose setup including NestJS, PostgreSQL, and Redis (if caching is used).
- Write unit and basic integration tests for core functionality.

## Deliverables
- Provide a GitHub repository link containing your code.
- Include a README file with clear setup instructions and API endpoint documentation.
- Docker-compose file for easy setup and deployment.
