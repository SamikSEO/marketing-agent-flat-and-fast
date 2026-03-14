# Skill: SEO Content

This skill governs all search-optimized content — blog posts, landing pages, pillar pages, glossary entries, and any content where organic search is a primary distribution channel. Use it alongside the root `CLAUDE.md` for brand voice, audiences, and legal guidelines.

---

## SEO Principles

1. **Write for people first, search engines second.** Google rewards content that genuinely helps readers. If it reads like it was written for an algorithm, rewrite it.
2. **Match search intent.** Before writing, understand what the searcher actually wants. A "what is X" query needs a definition, not a sales pitch.
3. **Earn the click and the stay.** Rankings get you impressions. A good title/meta gets you clicks. Quality content gets you dwell time and backlinks.
4. **Depth beats length.** A focused 1,500-word post that fully answers a question outperforms a 3,000-word post stuffed with filler.

---

## Keyword Strategy

### Keyword Research Process

<!-- TODO: Document your actual keyword research workflow. -->

1. **Start with a topic, not a keyword.** What question does your audience need answered?
2. **Research in [your SEO tool, e.g., Ahrefs, SEMrush]:**
   - Search volume (monthly)
   - Keyword difficulty (KD)
   - Search intent (informational, commercial, transactional, navigational)
   - SERP features (featured snippets, People Also Ask, video results)
3. **Select a primary keyword** and 3-5 secondary keywords per piece
4. **Check existing content** — do we already rank for this? Should we update an existing page instead of creating a new one?
5. **Log in [your content tracker, e.g., Airtable, spreadsheet, SEO tool]**

### Keyword Targeting Guidelines

| Content Type | KD Range | Volume Range | Intent |
|-------------|----------|-------------|--------|
| Blog post (awareness) | [e.g., 0-30] | [e.g., 500-5,000] | Informational |
| Blog post (consideration) | [e.g., 10-40] | [e.g., 200-2,000] | Commercial |
| Pillar page | [e.g., 30-60] | [e.g., 2,000-20,000] | Informational / Commercial |
| Landing page | [e.g., 20-50] | [e.g., 100-1,000] | Transactional |
| Glossary entry | [e.g., 0-20] | [e.g., 100-5,000] | Informational |
| Comparison page | [e.g., 10-40] | [e.g., 100-2,000] | Commercial |

### Topic Clusters

<!-- TODO: Define your pillar pages and supporting content clusters. -->

| Pillar Topic | Pillar Page URL | Supporting Topics (Clusters) |
|-------------|----------------|------------------------------|
| [e.g., "Customer Intelligence"] | [e.g., /customer-intelligence/] | [e.g., "what is customer intelligence," "customer data platforms," "churn prediction," "customer health scoring"] |
| [e.g., "Revenue Operations"] | [e.g., /revops/] | [e.g., "what is revops," "revops metrics," "revops tech stack," "revops vs sales ops"] |
| [Topic] | [URL] | [Cluster topics] |

---

## On-Page SEO Requirements

### Every SEO-Focused Page Must Have

- [ ] **Primary keyword** in the title tag (H1)
- [ ] **Primary keyword** in the URL slug
- [ ] **Primary keyword** in the first 100 words
- [ ] **Primary keyword** in at least one H2
- [ ] **Meta title** (50-60 characters, includes primary keyword)
- [ ] **Meta description** (150-160 characters, includes primary keyword, has a CTA or value prop)
- [ ] **At least 2-3 internal links** to related content
- [ ] **At least 1 external link** to a credible source (not a competitor)
- [ ] **Alt text** on all images (descriptive, includes keyword if natural)
- [ ] **Structured headers** (H1 > H2 > H3 hierarchy, no skipping levels)
- [ ] **Schema markup** where applicable (FAQ, HowTo, Article)

### Meta Title Formula

```
[Primary Keyword]: [Benefit or Clarifier] | [Company Name]
```

