# Day 5: Real-Life Use Cases and Prompt Strategy

## Objective

Start integrating LLMs into your regular workflows with clear strategies that deliver measurable value to your product management practice.

## Building on Previous Days

We've covered the fundamentals of LLMs, basic and advanced prompting techniques, and methods for evaluating and improving outputs. Today, we'll focus on practical applications and developing a sustainable strategy for incorporating AI into your PM toolkit.

## Prompting for Decision Support

Product management often involves making complex decisions with incomplete information. LLMs can help structure your thinking and explore options.

### Example: Feature Prioritization Support

**Prompt**:

```
I need help prioritizing these 7 potential features for our healthcare scheduling platform. I'll evaluate them using the RICE framework (Reach, Impact, Confidence, Effort), but I'd like your assistance in thinking through each component.

For each feature, help me think through:
1. Reach: What user segments would be affected and how many users that represents
2. Impact: How significantly this might improve core metrics (acquisition, retention, revenue)
3. Confidence: What evidence or assumptions we're working with
4. Effort: What technical and cross-functional components would be involved

Then suggest a structured approach to scoring each dimension on a 1-10 scale.

Features:
1. Multi-provider scheduling view for clinic admins
2. Patient self-service rescheduling with cancellation fee enforcement
3. Insurance eligibility verification during booking
4. Integration with popular EMR systems
5. Telehealth appointment prep workflow
6. Clinic-branded reminder templates
7. Wait list notifications for cancelled appointments
```

### Example: Pros/Cons Analysis

**Prompt**:

```
I'm deciding between two approaches for our mobile app authentication system:

Option A: Email-based magic links
Option B: Phone number + SMS verification

Help me analyze these options across multiple dimensions:
1. Security considerations
2. User experience and friction
3. Technical implementation complexity
4. Edge cases and potential points of failure
5. Scalability across markets (including international)
6. Cost implications

For each dimension, please:
- List key pros and cons for both options
- Identify any assumptions we should validate
- Suggest potential mitigations for the major cons

After the analysis, recommend which factors should be weighted most heavily in our decision given that our primary user base is healthcare professionals who value security but are often time-constrained.
```

### When to Use Decision Support Prompts

- Feature prioritization discussions
- Technical approach decisions
- Tradeoff analysis
- Risk assessment
- Go-to-market strategy planning

## Prompting for Stakeholder Communications

Crafting clear, persuasive communications is a core PM skill. LLMs can help you tailor your message for different audiences and purposes.

### Example: Technical to Executive Translation

**Prompt**:

```
I need to translate this technical explanation of our new machine learning feature into executive-friendly language for our quarterly business review.

The target audience includes our CEO (former sales leader), CFO, and CRO, who need to understand the business value without the technical details.

Please rewrite this explanation to:
1. Focus on business outcomes and customer value
2. Use max 1-2 sentences of simplified technical explanation
3. Include 2-3 compelling metrics or proof points
4. Address potential revenue and competitive advantage implications
5. Keep it under 3 paragraphs total

Technical explanation:
[Insert technical explanation]
```

### Example: Tailoring Communications for Different Teams

**Prompt**:

```
I need to announce our Q3 roadmap focus areas to different internal teams. Please help me adapt the core message for each audience, maintaining consistency while emphasizing what matters most to each group.

Core message:
"In Q3, we're focusing on three key areas: (1) Improving dashboard performance speed by refactoring our data processing pipeline, (2) Adding customizable alert thresholds for key metrics, and (3) Building our Salesforce integration to enable customer success teams to access product usage data."

Please create tailored 1-paragraph announcements for:

1. Engineering team: Emphasize technical challenges, learning opportunities, and implementation approach.

2. Sales team: Focus on competitive advantages, customer pain points addressed, and talking points for prospects.

3. Customer Success team: Highlight how these changes will help them better serve customers, any transition plans, and timeline.

4. Executive team: Stress business impact, strategic alignment, and expected outcomes tied to company goals.
```

### When to Use Communication Prompts

- Preparing for executive presentations
- Cross-functional project updates
- External customer communications
- Product launch announcements
- Complex feature explanations

## Using AI for Backlog Grooming or Sprint Planning

LLMs can help you organize, refine, and prioritize your backlog more effectively.

### Example: User Story Refinement

**Prompt**:

```
I need help refining these rough user stories for our next sprint planning session.

For each story, please:
1. Rewrite it in the standard format: "As a [user type], I want [action] so that [benefit]"
2. Add 3-5 acceptance criteria that would make the scope clear to developers
3. Identify any ambiguities or missing details that should be clarified
4. Suggest potential edge cases we should consider
5. Note any dependencies on other stories or systems

Rough stories:
1. Users should be able to export their analytics data
2. Dashboard needs to load faster
3. Add the ability to create saved views of common reports
4. Make it possible to share reports with external users
5. Fix the bug with date filtering on the performance tab
```

### Example: Epic Breakdown

**Prompt**:

