# Trial evidence for tt-a1i/archify#616

Measurements only — no proposed source change lives on this branch.

- `fixtures/` — six synthetic schema-v2 workflows, one node per lane/column cell
  and within-lane edges only (the ordinary swimlane shape that never satisfies
  `hasVerticalStack`). No `meta.viewBox`, so every canvas is renderer-sized.
- `patches/option1-only.patch` — option (1) as proposed: drop the two extra
  conditions from the `readerFit` gate.
- `patches/option1-plus-mintext.patch` — the same, plus
  `data-reader-min-text="7.5"`, pairing the declaration the way
  `render-architecture.mjs:941-946` already pairs it for automatic canvases.
- `receipts/` — `archify visual-check` results for all six fixtures on each of
  the three builds, at all four viewports.
- `captures/` — `tall-10lane` at 1440x900 light, 2x DPR, on each build.

Run on `dev` 470c072, Node 24, Chrome 141 on macOS arm64.
