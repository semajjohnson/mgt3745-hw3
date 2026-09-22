# Standards

Status: ACTIVE in Module 3. Adapt these rules to your feature and follow them.

1. Name JavaScript identifiers in descriptive camelCase that says what they hold or do, such as poolItems, savePool, and renderPool. Short conventional names like event, index, and item are fine when their role is obvious.
2. Keep structure in index.html, presentation in styles.css, and behavior in app.js. Keep application code inside the IIFE in app.js so nothing becomes an accidental global.
3. Comments explain why code exists, not what it does. Remove console.log and other debug output before submitting.
4. Commit messages name the behavior that changed and why, such as "Require a source name before saving a pool item," not "update app.js."
5. Forbidden: inserting user text with innerHTML. Track and source names are always rendered with textContent.
6. Every form control has a label, and success and error messages appear in announced elements. When savePool fails, the user's typed track and source stay in the inputs.
7. Every pool item shows the name of the person it came from. An item without a source name is never saved or displayed.

If this file and context/CLAUDE.md disagree, STANDARDS.md is the source of truth, and CLAUDE.md is repaired to match.
