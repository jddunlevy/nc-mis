---
type: research-instrument
class: MIS 430
title: Course Selection at New College — instrument v1
platform: Qualtrics (ua.qualtrics.com)
date: 2026-10-15
status: draft — terminology check required before launch
purpose: test §3 of the SOW; recruit interview participants for the Elicitation Report
related: "[[SOW - New College Course Navigator (v1.0)]]"
---
# Course Selection at New College — Instrument v1

**Platform:** Qualtrics (UA institutional, `ua.qualtrics.com`)
**Distribution:** Anonymous Link, posted to the New College GroupMe
**Length:** approx. 6 minutes (student path), 4 minutes (faculty path)
**Target N:** 40+ student responses for usable cross-tabulation; faculty responses treated as
qualitative regardless of count

Respondent-facing text is written in impersonal register throughout. Italicized notes are
analysis commentary for the team and do not appear in the survey.

## Design rationale

The instrument tests whether the problem stated in §3 of the SOW exists. §3 was written without
fieldwork, so every claim in it is an assumption. The design permits a negative result: methods
that would indicate no problem ("Academic advisor," "Registration dashboard") appear as ordinary
options rather than afterthoughts, one agreement item is reverse-scored, and open-response items
include explicit "if any" and "if you have not" escapes.

The primary metric is **delayed course awareness** (Block D): whether a respondent became aware
of a relevant course only after the opportunity to take it had passed. This measures the specific
gap the product claims to close, concerns a discrete recallable event rather than a general
impression, and can return a null result.

Question order runs behavior → outcome → attitude. Attitudinal items are placed last so they
cannot contaminate behavioral recall.

There is **no concept description and no purchase-intent question.** Demand is measured
indirectly at Q19, which asks what changes would improve the process without naming a solution.
Convergent unprompted descriptions constitute stronger evidence than agreement with a described
concept.

### Bias mitigation applied

| Risk | Mitigation |
|---|---|
| Demand characteristics | Impersonal register; no researcher identification beyond institutional affiliation; no statement of hypothesis |
| Leading item wording | No evaluative terms ("more effort than it should," "worry," "struggle") in any item stem or choice |
| Presupposition in open items | "if any," "if you have not, enter none" escapes on all three student open items and on F7 |
| Acquiescence bias | Agreement battery balanced: two positively worded items, one negatively worded |
| Order effects | Choice randomization on Q3, Q6, Q14, with "Other" anchored |
| Confirmation of premise | Null-result options present in Q6, Q8, Q11, Q16, F3 |

### Response requirement policy

- **Force Response** — only where an item drives branch logic or carries the analysis.
  Over-application is the primary cause of mid-survey abandonment.
- **Request Response** — soft prompt, respondent may continue. Demographics, estimates, and
  items a respondent may not be able to answer.
- **No requirement** — all open-response items.

---

## BLOCK A — Introduction

*Descriptive Text item, no question.*

> **Course Selection at New College**
>
> This survey is part of a student research project at the University of Alabama. It asks how
> New College students identify and select courses.
>
> The survey takes approximately 6 minutes. Responses are anonymous. No names, email addresses,
> or IP addresses are collected, and responses cannot be linked to individual respondents.
> Participation is voluntary and may be discontinued at any time. Most questions may be skipped.
>
> An optional form at the end allows participants to volunteer for a follow-up interview. That
> form is separate from this survey and is not linked to survey responses.
>
> Contact: [email]

> [!warning] The anonymity statement must be made true before launch
> In Survey Options, disable **Record IP address** and geolocation. The claim above is a
> commitment, not boilerplate.

---

## BLOCK B — Screener

### Q1. What is your affiliation with New College? — **Force Response**
*Multiple Choice, single answer*

- Student
- Faculty, advisor, or staff
- Neither

→ **Branch Logic:** Student → Block C. Faculty/staff → Block J. Neither → End of Survey.

---

## BLOCK C — Segmentation

### Q2. Which statement best describes your plans after graduation? — **Force Response**
*Multiple Choice, single answer*

- I have a specific direction in mind
- I have several possible directions in mind
- I have not determined a direction
- Prefer not to say

