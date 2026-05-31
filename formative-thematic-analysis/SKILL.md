---
name: formative-thematic-analysis
description: Analyze formative study interview transcripts using Braun and Clarke thematic analysis. Use when the user provides interview text containing interviewer/interviewee dialogue and wants open coding, themes, challenges, design goals, or an Excel design-analysis table for a system or HCI project.
---

# Formative Thematic Analysis

Use this skill to analyze interview transcripts for early-stage system design research. The input is usually a `.txt`, `.docx`, transcript, or pasted dialogue containing interviewer and interviewee turns. The output should help the user move from raw participant language to codes, themes, design challenges, and design goals.

## Method Basis

Use thematic analysis based on:

Braun, V., & Clarke, V. (2006). *Using thematic analysis in psychology*. *Qualitative Research in Psychology*, 3(2), 77-101. https://doi.org/10.1191/1478088706qp063oa

Treat thematic analysis as a qualitative method for identifying, analyzing, and reporting repeated patterns of meaning in textual data. Do not merely summarize the transcript. Preserve a clear evidence chain from participant language to design implications.

## Core Workflow

1. Read the transcript and identify speakers.
   - Separate interviewer prompts from interviewee responses.
   - Prioritize interviewee language as evidence.
   - Use interviewer prompts only as context, unless they reveal a study design issue.

2. Select meaningful data extracts.
   - Choose short, representative participant quotes.
   - Keep timestamps when available.
   - Avoid overlong quotes; excerpt only the part that supports the code.

3. Generate initial codes.
   - A code should capture what the participant is saying or implying in that extract.
   - Codes should be concise and close to the data.
   - Multiple extracts may share a code; one extract may support more than one code when needed.

4. Group codes into themes.
   - Multiple related codes can form one theme.
   - A theme should describe a recurring pattern of meaning, not just a topic label.
   - Themes should be internally coherent and clearly distinct from each other.

5. Derive challenges from themes.
   - Multiple themes can point to one design challenge.
   - A challenge should phrase the underlying design problem the system must address.
   - Prefer "How might the system..." or "How can the platform..." style wording.

6. Translate challenges into design goals.
   - Each challenge should map to one design goal.
   - Design goals should be actionable but not overly specific implementation details.
   - Add possible features only after the design goal.

## Required Output Structure

When generating an Excel workbook, use these sheets:

1. `Open Coding`
   - `Quote ID`
   - `Time`
   - `User Quote / Data Extract`
   - `Initial Code`
   - `Code Explanation`
   - `Theme ID`
   - `Challenge ID`
   - `Design Goal ID`

2. `Theme Grouping`
   - `Theme ID`
   - `Theme`
   - `Included Codes`
   - `Evidence Quote IDs`
   - `Theme Explanation`
   - `Challenge ID`

3. `Challenges & Design Goals`
   - `Challenge ID`
   - `Challenge`
   - `Source Themes`
   - `Design Goal ID`
   - `Design Goal`
   - `Possible Features`
   - `Notes`

4. `Method Notes`
   - Explain that the analysis follows Braun and Clarke thematic analysis.
   - State the analysis chain: data extract -> code -> theme -> challenge -> design goal.
   - State that multiple codes may form one theme, multiple themes may form one challenge, and each challenge maps to one design goal.
   - Note whether the analysis is preliminary if based on a small number of interviews.

## Analysis Rules

- Do not force every code to become its own theme.
- Do not force every theme to become its own challenge.
- Do not jump directly from a single quote to a design goal unless the user explicitly asks for a quick brainstorm.
- Distinguish `challenge` from `design goal`:
  - Challenge: the design problem exposed by themes.
  - Design goal: what the system should support to address the challenge.
- Preserve traceability: every theme should point back to evidence quote IDs, and every challenge should point back to source themes.
- When the transcript is Chinese, write tables in Chinese while retaining useful method terms such as `code`, `theme`, `challenge`, and `design goal`.

## Quality Checks

Before finalizing:

- Check that participant quotes are not accidentally invented or overly paraphrased.
- Check that codes are grounded in quotes.
- Check that themes are broader than individual codes.
- Check that challenges describe problems, not solutions.
- Check that design goals address the challenges.
- If creating Excel, verify the workbook exists and includes all required sheets.

## Suggested Method Note Text

This analysis follows Braun and Clarke's thematic analysis. The interview transcript was first reviewed to identify meaningful participant statements. These data extracts were assigned initial codes, related codes were grouped into themes, themes were further synthesized into design challenges, and each challenge was translated into a design goal. This preserves the analytic chain from user evidence to system design implications.
