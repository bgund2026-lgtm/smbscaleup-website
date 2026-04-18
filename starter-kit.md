# Small Business AI Agent Starter Kit

### Deploy your first AI agent in 5 days — even if you're not technical

---

## What You Get

This kit includes everything a small business owner needs to go from "AI sounds complicated" to "my agent handles 70% of my customer support while I sleep."

**12 documents, templates, and frameworks:**

1. ✅ **12 Ready-to-Deploy Agent Workflows** — Copy, customize, launch today
2. ✅ **25 Tested Business Prompts** — Customer service, sales, ops, finance, HR, strategy
3. ✅ **5-Day Sprint Plan** — Zero to deployed agent by Friday
4. ✅ **AI Cost Calculator** — Know exactly what your agent will cost to run
5. ✅ **25-Point Security Checklist** — Don't expose customer data
6. ✅ **Platform Comparison Guide** — Make.com vs Zapier vs N8N vs OpenClaw vs custom
7. ✅ **ROI Tracker Template** — Measure real time and money saved
8. ✅ **Scaling Playbook** — From 1 agent to 5 without breaking things
9. ✅ **Vendor Evaluation Scorecard** — Pick the right AI tools without getting sold
10. ✅ **Team Adoption Guide** — Get your employees to actually use the AI
11. ✅ **Quick-Start Cheat Sheet** — 1-page reference for daily operations
12. ✅ **Troubleshooting Playbook** — When your agent goes wrong (and it will)

---

## Chapter 1: The 70% Rule (And Why It Saves You 4-6 Weeks)

Most small business owners think they need an AI agent that handles 100% of a task perfectly. That's the trap. You'll spend months tweaking prompts, testing edge cases, and never shipping.

**The 70% Rule:** Ship your agent when it handles 70% of the task reliably. Have a human review the remaining 30%. Then iterate.

Why 70%?
- A customer support agent that answers 70% of tickets automatically still saves you **4+ hours per day**
- A scheduling agent that books 70% of appointments still eliminates **2+ hours of phone tag**
- A reporting agent that generates 70% of your weekly numbers still saves **3+ hours of spreadsheet work**

The remaining 30% is where your human judgment matters. The client who's furious and needs a real person. The appointment with weird constraints. The report with an anomaly that needs explanation.

**Ship at 70%. Review the 30%. Improve weekly.**

The alternative — waiting for 100% — means you ship nothing. Every week you delay is 20-40 hours of work your agent could be doing.

---

## Chapter 2: 12 Ready-to-Deploy Agent Workflows

Each workflow includes: what it does, what tools you need, estimated setup time, and monthly cost.

### Workflow 1: Customer Support Auto-Responder

**What it does:** Reads incoming support emails/chat messages, categorizes them (billing, technical, general, complaint), drafts a response, and either sends it or queues it for human review based on confidence.

**Tools:** OpenAI API ($5-20/mo) + your email inbox or chat tool

**Setup time:** 2-3 hours

**Monthly cost:** $5-20

**Prompt:**
```
You are a customer support agent for [BUSINESS NAME], a [INDUSTRY] company.

Read the customer message below and:
1. Categorize: billing, technical, general inquiry, complaint, or urgent
2. Draft a response using our standard tone: helpful, concise, professional
3. If the issue involves refunds over $[AMOUNT], account changes, or legal concerns → flag for human review
4. Otherwise → prepare to send

Our policies:
- Refunds under $[AMOUNT]: approve automatically
- Refunds over $[AMOUNT]: escalate to manager
- Technical issues: provide troubleshooting steps from our FAQ
- Response time SLA: under 2 hours during business hours

Customer message: [PASTE MESSAGE HERE]
```

**Human review trigger:** Any complaint, refund over your threshold, or message the AI flags as low-confidence.

---

### Workflow 2: Lead Qualification Agent

**What it does:** Receives inbound leads (form submissions, emails, DMs), asks qualifying questions, scores the lead (hot/warm/cold), and routes hot leads to you immediately.

**Tools:** OpenAI API ($5-15/mo) + your CRM or email

**Setup time:** 1-2 hours

**Monthly cost:** $5-15

**Prompt:**
```
You are a lead qualification agent for [BUSINESS NAME].

When a new lead comes in:
1. Send a friendly introduction: "Thanks for reaching out! A couple quick questions so I can connect you with the right person..."
2. Ask these qualifying questions:
   - What's the biggest challenge you're facing with [YOUR SERVICE AREA]?
   - What's your timeline for getting this resolved?
   - What's your budget range? (if appropriate for your industry)
   - How many [EMPLOYEES/LOCATIONS/UNITS]?
3. Score the lead:
   - HOT: Budget confirmed + timeline within 30 days + clear pain point
   - WARM: Expressed interest + some qualification met
   - COLD: Just browsing, no budget, no timeline
4. For HOT leads → immediately notify [YOUR NAME] at [PHONE/EMAIL]
5. For WARM leads → send more info, schedule follow-up in 3 days
6. For COLD leads → add to nurture sequence

Lead details: [PASTE LEAD INFO HERE]
```

---

### Workflow 3: Appointment Booking Agent

**What it does:** Handles the back-and-forth of scheduling — confirms availability, sends calendar invites, handles reschedules, and sends reminders.

**Tools:** Calendly/Cal.com (free tier) + OpenAI API ($3-10/mo)

**Setup time:** 1-2 hours