```
I have a large epic that needs to be broken down into manageable user stories for our team. The epic is:

"Enable financial advisors to create personalized investment plans for clients based on risk profiles, financial goals, and market conditions."

Please help me:
1. Identify the key user journeys within this epic
2. Break those journeys into 8-12 distinct user stories following the standard format
3. For each story, suggest a rough story point estimate (using Fibonacci: 1, 2, 3, 5, 8, 13)
4. Group the stories into logical phases or MVPs
5. Highlight which stories might be good candidates for further breakdown
6. Identify potential technical spikes or research stories needed

Additional context:
- Our sprint capacity is typically 30-35 points
- The team has 3 full-stack developers and 1 dedicated QA
- We have existing APIs for customer data and market information
```

### When to Use Backlog Management Prompts

- Sprint planning preparation
- Breaking down complex epics
- Refining vague requirements
- Creating consistent acceptance criteria
- Identifying dependencies and risks

## Measuring ROI: Time Saved vs. Quality Tradeoffs

To sustainably integrate LLMs into your workflow, you need to understand where they provide the most value and where human expertise remains essential.

### Time-Value Matrix for PM Tasks

| Task Type | Time Savings | Quality Impact | Best Approach |
|-----------|--------------|---------------|---------------|
| First drafts & ideation | High | Neutral/Positive | AI-first with human refinement |
| Routine communications | High | Neutral | AI templates with customization |
| Data analysis & synthesis | Medium | Depends on prompt | Human question formulation, AI processing |
| Creative problem-solving | Low | Mixed | Human-led with AI as thought partner |
| Strategic decisions | Low | Risk of oversimplification | Human decision with AI for structured analysis |

### Example: ROI Tracking Prompt

**Prompt**:

```
I want to track the ROI of using LLMs for various PM tasks. Help me create a simple measurement framework that considers:

1. Time saved (compared to traditional methods)
2. Quality impact (better, same, or worse than human-only work)
3. Learning curve (how much prompt engineering is needed)
4. Consistency of results (how reliable the outputs are)

For each of these categories, suggest:
- A simple 1-5 scale for evaluation
- 2-3 concrete metrics I could track
- A method for gathering data without excessive overhead

Then, recommend how I might visualize this data to identify which PM tasks benefit most from LLM assistance.
```

### When to Use LLMs vs. When Not To

Based on our experiences working with product managers, here's a practical guide:

**High-Value LLM Use Cases**:

- Converting rough notes into structured documents
- Generating first drafts of routine communications
- Processing and summarizing large volumes of feedback or research
- Creating variations of content for different audiences
- Brainstorming alternatives or edge cases

**Low-Value or Risky LLM Use Cases**:

- Final decisions on strategic direction
- Sensitive communications without human review
- Tasks requiring deep domain expertise without verification
- Complex technical feasibility assessments
- Highly contentious or political internal discussions

## Practice: Real PM Task with Prompt Support

### Exercise: PM Task Transformation

**Scenario**: Choose one real PM task you performed recently that was time-consuming or challenging. We'll transform how you approach it using prompt engineering.

#### Step 1: Analyze the Traditional Process

Document:

- What the task involved
- How long it typically takes
- What parts were most time-consuming
- Where quality or consistency issues occurred

#### Step 2: Design a Prompt Strategy

Create a prompt strategy that includes:

- Initial prompt to get started
- Follow-up prompts for refinement
- Evaluation criteria to check quality
- Human touchpoints for review and enhancement

#### Step 3: Execute and Compare

Complete the task using your prompt strategy and compare:

- Time spent
- Quality of output
- Parts that still required significant human input
- Overall satisfaction with the result

#### Example Task Transformation: Quarterly Business Review Preparation

**Traditional Process**:

- Manually gather metrics from multiple sources (3-4 hours)
- Create first draft of presentation (2-3 hours)
- Refine messaging for executive audience (1-2 hours)
- Prepare talking points and anticipate questions (1-2 hours)
- Total: 7-11 hours

**Prompt Strategy**:

*Initial Data Organization Prompt*:

```
I'm preparing for our quarterly business review and need to organize our key metrics. I have data on:
- User acquisition (up 15% QoQ)
- Retention (30-day: increased from 42% to 47%)
- Feature adoption (dashboard: 78%, reporting: 55%, mobile: 34%)
- Revenue (MRR up 22% QoQ)
- Customer satisfaction (NPS 42, up from 38)

Help me organize this into a logical structure that tells a cohesive story about our product health. For each metric:
1. Suggest a simple visualization approach
2. Identify 1-2 insights worth highlighting
3. Note any concerning trends or areas needing explanation
4. Suggest additional context that would make this more meaningful
```

*Presentation Structure Prompt*:

```
Based on the metrics and insights we've organized, create an outline for a 20-minute QBR presentation including:

1. A compelling narrative arc that connects our Q2 goals to our results
2. 5-7 main sections with 1-2 slides each
3. Suggested data visualizations for key metrics
4. Transition language between sections
5. Places to include forward-looking statements or next quarter's focus

The audience includes the executive team who wants to understand: (1) are we on track for our annual goals, (2) what's working/not working, and (3) how we're responding to challenges.
```

*Executive Messaging Refinement Prompt*:

