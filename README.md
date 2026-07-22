# su26-ai301-contribution
# Contribution [#894]: Add accessibility labels to Modal component
**Contribution Number:** [1 / **2** / 3]  
**Student:** [John Martin]
**Issue:** [https://github.com/Vets-Who-Code/vets-who-code-app/issues/894]  
**Status:** [**Phase 2**] [**Complete**]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]

This issue interests me because of my constant ignorance of ARIA labels and accessibility in my web projects. Whether it's out of laziness or a lack of experience with the screen reader, I make implementations that entirely neglect those who use screen readers, potentially making their experiences more difficulty. Having a grasp of good HTML usage, and more specifically ARIA, will help me sharpen the skills I need to put them in my own projects.
---

## Understanding the Issue

### Problem Description

Basically, the .tsx file is missing a lot of aria labels that don't have the best accessibility features.  

### Expected Behavior

In the example in the issue, some tags are missing the aria label or aria-modal entirely.

### Current Behavior

The aria attributes aren't there, so screen readers will default to a certain behavior or completely ignore important information about the page.

### Affected Components

src/components/ui/modal/modal.tsx

---

## Reproduction Process
https://github.com/johnj-0316/vets-who-code-app/tree/fix-issue-894

### Environment Setup
1. Make sure Docker is installed.
2. Change the Node version in Dockerfile and package.json to cover v22 instead of v18
3. run the devcontainer.json
Biggest problem was running the Docker container and realizing v18 won't work.


### Steps to Reproduce
1. Clone the repository
2. Make sure nvm, npm, node v18+, and git is installed.
3. Run nvm use, npm install, and npm run dev in the terminal.
4. Add the port 3000 in the port tab in VSCode.
5. Navigate to the link provided by VSCODE (ends in devtunnels.ms)


### Reproduction Evidence

<img width="944" height="809" alt="Screenshot 2026-07-21 at 10 38 12 PM" src="https://github.com/user-attachments/assets/2ae080db-5c06-49a8-84c8-867c344a3c86" />
^Proof that I have access to the modal.
---

## Solution Approach
1. The issue provides tasks to be done, so first we run the code and use the screen reader function to test what it reads out.
2. Add the desired ARIA attributes.
3. Make sure all the navigation works.

### Analysis
1. There are two types of modals. The current one needing labels is not used in the website itself. Further testing needs to be done to recreate the modal entirely.

### Proposed Solution
Complete all the tasks and do all of the verification steps. Test with screen reader. File has changed a bit since the issue, so multiple tests need to be done to prevent code clashing. When stuck, ask a maintainer/Slack for help. 

### Implementation Plan
Add all of the labels first, then use a screen reader to check. Then I'll make sure I'm following guidelines while also verifying through tests.

**Understand:** 
Finish all of the tasks in the issue (add ARIA labels and test with screen reader)
**Match:** 
Requires HTML, React, and TS/JS knowledge.
Another modal component exists, so I'll match the ARIA attributes from there.

**Plan:** 
Add role="dialog" to modal container

Add aria-modal="true"

Add aria-labelledby pointing to title

Add aria-describedby pointing to content

Add aria-label to close button

Add aria-hidden to decorative icons

Test with screen reader

Ensure keyboard navigation works (Tab, Escape)

Verify focus trap works correctly

**Implement:** 


**Review:** 
Make sure guidelines are followed and code is clean (follow the template in CONTRIBUTING.md and make sure all edited files are tracked)

**Evaluate:** 
Use screen reader and complete tests (modal still works, screen reader reads out everything accordingly).
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
