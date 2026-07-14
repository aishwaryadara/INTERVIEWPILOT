# Interview Room UX

## Goal

The interview room is the flagship product surface. It helps the interviewer listen, probe, capture evidence, and complete a structured evaluation without letting AI take over the conversation.

## Layout

Top Bar:

- Candidate name
- Interview type
- Timer
- Recording or transcription status
- End interview action

Left Panel:

- Candidate summary
- Role context
- Interview plan
- Key competencies

Center Panel:

- Live transcript
- Interviewer notes

Right Panel:

- AI follow-up suggestions
- Rubric scoring
- Evidence markers

## Transcript Panel

Requirements:

- Show speaker label.
- Show timestamp.
- Append transcript segments in order.
- Preserve transcript after refresh.
- Show a clear failure state if transcription fails.

Example transcript segment:

12:04 Candidate  
I would shard by organization ID because most queries are tenant-scoped.

## Notes Panel

Requirements:

- Autosave notes.
- Show saved or unsaved state.
- Keep typing fast.
- Support bullet notes.

## AI Follow-Up Panel

Each suggestion should include:

- Question
- Target competency
- Reason
- Actions: Use, Edit, Dismiss, Regenerate

Example suggestion:

Question: What trade-offs would change if this system needed to support 10x more traffic?

Target competency: Scalability

Reason: The candidate described the initial design but did not discuss growth constraints.

## Rubric Panel

Initial competencies:

- Problem solving
- Technical depth
- Communication
- Systems thinking
- Ownership

Score scale:

1 - Insufficient signal  
2 - Below expectations  
3 - Meets expectations  
4 - Above expectations  
5 - Exceptional

## AI Workflow

1. Transcript segment arrives.
2. Backend stores the segment.
3. Recent context is summarized or compacted.
4. AI service evaluates whether a follow-up is useful.
5. Backend emits a new AI suggestion event.
6. UI displays the suggestion.
7. Interviewer uses, edits, dismisses, or regenerates.

## Security Considerations

- Require authenticated user before joining session room.
- Verify user belongs to the interview organization.
- Prevent users from joining arbitrary Socket.IO rooms.
- Protect private notes.
- Require recording or transcription consent.

## Performance Considerations

- Debounce note autosave.
- Limit transcript payload size.
- Rate limit AI suggestion generation.
- Avoid re-rendering the entire transcript on each new segment.

## Code Review Checklist

- Can the interviewer run the session without leaving the interview room?
- Are transcription and recording states visible?
- Are AI suggestions actionable?
- Can AI suggestions be dismissed?
- Are notes autosaved without blocking typing?
- Is organization access enforced before Socket.IO room join?
- Are transcript events ordered and timestamped?
- Is AI output clearly a suggestion, not a decision?