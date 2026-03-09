# SOP: Initial Content Audit

## Goal
The goal of this directive is to ensure that all new content (Insights) added via the admin dashboard adheres to the "Warm Professional" design system and tone of voice.

## Inputs
- `insights.html` (for context)
- Data from `localStorage` (simulated for now)

## Execution
1. Read the latest entries from the admin logs.
2. Verify that titles are in Montserrat Alternates (if applicable via CSS).
3. Check for consistent use of keywords (Trust, Resilience, Human, Structure).

## Edge Cases
- Empty summaries: Refuse to generate if summary is too short.
- Missing categories: Suggest appropriate tags based on description.

## Learned Constraints
- Current implementation uses `localStorage`, making remote audits difficult without a bridge.
