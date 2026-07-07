# ADR-001: Product Scope For MVP

## Status

Accepted

## Context

The project could grow into many areas: applicant tracking, coding assessments, video interviewing, autonomous interviews, analytics, candidate portals, and enterprise hiring operations. Starting too broadly would create a shallow product that looks impressive but does not solve one painful workflow well.

## Decision

The MVP will focus on the technical interviewer workflow:

- Create candidate.
- Schedule interview.
- Run live interview room.
- Capture transcript and notes.
- Suggest follow-up questions.
- Generate structured summary.
- Suggest rubric-based scores.
- Let the interviewer review and finalize the report.

The AI will assist but not make final hiring decisions.

## Consequences

- The product remains focused on interviewer productivity and evaluation quality.
- The first version can be built with clear architecture and a credible user journey.
- Future ATS, analytics, notifications, and enterprise features can be added after the core workflow works.