**Monthly cost:** $3-10

**Prompt:**
```
You are a scheduling assistant for [BUSINESS NAME].

Available times: [YOUR AVAILABILITY — e.g., "Mon-Wed 9am-12pm, Thu-Fri 2pm-5pm"]

When someone wants to book:
1. Check their requested time against availability
2. If available → confirm and send: "Great! I've got you booked for [DATE/TIME]. You'll receive a calendar invite shortly."
3. If not available → offer 3 alternative times close to their request
4. If they need to reschedule → find the next available slot
5. 24 hours before appointment → send reminder with any prep instructions
6. 1 hour after appointment → send follow-up: "How did everything go?"

Always confirm the appointment type, duration, and any prep needed.
```

---

### Workflow 4: Invoice & Payment Follow-Up Agent

**What it does:** Monitors unpaid invoices, sends polite follow-ups on a schedule, escalates to you when payments are severely overdue.

**Tools:** Your accounting software API + OpenAI API ($5-10/mo)

**Setup time:** 2-3 hours

**Monthly cost:** $5-10

**Follow-up schedule:**
- 3 days before due: "Just a reminder, invoice #[X] is due on [DATE]"
- 1 day after due: "Hi [NAME], invoice #[X] for $[AMOUNT] is now past due. Let me know if you have any questions."
- 7 days overdue: "Following up on invoice #[X] — it's now a week past due. Can we get this sorted?"
- 14 days overdue: **ESCALATE** — flag for human to call

**Prompt for each follow-up:**
```
Write a [3-day-reminder / 1-day-past-due / 7-days-overdue] follow-up email for:
- Client: [NAME]
- Invoice: #[NUMBER]
- Amount: $[AMOUNT]
- Due date: [DATE]
- Days overdue: [X]

Tone: Professional, friendly, firm. Never accusatory. Assume they forgot, not that they're avoiding payment.
```

---

### Workflow 5: Social Media Content Agent

**What it does:** Generates weekly social media posts based on your business updates, industry news, and content themes you define.

**Tools:** OpenAI API ($5-15/mo) + scheduling tool (Buffer free tier, Later, etc.)

**Setup time:** 1-2 hours

**Monthly cost:** $5-15

**Prompt:**
```
You are a social media manager for [BUSINESS NAME], a [INDUSTRY] company in [CITY/REGION].

Content themes for this week:
1. [THEME 1 — e.g., "Behind the scenes"]
2. [THEME 2 — e.g., "Customer success story"]
3. [THEME 3 — e.g., "Industry tip"]

Generate 5 posts:
- 2 for [PLATFORM — Instagram/LinkedIn/Twitter]
- 1 how-to or tip post
- 1 engagement question
- 1 promotional (soft sell)

Each post: under 150 words, include 3-5 relevant hashtags, match our brand voice (professional but approachable).

Do NOT use: "Game-changing," "Revolutionize," "Synergy," or corporate buzzwords.
```

---

### Workflow 6: Weekly Reporting Agent

**What it does:** Pulls data from your tools (sales, support tickets, website traffic), generates a summary report, and emails it to you every Monday morning.

**Tools:** Make.com/Zapier (free tier) + OpenAI API ($5-10/mo) + your tools' APIs

**Setup time:** 2-3 hours

**Monthly cost:** $5-15

**Prompt:**
```
Generate a weekly business summary from the following data:

SALES:
- Revenue this week: $[AMOUNT]
- New customers: [NUMBER]
- Churned customers: [NUMBER]

SUPPORT:
- New tickets: [NUMBER]
- Resolved tickets: [NUMBER]
- Average response time: [TIME]

WEBSITE:
- Visitors: [NUMBER]
- Top pages: [LIST]
- Conversion rate: [PERCENTAGE]

For each section:
1. Compare to last week (↑↓→)
2. Flag anything that changed more than 20%
3. One-sentence recommendation for the biggest opportunity

End with: "Your #1 priority this week should be [RECOMMENDATION]."

Keep the whole report under 300 words. I'm reading this on my phone.
```

---

### Workflow 7: Employee Onboarding Agent

**What it does:** Sends new hires their onboarding materials on a schedule, collects signed documents, answers common questions, and notifies HR when steps are complete.

**Tools:** OpenAI API + email/Slack

**Setup time:** 2-3 hours

**Monthly cost:** $5-10

**Day 1 prompt:**
```
You are an onboarding assistant for [BUSINESS NAME].

Welcome [NEW HIRE NAME] to the team! Send them:
1. Welcome message with their start date, manager name, and first-day schedule
2. Employee handbook (link)
3. IT setup checklist: email, Slack, tools access
4. Benefits enrollment form (link + deadline)
5. First-week schedule overview

Be warm and helpful. They're probably nervous.
```

---

### Workflow 8: Inventory Alert Agent

**What it does:** Monitors stock levels, alerts you when items hit reorder points, and can automatically generate purchase orders.

**Tools:** Your inventory system + OpenAI API

**Setup time:** 1-2 hours

**Monthly cost:** $3-10

**Prompt:**
```
Check current inventory levels against reorder points:

CURRENT STOCK:
[ITEM]: [QUANTITY] on hand, reorder point: [THRESHOLD]

For any items at or below reorder point:
1. Flag as "REORDER NEEDED"
2. Suggest order quantity: [REORDER POINT × 2] or [LEAD TIME × AVG DAILY USAGE]
3. Check if vendor [VENDOR NAME] has this item on recurring order
4. If yes → confirm next delivery date
5. If no → draft purchase order for human approval

Priority: Items with zero stock first, then items below 50% of reorder point.
```

