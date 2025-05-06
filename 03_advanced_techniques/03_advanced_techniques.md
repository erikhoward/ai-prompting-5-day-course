# Day 3: Advanced Prompting Techniques

## Objective

Learn how to create more powerful prompts to improve the quality of your outputs and your efficiency as a Product Manager.

## Building on Previous Days

Over the past two days, we've covered the foundations of LLMs and core prompting techniques. Today, we'll level up with advanced methods that will help you tackle more complex PM challenges.

## Meta-Prompting

### What It Is

Meta-prompting is like giving the LLM instructions about how to approach your request before making the actual request. It's creating a "prompt about how to handle your prompt."

### Why It Works

This technique helps the LLM understand your expectations about:

- How thoroughly to analyze information
- What perspective to take
- What thinking process to follow
- What to prioritize or ignore

### Examples for Product Managers

**Basic Prompt**:

```
Help me create a roadmap for our fintech app.
```

**Meta-Prompt**:

```
I'm going to ask you to help create a product roadmap, but before you generate any content:
1. Ask me clarifying questions about timeframe, key business objectives, and resource constraints
2. Suggest a structure for the roadmap that balances strategic initiatives with tactical improvements
3. Help me think through dependencies between potential features
4. Challenge any assumptions you notice in my thinking

Once we've worked through those steps, then help me create the actual roadmap.

My initial request: I need a 6-month roadmap for our personal finance app that focuses on increasing user retention while we prepare for a Series B funding round.
```

**Another Example**:

```
When analyzing the competitive landscape I'm about to share:
1. Focus on identifying underserved user needs rather than just feature comparisons
2. Consider business model innovations, not just product features
3. Look for evidence of where competitors might be heading next, not just where they are now
4. Highlight potential white space opportunities

Here's data on our top 5 competitors in the healthcare scheduling market:
[Competitive data]
```

### When to Use It

- For complex, multi-stage discussions
- When you need a thinking partner, not just a response
- For strategic work where the approach matters as much as the output
- When you want the LLM to probe assumptions

## Summarization Power-Up

### What It Is

This technique involves crafting specialized prompts to extract the most relevant information from lengthy content like user research, meeting transcripts, or market reports.

### Why It Works

By giving specific instructions about what to focus on and how to organize the summary, you get more actionable insights rather than generic summaries.

### Examples for Product Managers

**Basic Prompt**:

```
Summarize this user research report.
```

**Powered-Up Summarization**:

```
I have a 15-page user research report on how enterprise customers use our analytics dashboard. As a product manager, I need to extract actionable insights that can inform our next quarter's roadmap.

Please summarize the report with this structure:
1. Top 3 user pain points, with severity and frequency noted
2. Capability gaps compared to user expectations
3. Unexpected user behaviors or workarounds discovered
4. Direct user quotes that effectively illustrate key points (maximum 5)
5. Specific feature requests or enhancement suggestions
6. Quick wins that could be implemented in 2-4 weeks

For each section, connect insights to potential business impact when possible (e.g., user acquisition, retention, revenue).

Here's the report:
[User research content]
```

**Another Example**:

```
Summarize this 90-minute product strategy meeting transcript, focusing on:
1. Decisions made (with clear owner and deadline if specified)
2. Open questions that need research
3. Action items by department (Product, Engineering, Design, Marketing)
4. Topics that caused significant debate
5. Ideas that received enthusiastic support

Format as bullet points grouped by category, ordered by apparent priority.

[Meeting transcript]
```

### When to Use It

- For processing lengthy research or meeting content
- When preparing executive briefings from detailed materials
- For quickly extracting action items from discussions
- When turning qualitative data into structured insights

## Extracting & Categorizing Information

### What It Is

This technique helps you pull specific types of information from unstructured text and organize it into useful categories, taxonomies, or frameworks.

### Why It Works

By specifying exactly what types of information you're looking for and how it should be organized, you can transform messy data into structured insights.

### Examples for Product Managers

**Basic Prompt**:

```
What can we learn from this customer feedback?
```

**Extraction & Categorization Prompt**:

