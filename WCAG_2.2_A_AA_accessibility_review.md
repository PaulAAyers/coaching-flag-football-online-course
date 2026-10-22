# Coaching Flag Football Principles — WCAG 2.2 A and AA Accessibility Review

**Review date:** October 22, 2026  
**Artifact:** `coaching_flag_football_materials.html`  
**Scope:** The HTML page (including its styles and navigation), not the contents of linked PDF/Word resources or other deployed website pages. An October 22 update added 10 matching form/worksheet resources and did not rerun the entire accessibility audit.  
**Standard:** [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/), all 55 Level A and AA Success Criteria. WCAG 2.2 does **not** include the obsolete WCAG 2.1 criterion 4.1.1 Parsing.

## Overall assessment

The remediated HTML had **no outstanding issue identified by the code, contrast and Chromium browser tests performed**. This is **not a formal WCAG conformance certification** or a VPAT. A final check in the live deployment with NVDA, JAWS, VoiceOver, mobile screen readers, and alternate zoom/high-contrast settings remains recommended. The ten linked PDF previews and ten original Word files must be audited separately if the whole course-materials experience is to claim WCAG conformance.

**Criterion assessment tally:** **27 reviewed**; **26 not applicable**; **2 site-wide follow-up**. "Reviewed" means no issue identified in the checks performed, not a guarantee of complete manual/assistive-technology conformance.

## Remediation applied

1. Added focusable destinations for all four Part headings and the main content skip target.
2. Fixed potential **2.5.3 Label in Name** mismatches by ensuring breadcrumb accessible names include the visible **Part I–IV** and **Chapters** text.
3. Raised non-text contrast for the navigation borders to **4.54:1** and focus outline color to **7.11:1** against white.
4. Made keyboard focus highly visible on navigation, links and jump-to destinations, and kept the skip link above sticky navigation when focused.
5. Added sticky-navigation scroll padding so chapter/part destinations and focused resource links remain visible.
6. Closed open navigation panels if focus moves outside the navigation, avoiding focus hidden by the popup.
7. Increased tap areas on breadcrumb controls, menu items, and resource actions; permitted resource action wrapping without horizontal overflow.

## Testing performed

- HTML source inspection for semantics, heading structure, language, focusability, landmarks, decorative glyphs and resource names.
- Chromium keyboard tests using **Tab, Enter and Escape**, including skip link, both menus, Part II, Chapter 18, and dismissal on focus leave.
- Chromium accessibility-tree inspection of disclosure controls and visible/accessible names.
- Reflow and text-spacing checks at **1694 × 900, 768 × 1024, 390 × 844, 320 × 640, and 320 × 256** CSS-pixel viewports; no horizontal page overflow.
- The October 22 update links **all 10 form/worksheet resources** (10 PDF title links + 10 PDF Open links + 10 Word Download links); actual file paths were validated in the new ZIP. See README for link test scope.
- Content preservation comparison: **256 text fragments in main** retained identically from the preceding site version, including all four Parts and 18 chapters.

## Color contrast samples

| Foreground / background | Computed ratio | Applicable threshold |
|---|---:|---:|
| White course-header text / maroon | 7.99:1 | 4.5:1 normal text |
| Body text / white | 14.74:1 | 4.5:1 normal text |
| Resource links / white | 10.00:1 | 4.5:1 normal text |
| Unavailable resource text / white | 5.74:1 | 4.5:1 normal text |
| Navigation control border / white | 4.54:1 | 3:1 non-text UI |
| Keyboard focus outline / white | 7.11:1 | 3:1 non-text UI |

## Level A and AA success criterion matrix