---

### Workflow 9: Competitor Monitoring Agent

**What it does:** Checks competitor websites/socials weekly, summarizes changes (new products, pricing changes, marketing shifts), and flags what matters.

**Tools:** Web scraping (free tools) + OpenAI API ($5-10/mo)

**Setup time:** 2 hours

**Monthly cost:** $5-10

**Prompt:**
```
Review the following competitor updates from the past week:

[COMPETITOR 1]: [SUMMARY OF CHANGES]
[COMPETITOR 2]: [SUMMARY OF CHANGES]
[COMPETITOR 3]: [SUMMARY OF CHANGES]

For each competitor, flag:
1. New products or services launched
2. Price changes (up or down)
3. Marketing campaigns or positioning shifts
4. Any customer complaints or negative press

Then answer:
- What's the biggest threat to our business this week?
- What's the biggest opportunity?
- Should we adjust anything immediately?

Keep it under 200 words. I'm a business owner, not an analyst.
```

---

### Workflow 10: Customer Feedback Analyzer

**What it does:** Collects reviews, survey responses, and support tickets, categorizes feedback by theme, and identifies patterns requiring action.

**Tools:** OpenAI API ($5-15/mo) + your review sources

**Setup time:** 1-2 hours

**Monthly cost:** $5-15

**Prompt:**
```
Analyze this week's customer feedback:

REVIEWS: [PASTE REVIEWS]
SURVEY RESPONSES: [PASTE SURVEYS]
SUPPORT TICKETS SUMMARY: [PASTE SUMMARY]

1. Categorize all feedback into themes (product quality, pricing, service speed, communication, etc.)
2. Rate sentiment: Positive / Neutral / Negative for each theme
3. Identify patterns: If 2+ people mention the same issue → ACTION ITEM
4. Highlight the single most impactful thing to fix this week
5. Highlight the single most valuable thing customers love (protect this)

Format:
- Theme | Sentiment | Mentions | Action needed?
- Top fix: [ONE THING]
- Top strength: [ONE THING]
```

---

### Workflow 11: Expense Categorization Agent

**What it does:** Reads your bank/credit card transactions, categorizes expenses, flags unusual spending, and prepares data for your bookkeeper.

**Tools:** Bank CSV export + OpenAI API ($3-10/mo)

**Setup time:** 1-2 hours

**Monthly cost:** $3-10

**Prompt:**
```
Categorize the following business expenses:

[TRANSACTION LIST — merchant, amount, date]

Categories: Office Supplies, Software/Subscriptions, Travel, Meals/Entertainment, Marketing, Professional Services, Equipment, Utilities, Insurance, COGS, Other

Rules:
- Meals with clients → Meals/Entertainment
- Amazon purchases → check description: likely Office Supplies or Equipment
- Unknown merchants over $500 → FLAG for review
- Recurring charges → flag if amount changed more than 20% from last month

Output as a table: Date | Merchant | Amount | Category | Flag?
```

---

### Workflow 12: Daily Briefing Agent

**What it does:** Every morning at 7am, compiles your day's meetings, deadlines, pending tasks, and any urgent notifications into a 2-minute briefing.

**Tools:** Calendar API + task manager API + OpenAI API ($3-10/mo)

**Setup time:** 1-2 hours

**Monthly cost:** $3-10

**Prompt:**
```
Generate a morning briefing for [NAME] at [BUSINESS NAME]:

TODAY'S CALENDAR:
[MEETINGS AND EVENTS]

DEADLINES THIS WEEK:
[TASKS AND DUE DATES]

URGENT ITEMS:
[ANY FLAGS FROM OTHER AGENTS — unpaid invoices, customer complaints, inventory alerts]

Format:
1. 🚨 URGENT (items needing response today)
2. 📅 Today's schedule (with prep time noted)
3. ⏰ This week's deadlines (ordered by due date)
4. 💡 One suggestion for today based on the above

Keep it under 200 words. I'm reading this while pouring coffee.
```

---

## Chapter 3: 25 Tested Business Prompts

These prompts are ready to use. Replace the [BRACKETS] with your info.

### Customer Service

**1. Respond to an angry customer**
```
A customer is upset because [ISSUE]. Write a response that:
- Acknowledges their frustration without being defensive
- Offers a specific solution (not "we'll look into it")
- Gives a timeline for resolution
- Ends with a way to follow up directly

Tone: Empathetic but professional. Not groveling.
Our policy: [YOUR REFUND/RESOLUTION POLICY]
```

**2. Handle a refund request**
```
Customer wants a refund for [PRODUCT/SERVICE] because [REASON].
Our refund policy: [POLICY — e.g., "30 days, no questions asked" or "case by case"]

Draft a response that:
- If eligible: Approve clearly, explain timeline, don't make them ask again
- If not eligible: Explain why respectfully, offer an alternative solution
- Either way: End on a positive note about their future business
```

**3. Follow up after a service call**
```
We just completed [SERVICE] for [CUSTOMER NAME] on [DATE].
Write a follow-up email that:
- Confirms the work is done
- Asks if everything meets their expectations
- Requests a review/testimonial (only if they seem happy)
- Mentions our referral program if we have one

Keep it short. 3-4 sentences max.
```

