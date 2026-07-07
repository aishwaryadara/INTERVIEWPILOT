# AI Live Interview Co-Pilot PRD

## Problem

Technical interviewers often run interviews under time pressure while trying to listen, evaluate, take notes, and think of effective follow-up questions. This leads to inconsistent evaluation, shallow evidence collection, weak interview notes, and avoidable bias.

The product helps interviewers conduct more structured, consistent, and evidence-backed interviews by providing real-time assistance during the interview and structured outputs after the interview.

## Target Users

- Technical interviewers who conduct coding, system design, behavioral, and role-specific interviews.
- Hiring managers who need consistent hiring signals across interview loops.
- Recruiters who coordinate interviews and need readable summaries.
- Engineering managers who review candidate evidence and make hiring recommendations.

## User Personas

### Technical Interviewer

Needs help capturing notes, asking strong follow-up questions, and mapping candidate responses to competencies without losing focus during the conversation.

### Hiring Manager

Needs consistent evidence across interviewers, comparable rubric scores, and concise summaries for hiring decisions.

### Recruiter

Needs interview status, summary visibility, and shareable artifacts for candidate follow-up and hiring committee coordination.

### Engineering Manager

Needs structured candidate signal across technical depth, communication, problem solving, ownership, collaboration, and role fit.

## MVP Features

- Authentication and organization-aware user model.
- Candidate creation and candidate profile.
- Interview scheduling and interview room.
- Live interview workspace with notes, transcript, and rubric panel.
- AI-generated follow-up question suggestions.
- AI-generated interview summary draft.
- Rubric-based competency scoring suggestions.
- Final interview report.

## Non-Goals

- The AI does not make final hiring decisions.
- The AI does not reject candidates automatically.
- The MVP does not replace ATS systems.
- The MVP does not include enterprise SSO on day one.
- The MVP does not support every interview format initially.
- The MVP does not provide legal compliance guarantees.

## Core User Journey

1. Interviewer signs up or joins an organization.
2. Interviewer creates or selects a candidate.
3. Interviewer schedules an interview with a role and interview type.
4. Interviewer starts the live interview room.
5. The system captures transcript segments and interviewer notes.
6. AI suggests context-aware follow-up questions.
7. Interviewer marks evidence against rubric competencies.
8. Interviewer ends the session.
9. AI generates a structured summary and score suggestions.
10. Interviewer reviews, edits, and finalizes the report.

## Success Metrics

- Interviewers complete reports faster than manual workflows.
- Interview summaries include clearer evidence and fewer vague statements.
- Interviewers use suggested follow-up questions during live sessions.
- Hiring managers report improved consistency across candidate evaluations.
- Users trust AI suggestions because they are editable and evidence-backed.

## Initial Domain Entities

- User
- Organization
- Candidate
- Interview
- InterviewSession
- TranscriptSegment
- AIInsight
- EvaluationRubric
- InterviewScore

## System Overview

The application has a frontend workspace for interviewers, a backend API for core business logic, a realtime Socket.IO layer for live interview sessions, MongoDB for persistent data, Cloudinary for recordings, and AI services for transcription, follow-up generation, summarization, and scoring suggestions.

## Privacy And Security Considerations

- Require consent before recording or transcribing interviews.
- Store authentication secrets outside source control.
- Protect organization data with role-based access control.
- Avoid exposing candidate data across organizations.
- Minimize sensitive data sent to AI providers.
- Maintain audit logs for critical actions.
- Encrypt data in transit and use secure storage providers.

## AI Safety Considerations

- AI outputs are suggestions, not decisions.
- AI-generated evaluations must cite evidence from the transcript or notes.
- Interviewers can edit or reject AI-generated summaries and scores.
- Bias warnings should be framed as review prompts, not accusations.
- Final hiring recommendations should remain human-owned.

## Open Questions

- Which interview type should the MVP support first: coding, system design, behavioral, or mixed?
- Should candidates see or consent through a candidate-facing page?
- How long should transcripts and recordings be retained?
- What rubric should ship as the default?
- Should realtime transcription be browser-based, server-streamed, or upload-based in the MVP?

