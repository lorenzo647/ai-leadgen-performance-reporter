# AI LeadGen Performance Reporter

> AI-powered marketing performance reporter for EdTech lead generation campaigns. 
> Uses Claude to analyze Meta Ads & Google Ads KPIs and generate executive reports 
> with actionable optimization recommendations.

## Overview

This project is a prompt-engineering showcase that transforms Claude (Anthropic) 
into a specialized AI Co-Pilot for marketing teams managing lead generation 
campaigns in the EdTech industry.

The system:
- Reads weekly KPI data from Meta Ads and Google Ads campaigns
- Calculates week-over-week variations on key metrics (CPL, CTR, conversion rate, budget)
- Identifies best and worst performing campaigns
- Generates an executive report in Italian, formatted for stakeholder communication
- Provides 2-3 concrete optimization recommendations per campaign

## How to use

1. Open Claude at https://claude.ai (Free plan is sufficient)
2. Copy the content of docs/system-prompt.md and paste it as the first message
3. Copy the content of data/week-19-kpi.csv and paste it as the second message
4. Claude will generate the full executive report in 15-20 seconds

## Project structure

- docs/system-prompt.md — Core system prompt for Claude
- docs/benchmark-edtech.md — Industry KPI benchmarks
- docs/kpi-glossary.md — KPI definitions in Italian
- data/week-19-kpi.csv — Current week dummy data
- data/week-18-kpi.csv — Previous week dummy data
- examples/ — Screenshots of system outputs

## Use case

Designed specifically for marketing teams in scale-up EdTech companies that:
- Run paid acquisition on Meta Ads and Google Ads
- Work with external media agencies
- Need fast, structured weekly reporting for executives
- Want AI-augmented decision-making for campaign optimization

## Built by

Lorenzo Ricci — Project Manager & Communications Specialist

Built as a showcase project for marketing roles in EdTech scale-ups.
