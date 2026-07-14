# Screen Map

## MVP Routes

/auth/login  
/auth/register  
/dashboard  
/candidates  
/candidates/:id  
/interviews/new  
/interviews/:id/live  
/interviews/:id/report  
/settings

## Primary Navigation

- Dashboard
- Candidates
- Interviews
- Reports
- Settings

## Screen Responsibilities

### Login

Authenticates existing users.

### Register

Creates a user account and organization workspace.

### Dashboard

Shows upcoming interviews, recent candidates, and pending reports.

Primary actions:

- Start interview
- Create candidate
- Schedule interview
- Open pending report

### Candidates

Lets users create, search, and open candidate profiles.

Primary actions:

- Create candidate
- Search candidate
- Open candidate profile

### Candidate Profile

Shows candidate details, interview history, and hiring context.

Primary actions:

- Schedule interview
- Open interview report
- Update candidate details

### Schedule Interview

Creates an interview with candidate, interview type, interviewer, time, and rubric.

Primary actions:

- Select interview type
- Select interviewer
- Select time
- Create interview

### Live Interview Room

Runs the live interview with transcript, notes, AI suggestions, and rubric scoring.

Primary actions:

- Start or stop transcription
- Write notes
- Use AI suggestion
- Score rubric
- End interview

### Interview Report

Lets users review, edit, and finalize the interview report.

Primary actions:

- Edit summary
- Adjust scores
- Add recommendation
- Finalize report

### Settings

Manages account and organization basics.