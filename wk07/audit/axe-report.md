# axe DevTools Audit Report — Week 7

**Date**: [2025-10-20]
**URL**: http://localhost:8080/tasks
**Tool**: axe DevTools 4.x
**Scope**: Full page scan (add form + task list)

---

## Summary
- **Critical**: 1
- **Serious**: 4
- **Moderate**: 0
- **Minor**: 0
- **Total**: 5 issues

---

## Critical Issues
### Issue 1: Images must have alternative text (Critical)
**Element**: <img src="/static/img/icon.png" width="16" height="16">
**Rule**: Non text content (WCAG 1.1.1)
**Description**: Ensure <img> elements have alternative text or a role of none or presentation.
**Impact**: Screen readers won't be able to describe what the image is showing.
**Fix**: Add in an 'alt' or an 'aria-label' describing what is shown in the image
**Status**: ❌ 

---

## Serious Issues

### Issue 2: Elements must meet minimum color contrast ration thresholds (Serious)
**Element**: <button type="submit">Add Task</button>
**Rule**: contrast minimum (WCAG 1.4.3)
**Description**: Form element does not have an associated label.
**Impact**: Makes it hard for some users to distinguish outlines and details, it can also make text hard to read
**Fix**: Ensure all text elements have sufficient color contrast between the text in the foreground and background color behind it
**Status**: ❌ 

### Issue 3: Elements must meet minimum color contrast ration thresholds (Serious)
**Element**: <button type="submit" aria-label="Delete task: Test Task">Delete</button>
**Rule**: `color-contrast` (WCAG 1.4.3)
**Description**: Ensure the contrast between foreground and background colors meets WCAG 2 AA minimum contrast ratio thresholds
**Impact**: People with low vision struggle to read button text.
**Fix**: Change button color to #495057 (darker gray, 7:1 contrast).
**Status**: ❌ 

### Issue 4: Elements must meet minimum color contrast ration thresholds (Serious)
**Element**: <button type="submit" aria-label="Delete task: Kotlin 2.2.21 works">Delete</button>
**Rule**: `color-contrast` (WCAG 1.4.3)
**Description**: Ensure the contrast between foreground and background colors meets WCAG 2 AA minimum contrast ratio thresholds
**Impact**: People with low vision struggle to read button text.
**Fix**: Change button color to #495057 (darker gray, 7:1 contrast).
**Status**: ❌ 

### Issue 5: Links must have discernable text (Serious)
**Element**: <a href="/about"></a>
**Rule**: link purpose (WCAG 2.4.4, 4.1.2)
**Description**: Ensure links have discernible text
**Impact**: Screen reader users also need to know where the link is going
**Fix**: Use an aria label to label the link
**Status**: ❌ 

---

## Moderate Issues
None detected.

---

## Minor Issues
None detected.

---

## Actions
1. **(Issue 1)**: Add aria label to image
2. **(Issue 2-4)**: Fix contrast ratio
3. **Verified (Issue 5)**: Add aria label to link

---

**Next step**: Manual testing to catch issues axe misses (focus order, SR announcements, keyboard traps).