**4. Respond to a negative review**
```
Someone left this negative review: [PASTE REVIEW]
Write a public response that:
- Acknowledges the issue
- Shows we take it seriously
- Moves the conversation offline (phone/email)
- Doesn't get defensive or argue

Other customers will read this. Be the person they'd want to do business with.
```

**5. Onboard a new client**
```
We just signed [CLIENT NAME] for [SERVICE].
Send a welcome email that:
- Confirms what they're getting and when
- Introduces their main contact (me)
- Lists next steps with deadlines
- Includes a way to reach us with questions
- Sets expectations for communication frequency

Tone: Professional and warm. They just gave us money — make them feel good about it.
```

### Sales

**6. Cold outreach to a potential client**
```
Write a cold outreach email to [PROSPECT NAME] at [COMPANY].
I noticed [SPECIFIC THING ABOUT THEM — recent news, website issue, industry challenge].

We help [TARGET COMPANIES] with [YOUR SERVICE].
One recent result: [SPECIFIC OUTCOME — e.g., "Cut a client's scope creep losses by 25%"]

Rules:
- No buzzwords
- Under 100 words
- One clear ask (a 15-minute call, not "let's explore synergies")
- Sound like a human, not a template
```

**7. Follow up after a proposal**
```
I sent a proposal to [CLIENT NAME] for [SERVICE] on [DATE]. Haven't heard back.
Write a follow-up that:
- Doesn't assume they rejected it
- Offers to answer questions or adjust scope
- Gives an easy out ("If the timing isn't right, no worries")
- One sentence max about the value, not a re-pitch

Tone: Low pressure. I want to work with them, not chase them.
```

**8. Handle a price objection**
```
[CLIENT NAME] said our price of $[AMOUNT] for [SERVICE] is too high. Their budget is $[THEIR BUDGET].
Draft a response that:
- Acknowledges their budget constraint
- Explains what they're getting for the price (value, not features)
- Offers options: reduced scope, phased approach, or payment plan
- Doesn't immediately discount — that signals we were overcharging

Remember: If they can't afford us, that's OK. Don't devalue our work to win the deal.
```

**9. Upsell an existing client**
```
[CLIENT NAME] has been using our [CURRENT SERVICE] for [TIME PERIOD].
Based on their usage, they'd benefit from [ADDITIONAL SERVICE].
Write a brief message that:
- References a specific win or result they've had with us
- Suggests the add-on naturally (not a hard pitch)
- Makes it easy to say yes (trial period, add to existing invoice, etc.)

Don't be salesy. Be helpful.
```

**10. Win-back a former client**
```
[CLIENT NAME] stopped working with us [TIME AGO] for [REASON IF KNOWN].
Write a re-engagement message that:
- Doesn't guilt trip them
- Mentions something new or improved since they left
- Offers a low-commitment way to reconnect
- Is genuinely friendly, not passive-aggressive
```

### Operations

**11. Create a project brief**
```
Create a project brief for [PROJECT NAME]:
- Client: [NAME]
- Goal: [WHAT SUCCESS LOOKS LIKE]
- Scope: [WHAT'S INCLUDED]
- Timeline: [DEADLINE]
- Budget: $[AMOUNT]

Include:
1. Project overview (2-3 sentences)
2. Deliverables with dates
3. Out of scope (explicit — this prevents scope creep)
4. Key contacts and roles
5. Success criteria
6. Risks and mitigation
```

**12. Write a standard operating procedure**
```
Write an SOP for [PROCESS NAME] at [BUSINESS NAME].

Include:
1. Purpose (why this exists)
2. Who's responsible
3. Step-by-step instructions (numbered, specific)
4. Tools/templates needed
5. Common mistakes to avoid
6. How to handle exceptions
7. When to escalate

Write for someone who's never done this before. Assume nothing.
```

**13. Meeting agenda and notes template**
```
Create a meeting agenda for [MEETING TYPE — client check-in, team standup, project kickoff]:
- Duration: [X] minutes
- Attendees: [LIST]
- Frequency: [weekly/biweekly/monthly]

Include:
1. Quick wins/updates (5 min)
2. Main discussion items (with time allocated)
3. Decisions needed
4. Action items (owner + deadline)

End with: "If we can't cover everything, what's the one thing that MUST be decided today?"
```

**14. Weekly review for the business owner**
```
Help me do a weekly review.

This week's outcomes:
- Completed: [LIST]
- Didn't complete: [LIST]
- Surprises: [LIST]

Key metrics:
- Revenue: $[AMOUNT]
- Customers: [NUMBER]
- Key metric: [VALUE]

Answer these questions:
1. What produced the most results this week?
2. What took the most time without proportional results?
3. What should I stop doing?
4. What should I start doing?
5. What's the #1 priority for next week?

Be direct. If I'm wasting time on something, say so.
```

**15. Quarterly business review**
```
Generate a quarterly review for [BUSINESS NAME].

QUARTER HIGHLIGHTS:
- Revenue: $[AMOUNT] (vs. $[PREV] last quarter)
- New customers: [NUMBER]
- Lost customers: [NUMBER]
- Biggest win: [DESCRIBE]
- Biggest challenge: [DESCRIBE]

1. Score each area 1-10: Sales, Operations, Customer Satisfaction, Team, Finances
2. What worked? (keep doing)
3. What didn't? (stop or change)
4. Top 3 priorities for next quarter
5. One bold bet I should consider

Be honest. I'm paying you to tell me what I don't want to hear.
```