```
Extract and categorize information from these 50 customer support tickets about our SaaS accounting platform. 

First, identify each unique issue mentioned.

Then categorize each issue as:
- Bug (something not working as designed)
- UX Friction (working but confusing or inefficient)
- Feature Request (request for new capability)
- Education Gap (user doesn't know how to use existing feature)
- Data Issue (problems with user's data, not the product)

For each issue identified:
1. Assign a category from above
2. Note frequency (how many tickets mention it)
3. Assess impact level (Low/Medium/High) based on user language and business impact
4. Tag with the relevant product area (Invoicing, Reporting, Tax Calculation, User Management, etc.)
5. Include a representative user quote if available

Present results as a markdown table sorted by frequency, then impact level.

[Customer support tickets]
```

**Another Example**:

```
From this collection of analyst reports on the fintech lending market, extract:

1. Market size estimates (current and projected)
2. Growth rates by segment (consumer, small business, mortgage)
3. Emerging technologies mentioned as disruptive
4. Regulatory concerns or changes
5. Competitive moves by major players
6. Customer behavior trends

Organize findings by level of consensus across reports (High, Medium, Low consensus) and note any significant disagreements between analysts.

[Analyst reports]
```

### When to Use It

- For processing customer feedback or support tickets
- When analyzing competitive intelligence
- For extracting insights from industry reports
- When identifying patterns in user behavior data

## Interactive and Iterative Prompting

### What It Is

This technique involves designing prompts that create a collaborative back-and-forth between you and the LLM, refining outputs over multiple steps rather than trying to get perfect results in one go.

### Why It Works

Complex work benefits from iteration and feedback cycles. By breaking the task into steps with feedback between each, you get better results than trying to solve everything at once.

### Examples for Product Managers

**Initial Prompt**:

```
I'm creating a positioning statement for our new healthcare scheduling platform. Let's work on this together over several steps:

1. First, ask me 3-5 targeted questions about our target customers, key differentiators, and competitor positioning
2. Based on my answers, propose 2-3 different positioning angles we could take
3. After I choose a direction, create a draft positioning statement
4. Then help me refine it by suggesting variations and improvements
5. Finally, help me test the statement against objections or misunderstandings stakeholders might have

Let's start with your questions for me.
```

**Example of the Conversation Flow**:

LLM: *Asks clarifying questions about target customers, etc.*

You: *Provide answers*

LLM: *Suggests positioning angles*

You: "I like the second approach focusing on reducing no-shows. Let's develop that further."

LLM: *Creates draft positioning statement*

You: "This is good but feels too technical. Can we make it more emotionally resonant for practice managers?"

LLM: *Refines the statement with variations*

You: "I like variation B. Now let's test it against some objections..."

### When to Use It

- For crafting important messaging or positioning
- When developing strategic frameworks that need refinement
- For complex decision-making processes
- When you want to explore multiple approaches before finalizing

## Structured Multi-Perspective Analysis

### What It Is

This technique involves deliberately analyzing a product decision or problem from multiple distinct perspectives to reveal insights that might be missed from a single viewpoint.

### Why It Works

Product decisions have implications across business objectives, technical constraints, user experience, and market positioning. By systematically examining each perspective, you catch potential issues early and develop more robust solutions.

### Examples for Product Managers

**Basic Prompt**:

```
Should we implement a freemium model for our B2B analytics product?
```

**Multi-Perspective Analysis Prompt**:

```
I'm considering implementing a freemium model for our B2B analytics SaaS product. Currently, we only offer paid plans starting at $299/month. Please analyze this potential change from these five perspectives:

1. User Acquisition: How might this affect our top-of-funnel metrics and user acquisition costs?

2. Revenue Impact: What are the potential positive and negative effects on our revenue model, including cannibalization risks?

3. Product Experience: What feature limitations make sense for the free tier without creating a poor experience?

4. Engineering & Support Costs: What technical and support implications should we consider?

5. Competitive Positioning: How would this change our position relative to key competitors?

For each perspective, provide:
- 2-3 key considerations
- Potential risks
- Potential opportunities
- 1 question we should answer before proceeding

After analyzing all perspectives, suggest what additional data we should gather before making this decision.
```

**Another Example**:

