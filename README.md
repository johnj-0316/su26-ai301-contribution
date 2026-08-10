# su26-ai301-contribution
# Contribution [#894]: Add accessibility labels to Modal component
**Contribution Number:** [1 / **2** / 3]  
**Student:** [John Martin]
**Issue:** [https://github.com/Vets-Who-Code/vets-who-code-app/issues/894]  
**Status:** [**Phase 4**] [**Completed**]

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
The aria labels seemed to track the class names in the suggestion, but the class names did not match with the current ones in the repo (presumably from commits further down the line).
As a result, I've modified the suggestion to include the new class names from components that matched or were similar to the functionality of the elements in the example. For instance, the suggestion included a close <button> tag in the modal, but the repo instead has a modal-close component entirely.

**Review:** 
Make sure guidelines are followed and code is clean (follow the template in CONTRIBUTING.md and make sure all edited files are tracked)

**Evaluate:** 
Use screen reader and complete tests (modal still works, screen reader reads out everything accordingly).
---

## Testing Strategy

### Unit Tests 
- [x] Test case 1: Render Modal with ModalHeader, ModalBody, and ModalClose; verify dialog exists and has role="dialog", aria-modal="true", aria-labelledby="modal-header", and aria-describedby="modal-body"
- [x] Test case 2: Verify ModalHeader renders id="modal-header" and ModalBody renders id="modal-body" so the ARIA references resolve correctly
- [x] Test case 3: Verify ModalClose button has aria-label="Close modal" and that its decorative content uses aria-hidden="true"

### Integration Tests
- [x] Integration scenario 1: Render a full modal usage path and confirm opening shows the dialog and the correct ARIA
- [x] Integration scenario 2: Verify keyboard behavior through Escape triggers onClose, and Tab/Shift keeping focus trapped inside the modal content

### Manual Testing
Open modal, confirm screen reader announcements, and tab/shift navigation functions as expected. Detailed actions provided above.

---

## Implementation Notes

### Week [3] Progress
2/3 done with Phase III, but I need to supply integration tests using the screen reader. The modal component doesn't seem to be used anywhere inside of the project, so some tests will also need to be conducted to test it there. Moreover, the suggested improvements don't match the current folder. I tried commenting on the issue to see what the maintainer wants, but it seems like they've either blocked me or removed commenting access. Either way, I've added the correct aria-labels according to the breakdown into different components and class names.

Will do tests on week 9. No PR until tests done.

### Week [4] Progress


### Code Changes

- **Files modified:** vets-who-code-app/src/components/ui/modal/modal-header.tsx, vets-who-code-app/src/components/ui/modal/modal-header.tsx
- **Key commits:** (fix) added aria-labels to modal-close.tsx and modal.tsx
- **Approach decisions:** 
The modal ui folder and component did not match the example suggestion, so I first tried to ask the maintainer. After no response, I've added the aria attributes to match the new class names while also keeping in line with the tasks required.
---

## Pull Request

**PR Link:** None

**PR Description:** 
Can't submit a PR, as I've either been blocked or blacklisted from the repo.

**Maintainer Feedback:**
<img width="1290" height="616" alt="Screenshot of cannot perform this action at top of page" src="https://github.com/user-attachments/assets/18178c0c-19fb-4322-963e-3531c7056ed9" />


**Status:** [Blocked]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]: TypeScript and ARIA labels, as well as the importance of a screen reader.

### Challenges Overcome
Learning TypeScript and understanding Docker, while also configuring the project and running it locally.

### What I'd Do Differently Next Time
Clearing things up with a maintainer before doing anything else!

---

## Resources Used

- [Link to helpful documentation]: https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-label
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]: https://github.com/Vets-Who-Code/vets-who-code-app/pull/1242
