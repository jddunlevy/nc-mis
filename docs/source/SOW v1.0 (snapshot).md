---
type: deliverable
class: MIS 430
title: Statement of Work — New College Course Navigator
version: v1.0
date: 2026-10-15
author: teammate draft
status: draft — incomplete sections
source: SOW_New_College_Course_Navigator.pdf
---
# Statement of Work — New College Course Navigator

Teammate's v1.0 draft. Several template sections are still blank (see [[#Gaps in v1.0]]).

## 1. Project Summary

| Field | Value |
|---|---|
| Project Name | New College Course Navigator |
| Team Name & Members | *(blank)* |
| Document Version & Date | v1.0, October 15, 2026 |
| Project Start / End Dates | *(blank)* |

## 2. Purpose

Help New College students build self-designed majors and minors by quickly finding the courses
each semester that best match their interests and career goals.

## 3. The Problem (from research)

**Who:** New College students designing their own majors or minors, and the advisors who help
them plan.

**What:** Students must search every course offered each semester one by one to find relevant
classes, which is slow and overwhelming. General AI tools give inaccurate recommendations.

**Why:** Course information is scattered and changes every semester, and general AI tools are not
connected to the actual course catalog, so they suggest classes that don't exist or aren't
offered.

## 4. Proposed Solution Approach

A web tool where a student enters their interests and/or target career. AI reads only the current
semester's real course list and returns a ranked list of the most relevant courses, with a short
reason for each. Grounding the AI in the actual catalog is what fixes the accuracy problem.

## 5. Scope

**In Scope**
- Loading the current semester's New College course catalog
- Student input form for interests and career goals
- AI ranking of relevant courses with a brief explanation for each

**Out of Scope**
- Automatic registration or enrollment — requires access to university systems we don't have
- Full multi-semester degree planning — ranking one semester at a time is the core need
- Official approval of majors/minors — that stays with advisors and the department

## 6. Prioritized Requirements

| Theme | User Story | MoSCoW |
|---|---|---|
| Input | As a student, I want to enter my interests and career goals so that recommendations fit me. | Must |
| Ranking | As a student, I want courses ranked by relevance so that I know which to prioritize. | Must |
| Accuracy | As a student, I want only courses actually offered this semester so that I can trust the results. | Must |
| Explanation | As a student, I want a short reason for each recommendation so that I understand why it fits. | Should |

## 7. Deliverables & Timeline

*(table blank in v1.0)*

## 8. Team Roles & Organization

*(table blank in v1.0)*

## 9. Risks

| ID | Risk | Likelihood | Impact | Mitigation / Owner |
|---|---|---|---|---|
| R1 | AI recommends irrelevant or non-existent courses | Medium | High | Limit AI to the real catalog; spot-check results |
| R2 | Course catalog data is hard to get or incomplete | Medium | High | Get data early; fall back to manual entry |
| R3 | Students rely on the tool instead of advisors | Low | Medium | Clearly label results as suggestions; encourage advisor review |

## 10. Reporting Plan

*(table blank in v1.0)*

## 11. Approval

*(table blank in v1.0)*

## Gaps in v1.0

Blank sections that have to be filled before submission:

- Team name & members (§1)
- Project start/end dates (§1)
- Deliverables & timeline, with firm vs. flexible marked (§7)
- Team roles & responsibilities (§8)
- Reporting plan (§10)
- Approval signatures (§11)

Italic template guidance must be deleted from the submitted version.

Substantive gaps beyond the blanks:

- §3 is asserted, not yet evidenced — the prompt warns that a problem statement writable without
  interviews isn't grounded. The GroupMe survey is the fieldwork that grounds it.
- No "Won't have (this time)" row in §6 — MoSCoW with no W is an incomplete prioritization.
- No advisor-side user story, though advisors are named in §3's *Who*.
- R3 is rated Low likelihood with no evidence behind the rating.
