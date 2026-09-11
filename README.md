# Standard Data docs

Mintlify source for Standard Data task-format and GDPx documentation.

## Sources of truth

- Repository layout and native evidence: [GDPx](https://github.com/Standard-Data-LLC/gdpx), checked at `92a0b8b91f2e73f5b50611704021f6b345b6de84`.
- API requests: live OpenAPI, v3 capabilities, and embedded review-bundle schemas at `https://api.standarddata.io`.
- Program review policy: `qc-stages-for-benchmark.mdx`. Do not infer QC completion from repository folders or API status.

Keep the repository's `TASK.json` / `run.json` / `traces/` structure distinct from the canonical API bundle. Do not reintroduce a separate batch-wide trajectory handoff, fixed reward filenames, or run-directory counts as trial counts.

`docs.json` groups the existing pages into Task guide, Evaluation and QC, API, and Guides. Preserve existing page URLs and redirects when reorganizing navigation.

## Validate and preview

```bash
npx mint validate
npx mint broken-links
npx mint dev
```

Run the command from this repository root.