### Finance

**16. Cash flow forecast**
```
Based on:
- Monthly revenue: $[AMOUNT]
- Monthly expenses: $[AMOUNT]
- Outstanding invoices: $[AMOUNT]
- Upcoming big expenses: [LIST WITH DATES]

Generate a 90-day cash flow forecast:
1. Month 1, 2, 3: projected inflow, outflow, net
2. Flag any weeks where balance goes negative
3. Suggest 3 ways to improve cash flow this quarter
4. Identify the single biggest cash flow risk

Assume nothing improves on its own. What action should I take?
```

**17. Pricing analysis**
```
I charge $[CURRENT PRICE] for [SERVICE/PRODUCT].
My costs are approximately $[COST] per unit.
Competitors charge: [RANGE]

Analyze:
1. My current margin: [CALCULATE]
2. Am I underpriced or overpriced relative to value?
3. If I raised prices 10%, how many customers could I lose and still make more money?
4. If I lowered prices 10%, how many new customers do I need to break even?
5. Recommend: raise, hold, or lower — and why

Be specific with numbers. No "it depends" without a clear recommendation.
```

**18. Tax preparation checklist**
```
I'm a small business owner in [COUNTRY/STATE/PROVINCE].
My business structure: [SOLE PROP / LLC / CORP]
Fiscal year: [CALENDAR / CUSTOM]

Generate a tax prep checklist:
1. Documents I need to gather (with sources)
2. Deadlines I can't miss
3. Common deductions I might forget
4. Red flags that trigger audits
5. What to give my accountant vs. what I can handle myself

Note: This is a checklist, not tax advice. I'll verify with my CPA.
```

### HR & Team

**19. Job posting**
```
Write a job posting for [ROLE] at [BUSINESS NAME].
We're a [INDUSTRY] company with [NUMBER] employees in [LOCATION/REMOTE].

Requirements: [LIST 3-5 MUST-HAVES]
Nice to have: [LIST 2-3 PREFERENCES]
Salary range: [RANGE] (or "competitive")
Benefits: [LIST]

Rules:
- No corporate jargon ("rockstar," "ninja," "fast-paced environment")
- Be honest about the work (not everyone should apply)
- Explain why someone would want this job specifically
- Include what the first 30 days look like
```

**20. Performance review framework**
```
Create a performance review for [EMPLOYEE ROLE] at [BUSINESS NAME].

Categories to evaluate:
- Quality of work
- Reliability and timeliness
- Communication
- Problem-solving
- Teamwork
- Growth potential

For each:
1. Rating: Exceeds / Meets / Needs Improvement
2. One specific example to discuss (placeholder)
3. One development goal for next quarter

End with: "What support do you need from me to do your best work?"
```

**21. Difficult conversation script**
```
I need to have a difficult conversation with [EMPLOYEE/CLIENT] about [ISSUE — e.g., missed deadlines, performance, boundary setting].

Write me:
1. Opening line (direct but not harsh)
2. The key points to make (3 max)
3. How to invite their perspective
4. How to land on a clear next step
5. What NOT to say (common mistakes)

Keep it practical. I'm not looking for HR language — I'm looking for human language.
```

### Strategy

**22. Competitive analysis**
```
My business: [BUSINESS NAME], a [INDUSTRY] company.
My competitors: [COMPETITOR 1], [COMPETITOR 2], [COMPETITOR 3]

For each competitor:
1. What they do better than us
2. What we do better than them
3. Their likely next move
4. One thing we should copy (ethically)
5. One thing they're vulnerable on

Then: What's our sustainable competitive advantage? (Not "we care more" — something defensible.)
```

**23. Business model stress test**
```
Stress test my business model:

Revenue sources: [LIST WITH % OF TOTAL]
Customer acquisition: [HOW YOU GET CUSTOMERS]
Key dependencies: [LIST — e.g., "One client = 40% of revenue", "Platform dependent on [X]"]

What happens if:
1. My biggest customer leaves?
2. My main acquisition channel stops working?
3. A new competitor enters at half my price?
4. My key employee quits?
5. A recession hits and budgets shrink 30%?

For each: Impact level (Low/Med/High) + mitigation action

End with: What's my biggest unaddressed risk?
```

**24. Decision framework**
```
I'm deciding whether to [DECISION — e.g., "hire a second employee," "expand to a new market," "launch a new product"].

Help me think through this:
1. What's the upside if it works?
2. What's the downside if it fails?
3. What does it cost to try? (money + time + opportunity cost)
4. What information would make this decision easier?
5. Can I test this small before going all in?
6. What's my gut saying? (Sometimes you already know.)

Don't make the decision for me. Help me see what I'm missing.
```

**25. Annual planning template**
```
It's [MONTH] [YEAR]. Help me plan the next 12 months for [BUSINESS NAME].

Last year:
- Revenue: $[AMOUNT]
- Customers: [NUMBER]
- Biggest win: [DESCRIBE]
- Biggest regret: [DESCRIBE]

Next year goals:
- Revenue target: $[AMOUNT]
- Key initiative: [THE BIG THING]
- Team growth: [PLANS]

Generate:
1. 4 quarterly milestones (specific, measurable)
2. 12 monthly themes (one focus per month)
3. The 3 things most likely to derail this plan
4. What I should start doing Jan 1 to make this real
5. How I'll know by March if this plan is working

No generic advice. Challenge my assumptions.
```

