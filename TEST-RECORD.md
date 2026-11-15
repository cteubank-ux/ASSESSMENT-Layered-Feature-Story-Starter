# L6 — Test record

**Project:** More Than Words: Keeping the Diné Language Alive  

| Test | Procedure | Result | Evidence / screenshot |
|---|---|---|---|
| HTML validation | Validate `index.html` and `composition-plan.html` with the Nu HTML Checker. Resolve errors and record any remaining warnings. | Passed. | 
| CSS validation | Validate `styles.css` with the W3C CSS Validation Service. Resolve errors and record any remaining warnings. | Passed. |
| CSS-disabled reading order | Disable CSS. Read from title through article and documentation; activate all links. | Passed |
| 320px viewport | Check no horizontal page overflow, clipped text, or overlapping badge/title. | Passed |
| 768px viewport | Check stacked navigation/article layout, readable measure, and normal-flow quote. | Passed |
| 1280px viewport | Check two-column Grid, sticky guide, quote overlap, and editorial shape wrap. | Passed |
| 200% zoom | Zoom to 200%; verify title, badge, nav, quote, links, and text remain visible and usable. | Passed |
| Keyboard focus | Use Tab and Shift+Tab through every link. Confirm visible focus and logical order. | Passed |
| Long title growth | Temporarily replace the title with a much longer title. Confirm header grows naturally and badge does not cover text. | Passed |
| Doubled paragraph growth | Duplicate at least two long paragraphs in the shape-wrap section. Confirm no fixed-height clipping and text returns to full measure after the float. | Passed |
| Sticky page/section boundary | Scroll from top to bottom. Confirm sticky guide sticks at its threshold and stops at the bottom of its containing grid row. | Passed |
| Pointer activation | Click each story navigation link and the external learning-resource link. Confirm targets and destinations work. | Passed |
| `clip-path` disabled | Disable `clip-path` in DevTools. Confirm full rectangular image and caption remain visible. | Passed |
| `shape-outside` disabled | Disable `shape-outside` / feature support. Confirm portrait returns to normal flow and prose remains complete. | Passed |
| Stacking-context inspection | Inspect `.issue-badge`, `.story-guide`, and `.pull-quote`. Record computed position and z-index; confirm only token values are used and no content or focus is obscured. | Passed | 
