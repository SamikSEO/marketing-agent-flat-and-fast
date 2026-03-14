# Skill: Analytics & Reporting

This skill governs how to pull, analyze, and present marketing data. Use it when building reports, interpreting campaign performance, defining metrics, or answering data questions. Use alongside the root `CLAUDE.md` for KPI definitions, tool references, and team context.

---

## Reporting Principles

1. **Start with the question, not the data.** Every report should answer a specific question: "Is this campaign working?" "Where should we invest next quarter?" "Why did MQLs drop?" If you can't state the question, don't build the report.
2. **Context over numbers.** A number without context is noise. Always include: the time period, the comparison (vs. target, vs. prior period, vs. benchmark), and the "so what."
3. **Make it actionable.** End every report section with a recommendation. "Organic traffic is down 12%" is an observation. "Organic traffic is down 12% — driven by 3 pages that lost rankings. Recommend refreshing these pages this sprint." is actionable.
4. **Be honest about what the data doesn't tell you.** If attribution is fuzzy, say so. If the sample size is too small, flag it. Overstating data confidence erodes trust.

---

## Data Sources & Access

<!-- TODO: Fill in your actual tools, access methods, and data owners. -->

| Data Source | Tool | What It Tells You | Access Method | Data Owner |
|------------|------|-------------------|--------------|------------|
| Website traffic | [e.g., Google Analytics 4] | Sessions, pageviews, conversions, user behavior | [e.g., Direct access, Looker dashboard] | [e.g., Marketing Ops] |
| Search performance | [e.g., Google Search Console] | Impressions, clicks, CTR, average position by query | [e.g., Direct access] | [e.g., SEO team] |
| Email performance | [e.g., HubSpot] | Open rates, CTR, conversions, list health | [e.g., HubSpot reports] | [e.g., Marketing Ops] |
| Social media | [e.g., Sprout Social] | Impressions, engagement, follower growth | [e.g., Sprout dashboards] | [e.g., Social lead] |
| Paid media | [e.g., Google Ads, LinkedIn Ads] | Spend, impressions, clicks, CPA, ROAS | [e.g., Platform dashboards, Looker] | [e.g., Growth team] |
| Pipeline & revenue | [e.g., Salesforce] | MQLs, SQLs, pipeline created, closed-won | [e.g., Salesforce reports, BI tool] | [e.g., Revenue Ops] |
| SEO rankings | [e.g., Ahrefs] | Keyword rankings, backlinks, domain authority | [e.g., Ahrefs dashboard] | [e.g., SEO team] |
| Product usage | [e.g., Amplitude, Mixpanel] | Feature adoption, activation, retention | [e.g., BI tool] | [e.g., Product team] |
| Customer feedback | [e.g., Zendesk, Intercom, G2] | NPS, support themes, review sentiment | [e.g., CS dashboards] | [e.g., Customer Success] |

---

## KPI Definitions

<!-- TODO: Precise definitions prevent misunderstandings. Two people looking at "MQLs" should see the same number. -->

### Lead & Pipeline Metrics

| Metric | Definition | How It's Calculated | Where It Lives |
|--------|-----------|-------------------|----------------|
| Marketing Qualified Lead (MQL) | [e.g., A contact who has reached a lead score of 50+ or completed a high-intent action (demo request, pricing page visit + content download within 7 days)] | [e.g., Automated via HubSpot lead scoring] | [e.g., HubSpot] |
| Sales Qualified Lead (SQL) | [e.g., An MQL that has been accepted by sales and has a confirmed meeting or active opportunity] | [e.g., Sales rep marks as SQL in Salesforce] | [e.g., Salesforce] |
| MQL-to-SQL Conversion Rate | SQLs / MQLs in a given period | [e.g., Calculated monthly, uses MQL creation date] | [e.g., Salesforce report] |
| Pipeline Generated | Total dollar value of new opportunities attributed to marketing | [e.g., Opportunities where marketing sourced = true, using first-touch attribution] | [e.g., Salesforce] |
| Pipeline Influenced | Total dollar value of opportunities where marketing played a role (any touch) | [e.g., Any opportunity where a contact engaged with marketing before or during the sales cycle] | [e.g., Salesforce + HubSpot] |
| Win Rate | Closed-won / (Closed-won + Closed-lost) | [e.g., Excludes opportunities disqualified or merged] | [e.g., Salesforce] |
| Sales Cycle Length | Average days from opportunity creation to close | [e.g., Median, not mean — outliers skew the average] | [e.g., Salesforce] |

### Engagement Metrics

| Metric | Definition | How It's Calculated | Where It Lives |
|--------|-----------|-------------------|----------------|
| Website Sessions | Total visits to the website (not unique visitors) | [e.g., GA4 session model] | [e.g., GA4] |
| Organic Traffic | Sessions where the source/medium is organic search | [e.g., GA4 filtered by source] | [e.g., GA4 + Looker] |
| Conversion Rate (Website) | Goal completions / sessions | [e.g., Goals: demo request, signup, content download] | [e.g., GA4] |
| Email Open Rate | Unique opens / delivered emails | [e.g., Note: iOS 15 MPP inflates this. Track trends, not absolutes.] | [e.g., HubSpot] |
| Email CTR | Unique clicks / delivered emails | [More reliable than open rate post-iOS 15] | [e.g., HubSpot] |
| Social Engagement Rate | (Likes + comments + shares + clicks) / impressions | [e.g., Calculated per post and averaged monthly] | [e.g., Sprout Social] |
| Content Downloads | Number of gated content downloads | [e.g., Form submissions on gated content pages] | [e.g., HubSpot] |