```
Review this draft presentation outline for our QBR and help me refine the messaging to be more executive-friendly:

1. Reduce jargon and technical details
2. Strengthen the connection to business outcomes
3. Highlight decision points or places we need executive input
4. Add 1-2 memorable statements that capture our quarterly story
5. Suggest places where customer quotes or examples would strengthen the narrative

[Draft outline]
```

*Anticipated Questions Prompt*:

```
Based on this QBR presentation outline, help me prepare for the Q&A session by:

1. Identifying 7-10 challenging questions executives might ask
2. For each question, drafting a concise, honest response
3. Noting what additional data I should have on hand
4. Suggesting areas where we might want to proactively address concerns

[Final outline]
```

**New Process**:

- Gather metrics (still requires 2-3 hours)
- Use LLM to organize and create initial structure (30 minutes)
- Review and refine LLM-generated presentation outline (1 hour)
- Use LLM to improve executive messaging and prepare for questions (30 minutes)
- Total: 4-5 hours (reduction of 40-60%)

## Developing Your Prompt Strategy

A good prompt strategy integrates LLMs into your workflow in a systematic, repeatable way.

### Components of an Effective PM Prompt Strategy

1. **Task Evaluation Framework**
   - Which tasks benefit most from LLM assistance?
   - Which require mostly human input?
   - Which can be partially automated?

2. **Prompt Template Library**
   - Core templates for common PM tasks
   - Organizational conventions for formats and structures
   - Examples of successful prompts with explanations

3. **Quality Control Process**
   - How to verify outputs before using them
   - When human review is mandatory
   - How to improve prompts based on results

4. **Knowledge Management Approach**
   - How to store and share effective prompts
   - Process for updating templates as needs evolve
   - Training for team members on effective prompting

### Example: Personal PM Prompt Playbook Structure

```markdown
# My PM Prompt Playbook

## Daily Tasks
- Stand-up summary generation
- Meeting note structuring
- Email drafting for common scenarios

## Weekly Tasks
- Sprint planning preparation
- Progress report generation
- Stakeholder update templating

## Monthly/Quarterly Tasks
- Roadmap review prompts
- Business review preparation
- OKR progress analysis

## Documents & Artifacts
- PRD templates
- User story formula
- Competitor analysis framework
- Launch plan checklist

## Decision Support
- Prioritization framework prompts
- Trade-off analysis structure
- Risk assessment template

## Team Collaboration
- Feedback consolidation
- Multi-stakeholder communication
- Technical-to-business translation
```

## Tips for Sustainable AI Integration

- **Think like a system designer**: Good prompt engineering is like building small tools that fit into your larger workflow
- **Pair prompts with templates, checklists, and workflows** you already use
- **Start small** with non-critical tasks until you build confidence
- **Document what works** and iterate on your approach
- **Share knowledge** with your team to build collective capability
- **Set appropriate expectations** with stakeholders about AI-assisted work
- **Maintain critical thinking** and don't outsource judgment

## Final Exercise: Build Your 30-Day AI Integration Plan

Create a 30-day plan to integrate LLMs into your PM workflow:

### Week 1: Foundation

- Identify 2-3 routine tasks for initial AI assistance
- Create and test basic prompts for these tasks
- Document time savings and quality impacts

### Week 2: Expansion

- Add 2-3 more complex tasks
- Develop multi-step prompt strategies
- Start building your personal prompt library

### Week 3: Refinement

- Review results and refine approaches
- Address any quality issues
- Begin standardizing successful templates

### Week 4: Systematization

- Create your personal prompt playbook
- Establish regular review and improvement process
- Share learnings with interested colleagues

## Conclusion and Next Steps

You've now completed our 5-day course on AI Prompting for Product Managers. You should have:

1. A solid understanding of how LLMs work and what they're good at
2. Practical experience with basic and advanced prompting techniques
3. Skills for evaluating and improving LLM outputs
4. Strategies for integrating LLMs into your daily PM workflow
5. Templates and examples you can immediately apply to your work

### How to Continue Your AI Journey

1. **Practice regularly**: The only way to master prompt engineering is through consistent practice. Try to use these techniques daily.

2. **Build your template library**: Save successful prompts and continue to refine them as you learn what works best.

3. **Stay current**: LLM capabilities evolve rapidly. What works today may be replaced by better approaches tomorrow. Follow blogs and communities focused on prompt engineering. Are you subscribed to my [newsletter](https://substack.com/@llmwire) yet?

4. **Share and learn from peers**: Exchange effective prompts and strategies with other PMs. Different perspectives lead to better approaches.

5. **Measure impact**: Track how LLM use affects your productivity and work quality to justify continued investment in these skills.

### Final Thought

Remember that LLMs are tools to amplify your expertise as a Product Manager, not replace it. Your product sense, strategic thinking, and human relationships remain your most valuable assets. AI can help you work more efficiently and effectively, giving you more time to focus on what truly matters: creating products that solve real problems for real people.

Thank you for completing this course! We hope these techniques help you thrive in the rapidly evolving world of AI-assisted product management.

---
Up Next: [Bonus Module: AI Use – Ethically and Effectively](06_ethics/06_ethics.md)