---

## Chapter 4: The 5-Day Sprint — Zero to Deployed Agent

### Day 1 (Monday): Pick Your First Agent

**Goal:** Choose which workflow to deploy first

Don't overthink this. Pick the task that:
- Takes the most of your time weekly
- Is repeatable (same type of work, different inputs)
- Has clear inputs and outputs
- A mistake is recoverable (not surgery)

**Best first agents for small businesses:**
1. Customer support auto-responder (most businesses)
2. Invoice follow-up (if you have unpaid invoices)
3. Lead qualification (if you get regular inbound leads)
4. Weekly reporting (if you spend hours on reports)

**Today's deliverable:** One agent selected, one workflow from Chapter 2 chosen.

---

### Day 2 (Tuesday): Set Up Your Platform

**Goal:** Get your automation platform working

**For non-technical users:**
1. Sign up for Make.com (free tier: 1,000 operations/month)
2. Connect your email account
3. Connect OpenAI (create API key at platform.openai.com, add $10 credit)
4. Test a simple flow: "When I receive an email → send me a notification"

**For slightly technical users:**
1. Try N8N (self-hosted, free, more powerful)
2. Or use OpenClaw for agent-first approach

**Today's deliverable:** Platform connected, test flow working.

---

### Day 3 (Wednesday): Build Your Agent

**Goal:** Implement the workflow you chose

1. Copy the prompt from Chapter 2
2. Replace [BRACKETS] with your actual business info
3. Build the automation in your platform:
   - Trigger: "When [EVENT happens]"
   - Action: "Send to OpenAI with [YOUR PROMPT]"
   - Output: "Send response to [DESTINATION]"
4. Test with 5 real examples from your business
5. Adjust the prompt based on results

**Today's deliverable:** Agent handles 5 test cases with acceptable results.

---

### Day 4 (Thursday): Add Human-in-the-Loop

**Goal:** Set up the safety net

1. Add a rule: "If confidence is low → route to human"
2. For email agents: BCC yourself on all automated responses for the first week
3. For support agents: Require human approval for anything involving refunds, complaints, or account changes
4. Set up a daily review: "Show me everything the agent did today" (5 minutes)

**Today's deliverable:** Agent runs with human review safety net.

---

### Day 5 (Friday): Go Live and Measure

**Goal:** Your agent is working for you

1. Turn it on for real inputs
2. Set up your ROI tracker (see Chapter 7)
3. Plan your first week review (Day 12): "What did the agent handle? What did it miss? What should I tweak?"
4. Start thinking about Agent #2 (from Chapter 8: Scaling Playbook)

**Today's deliverable:** Agent is live and saving you time.

---

## Chapter 5: AI Cost Calculator

### How Much Will Your Agent Actually Cost?

**OpenAI API Pricing (GPT-4o-mini — best for most business agents):**
- Input: $0.15 per 1M tokens (~750,000 words)
- Output: $0.60 per 1M tokens (~750,000 words)

**Typical monthly costs by agent type:**

| Agent Type | Messages/Month | Est. Monthly Cost |
|------------|----------------|-------------------|
| Customer support auto-responder | 200-500 emails | $3-8 |
| Lead qualification | 50-100 leads | $2-5 |
| Invoice follow-up | 20-50 invoices | $1-3 |
| Social media content | 20-30 posts | $2-4 |
| Weekly reporting | 4 reports | $1-2 |
| Daily briefing | 22 days | $2-4 |
| Competitor monitoring | 4 reports | $1-3 |

**Total for 3 agents: $5-20/month**
**Total for 5 agents: $10-40/month**

**Platform costs:**
- Make.com: Free tier (1,000 ops) or $9/mo
- Zapier: Free tier (100 tasks) or $20/mo
- N8N: Free (self-hosted) or $20/mo (cloud)

**All-in monthly cost for a typical small business running 3 agents: $15-40/month**

That's less than one hour of employee time. If your agents save you 2+ hours per week (and they should), the ROI is 10-20x.

---

## Chapter 6: 25-Point Security Checklist

Before deploying any AI agent, verify these:

