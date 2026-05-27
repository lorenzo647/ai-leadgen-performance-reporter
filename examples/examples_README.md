# Examples — AI LeadGen Performance Reporter in Action

This folder contains screenshots demonstrating the AI LeadGen Performance Reporter in action, powered by Claude (Sonnet 4.6, Free plan) and the system prompt provided in `/docs/system-prompt.md`, using the dummy datasets in `/data/`.

## Screenshots

1. **`01-claude-system-prompt-loaded.png`** — Claude receives the full system prompt (visible as "PASTED" block) and confirms readiness to operate as senior AI Marketing Analyst.

2. **`02-input-data-csv.png`** — User provides 2 weeks of structured CSV data covering 6 campaigns across Meta Ads and Google Ads (Awareness, Conversion, Retargeting, Search Brand, Search Generic, Performance Max).

3. **`03-calcoli-interni-executive-summary.png`** — Claude generates the report following the structured format: first a mandatory `<calcoli_interni>` chain-of-thought block with all aggregate totals computed step-by-step (deterministic arithmetic), then the Executive Summary in Italian with total spend, leads, weighted CPL, and overall trend.

4. **`04-report-output-detail.png`** — Per-campaign analysis with W-on-W variations, verdict icon, strategic insight + Top 3 Insights of the week. Operational recommendations with specific, measurable, time-bound actions are available in the full `sample-output-W19.md` in this folder.

## Sample output highlights

For the provided dataset, the system identifies:
- **Top performers:** Conversion Meta (CPL €14.19, conversion rate 10.41%) and Retargeting Meta (CPL €9.78, conversion rate 9.95%)
- **Underperformer:** PerformanceMax Google (CPL €22.27, conversion rate 4.68% — below benchmark threshold)
- **Strategic insight:** Meta beats Google on CPL efficiency in W19 by 33% on average
- **Actionable recommendation:** Test a +15-20% budget increase on Conversion Meta with CPL monitoring at 48h

## How to reproduce

1. Open Claude at https://claude.ai in a new conversation (Free plan is sufficient)
2. Paste the content of `/docs/system-prompt.md` as the first message
3. Paste the content of `/data/week-18-kpi.csv` (baseline) and then `/data/week-19-kpi.csv` (current week) as the second message
4. Claude produces the full executive report following the structured format in 15-25 seconds