```
Analyze our plan to integrate an AI-powered recommendation system in our health app from these perspectives:

1. User Privacy & Ethics: What are the privacy implications and ethical considerations?

2. Technical Feasibility: Given our current stack (React Native, Node.js backend), what implementation challenges exist?

3. Business Impact: How might this affect key metrics like retention and premium conversions?

4. Regulatory Compliance: What HIPAA and other healthcare regulations must we consider?

5. User Trust: How might users perceive AI-driven recommendations for health decisions?

For each perspective, highlight the most critical consideration we might overlook.
```

### When to Use It

- For major strategic decisions
- When evaluating significant feature additions
- For changes to your business model
- When entering new markets or user segments

## Practice: Advanced Prompting for User Feedback Analysis

Let's combine several of these advanced techniques in a practical exercise relevant to product managers.

### The Scenario

Your team has conducted user interviews with 10 customers of your SaaS advertising platform. You have pages of notes that need to be synthesized into actionable insights to guide your next quarter's roadmap.

### Exercise: Create a Powerful Prompt for User Feedback Analysis

```
I need to analyze user feedback from 10 customer interviews about our advertising analytics platform. I'll use a meta-prompt approach combined with structured extraction and multi-perspective analysis.

## Your Approach
When analyzing this user feedback:
1. First, extract key patterns without rushing to conclusions
2. Look for underlying needs beyond explicit feature requests
3. Consider both functional and emotional aspects of user feedback
4. Connect feedback to our business metrics and KPIs
5. Identify both quick wins and strategic opportunities

## Extraction Task
From the interview notes below, please:
1. Identify and categorize all pain points mentioned
2. Extract specific feature requests or enhancement ideas
3. Capture positive feedback and what users value most
4. Note any competitive mentions or comparisons
5. Highlight usability issues or friction points

## Multi-Perspective Analysis
Then, analyze the findings from these perspectives:
1. User Retention: What issues might cause customers to churn?
2. Revenue Expansion: What opportunities exist for upselling?
3. Competitive Advantage: What would meaningfully differentiate us?
4. Technical Feasibility: What seems feasible for our next quarterly release?
5. UX Improvements: What patterns suggest needed usability enhancements?

## Output Format
Present your analysis as:
1. An executive summary (3-5 bullet points of highest-priority insights)
2. A categorized table of findings with frequency counts
3. Recommended priority order for addressing issues
4. 3-5 specific, actionable next steps for the product team

Here are the interview notes:
[Interview notes would go here]
```

### Sample Results

When you run a prompt like this with real user feedback, you get:

1. Structured insights rather than generic summaries
2. Multiple perspectives on the same data
3. Clear prioritization to guide decision-making
4. Specific next steps rather than just analysis

## Additional Practice Activities

### Practice Activity 1: Meta-Prompt for Competitive Analysis

Create a meta-prompt to help you analyze 5 competitors in the health tech space, focusing on how they approach user onboarding, engagement features, and monetization strategies.

### Practice Activity 2: Summarization Power-Up for Industry Reports

Take a lengthy industry report about fintech trends and create a summarization prompt that extracts only the information relevant to your specific product niche, organizing it into implications for your roadmap.

### Practice Activity 3: Interactive Prompting for Messaging Development

Design an interactive prompt sequence to develop positioning and messaging for a new feature launch, including how to test message variations with different user personas.

## Tips

- **Combine techniques**: The most powerful prompts often use multiple techniques together
- **Build a personal library**: Save your most effective prompts as templates for future use
- **Iterate on your approaches**: Advanced prompting is a skill that improves with practice
- **Share with your team**: Consider creating a team repository of effective prompting strategies

## Homework

1. Choose one complex PM deliverable you need to create (competitive analysis, feature prioritization, user research synthesis, etc.)
2. Design an advanced prompt combining at least two techniques from today
3. Test it with an LLM and iterate on the prompt at least once
4. Document what worked well and what you would change next time

Tomorrow, we'll learn how to critically evaluate LLM outputs and refine our prompts for even better results!

## 🎉Congratulations!

**You've completed Day 3 of the course!**

Considering sharing what you like or don't like about the course with me. It helps me improve it for future participants. Also, consider subscribing to my newsletter, [LLM Wire](https://substack.com/@llmwire), for updates on prompt engineering and related topics.

---
Up Next: [Day 4: Evaluating and Iterating on LLM Output](../04_evaluation/04_evaluation.md)
