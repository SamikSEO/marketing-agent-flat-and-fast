# Skill: Email Campaigns

This skill governs all email marketing content — nurture sequences, newsletters, product announcements, event invitations, and transactional emails. Use it alongside the root `CLAUDE.md` for brand voice, audiences, and legal guidelines.

---

## Email Principles

1. **Respect the inbox.** Every email must earn the open and justify the reader's time. If you can't articulate why someone should care about this email, don't send it.
2. **One email, one job.** Each email should have a single primary CTA. Supporting links are fine, but the reader should never wonder "what do they want me to do?"
3. **Write for scanners.** Most people skim email. Use short paragraphs, bold key points, and clear structure.
4. **Test everything.** Subject lines, send times, CTAs, and content length should be tested systematically, not guessed at.

---

## Subject Lines

### Rules

- **Length:** 30-50 characters (6-10 words) for best open rates. Preview text extends this — use it.
- **Preview text:** Always write custom preview text (40-90 characters). It should complement the subject line, not repeat it.
- **Personalization:** Use `[First Name]` in subject lines sparingly — max once per sequence. It increases open rates but loses impact with overuse.
- **Urgency:** Real urgency is fine ("Registration closes Friday"). Manufactured urgency is not ("LAST CHANCE" on an evergreen offer).
- **Emoji:** [e.g., "Use max one emoji per subject line. Test before committing to regular use. Never use in enterprise-focused emails."]

### Subject Line Formulas

| Formula | Example | Best For |
|---------|---------|----------|
| Benefit + Specificity | "Cut your reporting time by 60%" | Product emails, nurture |
| Question | "Is your attribution model lying to you?" | Thought leadership, nurture |
| How-to | "How to build a churn prediction model in 20 min" | Educational, nurture |
| Social proof | "How [Customer] reduced churn by 30%" | Case study, bottom-of-funnel |
| News / Update | "[Product] now connects to Snowflake" | Product updates |
| Curiosity gap | "The metric your board actually cares about" | Newsletter, thought leadership |
| Direct | "Your monthly marketing report is ready" | Reports, transactional |

### Subject Lines to Avoid

- ALL CAPS or excessive punctuation (!!!)
- "Newsletter #47" or any numbered-issue format with no hook
- "Quick question" or "Touching base" (sounds like sales spam)
- Misleading subjects that don't match the email body
- "Re:" or "Fwd:" when it's not actually a reply or forward
- [Add your own anti-patterns]

---

## CAN-SPAM & Compliance

<!-- TODO: Have legal review this section. Non-compliance carries real fines. -->

### Required Elements (Every Marketing Email)

- **Physical mailing address:** [Your company address] must appear in the footer
- **Unsubscribe link:** Must be visible, functional, and honored within 10 business days
- **Accurate "From" name:** Must clearly identify the sender as [Company Name] or an employee of [Company Name]
- **Accurate subject line:** Must reflect the content of the email
- **Commercial identification:** If the email is an ad, it must be identified as such

### GDPR Requirements (If Emailing EU/UK Contacts)

- Recipients must have explicitly opted in to receive marketing emails
- Unsubscribe must be one-click (no "login to manage preferences" as the only option)
- Data processing basis must be documented in your CRM
- Include a link to your privacy policy in the footer

### CASL Requirements (If Emailing Canadian Contacts)

<!-- TODO: Add if you market to Canada. Remove if not. -->

- Express consent required (implied consent expires after 2 years)
- Must include sender identification and contact information
- Unsubscribe mechanism must remain active for at least 60 days

### Email Footer Template

<!-- TODO: Customize this template with your actual information. -->

```
[Company Name] | [Street Address], [City], [State] [ZIP]
You're receiving this because you [signed up / downloaded / attended].
[Unsubscribe] | [Manage Preferences] | [Privacy Policy]
```

---

## Email Types & Templates

### Nurture Sequence

**Purpose:** Move leads from awareness to consideration to decision.

**Structure:**
<!-- TODO: Customize the sequence length, timing, and content for your buyer journey. -->

| Email # | Timing | Subject Formula | Content Focus | CTA |
|---------|--------|----------------|--------------|-----|
| 1 | Immediately after opt-in | Welcome + value delivery | Deliver the promised resource. Set expectations for future emails. | Consume the resource |
| 2 | Day 3 | Educational — pain point | Address the #1 pain point for this segment. Teach something useful. | Read blog post or guide |
| 3 | Day 7 | Social proof | Share a customer story relevant to their segment. | Read case study |
| 4 | Day 12 | Product-led insight | Show how [Product] solves the problem discussed in email 2. | Watch demo or try free |
| 5 | Day 18 | Objection handling | Address the top objection for this segment. | Talk to sales / start trial |
| 6 | Day 25 | Last touch | Direct ask or valuable resource. Respect their time. | Final CTA or "no hard feelings" |

**Nurture email template:**

```
Subject: [Subject line]
Preview: [Preview text]

Hi [First Name],

[Opening hook — one sentence that connects to their pain point or interest]

[2-3 short paragraphs of value. Teach something, share an insight, or tell a story.
Every paragraph should earn its place.]

[Transition to CTA — connect the value to the next step]

[CTA Button or Link: Clear, action-oriented text]

[Optional: P.S. line with a secondary link or personal touch]

--
[Sender Name]
[Title], [Company Name]
```

### Newsletter

**Purpose:** Regular touchpoint that builds trust and keeps [Company Name] top of mind.

- **Cadence:** [e.g., Biweekly, every other Tuesday]
- **Audience:** [e.g., All opted-in contacts, or specific segments]
- **Length:** 300-500 words
- **Sections:**
  1. **Lead story:** One insight, trend, or POV (not a product pitch)
  2. **Quick hits:** 2-3 links to recent content, industry news, or resources
  3. **Product corner:** One brief product update or tip (keep it under 20% of the email)
  4. **CTA:** One clear next step

