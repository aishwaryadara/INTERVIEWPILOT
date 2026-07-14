# User Stories

## Technical Interviewer

### View Interview Day

As a technical interviewer, I want to see upcoming interviews, so that I can prepare for the right candidate and interview type.

Acceptance criteria:

- Dashboard shows upcoming interviews for the current organization.
- Each interview shows candidate name, role, interview type, and scheduled time.
- Empty dashboard shows actions to create a candidate or schedule an interview.

### Create Candidate

As a technical interviewer, I want to create a candidate profile, so that interviews and reports are attached to the correct person.

Acceptance criteria:

- Valid candidate data creates a candidate.
- Missing required fields show field-level errors.
- Candidate records are scoped to the user's organization.

### Schedule Interview

As a technical interviewer, I want to schedule an interview, so that the session has a candidate, interview type, time, interviewer, and rubric.

Acceptance criteria:

- Interviewer can choose candidate, interview type, date, time, and rubric.
- Scheduled interview appears on the candidate profile.
- Unauthorized users cannot schedule interviews.

### Start Live Interview

As a technical interviewer, I want to start a live interview room, so that I can use transcript, notes, rubric, and AI suggestions in one workspace.

Acceptance criteria:

- Starting a scheduled interview creates a live session.
- Interview room shows candidate context, notes, transcript, AI suggestions, and rubric.
- Transcription status is visible.

### Receive Follow-Up Suggestions

As a technical interviewer, I want AI-generated follow-up questions, so that I can probe candidate responses more deeply.

Acceptance criteria:

- AI suggests follow-ups after enough transcript context exists.
- Suggestions can be used, edited, dismissed, or regenerated.
- Used suggestions are tracked for later product analytics.

### Generate Interview Report

As a technical interviewer, I want an AI-generated report draft, so that I can submit a strong evaluation faster.

Acceptance criteria:

- Report contains summary, strengths, concerns, scores, and evidence.
- Interviewer can edit AI-generated content.
- Final report is shared only with authorized users.