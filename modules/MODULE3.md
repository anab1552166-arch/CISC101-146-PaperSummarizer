# Module 3: Guardrails

#### Change Log:
##### added strict evidence mode to only include information from the paper.
##### added standardized section warnings for missing or very short sections.

##### evidence mode = "strict" # Options: "strict" or "lenient"

### Purpose
- Mitigate risks: missing/empty content, short sections, hallucination, long papers.

### Missing/empty sections
- Detect via Diagnostics.
- Action: insert notices in Checks & Warnings.

### <50-word sections
- Flag and warn.
- Provide minimal summary.

### Hallucination mitigation
- Summaries must reflect only provided text.
- Use exact terminology.
- No invented claims or citations.

### Long-paper chunking
- If tokenCount too high:
    - split sections into chunks
    - summarize each chunk seperately
    - merge chunk summaries hierarchically
- Respect word caps (<= 150 words per section, and maintain an academic tone throughout)

### Utilities
- Word limiter to enforce section word limits
- Consistency checker for terminology and tone

### Strict evidence mode
#### When evidence_mode = "strict":
####     Only include claims, equations, and results that appear in the provided text.
#### If a section does not have enough information, output: "The source text does not provide enough detail to summarize this section in strict evidence mode."