### Product Announcement

**Purpose:** Inform customers and prospects about new features, updates, or launches.

- **Subject formula:** "[Feature Name]: [Benefit in 5 words or less]"
- **Structure:**
  1. What's new (1 sentence)
  2. Why it matters to you (2-3 sentences tied to their workflow)
  3. How it works (bullet points or short paragraph)
  4. CTA (try it, learn more, watch a demo)
- **Audience targeting:** Send to segments most likely to use the feature. Don't blast everyone.

### Event Invitation

**Purpose:** Drive registrations for webinars, conferences, or community events.

- **Send cadence:**
  - Invite: 2-3 weeks before
  - Reminder 1: 1 week before
  - Reminder 2: Day before or morning of
  - Follow-up: Day after (recording + key takeaways)
- **Subject formula:** "[Event type]: [Compelling topic] | [Date]"
- **Key elements:** Date/time with timezone, speaker names, what attendees will learn, registration CTA

---

## Segmentation Strategy

<!-- TODO: Define your segmentation approach. The more targeted your emails, the better they perform. -->

### Segmentation Dimensions

| Dimension | Values | Used For |
|-----------|--------|----------|
| Lifecycle stage | Subscriber, Lead, MQL, SQL, Customer, Churned | Matching content to buyer journey |
| Industry | [Your target industries] | Industry-specific messaging and case studies |
| Role / persona | [Map to audience segments in CLAUDE.md] | Pain-point-specific content |
| Company size | [e.g., SMB, Mid-market, Enterprise] | Adjusting language and proof points |
| Product interest | [e.g., by feature or use case] | Targeted product content |
| Engagement level | Active, Lapsed, Dormant | Re-engagement campaigns, frequency adjustments |
| [Your dimension] | [Values] | [Purpose] |

### Suppression Rules

Always suppress the following from marketing sends:

- Contacts who have unsubscribed (legally required)
- Contacts marked as "Do Not Email" in the CRM
- Contacts who have bounced [e.g., 3+] times
- Active sales opportunities (unless the sales rep approves)
- Customers currently in an active support escalation
- [Add your own suppression rules]

---

## A/B Testing

### What to Test

| Element | Priority | Sample Size Needed | Notes |
|---------|----------|-------------------|-------|
| Subject line | High | 1,000+ per variant | Test one variable at a time. Run for at least 2-4 hours before picking a winner. |
| Send time | High | 2,000+ per variant | Test day of week and time of day separately. |
| CTA text | Medium | 1,000+ per variant | "Start free trial" vs. "See it in action" vs. "Book a demo" |
| From name | Medium | 2,000+ per variant | Company name vs. person name vs. "Name at Company" |
| Email length | Low | 2,000+ per variant | Test meaningfully different lengths, not minor edits |
| Design (text vs. HTML) | Low | 2,000+ per variant | Plain text often wins for nurture; HTML for newsletters |

### Testing Rules

1. **One variable at a time.** If you change the subject line and the CTA, you don't know which drove the result.
2. **Statistical significance matters.** Don't call a winner until you have enough data. Use [your testing tool]'s built-in significance calculator.
3. **Document results.** Log every test and result in [e.g., a shared spreadsheet or Notion database] so the team learns over time.
4. **Test for the right metric.** Subject lines should be tested on open rate. CTAs should be tested on click rate. Sequences should be tested on conversion rate.

---

## Deliverability Best Practices

- **Sender reputation:** Monitor your domain and IP reputation with [e.g., Google Postmaster Tools, Sender Score]
- **Authentication:** Ensure SPF, DKIM, and DMARC are configured for your sending domain
- **List hygiene:** Remove hard bounces immediately. Sunset contacts with no engagement in [e.g., 6 months]
- **Warm-up:** When sending from a new domain or IP, warm up gradually — start with your most engaged contacts
- **Spam trigger words:** Avoid excessive use of "free," "guarantee," "act now," "limited time" — especially in subject lines
- **Image-to-text ratio:** Keep it balanced. Don't send image-only emails. Many clients block images by default.
- **Unsubscribe rate:** If any send exceeds [e.g., 0.5%] unsubscribe rate, review the content and targeting before sending again

---

## Measurement

### Email KPIs

| Metric | Definition | Target | Tool |
|--------|-----------|--------|------|
| Open rate | Unique opens / delivered | [e.g., 30-40%] | [e.g., HubSpot] |
| Click-through rate (CTR) | Unique clicks / delivered | [e.g., 3-5%] | [e.g., HubSpot] |
| Click-to-open rate (CTOR) | Unique clicks / unique opens | [e.g., 10-15%] | [e.g., HubSpot] |
| Conversion rate | Desired action / delivered | [e.g., varies by campaign] | [e.g., HubSpot + GA4] |
| Unsubscribe rate | Unsubscribes / delivered | [e.g., <0.3%] | [e.g., HubSpot] |
| Bounce rate | Bounces / sent | [e.g., <2%] | [e.g., HubSpot] |
| List growth rate | (New subscribers - unsubscribes) / total list | [e.g., 5%/month] | [e.g., HubSpot] |
| Revenue influenced | $ pipeline or revenue touched by email | [e.g., tracked quarterly] | [e.g., CRM attribution] |

### Reporting Cadence

- **Per send:** Open rate, CTR, unsubscribes, bounces (automated)
- **Weekly:** Campaign performance summary, A/B test results
- **Monthly:** Full funnel metrics, list health, deliverability audit
- **Quarterly:** Strategy review, sequence performance, ROI analysis
