# Module 3: Guardrails

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
- If tokenCount too high, split into chunks.
- Summarize chunks → merge hierarchically.
- Respect word caps.

### Utilities
- Word limiter.
- Consistency checker.