**Examples:**
- `Customer Health Scoring: How to Predict and Prevent Churn | [Company Name]`
- `RevOps Metrics: 15 KPIs Every Revenue Team Should Track | [Company Name]`
- `[Product] vs. [Competitor]: Honest Comparison for [Year] | [Company Name]`

**Rules:**
- 50-60 characters (Google truncates after ~60)
- Primary keyword as close to the front as possible
- Include brand name at the end (separated by `|`)
- Don't stuff keywords. It should read naturally.

### Meta Description Formula

```
[What the reader will learn/get]. [Why it matters or what makes this unique]. [CTA or hook].
```

**Examples:**
- `Learn how to build a customer health score that actually predicts churn. Includes a free template and step-by-step walkthrough. Read the guide.`
- `Compare [Product] and [Competitor] across pricing, features, and real user reviews. Updated for 2026.`

**Rules:**
- 150-160 characters
- Include the primary keyword naturally
- Write it like ad copy — this is your pitch to the searcher
- Don't use quotes or special characters that might get truncated

### URL Structure

- **Format:** `yoursite.com/[category]/[keyword-slug]`
- **Rules:**
  - Lowercase only
  - Hyphens between words (no underscores)
  - No stop words unless needed for readability
  - Keep it short — ideally 3-5 words after the domain
  - Never change a published URL without a 301 redirect

**Examples:**
- Good: `/blog/customer-health-scoring`
- Bad: `/blog/2026/03/14/the-ultimate-guide-to-customer-health-scoring-for-saas-companies`

---

## Content Structure Templates

### Blog Post (Informational / "What Is")

```markdown
# [What Is / Understanding] [Topic]: [Subtitle with Benefit]

[Opening paragraph: Define the concept in 2-3 sentences. Address the search intent directly.
Include the primary keyword naturally.]

## What Is [Topic]?

[Clear definition. 2-3 paragraphs. Use an analogy if it helps.]

## Why [Topic] Matters [for Your Audience]

[Connect the concept to the reader's goals. Use specific data or examples.]

## [Key Components / How It Works / Types of X]

### [Component 1]
[Explanation]

### [Component 2]
[Explanation]

### [Component 3]
[Explanation]

## How to [Implement / Get Started With] [Topic]

[Step-by-step if possible. Numbered list. Each step gets a brief explanation.]

## [Common Mistakes / Challenges / FAQ]

[Address the "People Also Ask" questions from the SERP.]

## [Key Takeaways / Next Steps]

[Summarize the 3-5 main points. Include a CTA — download, try the product, read related content.]
```

### Blog Post (Listicle / "Best / Top")

```markdown
# [Number] [Adjective] [Topic] [for Audience / Use Case] in [Year]

[Opening: Why this list matters. What criteria you used. 2-3 sentences.]

## Quick Summary

[Table or bulleted list of all items for scanners who don't want to read the full post.]

## 1. [Item Name]

**Best for:** [Use case]
**Key features:** [Bullets]
**Pricing:** [Range]
[2-3 paragraph review with honest pros/cons]

## 2. [Item Name]
[Same structure]

...

## How to Choose [Topic]

[Buying criteria, decision framework, or comparison table.]

## FAQ

[3-5 frequently asked questions pulled from SERP data.]
```

### Pillar Page

```markdown
# The Complete Guide to [Topic]

[Comprehensive introduction. This is your most thorough piece on this topic.
Establish authority. 3-5 paragraphs.]

## Table of Contents

[Link to every H2 section — helps UX and can win sitelinks in SERPs.]

## [Section 1: Foundation / Definition]
[Thorough coverage. Link to cluster content for deeper dives.]

## [Section 2: Why It Matters]
[Data, research, trends.]

## [Section 3: Core Components]
[Break into subsections. Each links to a dedicated blog post.]

## [Section 4: How to Implement]
[Step-by-step framework.]

## [Section 5: Tools & Resources]
[Mention your product naturally if relevant.]

## [Section 6: Advanced Topics]
[For readers who already know the basics.]

## [Section 7: FAQ]
[Comprehensive FAQ targeting long-tail queries. Use FAQ schema.]
```

