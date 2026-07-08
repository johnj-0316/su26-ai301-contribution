# su26-ai301-contribution
# Contribution [#414]: Turn down sensitivity of URLParams

**Contribution Number:** [1 / **2** / 3]  
**Student:** [John Martin]
**Issue:** [https://github.com/appbaseio/reactivesearch/issues/414]  
**Status:** [**Phase I**] [**Complete**]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]
This issue interests me because of my interest in React, especially URLParams and familiarizing myself with it for my own personal projects. Right now, I'm facing a similar issue with a searchbar and decision making with URLParams, specifically how I should improve the UX. I am somewhat familiar with React and React Router, but I need to reinforce what I've learned by applying it.

I hope to fully wrap my head around URLParams, debouncing in React, and how to contribute to future React-like projects. I want to be able to use what I've learned here, whether my PR is merged or not, and apply it to my own website in the future.
---

## Understanding the Issue

### Problem Description

Basically, typing into the textfield updates URLParams every keystroke. This adds each new character to the URL and adds it to the stack of pages visited. 

### Expected Behavior

One of two things, either going back removes one word, or debouncing is implemented so the back button goes back to the latest user pause.

### Current Behavior

Whenever a user wants to go back to the previous page, they have to click the left arrow for each character they typed in order to go back. This makes for bad UX, as the user does not need to go back one character every click. 

### Affected Components

packages/web/src/components/search/SearchBox.js
packages/web/src/components/basic/URLParamsProvider.js

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