> *Primary independent variable. Cross-tabulate all downstream items against it. Respondents with
> a specific direction require precision — retrieval against a known target. Respondents without
> one require discovery — surfacing options they would not search for. These are different
> product capabilities. If the population skews undetermined, a ranking built on stated career
> goals addresses the smaller segment, which should reshape the backlog.*

### Q3. Which of the following contributed to your decision to enroll in New College? Select all that apply. — Request Response
*Multiple Choice, multiple answer. Randomize choices; anchor "Other" last.*

- The ability to build a major around specific goals
- The ability to explore multiple areas before committing to one
- The ability to combine interests across departments
- Access to opportunities specific to New College
- The structure and flexibility of the program
- Other: ___

### Q4. What is your current class standing? — Request Response
*Multiple Choice, single answer*

First year / Sophomore / Junior / Senior / Other

### Q5. What is the current status of your self-designed major or minor? — Request Response
*Multiple Choice, single answer*

- Not started
- In development
- Planned but not formally submitted
- Submitted or approved
- Not applicable

> [!note] Terminology check required
> Replace with the terms New College actually uses for the proposal document and approval step.
> Local vocabulary materially affects response rate and answer quality; generic phrasing reads as
> external market research.

---

## BLOCK D — Current behavior

### Q6. Which of the following do you use when identifying courses to take? Select all that apply. — **Force Response**
*Multiple Choice, multiple answer. Randomize; anchor final two choices and "Other."*

- Registration dashboard
- Course catalog or bulletin
- Academic advisor
- Faculty members, outside of advising
- Other students
- AI tools (ChatGPT, Claude, Gemini, or similar)
- Web resources other than AI tools (department sites, course review sites, forums)
- Requirements of graduate programs or curricula at other institutions
- DegreeWorks or degree audit
- Enrolling in courses and dropping those that do not fit
- Other: ___

> *Two options carry disproportionate information. "Requirements of graduate programs or
> curricula at other institutions" indicates students working backward from a target program,
> which implies the tool should accept a program as input rather than only a career. "Enrolling
> and dropping" quantifies the current cost of inadequate discovery in concrete add/drop terms.*

### Q7. Which of the above do you rely on most? — **Force Response**
*Multiple Choice, single answer.* **Carry Forward Choices** → Selected Choices from Q6.

> *Breadth without primacy is weakly interpretable. "60% use advisors" and "advisors are the
> primary method for 15%" support very different claims.*

### Q8. What was the result when you used AI tools to identify courses? Select all that apply. — **Force Response**
*Multiple Choice, multiple answer.* **Display Logic:** shown if Q6 includes "AI tools."

- Recommended courses that did not exist
- Recommended courses that were not offered that semester
- Provided accurate and useful recommendations
- Accuracy could not be determined
- Recommendations were not acted on
- Other: ___

> *This block tests the second claim in §3, that general AI tools produce inaccurate
> recommendations — currently unevidenced. Options 3 and 4 permit the claim to fail. If
> respondents report accurate results, catalog grounding is not the differentiator, and §4's
> entire technical premise requires revision.*

### Q9. The last time you selected courses, approximately how much time did you spend identifying and comparing options? — Request Response
*Multiple Choice, single answer*

- Less than 30 minutes
- 30 to 60 minutes
- 1 to 3 hours
- 3 to 6 hours
- More than 6 hours
- Time was distributed across multiple weeks

> *The final option is substantive. If it predominates, the cost is fragmentation rather than
> duration — the task has no boundary and no completion state. That implies a different product
> framing than time savings.*

### Q10. When identifying courses, which best describes the range of departments you consider? — Request Response
*Multiple Choice, single answer*

- Primarily departments already familiar to me
- A few related departments
- The full university catalog
- No consistent approach

> *A self-designed major makes the entire catalog relevant in principle. If respondents in
> practice remain within familiar departments, the constraint is awareness rather than search,
> and the product's function is surfacing unknown options rather than ranking known ones.*

---

## BLOCK E — Delayed course awareness *(primary metric)*

### Q11. Have you become aware of a course relevant to your major after the opportunity to take it had passed? — **Force Response**
*Multiple Choice, single answer*