---

## Internal Linking Strategy

### Rules

1. **Every new post must link to at least 2-3 existing pages** on your site
2. **Every new post should be linked FROM at least 2-3 existing pages** — go back and add links
3. **Anchor text should be descriptive** — use the target page's primary keyword when natural. Avoid "click here."
4. **Link to the pillar page** from every cluster post, and link from the pillar to every cluster post
5. **Don't over-link.** One internal link per 200-300 words is a good ratio.
6. **Prioritize contextual links** (within body text) over sidebar or footer links

### Internal Link Audit

<!-- TODO: Set a cadence for auditing internal links. -->

- **Frequency:** [e.g., Monthly]
- **Tool:** [e.g., Screaming Frog, Ahrefs Site Audit]
- **Check for:** Orphan pages (no internal links pointing to them), broken links, pages with too few or too many links

---

## Technical SEO Checklist

<!-- TODO: Customize based on your CMS and tech stack. -->

- [ ] Page loads in under [e.g., 3 seconds] (check with PageSpeed Insights)
- [ ] Mobile-friendly (responsive design, no horizontal scroll, tap targets spaced properly)
- [ ] Canonical tags set correctly (avoid duplicate content issues)
- [ ] XML sitemap includes the page and is submitted to Google Search Console
- [ ] robots.txt is not blocking the page
- [ ] No orphan pages — every page has at least one internal link
- [ ] Images are compressed and served in modern formats (WebP)
- [ ] Structured data / schema markup validates without errors
- [ ] HTTPS (no mixed content warnings)
- [ ] Hreflang tags if you have multi-language content

---

## Content Update Strategy

Existing content often has more SEO potential than new content. Prioritize updates when:

- A page ranks positions 5-20 (striking distance — a refresh could push it to page 1)
- A page has declining traffic over 3+ months
- The content is outdated (old stats, deprecated features, stale examples)
- A competitor has published something better on the same topic
- New internal pages exist that should be linked from this content

### Update Process

1. Pull current performance data (rankings, traffic, CTR) from [your SEO tool]
2. Analyze the SERP — what are top-ranking pages doing that we aren't?
3. Update content: refresh stats, add new sections, improve structure, update examples
4. Optimize meta title and description if CTR is below average
5. Add new internal links (to and from the page)
6. Republish with updated date (if your CMS supports it)
7. Resubmit to Google Search Console for indexing

---

## Measurement

### SEO KPIs

| Metric | Definition | Target | Tool |
|--------|-----------|--------|------|
| Organic sessions | Monthly visits from organic search | [e.g., 50,000/month] | [e.g., GA4] |
| Keyword rankings | Number of keywords ranking in positions 1-3, 4-10, 11-20 | [e.g., 50 in top 3] | [e.g., Ahrefs] |
| Organic CTR | Clicks / impressions from Google Search Console | [e.g., 3-5% average] | [e.g., GSC] |
| Backlinks | New referring domains per month | [e.g., 20/month] | [e.g., Ahrefs] |
| Page-level conversions | Organic visitors who complete a goal (signup, demo request) | [e.g., 2% conversion rate] | [e.g., GA4] |
| Content velocity | New SEO pages published per month | [e.g., 8/month] | [e.g., Content tracker] |
| Domain authority / rating | Overall domain strength | [e.g., DR 60+] | [e.g., Ahrefs] |

### Reporting Cadence

- **Weekly:** New content published, keyword movement (top movers up/down), quick wins identified
- **Monthly:** Full organic traffic report, page-level performance, technical issues, backlink report
- **Quarterly:** Content audit, topic cluster performance, competitive gap analysis, strategy adjustments