### Data Protection
- [ ] **1.** No customer PII (names, emails, phone numbers, SSNs) is sent to AI without encryption
- [ ] **2.** API keys are stored in environment variables, never in code or prompts
- [ ] **3.** Agent cannot access data outside its intended scope
- [ ] **4.** Customer data sent to AI is not used for training (check your AI provider's data policy)
- [ ] **5.** Sensitive documents (contracts, financials) require human approval before AI processing

### Access Control
- [ ] **6.** Each agent has its own API key (not shared with humans)
- [ ] **7.** Agent permissions follow least-privilege (can only do what it needs)
- [ ] **8.** Human review is required for actions exceeding $[YOUR THRESHOLD]
- [ ] **9.** Agent cannot delete data, only flag for human deletion
- [ ] **10.** All agent actions are logged with timestamp and details

### Financial Safeguards
- [ ] **11.** Agent cannot authorize payments above $[YOUR LIMIT] without human approval
- [ ] **12.** Monthly spend caps on AI API usage are set
- [ ] **13.** Agent cannot modify pricing, discounts, or contract terms
- [ ] **14.** Refunds and credits above $[AMOUNT] require human sign-off
- [ ] **15.** Billing alerts are set up if API costs exceed 2x normal

### Communication Safety
- [ ] **16.** Agent identifies itself as AI in customer-facing communications
- [ ] **17.** Automated emails include a way to reach a human
- [ ] **18.** Agent cannot send communications to your full customer list without approval
- [ ] **19.** Social media posts require human review before publishing
- [ ] **20.** Agent cannot make legal claims or guarantees

### Operational Resilience
- [ ] **21.** If the AI API goes down, your business doesn't stop (fallback process documented)
- [ ] **22.** Agent errors trigger alerts, not silence
- [ ] **23.** You review agent performance weekly for the first month
- [ ] **24.** You can disable any agent in under 5 minutes
- [ ] **25.** You have a written policy for what the agent does and doesn't do (share with your team)

---

## Chapter 7: ROI Tracker Template

### Weekly Agent Performance Log

**Agent name:** [NAME]
**Week of:** [DATE]

| Metric | Target | Actual | Notes |
|--------|--------|--------|-------|
| Tasks handled | [#] | [#] | |
| Tasks escalated to human | [#] | [#] | |
| Avg response time | [TIME] | [TIME] | |
| Customer satisfaction (if measurable) | [%] | [%] | |
| Errors requiring correction | 0 | [#] | |
| Time saved (your estimate) | [# hours] | [# hours] | |
| AI API cost | $[X] | $[X] | |

**Weekly savings calculation:**
- Hours saved × Your hourly rate ($[X]) = $[SAVINGS]
- Minus AI cost ($[X])
- **Net weekly savings: $[X]**

**Monthly projection: Net weekly savings × 4.3 = $[MONTHLY]**
**Annual projection: Monthly × 12 = $[ANNUAL]**

---

### Monthly Business Impact Summary

**Month:** [MONTH YEAR]

| Agent | Time Saved | Cost | Net Savings | Satisfaction |
|-------|-----------|------|-------------|-------------|
| [Agent 1] | [# hrs] | $[#] | $[#] | [Rating] |
| [Agent 2] | [# hrs] | $[#] | $[#] | [Rating] |
| [Agent 3] | [# hrs] | $[#] | $[#] | [Rating] |
| **Total** | **[# hrs]** | **$[#]** | **$[#]** | |

**Hours reinvested into:** [What did you do with the time you got back?]

---

## Chapter 8: Scaling Playbook — From 1 Agent to 5

### The Right Order to Add Agents

**Agent 1 (Week 1-2):** Customer support or lead handling
→ Why: Biggest time drain, easiest to measure ROI, most forgiving of mistakes

**Agent 2 (Week 3-4):** Invoice follow-up or scheduling
→ Why: Second biggest time drain, builds confidence in the system

**Agent 3 (Month 2):** Reporting or content
→ Why: Nice-to-have that saves hours but isn't urgent

**Agent 4 (Month 2-3):** Competitor monitoring or feedback analysis
→ Why: Strategic, not operational — add when basics are running smoothly

**Agent 5 (Month 3-4):** Daily briefing or expense categorization
→ Why: Optimization layer — you're now running a multi-agent system

### Warning Signs You're Scaling Too Fast

- You can't explain what each agent does in one sentence
- You're spending more time fixing agents than the agents save
- Errors are cascading (Agent 1's output feeds Agent 2, and mistakes compound)
- You haven't reviewed agent performance in 2+ weeks
- Your AI costs doubled without clear additional value

### The Scaling Rule: One Agent Per Critical Process

Don't build 3 customer support agents. Build 1 support agent, 1 billing agent, 1 reporting agent. Each agent owns one process end-to-end.

---

## Chapter 9: Platform Comparison Guide

### Make.com vs Zapier vs N8N vs OpenClaw

| Feature | Make.com | Zapier | N8N | OpenClaw |
|---------|-----------|--------|-----|----------|
| **Free tier** | 1,000 ops/mo | 100 tasks/mo | Self-hosted: unlimited | Limited trial |
| **Entry price** | $9/mo | $20/mo | Free (self-hosted) or $20/mo | Custom |
| **AI integration** | HTTP module + OpenAI | OpenAI app built-in | OpenAI node built-in | Native AI agents |
| **Ease of setup** | Medium | Easy | Medium-Hard | Medium |
| **Best for** | Visual thinkers | Non-technical users | Technical/tinkerers | Agent-first workflows |
| **Scaling** | $16-$29/mo for 10K ops | $20-$73/mo | Free if self-hosted | Usage-based |
| **Canadian?** | Yes (founded in Prague, EU office) | No (US) | No (Germany) | No (US) |
| **Data residency** | EU available | US only | Self-hosted = your choice | US |

**Recommendation for most small businesses:**
- **Just getting started:** Make.com free tier. It's enough for 2-3 agents.
- **Want it dead simple:** Zapier. Pay more, but setup is faster.
- **Technical and want control:** N8N self-hosted. Free, powerful, you own the data.
- **Agent-first mindset:** OpenClaw. Built for multi-agent orchestration.

---

## Chapter 10: Vendor Evaluation Scorecard

When an AI vendor pitches you, score them:

| Criteria | Weight | Vendor 1 | Vendor 2 | Vendor 3 |
|----------|--------|----------|----------|----------|
| **Data privacy** | 25% | /5 | /5 | /5 |
| **Real cost (not intro price)** | 20% | /5 | /5 | /5 |
| **Ease of setup (< 1 day?)** | 15% | /5 | /5 | /5 |
| **Exit strategy (can I leave?)** | 15% | /5 | /5 | /5 |
| **References from my industry** | 10% | /5 | /5 | /5 |
| **Support quality** | 10% | /5 | /5 | /5 |
| **Canadian compliance** | 5% | /5 | /5 | /5 |
| **TOTAL** | 100% | **/5** | **/5** | **/5** |

**Red flags:**
- Won't tell you the real price after intro period ends
- No data export or migration tool
- "You don't need to understand how it works"
- No references in your industry
- Long-term contract required

---

## Chapter 11: Team Adoption Guide

### Getting Your Employees to Actually Use AI

**The #1 mistake:** Deploying AI and saying "use this." They won't.

**What works:**

1. **Show, don't tell.** Run the agent yourself for 2 weeks. Show them the results. "I used to spend 3 hours on this. The agent does it in 5 minutes. I just review the output."

2. **Start with their biggest pain.** Don't automate the thing they like doing. Automate the thing they hate. (Usually: data entry, repetitive emails, report formatting.)

3. **Give them veto power.** "The agent will draft responses. You decide if they go out. Nothing sends without your approval for the first month."

4. **Measure their time savings.** "This saved you 4 hours this week. What did you do with that time?" Make it visible.

5. **Address the fear directly.** "This isn't replacing you. It's handling the work you don't have time for, so you can focus on the work that actually needs you."

6. **Train on the review process.** The hardest skill isn't using AI — it's knowing when the AI is wrong. Teach: "Read the output. If it sounds off, it probably is. Send it to me and we'll fix the prompt."

7. **Celebrate the wins.** "Agent handled 47 support tickets this week with a 95% approval rate." Share these numbers.

---

## Chapter 12: Quick-Start Cheat Sheet

*Print this. Put it on your wall.*

```
═══════════════════════════════════════════════════
     YOUR AI AGENT — QUICK REFERENCE
═══════════════════════════════════════════════════

AGENT NAME: ___________________
DEPLOYED: ___/___/______
PLATFORM: ___________________

WHAT IT DOES:
_____________________________________________

WHAT IT DOESN'T DO:
_____________________________________________

HUMAN REVIEW TRIGGER:
□ Refunds over $____
□ Complaints
□ New client types
□ Anything flagged "low confidence"

DAILY CHECK (2 min):
□ Check agent log for errors
□ Review any escalated items

WEEKLY REVIEW (15 min):
□ How many tasks handled?
□ How many escalated?
□ Any patterns in errors?
□ Adjust prompt if needed

EMERGENCY SHUTOFF:
□ [HOW TO DISABLE IN UNDER 5 MIN]

COST: $___/month
TIME SAVED: ___hrs/week
ROI: ____x

═══════════════════════════════════════════════════
```

---

## Chapter 13: Troubleshooting Playbook

### When Your Agent Goes Wrong

**Problem: Agent gives generic, unhelpful responses**
→ Fix: Add more specific context to your prompt. Include examples of good responses. Tell it what NOT to say.
→ Example: Instead of "handle support emails," say "handle billing questions by checking their invoice number and confirming the amount. If the amount doesn't match our records, escalate."

**Problem: Agent is too cautious, escalates everything**
→ Fix: Lower the escalation threshold. Give it explicit permission to handle common cases.
→ Example: "You may approve refunds under $50 without escalation. You may answer these FAQ topics without checking: [LIST]."

**Problem: Agent makes things up (hallucination)**
→ Fix: Add "Only use information provided. If you don't know, say 'Let me get a human to help with this.'" Never let it improvise facts.

**Problem: Costs are higher than expected**
→ Fix: Check your token usage. Shorter prompts + shorter expected responses = lower cost. Switch from GPT-4 to GPT-4o-mini for most tasks. Set monthly spend limits in your OpenAI dashboard.

**Problem: Agent works in testing but fails in production**
→ Fix: Your test cases were too clean. Real inputs are messier. Test with the worst, most confusing customer messages you can find. Add handling for: typos, angry tone, multiple questions in one message, incomplete information.

**Problem: Agent works great but customers hate it**
→ Fix: Two things to check. (1) Does the agent identify itself as AI? People are more forgiving when they know. (2) Is there always an option to reach a human? If not, add one immediately.

**Problem: You're spending more time fixing the agent than it saves**
→ Fix: You're over-engineering. Simplify the prompt. Reduce the scope. A working agent that does 3 things reliably beats a broken agent that tries to do 10.

---

## Appendix: Getting Started Checklist

- [ ] Choose your first agent (Chapter 2)
- [ ] Sign up for automation platform (Chapter 9)
- [ ] Create OpenAI API key + add $10 credit
- [ ] Copy and customize your prompt (replace [BRACKETS])
- [ ] Build the workflow in your platform
- [ ] Test with 5 real examples
- [ ] Add human-in-the-loop safety net (Chapter 6)
- [ ] Run the security checklist (Chapter 6)
- [ ] Set up ROI tracker (Chapter 7)
- [ ] Go live
- [ ] Review daily for week 1
- [ ] Review weekly after that
- [ ] Plan Agent #2 (Chapter 8)

---

*This kit was built by SMB Scale Up — practical tools from people who actually run small businesses. Free lifetime updates included. Questions? support@smbscaleup.com*