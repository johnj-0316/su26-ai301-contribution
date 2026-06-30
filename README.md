# su26-ai301-contribution
# Contribution [#13773]: [Worlds Without Number] Text is barely readable/showing the wrong color in the roll macro window

**Contribution Number:** [**1** / 2 / 3]  
**Student:** [John Martin]
**Issue:** [https://github.com/Roll20/roll20-character-sheets/issues/13773]  
**Status:** [Phase I / **Phase II** / Phase III / Phase IV] [In Progress / **Complete**]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]
This issue interests me because of my recent accomplishments in CSS. I've spent a lot of time practicing and learning CSS properties and developing an eye for good UI/UX. I want to put these newly trained skills to use by fixing the styling issue (color contrast/visibility). Doing so will help reaffirm my newfound work in learning CSS, as well as giving me an opportunity to contribute to a real project! I hope to learn any nuances when editing CSS in an open project, as well as pushing the issue back into the origin to build muscle memory with the command lines.
---

## Understanding the Issue

### Problem Description

[In your own words, what's broken or missing?]

### Expected Behavior

[What should happen?]

### Current Behavior

[What actually happens?]

### Affected Components

[Which parts of the codebase are involved?]

---

## Reproduction Process

### Environment Setup

All reproduction takes place on the roll20 website. Requires an account to be made, a game to be created, and knowledge about roll macros, the chat feature, and how to trigger it.
Note: Choose Without Number System By Sine Nomine (NOT Worlds Without Number)

### Steps to Reproduce

1. Create a Roll20 account if not already.
2. Go to top bar and click Play --> My Games --> Create New Game
3. Under "Recommended: Pick a Character Sheet," choose Without Number System By Sine Nomine --> Launch Game
4. On the right sidebar, go to the top and click the Gear icon (the last icon on the right)
5. Scroll down, and under Accessibility, toggle Dark Mode ON.
6. Then on the same sidebar at the top, click the "book icon" (hover over and it should say journal / the third icon from the left), then click + Character --> Save Changes
7. Once the character loads, under Saving Throws, click any of the 4 buttons above the label (Physical, Mental, etc.). A message should appear in the chat (first icon at the top/bubble messages)
8. Next to PC/NPC and the pencil, click the Gear icon.
9. Under system options, click the dropdown next to System list and choose between Worlds Without Number, Cities Without Number, etc.
10. Repeat step 7 through 9 until enough messages are in the chat to highlight the issue.
11. The chat should show result boxes with a colored name, but dark gray/black text inside holding the results (should faintly see numbers to the right) that is barely visible with the background.

### Reproduction Evidence

- **Commit showing reproduction:** [https://github.com/johnj-0316/roll20-character-sheets/tree/fix-issue-worlds-without-number-text-contrast]
- **Screenshots/logs:** <img width="296" height="357" alt="Screenshot 2026-06-17 at 1 32 39 AM" src="https://github.com/user-attachments/assets/4ea5d832-6008-4d09-a427-b43b45ea6d2a" />
- **My findings:** [Only affects Dark Mode]

---

## Solution Approach

### Analysis

Text color styling upon dark mode class application to surrounding div does not change, meaning text stays same color as if it were light mode.

### Proposed Solution

Either lighten the background in dark mode, or, the recommended/proposed solution by the person bringing up the issue, change the text color (either manually or adding a toggle) to make the text readable.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** Text color contrast/visibility problem in CSS with a specific styling sheet

**Match:** Mostly just identifying and editing the problem directly while adding flexibility for the user (toggle button)

**Plan:** [Step-by-step implementation plan]
1. Modify scss/roll_template.scss, or at least a scss file in the directory.
2. Change the background and/or color to a contrast about 7 according to standard.
4. Recreate changes in the actual dev-console to mimic applied changes.

**Implement:** [https://github.com/johnj-0316/roll20-character-sheets/tree/fix-issue-worlds-without-number-text-contrast]

**Review:** [Guidelines mostly specify using clean HTML/CSS code, no table, and no harassment. Main result should be Chrome/Firefox compatible as well.]

**Evaluate:** [Change issues first in dev console, then in the css file in VSCode once correctly traced/identified, then recreate and solve problems in Chrome/Firefox. If necessary, will ask AI to find the best color scheme/readable syntax.]

---

## Testing Strategy

### Unit Tests (Since it's just CSS, I won't write code, but play around with the HTML environment in the DevTools while the fix is active to spot any edge cases.
- [X] Test case 1: Works after dark mode is toggled on and off again.
- [X] Test case 2: Works after creating more roll macro templates in the chat (consistent)
- [X] Test case 3: Works after changing tabs and changing between the System list.

### Integration Tests

- [X] Integration scenario 1
- [X] Integration scenario 2

### Manual Testing

[Removing "color: initial" on the dark mode class fixes the issue, but likely not the intended solution. Moved designated color property down to its first child to add more specificity instead.]

---

## Implementation Notes

### Week [3] Progress

I changed the font color of the text in the roll macro attribute to its correct shade. After testing in the DevTools console, I noticed that dark mode had its own class with one property: "color: initial". This meant that I was likely not allowed to change anything about the class, as no other issues facing contrast problems had, and that the color property was overriding the one on the parent div. As a result, I had to move the color property down a class to add more specificity to the property, allowing it to take precedence over the one in the dark mode class. By doing so, I refrain from adding any new code while fixing the bug entirely.

### Week [4] Progress

Currently in the process of reviewing my PR, keeping it updated, and submitting for review! Making sure the code passes all the tests is definitely hard, but not as hard as recreating the issue in an environment I have no experience working with.

### Code Changes

- **Files modified:** [Without Numbers/Source/scss/roll_template.scss]
- **Key commits:** [https://github.com/johnj-0316/roll20-character-sheets/commit/c3743065579f85e7a7e1ec7aef908d00b4a89495]
- **Approach decisions:** [No code additions while still fixing the bug, keeping the size of the file the same]

---

## Pull Request

**PR Link:** [https://github.com/Roll20/roll20-character-sheets/pull/15236]

**PR Description:** [PR moves the color attribute on the class (.sheet-rolltemplate-swn-xxxx) to a more specific class (.sheet-container). This avoids new code and editing any other classes outside the scope of the stylesheet.]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]: No feedback received as of 6:13PM ET on June 30, 2026. Next steps will be to look into more issues on the same or different repositories!
- [Date]: [How you addressed it]

**Status:** [**Awaiting review **/ Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]: A small window into the many actions I will take and have to build into muscle memory in order to contribute to open source!

### Challenges Overcome

[Definitely replicating the environment and recreating the issue! Of course, there were parts where I was nervous to click something wrong and get confused on how to revert any mistakes. Other than that, it was definitely recreating an issue on a website I've never used!]

### What I'd Do Differently Next Time

[Spend more time reading documentation and researching the website before immediately jumping it. It would've saved a lot of time if I completely understood the issue to recreate instead of guessing along the way.]

---

## Resources Used

- [Link to helpful documentation]: https://wiki.roll20.net/Character_Sheet_Development/Dark_Mode#Roll_Template
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]: The CodePath Step-By-Step Procedures really help. Besides some help from Gemini for quick pointers on what to click and buttons to press along the way, most of my help came from the procedures in the hub on CodePath.