- Yes, more than once
- Yes, once
- No
- Unsure

### Q12. How did you become aware of that course? Select all that apply. — Request Response
*Multiple Choice, multiple answer.* **Display Logic:** Q11 = "more than once" or "once."

- Another student
- An academic advisor
- Browsing the catalog or registration dashboard
- A faculty member
- A syllabus, department page, or another student's schedule
- Do not recall
- Other: ___

### Q13. What was the outcome? — Request Response
*Multiple Choice, single answer.* **Display Logic:** same as Q12.

- Took the course in a later semester
- Course was not offered again before graduation
- Did not take the course
- No effect
- Other: ___

> *Q11 establishes incidence; Q13 establishes consequence. Together they produce the quantitative
> basis for the problem statement. A low incidence rate on Q11 indicates the discovery gap is not
> present at scale, which is a valid and reportable result.*

---

## BLOCK F — Selection criteria

### Q14. Which factors do you consider when determining whether a course belongs in your major? Select up to three. — Request Response
*Multiple Choice, multiple answer. Validation: maximum 3. Randomize; anchor "Other."*

- Personal interest
- Fit with the theme of the major
- Contribution to the coherence of the major as presented for approval
- Relevance to a specific career
- Relevance to graduate programs or other institutions
- The instructor
- Schedule compatibility
- Requirement fulfillment
- Other: ___

> *"Contribution to the coherence of the major as presented for approval" is absent from the SOW.
> §4 proposes ranking by interests and career goals, but a self-designed major is a set that must
> be defended as coherent. If this factor ranks highly, relevance ranking alone under-specifies
> the task.*

### Q15. When selecting courses, which time frame do you primarily consider? — **Force Response**
*Multiple Choice, single answer*

- The next semester only
- Approximately the next year
- All remaining semesters
- Varies

> *Tests a scope decision rather than the problem. §5 excludes multi-semester planning on the
> stated grounds that single-semester ranking is the core need — unevidenced. If "all remaining
> semesters" predominates, that exclusion is incorrect and should be revised before build rather
> than discovered during user testing.*

---

## BLOCK G — Agreement

### Q16. Indicate your level of agreement with each statement. — **Force Response**
*Matrix Table, 5-point Strongly disagree → Strongly agree. Do not randomize.*

| Statement | Construct | Polarity |
|---|---|---|
| I know what courses are available that relate to my major | awareness | positive |
| The process of identifying courses related to my major is straightforward | friction | positive |
| There are likely courses relevant to my major that I am not aware of | unknown coverage | negative |

> *Three items, balanced two positive to one negative so acquiescence bias does not operate in a
> single direction. High agreement on the first two indicates no problem. Placed after the
> behavioral blocks so behavioral recall is not primed.*

---

## BLOCK H — Open response

*All three: Text Entry, essay box, no response requirement.*

### Q17. If you have encountered difficulty identifying courses, describe what occurred. If you have not, enter "none."

> *Critical incident method, with an explicit null option so the item does not presuppose a
> failure. Responses supply the direct quotations for the Elicitation Report.*

### Q18. How, if at all, does the structure of New College affect the process of identifying courses?

> *Two-sided by construction. Permits the response that program flexibility is beneficial.*

### Q19. What changes, if any, would improve the process of identifying courses?

> *Indirect demand measurement. Unprompted convergent descriptions of a solution resembling the
> product constitute stronger evidence than agreement with a described concept, and cannot be
> attributed to leading. Absence of such descriptions is equally informative.*

---

## BLOCK I — Close (student path)

*Descriptive Text, then End of Survey.*

> Your responses have been recorded. Thank you for participating.
>
> To volunteer for a 20-minute follow-up interview, use the following link: **[link]**
>
> That form is separate from this survey and is not linked to your responses.

> [!note] Contact form setup
> Build as a **second Qualtrics survey** (name, email, student or faculty, availability). Link to
> its anonymous link as plain text, or use an End of Survey element with Redirect to URL. Either
> keeps the datasets unlinked, which is what makes the anonymity statement accurate.

---

## BLOCK J — Faculty / advisor path