### Efficiency Metrics

| Metric | Definition | How It's Calculated | Where It Lives |
|--------|-----------|-------------------|----------------|
| Customer Acquisition Cost (CAC) | Total sales + marketing spend / new customers acquired | [e.g., Fully loaded — includes salaries, tools, ad spend] | [e.g., Finance dashboard] |
| Marketing CAC | Marketing spend only / new customers acquired where marketing sourced = true | [Isolates marketing efficiency] | [e.g., Finance + Salesforce] |
| LTV:CAC Ratio | Customer lifetime value / CAC | [e.g., Target is 3:1 or higher] | [e.g., Finance dashboard] |
| Cost Per MQL | Marketing spend / MQLs generated | [e.g., Break down by channel for channel-level efficiency] | [e.g., Calculated in BI tool] |
| ROAS (Paid) | Revenue attributed to ads / ad spend | [e.g., Uses 90-day attribution window] | [e.g., Ad platforms + CRM] |

---

## Attribution Model

<!-- TODO: Document your attribution model clearly. Attribution is one of the most common sources of confusion and conflict on marketing teams. -->

### Model Details

- **Model type:** [e.g., Multi-touch, linear / First-touch for sourcing, multi-touch for influence / Custom model]
- **Attribution window:** [e.g., 90 days from first touch to opportunity creation]
- **Source of truth:** [e.g., HubSpot attribution reports for marketing-sourced pipeline; Salesforce for total pipeline]
- **Known limitations:**
  - [e.g., "Dark social and word-of-mouth are under-attributed. We supplement with self-reported attribution ('How did you hear about us?') on demo request forms."]
  - [e.g., "Multi-device journeys may be undercounted — GA4 doesn't always stitch sessions across devices."]
  - [e.g., "Content influence on existing pipeline is tracked but not included in marketing-sourced numbers."]

### Channel Definitions

<!-- TODO: Define what counts as each channel to avoid misclassification. -->

| Channel | Definition | UTM Source Values |
|---------|-----------|-------------------|
| Organic Search | Traffic from unpaid search engine results | google, bing, duckduckgo (medium=organic) |
| Paid Search | Traffic from paid search ads | google, bing (medium=cpc) |
| Organic Social | Traffic from unpaid social media posts | linkedin, twitter, facebook (medium=social) |
| Paid Social | Traffic from paid social ads | linkedin, twitter, facebook (medium=paid-social) |
| Email | Traffic from email campaigns | hubspot, [tool] (medium=email) |
| Direct | Traffic with no referral or UTM data | (direct) / (none) |
| Referral | Traffic from other websites linking to us | Various (medium=referral) |
| [Channel] | [Definition] | [UTM values] |

---

## Report Templates

### Weekly Marketing Snapshot

**Purpose:** Quick pulse check for the marketing team.
**Audience:** Marketing team, marketing leadership
**Delivery:** [e.g., Slack, email, Monday standup]

```
## Weekly Marketing Snapshot: [Week of Date]

### Headline Numbers
| Metric | This Week | Last Week | Change | Target |
|--------|----------|----------|--------|--------|
| MQLs | X | X | +/-X% | X |
| Website sessions | X | X | +/-X% | X |
| Organic sessions | X | X | +/-X% | X |
| Email sends | X | -- | -- | -- |
| Avg open rate | X% | X% | +/-X pp | X% |

### Wins
- [Top-performing content, campaign, or milestone]
- [Notable metric improvement]

### Watch List
- [Any metric trending in the wrong direction]
- [Upcoming risk or dependency]

### This Week's Priorities
- [Key initiative 1]
- [Key initiative 2]
```

### Monthly Marketing Report

**Purpose:** Comprehensive performance review against targets.
**Audience:** Marketing leadership, exec team
**Delivery:** [e.g., Slide deck, Notion doc, email]

