# System Overview

## High-Level Architecture

```txt
Frontend App
  React or Next.js
  TypeScript
  Tailwind CSS
  shadcn/ui
  Socket.IO Client

Backend API
  Node.js
  Express.js
  REST APIs
  JWT authentication
  DTO validation
  Service layer
  Repository layer

Realtime Layer
  Socket.IO
  Interview rooms
  Transcript events
  AI insight events

Database
  MongoDB Atlas
  Mongoose models

AI Services
  Transcription workflow
  Follow-up generation
  Summary generation
  Rubric score suggestions

Storage
  Cloudinary for recordings

Infrastructure
  Vercel frontend
  Render or Railway backend
  GitHub Actions CI/CD
  Docker
  Sentry
```

## Backend Layering

```txt
Route -> Controller -> Service -> Repository -> Database
```

### Routes

Define HTTP endpoints and attach middleware.

### Controllers

Parse request data, call services, and return HTTP responses.

### Services

Own business logic and orchestration.

### Repositories

Own database queries and persistence details.

### Shared Layer

Contains reusable errors, logger, validation helpers, constants, and DTO schemas.

## Realtime vs Async Work

### Realtime

- Interview session status.
- Transcript segment updates.
- Follow-up suggestions.
- Live AI insights.

### Async

- Recording upload.
- Long-form transcription.
- Final interview summary.
- PDF report generation.
- Analytics aggregation.

## Security Baseline

- JWT authentication.
- Role-based access control.
- Organization-scoped queries.
- Request validation.
- Rate limiting.
- Secure environment variable handling.
- Audit logs for sensitive actions.

