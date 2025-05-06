# Day 2: Core Prompting Techniques for Clearer Results

## Objective

Learn the core building blocks of great prompts and prompting techniques that get reliable results for product management tasks.

## Building on Day 1

Yesterday, we learned about what LLMs are, how they work (at a high level), and the basic structure of good prompts. Today, we'll dive into specific techniques that give you more control over your results.

Think of these techniques as different tools in your product management toolbox – each one helps in specific situations.

## Role Prompting

### What It Is

Role prompting means asking the LLM to adopt a specific persona or perspective when responding. This creates context that shapes how the model processes and responds to your request.

### Why It Works

LLMs have been trained on content written by people in various professional roles. By assigning a role, you tap into the patterns associated with how people in that role typically communicate.

### Examples for Product Managers

**Basic Prompt**:

```
Analyze these user feedback comments.
```

**Role Prompt**:

```
You are an experienced UX researcher who specializes in identifying patterns in qualitative user feedback. Analyze these user comments from our mobile banking app and categorize the feedback into usability issues, feature requests, and positive experiences.

[User comments here]
```

**Another Example**:

```
You are a senior product manager at a B2B SaaS company with experience presenting to C-level executives. Create a two-paragraph executive summary of our new analytics feature that highlights business value without technical jargon.
```

### When to Use It

- When you need specialized knowledge or perspective
- For creating content in a specific professional tone
- When you want frameworks or approaches typical of a certain role

## Few-Shot Learning

### What It Is

Few-shot learning means providing examples of what you want before asking the LLM to create something similar. It's like saying "here are some examples of what good looks like, now create something in the same pattern."

### Why It Works

By showing examples, you create a clear pattern for the LLM to follow. This helps it understand exactly what you want much better than just describing it.

### Examples for Product Managers

**Basic Prompt**:

```
Write user stories for a food delivery app.
```

**Few-Shot Prompt**:

```
I need to write user stories for a food delivery app. Here are two examples of the format and detail level I want:

Example 1:
As a hungry customer, I want to filter restaurants by cuisine type, so that I can quickly find food that matches my current preferences.
Acceptance Criteria:
- User can select multiple cuisine types from a predefined list
- Selected filters appear as chips/tags at the top of the screen
- Results update immediately when filters change
- If no restaurants match filters, show a "No results" message with suggestions

Example 2:
As a returning customer, I want to reorder from my order history with one tap, so that I can easily get my favorite meals again.
Acceptance Criteria:
- Order history shows the last 10 orders
- Each past order has a "Reorder" button
- Tapping "Reorder" adds all items to cart and navigates to checkout
- If items are unavailable, show alternatives before checkout

Using this same format and detail level, write 3 more user stories for the following features:
1. Restaurant ratings and reviews
2. Estimated delivery time tracking
3. Special dietary requirements filtering
```

### When to Use It

- When format and structure matter
- For tasks that can be demonstrated better than explained
- When you want consistent outputs that match existing work

## Chain-of-Thought (CoT) Prompting

### What It Is

Chain-of-Thought prompting asks the LLM to break down complex thinking into step-by-step reasoning. Instead of just asking for a conclusion, you ask for the thinking process that leads to the conclusion.

### Why It Works

This technique helps LLMs solve more complex problems by breaking them down into manageable steps. It reduces errors in reasoning and helps uncover assumptions.

### Examples for Product Managers

**Basic Prompt**:

```
Should we build a desktop app version of our mobile product?
```

**Chain-of-Thought Prompt**:

```
I need to decide whether we should invest in developing a desktop version of our mobile productivity app. Let's think through this step by step:

1. First, analyze our current user data to understand if there's evidence users want a desktop experience
2. Then, evaluate the technical complexity and resource requirements for building a desktop version
3. Next, identify potential revenue impacts and business model considerations
4. Consider competitive landscape and what alternatives already exist
5. Weigh the opportunity cost against other potential initiatives
6. Finally, make a recommendation with supporting rationale

Based on:
- 30% of our users have requested desktop functionality in surveys
- Our tech stack is React Native which could potentially be leveraged for desktop
- Our primary competitors all offer cross-platform solutions
- Current team has no desktop development experience
```

### When to Use It

- For complex decision-making support
- When analyzing trade-offs
- For prioritization exercises
- To surface hidden assumptions

## Constraints and Output Formatting

### What It Is

This technique involves explicitly specifying the format, structure, or limitations you want in the output. It's like giving the LLM a template to fill in.

### Why It Works

Constraints give the LLM clear boundaries and expectations, resulting in more predictable and usable outputs.

### Examples for Product Managers

**Basic Prompt**:

```
Compare these three payment processing solutions.
```

**Constrained Prompt**:

```
Compare these three payment processing solutions (Stripe, PayPal, Square) for our e-commerce platform. Present your analysis in a table with the following columns:
- Solution name
- Integration complexity (Low/Medium/High)
- Fee structure
- Key advantages
- Key limitations
- Best suited for (type of business)

After the table, provide a 3-sentence recommendation based on our needs: global payment support, mobile checkout optimization, and transaction fees under 3%.
```

**Another Example**:

```
Analyze the user feedback below and output your analysis in JSON format with the following structure:
{
  "main_issues": [array of top 3 issues],
  "sentiment": "positive", "neutral", or "negative",
  "feature_requests": [array of feature requests],
  "quick_wins": [array of 2-3 easy improvements],
  "user_quotes": [array of 2-3 representative quotes]
}

User feedback:
[Feedback text here]
```

### When to Use It

- When you need structured data for further processing
- For creating consistent reports or documentation
- When you need to integrate the output with other systems or workflows
- For side-by-side comparisons

## Stakeholder Prompts

### What It Is

Stakeholder prompting involves tailoring your prompts and outputs for different audiences within your organization.

