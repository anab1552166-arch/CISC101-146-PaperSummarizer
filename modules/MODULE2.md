# Module 2: Section loop

# Change log:
# Added summary_level variable with "short" and "detailed" options
# Added conditional behavior in the section loop to support different summary levels.

summary_level = "short" # options: "short" or "detailed"

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
  if section is empty:
      summary = "No content provided."
  else:
    if summary_level== "short":
      # generate 1-2 sentence summary
      summary = summarize_short(section)
  elif summary_level == "detailed":
      # Generate paragraph + bullet list
      summary = summarize_detailed(section)
      key_points = extract_3_to_5_keypoints(section)

# Instructions:
# 1. For each section, check if it is emepty.
# 2. If "short", generate a very brief 1-2 sentence summary.
# 3. If "detailed", generate a short paragraph and a bullet list of 3-5 key points.
# 4. Continue till all of the sections are summarized.
  

