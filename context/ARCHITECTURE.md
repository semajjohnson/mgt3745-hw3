# Architecture

Status: ACTIVE in Module 3.

## Gate

**Feature under decision:** the pool — a list where every track carries the name of the person it came from, and the list survives a reload. Acceptance criterion A5 in [FEATURES.md](FEATURES.md).

### Hard constraints

An option failing either is rejected before scoring. All three options passed.

1. **No new spending.** Originally "zero budget." Reworded because Spotify's Web API now requires the app owner to hold an active Premium subscription. I already pay for Premium personally, so the marginal cost is zero — but that subscription becomes a dependency of the app, which is recorded as a consequence in ADR-001 rather than hidden here.
2. **Runs from a fresh Codespace with Live Server.** Every grader and reviewer sees the same environment.

Serving both Spotify and Apple Music users was considered as a hard constraint and deliberately demoted. As a constraint it would have rejected both Spotify-based options before scoring and left the comparison with nothing to compare. It is scored instead, through switching cost and fit to spec.

### Options

- **Hand-built option (Build):** hand-written HTML, CSS and JavaScript with `localStorage`. Tracks and source names are entered by hand. No platform dependency.
- **Existing-service option (Buy — Spotify Web API):** tracks are selected from Spotify's catalog, and the pool stores real Spotify track IDs with a source name attached. Apple MusicKit was tested as the alternative platform; see the switching cost note.
- **AI-assisted build (Delegate):** Copilot or a coding agent builds the Spotify integration, and I inspect the result.

### Weights and anchors

Weights were fixed before any option was scored. Scores run 1–5, and **5 is always most favorable**.

| Criterion | Weight | 1 | 3 | 5 |
|---|---:|---|---|---|
| Cost to start | 3 | New spending required | No new spending, but accounts or setup | Nothing to sign up for |
| Cost to maintain | 2 | A third party can break it unilaterally | Occasional dependency updates | Nothing external to break |
| Time to working | 3 | Weeks, or gated on outside approval | Days | Hours |
| Inspectability | 4 | I can't read it | I can read it with real effort | I wrote it and can explain every line |
| Switching cost | 4 | Leaving means redesign | Portable with rework | Plain data, no lock-in |
| Fit to spec | 5 | Doesn't fit spec | Meets spec with gaps | Meets and respects the spec's non-goals |

## ADR-001

Title and date:
Status:
Door / concrete acquisition and execution choice:
Context:
Decision:
Consequences and revisit trigger:

Keep superseded ADRs. The pedagogical browser build can coexist with a different architecture recommendation; explain the distinction.