| WCAG | Success Criterion | Level | Assessment | Evidence / caveat |
|---|---|---|---|---|
| 1.1.1 | Non-text Content | A | Reviewed | Decorative breadcrumb symbols are hidden from assistive technology; no substantive images on the HTML page. |
| 1.2.1 | Audio-only and Video-only (Prerecorded) | A | Not applicable | No prerecorded audio or video embedded in the HTML. |
| 1.2.2 | Captions (Prerecorded) | A | Not applicable | No prerecorded synchronized media embedded. |
| 1.2.3 | Audio Description or Media Alternative (Prerecorded) | A | Not applicable | No prerecorded synchronized media embedded. |
| 1.2.4 | Captions (Live) | AA | Not applicable | No live synchronized media embedded. |
| 1.2.5 | Audio Description (Prerecorded) | AA | Not applicable | No prerecorded synchronized video embedded. |
| 1.3.1 | Info and Relationships | A | Reviewed | Semantic header, nav, main, headings, sections and lists inspected; screen-reader validation recommended. |
| 1.3.2 | Meaningful Sequence | A | Reviewed | DOM order follows visual order, section reading order and list groupings. |
| 1.3.3 | Sensory Characteristics | A | Reviewed | Instructions do not depend only on visual location, color, shape or sound. |
| 1.3.4 | Orientation | AA | Reviewed | No orientation lock; narrow and wide viewport layouts exercised. |
| 1.3.5 | Identify Input Purpose | AA | Not applicable | No personal-information input controls. |
| 1.4.1 | Use of Color | A | Reviewed | Links are identifiable by underline; interactive states also use outlines/underlines. |
| 1.4.2 | Audio Control | A | Not applicable | No automatically playing audio. |
| 1.4.3 | Contrast (Minimum) | AA | Reviewed | Colors checked: header white/maroon 7.99:1, links 10.00:1, body 14.74:1, status 5.74:1. |
| 1.4.4 | Resize Text | AA | Reviewed | Responsive narrow viewport checks passed; final 200% browser text-zoom check recommended in deployment. |
| 1.4.5 | Images of Text | AA | Not applicable | Text is HTML, not image-based. |
| 1.4.10 | Reflow | AA | Reviewed | No horizontal document overflow at 320px, 390px, 768px and desktop test widths. |
| 1.4.11 | Non-text Contrast | AA | Reviewed | Navigation borders are 4.54:1 and focus outlines are 7.11:1 against white. |
| 1.4.12 | Text Spacing | AA | Reviewed | WCAG text-spacing override produced no page-level horizontal overflow at all tested viewport sizes. |
| 1.4.13 | Content on Hover or Focus | AA | Not applicable | Dropdown content opens by activation, not hover or focus alone. |
| 2.1.1 | Keyboard | A | Reviewed | Tab, Enter, Escape and menu links tested in Chromium; native details/summary semantics preserved. |
| 2.1.2 | No Keyboard Trap | A | Reviewed | Focus can enter and leave navigation, and Escape dismisses opened menus. |
| 2.1.4 | Character Key Shortcuts | A | Not applicable | No single-character keyboard shortcuts. |
| 2.2.1 | Timing Adjustable | A | Not applicable | No time-limited interaction. |
| 2.2.2 | Pause, Stop, Hide | A | Not applicable | No automatically moving, blinking, scrolling or updating content requiring a pause. |
| 2.3.1 | Three Flashes or Below Threshold | A | Not applicable | No flashing material. |
| 2.4.1 | Bypass Blocks | A | Reviewed | Skip to course materials link is keyboard-first and visibly focused; main is programmatically focusable. |
| 2.4.2 | Page Titled | A | Reviewed | Descriptive HTML title: Coaching Flag Football Principles | Course Materials. |
| 2.4.3 | Focus Order | A | Reviewed | Focus order follows header, nav, disclosed menu, then course links; focus is transferred to jump targets. |
| 2.4.4 | Link Purpose (In Context) | A | Reviewed | Course links use descriptive chapter/part labels; resource links have contextual open/download accessible names. |
| 2.4.5 | Multiple Ways | AA | Site-wide follow-up | Only the packaged HTML and resource files were in scope; evaluate within the deployed multi-page site. |
| 2.4.6 | Headings and Labels | AA | Reviewed | Meaningful Part, Required/Optional Reading, Objectives and Chapter headings; menu labels updated. |
| 2.4.7 | Focus Visible | AA | Reviewed | All actionable links/disclosures receive high-contrast blue visible outlines. |
| 2.4.11 | Focus Not Obscured (Minimum) | AA | Reviewed | Sticky-navigation scroll padding, anchor offsets and auto-close on focus exit tested at five viewport sizes. |
| 2.5.1 | Pointer Gestures | A | Not applicable | No multipoint or path-based gestures are required. |
| 2.5.2 | Pointer Cancellation | A | Reviewed | Native links and summary disclosures activate on click, not on pointer down. |
| 2.5.3 | Label in Name | A | Reviewed | Removed aria-labels that masked visible Part I / Chapters; Chromium accessibility tree names retain visible text. |
| 2.5.4 | Motion Actuation | A | Not applicable | No motion/tilt/shake activation. |
| 2.5.7 | Dragging Movements | AA | Not applicable | No dragging interfaces. |
| 2.5.8 | Target Size (Minimum) | AA | Reviewed | Breadcrumb controls 42-44px minimum height; menu items 40px; resource actions have larger padding. |
| 3.1.1 | Language of Page | A | Reviewed | HTML lang=en. |
| 3.1.2 | Language of Parts | AA | Not applicable | No passages in another natural language require separate language markup. |
| 3.2.1 | On Focus | A | Reviewed | Focusing controls alone does not trigger navigation or context change. |
| 3.2.2 | On Input | A | Not applicable | No data input or settings controls. |
| 3.2.3 | Consistent Navigation | AA | Site-wide follow-up | Check consistency with other site pages after deployment; this artifact has one HTML page. |
| 3.2.4 | Consistent Identification | AA | Reviewed | Part/Chapter selectors and resource open/download controls are labeled consistently within the page. |
| 3.2.6 | Consistent Help | A | Not applicable | No help mechanism repeated across multiple pages. |
| 3.3.1 | Error Identification | A | Not applicable | No user data entry/validation errors. |
| 3.3.2 | Labels or Instructions | A | Not applicable | No user data input. |
| 3.3.3 | Error Suggestion | AA | Not applicable | No input validation. |
| 3.3.4 | Error Prevention (Legal, Financial, Data) | AA | Not applicable | No user-submitted transaction or stored data operation. |
| 3.3.7 | Redundant Entry | A | Not applicable | No repeated data entry process. |
| 3.3.8 | Accessible Authentication (Minimum) | AA | Not applicable | No authentication interaction. |
| 4.1.2 | Name, Role, Value | A | Reviewed | Chromium accessibility tree shows native DisclosureTriangle, correct names, links and state; AT testing recommended. |
| 4.1.3 | Status Messages | AA | Not applicable | No non-focused status messages are generated from user interaction. |

## Limits and follow-up

- **Assistive technology:** This review inspected the browser accessibility tree but did not constitute a human-led NVDA, JAWS, VoiceOver, TalkBack, switch control, or speech-input usability test.
- **Website-wide requirements:** Multiple Ways (2.4.5) and Consistent Navigation (3.2.3) need testing in the wider deployed website, if the page is part of one.
- **Linked documents:** Ten PDF previews and ten original Word form/worksheet files are linked. The original Word files were preserved unmodified, and PDF previews were generated for browser viewing; their tagging, form fields, reading order, contrast, metadata, and keyboard behavior were **not** remediated or certified as part of this HTML-only request.
- **Missing resources:** The page still displays "File not yet supplied" beside 17 excerpts/forms/worksheet references that are not available. These do not point to broken links.
- **Production QA:** Verify against your live URL with a screen reader and the native browser zoom at 200%/400%; test Windows high-contrast/forced-colors and keyboard focus for final sign-off.
