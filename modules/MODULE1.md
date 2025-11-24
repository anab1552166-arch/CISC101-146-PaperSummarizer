# Module 1: Intake & setup

### Purpose
- Normalize inputs: parse and validate the paper, section list, audience, detail level, and length constraints.
- Detect issues: identify missing, empty, or very short sections; flag anomalies early.

### Inputs
- PaperText: raw text with labeled sections.
- SectionList: ordered array of section names to process.
- Audience: “academic” default; optional “lay” variant requested.
- DetailLevel: integer in [0,5].
- LengthTargets: optional target words; hard caps enforced: 150/section, 300/final.

### Outputs
- NormalizedSections: array of {name, text, tokens, wordCount}.
- Diagnostics: {missingSections[], emptySections[], shortSections[] (<50 words), unknownSections[]}.
- Config: {audience, detailLevel, caps: {perSection:150, final:300}, style: “academic”}.

### Process
1. Parse sections → extract headings, normalize text.
2. Validate presence → mark missing, empty, short.
3. Compute metrics → word and token counts.
4. Assemble Config → enforce caps and style.

### Guardrails
- No reassignment of content.
- No re-labeling unless explicitly instructed.
