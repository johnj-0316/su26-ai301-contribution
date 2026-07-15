# su26-ai301-contribution
# Contribution [#1389]: COALESCE isn`t work

**Contribution Number:** [1 / **2** / 3]  
**Student:** [John Martin]
**Issue:** [https://github.com/appbaseio/reactivesearch/issues/414]  
**Status:** [**Phase I**] [**Complete**]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]
This issue interests me because of my focus on consistently practicing SQL, along with learning JavaScript. I never understood the idea of combining SQL, a backend/database language, with JS, a frontend language, so learning it now in preparation for Next.js will really help my learning process. I know enough about both languages to help contribute and fix the inconsistency described in the issue.
---

## Understanding the Issue

### Problem Description

Basically, the COALESCE keyword is not behaving as it would in SQL and returning inaccurate values.

### Expected Behavior

In the example in the issue, COALESCE(sample,""), where sample is null, should return "", but instead returns sample, which contradicts the function.

### Current Behavior

COALESCE, which should return the first non-null value in its parameters, is not working and returning null as a value (which it will do when there aren't any non-null values) even when there are non-null characters.

### Affected Components

src/61date.js
dist/alasql.js
dist/alasql.min.js

---

## Reproduction Process

### Environment Setup



### Steps to Reproduce



### Reproduction Evidence

---

## Solution Approach


### Analysis


### Proposed Solution


### Implementation Plan


**Understand:** 

**Match:** 

**Plan:** [Step-by-step implementation plan]

**Implement:** 

**Review:** 

**Evaluate:** 

---

## Testing Strategy

### Unit Tests 
- [] Test case 1: 
- [] Test case 2: 
- [] Test case 3: 

### Integration Tests

- [] Integration scenario 1
- [] Integration scenario 2

### Manual Testing


---

## Implementation Notes

### Week [3] Progress

### Week [4] Progress


### Code Changes

- **Files modified:** 
- **Key commits:** 
- **Approach decisions:** 

---

## Pull Request

**PR Link:** 

**PR Description:** 

**Maintainer Feedback:**
- [Date]: [Summary of feedback received] 
- [Date]: [How you addressed it]

**Status:** [Awaiting review/ Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]: 

### Challenges Overcome


### What I'd Do Differently Next Time


---

## Resources Used

- [Link to helpful documentation]: 
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]: 