```
## Monthly Marketing Report: [Month Year]

### Executive Summary
[3-5 sentences: Did we hit our targets? What drove performance? What are we doing about gaps?]

### Pipeline & Revenue
| Metric | Actual | Target | % to Target | MoM Change |
|--------|--------|--------|-------------|-----------|
| MQLs | | | | |
| SQLs | | | | |
| MQL > SQL conversion | | | | |
| Pipeline generated ($) | | | | |
| Pipeline influenced ($) | | | | |

### Channel Performance
| Channel | Sessions | Leads | MQLs | Pipeline | Cost | CPA |
|---------|----------|-------|------|---------|------|-----|
| Organic search | | | | | $0 | |
| Paid search | | | | | | |
| Paid social | | | | | | |
| Email | | | | | | |
| Organic social | | | | | | |
| Referral | | | | | | |
| Direct | | | | | | |

### Content Performance
Top 5 pages by traffic: [list]
Top 5 pages by conversion: [list]
New content published: [count and titles]

### Email Performance
| Campaign | Sent | Open Rate | CTR | Conversions |
|----------|------|-----------|-----|-------------|
| | | | | |

### Social Performance
| Platform | Impressions | Engagement Rate | Followers (net) | Top Post |
|----------|------------|----------------|----------------|---------|
| | | | | |

### SEO Performance
| Metric | Current | Previous | Change |
|--------|---------|----------|--------|
| Organic sessions | | | |
| Keywords in top 3 | | | |
| Keywords in top 10 | | | |
| Domain rating | | | |
| New backlinks | | | |

### Key Takeaways & Recommendations
1. [Insight + recommendation]
2. [Insight + recommendation]
3. [Insight + recommendation]

### Next Month Priorities
1. [Priority]
2. [Priority]
3. [Priority]
```

### Campaign Post-Mortem

**Purpose:** Evaluate a specific campaign's performance and capture learnings.
**Audience:** Marketing team, stakeholders
**When:** Within 2 weeks of campaign completion

```
## Campaign Post-Mortem: [Campaign Name]

### Overview
- **Objective:** [What were we trying to achieve?]
- **Audience:** [Who did we target?]
- **Channels:** [Where did we run it?]
- **Timeline:** [Start and end dates]
- **Budget:** [Total spend]

### Results vs. Goals
| Metric | Goal | Actual | % to Goal | Notes |
|--------|------|--------|----------|-------|
| [Primary KPI] | | | | |
| [Secondary KPI] | | | | |
| [Efficiency metric] | | | | |

### What Worked
- [Specific tactic or element that exceeded expectations, with data]
- [Another]

### What Didn't Work
- [Specific tactic or element that underperformed, with data]
- [Another]

### Key Learnings
1. [Learning that should inform future campaigns]
2. [Learning]
3. [Learning]

### Recommended Next Steps
- [Action item with owner and timeline]
- [Action item]
```

---

## Data Hygiene & Governance

### UTM Standards

<!-- TODO: Enforce these standards across your team. Inconsistent UTMs make attribution impossible. -->

| Parameter | Format | Example |
|-----------|--------|---------|
| utm_source | Lowercase, platform name | `linkedin`, `google`, `hubspot` |
| utm_medium | Lowercase, channel type | `paid-social`, `email`, `cpc`, `organic-social` |
| utm_campaign | Lowercase, hyphenated, descriptive | `q1-2026-webinar-series`, `product-launch-featurex` |
| utm_content | Lowercase, hyphenated, identifies the variant | `cta-button-blue`, `hero-image-v2`, `audience-vp-revops` |
| utm_term | Lowercase, the keyword (paid search) | `customer-intelligence-platform` |

### UTM Builder

- **Tool:** [e.g., Google Campaign URL Builder, internal spreadsheet, UTM.io]
- **Where to log:** [e.g., Shared spreadsheet at [URL] — every campaign UTM must be logged here]

### Data Quality Rules

- **No manual data entry** for metrics that can be automated. If it's in a dashboard, pull from the dashboard.
- **Timestamp everything.** Every number needs a date range.
- **Cite your source.** Every metric in a report should reference the tool and the specific report/view.
- **Flag anomalies.** If a number looks wrong (sudden spike, zero where there should be data), investigate before reporting.
- **Don't mix timeframes.** If you're comparing month-over-month, make sure both months have the same number of days, or normalize.

---

## Common Analysis Requests

When asked to perform analysis, follow these frameworks:

### "Why did [metric] change?"

1. Identify the time period and magnitude of the change
2. Segment by channel — is it one channel or all channels?
3. Segment by audience — is it one segment or all segments?
4. Check for external factors (seasonality, industry events, algorithm updates)
5. Check for internal factors (content changes, technical issues, campaign launches/pauses)
6. Quantify the impact of each contributing factor
7. Recommend corrective action with expected impact

### "How is [campaign] performing?"

1. State the campaign objective and primary KPI
2. Report actual vs. target for each KPI
3. Break down by channel/tactic if multi-channel
4. Compare to benchmarks (internal historical or industry)
5. Identify the top-performing and underperforming elements
6. Recommend optimizations or next steps

### "What should we invest in next quarter?"

1. Pull performance by channel for the current quarter
2. Calculate efficiency metrics (CPA, ROAS, pipeline per dollar) by channel
3. Identify channels with the best efficiency and room to scale
4. Identify channels that are underperforming or at diminishing returns
5. Factor in strategic priorities beyond pure efficiency
6. Present a recommended allocation with rationale

---

## Measurement

### Reporting KPIs (Meta-Metrics)

| Metric | Target | Notes |
|--------|--------|-------|
| Report delivery on time | 100% | Weekly reports by [day/time], monthly by [day/time] |
| Data accuracy | 99%+ | Spot-check 3 metrics per report against source |
| Stakeholder satisfaction | [e.g., quarterly survey or feedback] | Are reports useful and actionable? |
| Time to insight | [e.g., <24 hours for ad-hoc requests] | How fast can we answer data questions? |
