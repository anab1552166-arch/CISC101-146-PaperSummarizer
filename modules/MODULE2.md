# Module 2: Section loop

### Purpose
- Summarize each section within 150 words.
- Enforce constraints per PS2 specification.

### Inputs
- NormalizedSections, Config, Diagnostics.

### Outputs
- SectionSummaries: {name, summaryText, keyIdeas[], keyTerms[], wordCount}.
- SectionTableRows: {name, claims, methods, terminology}.

### Strategy
- DetailLevel 0–1: high-level objectives only.
- DetailLevel 2–3: include methods and main results.
- DetailLevel 4–5: add datasets, statistical tests, limitations.

### Constraint enforcement
- ≤150 words per section.
- Terminology consistency.
- Academic tone.

### Pseudocode
for section in NormalizedSections:
  if empty → summary = "No content provided."
  else → extract salient points, key terms, compose summary ≤150 words.