*Short by design. Observational items. Faculty cannot report student behavior directly but
observe patterns across many students, which no student-side survey produces.*

### F1. What is your role? — Request Response
Academic advisor / Faculty member teaching New College students / New College staff or
administration / More than one of the above / Other: ___

### F2. How frequently do students request assistance with course selection? — Request Response
- Frequently; it is a substantial part of the role
- Regularly, during advising periods
- Occasionally
- Rarely

### F3. What do students most commonly request assistance with regarding course selection? Select all that apply. — Request Response
- Identifying what is offered
- Evaluating a large number of options
- Determining whether a course fits their major
- Establishing coherence across the major
- Timing and prerequisites
- Choosing among similar options
- Nothing in particular
- Other: ___

> *"Nothing in particular" is the null option and must remain.*

### F4. When a student asks about courses outside your own areas, what action do you typically take? Select all that apply. — Request Response
- Refer the student to a colleague in that department
- Search the catalog together with the student
- Provide information already known to me
- Direct the student to a resource
- Other: ___

> *Measures the distribution of catalog knowledge across advising staff. No individual advisor
> holds the full university catalog, which is a structural property rather than a performance
> issue. Framing the problem structurally also matters for eventual adoption: the finding is that
> the task exceeds what any individual can hold, not that advising is deficient.*

### F5. Have you observed a student miss a course that was relevant to their major? — Request Response
Yes, more than once / Yes, once or twice / Not to my knowledge / Unsure

### F6. What would improve the course identification process for students? — *no requirement*
*Text Entry, essay*

### F7. What concerns, if any, would you have regarding a tool that used AI to recommend courses to New College students? — *no requirement*
*Text Entry, essay*

> *Retain this item. It is the only source of externally generated input for Deliverable 6 (Harm
> & Guardrail Analysis), and it identifies the resisting stakeholder required by the Change
> Management Plan while the design is still inexpensive to change.*

### F8. Close
*Descriptive Text, End of Survey. Same text as Block I.*

---

## Qualtrics build checklist

1. **Survey Flow:** Intro → Screener (Q1) → Branch on Q1 → {Student: C, D, E, F, G, H, I} /
   {Faculty: J} / {Neither: End of Survey}.
2. **Force Response:** Q1, Q2, Q6, Q7, Q8, Q11, Q15, Q16. No others.
3. **Request Response:** Q3, Q4, Q5, Q9, Q10, Q12, Q13, Q14, F1–F5.
4. **No requirement:** Q17, Q18, Q19, F6, F7.
5. **Carry Forward Choices** on Q7, Selected Choices from Q6.
6. **Display Logic:** Q8 if Q6 includes AI tools; Q12 and Q13 if Q11 ∈ {more than once, once}.
7. **Randomize choices** on Q3, Q6, Q14; anchor "Other" and Q6's final two.
8. **Validation:** Q14 maximum 3 selections.
9. **Survey Options:** anonymize responses; IP address recording off; geolocation off; progress
   bar on; back button on.
10. **Add text entry** to every "Other" choice (the TXT import does not carry this).
11. **Distribution:** Anonymous Link.
12. **Pilot with three respondents before posting.** Observe where they reread a question.
    Rereading indicates ambiguity; a "wrong" answer does not.

## Pre-launch terminology pass

Substitute actual New College terminology in Q5 and anywhere "major or minor" appears.

## Stated limitations

Report these in the Elicitation Report. The rubric rewards acknowledged limitations.

- **Self-selection.** Respondents who find course identification difficult are more likely to
  complete a survey about course identification. The incidence rate at Q11 is likely an
  overestimate of the population rate.
- **Recall bias.** Q9 duration estimates and Q11 incidence counts are recalled, not measured.
- **Sampling frame.** The GroupMe excludes anyone not in it, plausibly including the least
  engaged students.
- **Faculty N.** With an estimated 10–20 faculty, faculty results are qualitative. Report counts
  and quotations, not percentages.
- **Stated versus revealed preference.** Q19 captures what respondents report wanting, which is
  not equivalent to what they would use. Interviews and user testing address this; the survey
  cannot.
