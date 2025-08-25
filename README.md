Rita (Nathaniel) Tetterton
SNHU CS-250
Professor Denis Washington
# SlideShow Complete 2 — Sprint Review and Retrospective

## Overview
SlideShow Complete 2 is a Java Swing application that presents a slideshow of world landmarks with previous and next navigation and descriptive text. This README captures the Sprint Review and Retrospective for the final project and documents the Agile and Scrum practices used throughout development.

- Language: Java (Swing)
- Source: `src/SlideShow.java`
- Assets: `resources/` contains landmark images

---

## Sprint Goal
Deliver a usable slideshow application that cycles through curated landmark images with smooth navigation, clear status feedback, and resilient error handling.

---

## Increment (What Was Delivered)
- Navigable slideshow with Previous and Next buttons
- Five curated landmark images packaged under `resources/`
- Error handling for missing assets and image load failures
- Clean, readable UI layout using Java Swing components

Definition of Done:
- Code compiles with `javac` without warnings
- Manual test pass across all five images for both directions
- No unhandled exceptions during normal navigation
- README updated with build and run instructions

---

## How to Build and Run
From the project root:

```bash
# Compile
javac -d out -cp src src/SlideShow.java

# Run
java -cp out SlideShow
```

Notes:
- Ensure the `resources` directory remains alongside the compiled classes or adjust the image-loading paths within `SlideShow.java` accordingly.

---

## Product Backlog (Excerpt)
1. As a user, I want to navigate forward and backward through images so that I can control the pace of the slideshow.
   - Acceptance: Buttons enable/disable correctly at bounds or wrap around; clicking updates the displayed image and caption.
2. As a user, I want informative messages when images are missing so that the app does not crash.
   - Acceptance: Missing files are caught and a friendly message is shown; app remains responsive.
3. As a user, I want image captions with context so that I learn what I am viewing.
   - Acceptance: Each image displays a short landmark name or description.
4. As a user, I want consistent window sizing so that images are displayed cleanly.
   - Acceptance: Window size fits the largest image with padding; no overlapping controls.

Done in this sprint: 1–4
Deferred: Keyboard shortcuts, auto-play mode, configuration file for custom slideshows

---

## Sprint Review Summary
- Demo: Showed end-to-end navigation through all five landmarks with smooth transitions and captions.
- Stakeholder feedback: Positive on simplicity and clarity; requested optional auto-play and keyboard shortcuts for accessibility.
- Backlog updates: Added stories for Auto-play, Keyboard shortcuts, and Configurable image lists.

---

## Sprint Retrospective
What went well:
- Kept the scope small and achievable, resulting in a stable increment
- Early decision on image resource structure simplified loading logic
- Clear user stories with acceptance criteria guided implementation and testing

What could be improved:
- Add unit tests for image-loading utilities to prevent regressions
- Introduce CI to validate compilation and simple UI smoke tests
- Time-box spikes on image scaling behavior to reduce rework

Action items for next sprint:
- Set up a minimal CI workflow with Java 17 and a headless UI smoke check
- Implement auto-play with configurable delay
- Add keyboard navigation (Left/Right arrows) and accessibility labels

---

## Agile and Scrum Practices Used
- Scrum events: Sprint Planning, ad-hoc Daily check-ins, Sprint Review, Retrospective
- Artifacts: Product Backlog, Sprint Backlog, Increment, updated README (this document)
- Definition of Done established prior to coding
- User stories with clear acceptance criteria to capture user needs
- Lightweight task breakdown and WIP limits to maintain flow

---

## Essential Questions Reflection

1) How do I interpret user needs and implement them into a program? How do user stories help with this?
- I start by translating user goals into user stories expressed from the user perspective. Each story includes acceptance criteria that anchor implementation details to observable behavior. For the slideshow, needs like go forward and backward, avoid crashes on missing images, and see context were implemented as navigation controls, guarded image loading, and captions. User stories prevent scope drift and keep solutions focused on value.

2) How do I approach developing programs? What Agile processes will I incorporate going forward?
- I iterate in small, testable increments, using a prioritized backlog to guide work. I will continue to use Sprint Planning to set a realistic goal, lightweight Daily check-ins to surface blockers early, and Sprint Reviews to validate with stakeholders. Retrospectives drive continuous improvement; adding CI and basic automated tests will strengthen feedback loops in future work.

3) What does it mean to be a good team member in software development?
- Communicate clearly, commit to shared goals, and make work visible. Offer help when others are blocked, give and receive feedback respectfully, and uphold the Definition of Done. Favor pairing on tricky tasks and write documentation that lowers the barrier for teammates and future maintainers.

---

## Testing Notes
- Manual test matrix covered: first/last image navigation, rapid clicking, missing file simulation, window resize behavior
- No crashes under these scenarios; minor cosmetic scaling artifacts noted for future improvement

---

## Future Enhancements
- Auto-play with configurable interval and pause/resume
- Keyboard navigation and accessibility improvements (mnemonics, focus order, alt text)
- External configuration for image lists and captions (JSON or properties file)
- Basic unit tests around image loading and index management

---

## Project Structure
- `src/SlideShow.java` — Main Swing application
- `resources/` — JPEG images for landmarks

