# Evidence for tt-a1i/archify#632 (issue #617)

Visual evidence only — this branch is not part of the pull request and contains
no source changes.

`before.html` and `after.html` are rendered from the same input
(`cards.architecture.json`, the bundled `web-app.architecture.json` with one
extra card whose first item is an unbreakable slash-joined run). They differ by
exactly one CSS declaration, `overflow-wrap: anywhere` on `.card`:

```
$ diff <(tr '>' '\n' < before.html) <(tr '>' '\n' < after.html)
      overflow-wrap: anywhere;
```

Screenshots are 1440x900, `captureBeyondViewport`, light and dark, captured
after `Page.loadEventFired` and two rounds of the reader's own
`whenStable()` settle. `measurements.json` holds the DOM numbers.
