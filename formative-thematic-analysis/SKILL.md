---
name: formative-thematic-analysis
description: Analyze formative study interview transcripts using Braun and Clarke thematic analysis. Use when the user provides interviewer/interviewee dialogue and wants codes, themes, design challenges, proposed design solutions, and an Excel design-analysis table for an HCI or system-design project.
---

# Formative Thematic Analysis

Use this skill to analyze formative interview transcripts for early-stage system design research. The input is usually a `.txt`, `.docx`, transcript, or pasted dialogue containing interviewer and interviewee turns. The output should help the user move from participant language to codes, themes, design challenges, and proposed design solutions.

## Method Basis

Use thematic analysis based on:

Braun, V., & Clarke, V. (2006). *Using thematic analysis in psychology*. *Qualitative Research in Psychology*, 3(2), 77-101. https://doi.org/10.1191/1478088706qp063oa

Treat thematic analysis as a qualitative method for identifying, analyzing, and reporting repeated patterns of meaning in textual data. Do not merely summarize the transcript. Preserve a clear evidence chain from participant language to design implications.

## Core Workflow

1. Read the transcript and identify speakers.
   - Separate interviewer prompts from interviewee responses.
   - Prioritize interviewee language as evidence.
   - Use interviewer prompts only as context.

2. Select meaningful data extracts.
   - Choose short, representative participant quotes.
   - Do not include separate ID, timestamp, or speaker columns in the final workbook unless the user explicitly asks.
   - Avoid overlong quotes; excerpt only the part that supports the code.

3. Generate initial codes.
   - A code should capture what the participant is saying or implying.
   - Keep codes concise and close to the data.
   - Multiple extracts may share a code.

4. Group codes into themes.
   - Multiple related codes can form one theme.
   - A theme should describe a recurring pattern of meaning, not just a topic label.
   - Themes should be internally coherent and distinct from each other.

5. Derive design challenges from themes.
   - Multiple themes can point to one design challenge.
   - Generate 5-10 design challenges when the transcript has enough evidence.
   - A challenge should phrase the underlying design problem the system must address.
   - Prefer "How might the system..." / "How can the platform..." wording in English work, or "如何..." wording in Chinese work.

6. Translate each challenge into a design proposed solution.
   - Each challenge should map to one proposed solution.
   - Proposed solutions should be actionable system directions, not vague design goals.
   - Add concrete feature ideas only after the proposed solution.

## Required Excel Output

When generating an Excel workbook, use two sheets:

1. `Analysis Table`
   - `User Data`
   - `Code`
   - `Theme`
   - `Design Challenge`
   - `Design Proposed Solution`
   - `Feature Ideas`

2. `Method Notes`
   - Explain that the analysis follows Braun and Clarke thematic analysis.
   - State the analysis chain: data extract -> code -> theme -> design challenge -> design proposed solution.
   - State that multiple codes may form one theme, multiple themes may point to one challenge, and each challenge maps to one proposed solution.
   - Note whether the analysis is preliminary if based on a small number of interviews.

## Workbook Formatting

- Put all analysis content except method notes in one `Analysis Table` sheet.
- Do not include ID, time, speaker, or explanation columns unless the user explicitly requests them.
- Merge repeated cells where possible, especially repeated themes, challenges, proposed solutions, and feature ideas.
- Center table content horizontally and vertically.
- Enable text wrapping.
- Make `User Data` and `Code` columns wide enough to contain the text.
- Add visible black line borders around the table cells.
- Keep `Method Notes` as a separate sheet.

## Analysis Rules

- Do not force every code to become its own theme.
- Do not force every theme to become its own challenge.
- Do not jump directly from a single quote to a proposed solution unless the user explicitly asks for a quick brainstorm.
- Distinguish `design challenge` from `design proposed solution`:
  - Challenge: the design problem exposed by themes.
  - Proposed solution: what the system should provide to address the challenge.
- Preserve traceability: every theme should be grounded in participant quotes, and every challenge should be grounded in one or more themes.
- When the transcript is Chinese, write tables in Chinese while retaining useful method terms such as `Code`, `Theme`, `Design Challenge`, and `Design Proposed Solution`.

## Quality Checks

Before finalizing:

- Check that participant quotes are not invented or overly paraphrased.
- Check that codes are grounded in quotes.
- Check that themes are broader than individual codes.
- Check that challenges describe problems, not solutions.
- Check that proposed solutions address the challenges.
- If creating Excel, verify the workbook exists, includes `Analysis Table` and `Method Notes`, and has visible borders.

## Suggested Method Note Text

This analysis follows Braun and Clarke's thematic analysis. The interview transcript was first reviewed to identify meaningful participant statements. These data extracts were assigned initial codes, related codes were grouped into themes, themes were further synthesized into design challenges, and each challenge was translated into a design proposed solution. This preserves the analytic chain from user evidence to system design implications.
