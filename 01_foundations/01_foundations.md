# Day 1: Foundations of LLMs & Prompt Engineering

## Objective

Understand the capabilities, limitations, and ideal use cases of Large Language Models (LLMs) so you can start identifying where they fit in your workflow.

## What is a Large Language Model? (without the math)

Imagine you have an incredibly well-read assistant who has devoured millions of books, articles, websites, and code repositories. This assistant has an amazing talent for pattern recognition and can predict what should come next in any text. That's essentially what an LLM is!

### How LLMs Work (The Simple Version)

Think of an LLM as having gone through a three-step process:

1. **Training**: The model reads an enormous amount of text from the internet, books, articles, and code. It's like a child who has read everything humans have written.

2. **Pattern Recognition**: As it reads, it learns patterns - which words tend to follow others, how ideas connect, and how language is structured in different contexts (technical docs vs. casual conversations).

3. **Completion**: When you prompt an LLM, it uses those learned patterns to predict what should come next - completing your thought in a way that matches the patterns it's seen.

It's like having a conversation with the collective knowledge of the internet, but filtered through a probability machine that predicts what a helpful human might say next.

### What Makes LLMs Powerful for PMs

Unlike simple search or rule-based systems, LLMs can:

- **Understand context**: They grasp the meaning behind your words, not just keywords
- **Generate new content**: They don't just retrieve - they create
- **Adapt to different formats**: They can write emails, requirements, user stories, or analysis in the right tone and structure
- **Connect ideas**: They can spot relationships between concepts that might not be obvious

### Limitations You Should Know

LLMs aren't magic, and understanding their limitations helps you use them effectively:

- **Knowledge cutoffs**: They don't know about events after their training cutoff date
- **Hallucinations**: They can confidently state incorrect information, especially about specific facts and figures
- **Context windows**: They can only consider a limited amount of text at once
- **Reasoning limitations**: Complex multi-step reasoning can be challenging for them
- **No true understanding**: They predict text patterns but don't truly "understand" in a human sense

## Use Cases for Product Managers

Let's translate these capabilities into practical PM applications:

### 1. First Drafts & Idea Generation

- Draft initial product requirements
- Generate feature ideas based on specific user problems
- Create starter templates for user stories
- Brainstorm potential edge cases and user scenarios

**Example**: Instead of starting with a blank PRD, prompt: "Draft initial requirements for a feature that allows financial advisors to quickly view client portfolio performance across multiple time periods."

### 2. Communication Acceleration

- Draft stakeholder emails
- Create meeting agendas
- Transform technical specs into executive summaries
- Generate presentation outlines

**Example**: "Write an email to the engineering team explaining why we're prioritizing performance improvements over new features this quarter. Use data points: 40% increase in load times, 15% drop in user engagement."

### 3. Research & Analysis Support

- Summarize user interviews or feedback
- Analyze patterns in qualitative data
- Generate comparison matrices of competitors
- Synthesize market research

**Example**: "Based on these 5 user interview transcripts, identify common pain points and group them by severity and frequency."

### 4. Decision Support

- List pros and cons of different approaches
- Generate evaluation criteria for options
- Play devil's advocate on your assumptions
- Create structured frameworks for decisions

**Example**: "Help me evaluate whether to build this feature in-house or use a third-party API. Consider development time, maintenance costs, flexibility, and user experience."

## Prompt Engineering 101

Now that you understand what LLMs can do, let's learn how to talk to them effectively.

### What is Prompt Engineering?

Prompt engineering is the art and science of crafting inputs to LLMs that reliably produce useful outputs. Just as you wouldn't give vague requirements to your development team, you shouldn't give vague prompts to an LLM.

### The Anatomy of a Good vs. Bad Prompt

#### Elements of a Prompt

A complete prompt often has these components:

1. **Instruction**: What you want the LLM to do
2. **Context**: Relevant background information
3. **Input Data**: Specific information to work with
4. **Output Format**: How you want the response structured
5. **Examples**: Samples of what you're looking for (optional)

#### Compare These Prompts

**Bad Prompt**:

```
Write user stories.
```

**Why it's bad**: No context, no specifics about the product, no format guidance, no examples.

**Better Prompt**:

```
Write 3-5 user stories for a mobile banking app feature that allows users to split bills with friends. Use the standard format: "As a [type of user], I want [action] so that [benefit]". Include acceptance criteria for each story. Focus on the core user journey, security considerations, and error states.
```

**Why it's better**: Clear instruction, specific context about the product, defined output format, guidance on important aspects to cover.

### Subtle Changes That Make Big Differences

Small changes in prompts can dramatically change results:

**Original**: "List features for our product."

**Improved**: "You are a product manager with 15 years of experience in fintech. List 5-7 must-have features for a personal finance app targeting young professionals who are starting to invest, ordered by user impact."

The difference? The improved version:

- Assigns a role/expertise level
- Specifies an exact number of items
- Defines the target user
- Requests prioritization
- Focuses on a specific domain

## Practice: Bad Prompts → Better Prompts

Let's practice improving vague prompts into effective ones.

### Exercise 1: Feature Prioritization

**Vague Stakeholder Request**: "We need to decide what features to build next."

**Bad Prompt**: "What features should we prioritize for our product?"

**Better Prompt**:

```
I'm prioritizing features for Q3 for our healthcare scheduling app. I'll provide our top 10 feature candidates with data on:
1. Development effort (in story points)
2. Revenue potential (low/medium/high)
3. User request frequency (number of mentions)

For each feature, help me analyze:
- Which would deliver the most user value in the short term
- Which might create the strongest network effects
- Which address our most critical user pain points

Then recommend a prioritized list of the top 5 features with brief rationales.

Here are the features:
[List of features with data]
```

### Exercise 2: User Research Synthesis

**Vague Stakeholder Request**: "Tell me what the users think."

**Bad Prompt**: "Summarize this user feedback."

**Better Prompt**:

```
I've conducted 8 user interviews about our B2B SaaS analytics dashboard. I need to synthesize key insights for our product team.

Here are the interview notes:
[Interview transcripts or notes]

Please:
1. Identify the top 3 pain points mentioned by multiple users
2. Extract specific feature requests or improvement suggestions
3. Note any surprising or unexpected feedback
4. Highlight quotes that would be powerful for stakeholder communication
5. Suggest 2-3 quick wins we could implement in the next sprint

Format the output as a structured research summary with sections for each of the above categories.
```

## Tips

- **Be specific**: LLMs thrive on details and context. The more specific your prompt, the better.
- **If it sounds vague to a person, it's worse for an AI**: Always err on the side of giving more context rather than less.
- **Iterate**: Don't expect perfect results on the first try. Refine your prompts based on the outputs you get.
- **Set expectations**: Be clear about what format, length, or style you want in the response.

## Homework

Before tomorrow's session:

1. Take a recent vague request you received from a stakeholder
2. Transform it into a clear, detailed prompt following the patterns we've discussed
3. Test it with an LLM of your choice (Claude, ChatGPT, etc.)
4. Note what worked well and what could be improved

Tomorrow, we'll build on these foundations and learn more advanced prompting techniques that will give you even more control over LLM outputs.

---
Up Next: [Day 2: Core Prompting Techniques for Clearer Results](../02_core_techniques/02_core_techniques.md)
