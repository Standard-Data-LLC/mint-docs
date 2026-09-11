# Standard Data docs

Mintlify source for Standard Data task-format and GDPx documentation.

## Sources of truth

- Customer-facing task layout and evidence: `gdpx/quickstart.mdx` and `gdpx/benchmark-task-package.mdx`.
- API requests: live OpenAPI, v3 capabilities, and embedded review-bundle schemas at `https://api.standarddata.io`.
- Program review policy: `qc-stages-for-benchmark.mdx`. Do not infer QC completion from evidence folders or API status.

Customer docs must be self-contained. Do not reference internal source-code locations or assume customers can browse internal files. Explain required layouts, metadata, and delivery steps directly in the guides.

Keep source task metadata and `run.json` / `traces/` evidence distinct from the canonical API bundle. Do not reintroduce a separate batch-wide trajectory handoff, fixed reward filenames, or run-directory counts as trial counts.

`docs.json` groups the existing pages into Task guide, Evaluation and QC, API, and Guides. Preserve existing page URLs and redirects when reorganizing navigation.

## Validate and preview

```bash
npx mint validate
npx mint broken-links
npx mint dev
```

Run the commands from the docs project root.
