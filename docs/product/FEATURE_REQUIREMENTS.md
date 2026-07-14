# Feature Requirements

## Dashboard

Requirements:

- Show upcoming interviews.
- Show recent candidates.
- Show pending reports.
- Provide quick actions for candidate creation and scheduling.

API contract:

GET /api/dashboard

Security:

- Require authentication.
- Return only organization-scoped data.
- Filter results by user role.

## Candidate Management

Requirements:

- Create candidate.
- List candidates.
- View candidate profile.
- View interview history.

API contracts:

GET /api/candidates  
POST /api/candidates  
GET /api/candidates/:candidateId

Backend logic:

- Validate candidate DTO.
- Attach organizationId from authenticated user.
- Prevent cross-organization access.

## Interview Scheduling

Requirements:

- Select candidate.
- Select interviewer.
- Select interview type.
- Select scheduled time.
- Attach rubric template.

API contract:

POST /api/interviews

## Live Interview Room

Requirements:

- Start interview session.
- Join Socket.IO room.
- Show candidate context.
- Show transcript.
- Capture notes.
- Suggest AI follow-up questions.
- Score rubric competencies.
- End interview.

Socket events:

- session:join
- transcript:new
- ai:suggestion:new
- note:updated
- rubric:scoreUpdated
- session:ended

## Interview Report

Requirements:

- Generate AI summary draft.
- Show strengths, concerns, evidence, and score suggestions.
- Allow interviewer edits.
- Finalize report.