### Why It Works

Different stakeholders need different levels of detail and focus areas. By specifying the audience in your prompt, you get content that's immediately useful without further editing.

### Examples for Product Managers

**Technical Stakeholder Prompt**:

```
Create a feature specification for our engineering team describing the implementation of a two-factor authentication system. Include API requirements, database changes, and potential security considerations. Use technical terminology appropriate for senior developers.
```

**Executive Stakeholder Prompt**:

```
Create a business case summary for our executive team explaining why we should implement two-factor authentication. Focus on risk reduction, competitive advantage, and customer trust. Limit to 5 bullet points, each under 20 words, with no technical jargon.
```

**Marketing Stakeholder Prompt**:

```
Draft three key selling points for our marketing team about our new two-factor authentication feature. Emphasize customer benefits, use metaphors that make security tangible, and compare favorably (but factually) to competitors' offerings.
```

### When to Use It

- When preparing materials for meetings with different departments
- For creating multi-level communication plans for product launches
- When translating technical concepts for non-technical audiences (and vice versa)

## Practice Exercise: Creating a PRD using Prompting Techniques

Now, let's combine these techniques to create a Product Requirements Document (PRD) for a new feature.

### The Scenario

Your company runs a B2B SaaS platform for scheduling and managing healthcare appointments. Based on customer feedback and competitive analysis, you've decided to add a new "Patient Reminder System" feature that will send automated reminders via multiple channels (SMS, email, in-app).

### Exercise: Create a PRD using These Techniques

#### Step 1: Role Prompting for the Executive Summary

```
You are a senior product manager at a healthcare SaaS company communicating with the executive team. Write a concise executive summary (3-4 sentences) for a PRD about a new "Patient Reminder System" feature. Focus on business impact, addressing the fact that missed appointments cost our clients an average of $200 per occurrence and happen at a 12% rate currently.
```

#### Step 2: Few-Shot Learning for User Stories

```
I need to write user stories for our Patient Reminder System. Here are two examples of the format I want:

Example 1:
As a healthcare provider, I want to customize reminder templates for different appointment types, so that patients receive relevant preparation instructions.
Acceptance Criteria:
- Provider can create templates for at least 5 different appointment types
- Templates support dynamic fields (patient name, doctor name, location, date/time)
- Changes save automatically and are version-controlled
- Preview function shows exactly how patients will see the reminder

Example 2:
As a patient, I want to choose my preferred reminder methods, so that I receive notifications in the way most convenient for me.
Acceptance Criteria:
- Patients can select any combination of SMS, email, and in-app notifications
- Patients can set preferred reminder timing (1 day before, 2 days before, etc.)
- Settings are accessible from patient profile and during appointment booking
- Changes apply to all future appointments until changed again

Using this same format and detail level, write 3 more user stories for:
1. Confirmation tracking for clinic administrators
2. Reminder escalation for high-priority appointments
3. Analytics dashboard for reminder effectiveness
```

#### Step 3: Chain-of-Thought for Technical Considerations

```
Let's think through the technical considerations for implementing the Patient Reminder System in our healthcare scheduling platform:

1. First, identify the current systems we need to integrate with
2. Then, analyze data requirements and where this information will be stored
3. Next, consider security and HIPAA compliance implications
4. Evaluate performance impact on our existing systems
5. Assess the timeline and phasing approach
6. Identify potential technical risks and mitigations

Based on:
- Our platform uses AWS for hosting
- We have a PostgreSQL database for patient records
- We currently use Twilio for occasional SMS alerts
- HIPAA compliance is mandatory for all features
- Our development team has 4 full-stack engineers available
```

#### Step 4: Constraints for Technical Requirements

```
Create a technical requirements section for the Patient Reminder System PRD with the following structure:

## Technical Requirements

### Integrations
[List all systems this feature needs to integrate with]

### Data Storage
[Table with: Data Element | Storage Location | Retention Period | Security Level]

### API Requirements
[Bullet points for each required API endpoint with method, basic parameters, and purpose]

### Performance Requirements
- System must support sending [X] reminders per minute
- Reminder delivery success rate must exceed [X]%
- End-to-end latency from trigger to delivery must be under [X] seconds

### Security Requirements
[Security requirements in bullet form]
```

#### Step 5: Stakeholder Prompts for Implementation Plan

```
Create three different versions of the implementation timeline for the Patient Reminder System:

1. For the development team: A detailed breakdown of development phases with technical dependencies and testing milestones. Include estimated story points per phase.

2. For the executive team: A high-level quarterly view showing key milestones, resource requirements, and expected completion date. Focus on business outcomes at each stage.

3. For the sales team: A customer-facing roadmap showing when different capabilities will be available, with emphasis on benefits and competitive differentiation, but without committing to specific dates.
```

### Sample Solution:

[Instructor Note: After completing this exercise, we'll share a complete PRD created using these prompting techniques, showing how each section benefits from a different approach.]

## Tips

- **Structure beats creativity**: Give the LLM the format you want first, then ask for content.
- **Add "Instructions," not just "questions"**: Phrases like "Your task is to..." or "Please provide..." set clearer expectations than questions.
- **Combine techniques for complex tasks**: Mix and match these methods based on your specific needs.
- **Start simple, then elaborate**: Begin with basic prompts and add complexity as needed.

## Homework

1. Choose an actual document you need to create for your product (competitive analysis, feature spec, roadmap, etc.)
2. Apply at least three of the prompting techniques we learned today
3. Document which techniques worked best for different sections
4. Come prepared to share your experience tomorrow

Tomorrow, we'll build on these foundations with advanced prompting techniques that unlock even more powerful capabilities!

---
Up Next: [Day 3: Advanced Prompting Techniques](../03_advanced_techniques/03_advanced_techniques.md)
