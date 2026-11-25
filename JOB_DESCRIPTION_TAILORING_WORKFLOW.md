# One-Step Resume Tailoring Workflow

## Goal
Tailor a resume summary and skills ordering to a pasted job description without inventing experience.

## User workflow
1. Open `prompts/AI_PROMPT_LIBRARY.md`.
2. Copy Prompt 3.
3. Paste the current resume draft and the job description.
4. Ask the AI to identify supported keywords, missing skills and truthful edits.
5. Accept only edits supported by actual experience.
6. Save a new role-specific resume copy.
7. Run Prompt 8 to verify all claims.
8. Export to PDF and inspect the result.

## Simple automation logic (pseudocode)
INPUT: verified_resume, job_description
OUTPUT: suggested_edits, unsupported_keyword_list
1. Extract role keywords from job_description.
2. Compare them with verified_resume.
3. Label each keyword as supported, partially supported or not supported.
4. Generate edits only for supported content.
5. Flag unsupported keywords; never insert them as skills.
6. Ask the student to approve all changes.
7. Save a separate tailored draft.

## Demonstration
Use a sample job description such as:
“Seeking a student intern with basic programming knowledge, HTML, CSS, JavaScript, teamwork and willingness to learn.”
Expected supported terms from this profile: programming, HTML, CSS, JavaScript, teamwork, willingness to learn. Do not add React, Python, SQL or cloud skills unless independently verified.

## Limitation
This is a documented AI-assisted workflow, not a live integration with an employer's ATS. AI tools may be wrong; the student approves every change.
