# Day 4: Evaluating and Iterating on LLM Output

## Objective

Learn how to critically evaluate LLM responses and refine your prompts for better output, creating a continuous improvement cycle for your AI-assisted workflows.

## Building on Previous Days

So far, we've covered the foundations of LLMs, core prompting techniques, and advanced methods to get better results. Today focuses on a critical skill: how to evaluate outputs and iterate on your prompts when results aren't quite right.

## The Importance of Evaluation

As a product manager, you're used to testing hypotheses and iterating on product features. The same mindset applies to working with LLMs:

1. You create a prompt (hypothesis)
2. You get a response (experiment)
3. You evaluate the results (analysis)
4. You refine your approach (iteration)

Let's look at techniques for steps 3 and 4.

## Spotting Subtle Errors and Hallucinations

### What Are Hallucinations?

"Hallucinations" are when LLMs generate information that sounds plausible but is factually incorrect or entirely fabricated. These can be particularly dangerous because they often sound confident and authoritative.

### Common Types of Errors in LLM Outputs

1. **Factual errors**: Incorrect data, statistics, or information
2. **Logical inconsistencies**: Arguments that don't hold up to scrutiny
3. **Contradictions**: Statements that conflict with other parts of the response
4. **Fabricated examples**: Made-up case studies, research, or references
5. **Temporal confusion**: Mixing up timelines or claiming outdated information is current

### How to Spot These Issues

**Example of Flawed Output**:

```
Our competitive analysis shows that 87% of enterprise SaaS products now include AI-driven analytics, according to the 2023 Gartner Magic Quadrant. The three market leaders (Tableau, Microsoft Power BI, and QlikView) have all implemented advanced natural language querying since 2021, with Tableau's implementation being rated highest for accuracy at 97.3%.
```

**Problems with this output**:

- Suspiciously precise statistics (87%, 97.3%)
- Reference to a specific Gartner report without actual citation
- Confident statements about all competitors' features that would require extensive research
- Highly specific technical claims that would be difficult to verify

### Techniques for Verification

1. **Check for suspiciously precise numbers**: Round numbers (like 30%) are more likely to be real than very specific ones (87.3%).

2. **Look for source attribution**: Be skeptical of claims without clear sources.

3. **Verify with your own knowledge**: Use what you know to spot obvious errors.

4. **Question convenient narratives**: If the output perfectly supports what you hoped to hear, be extra cautious.

5. **Break down complex claims**: Separate multi-part statements and verify each piece.

## Sanity-Checking for Internal Logic and Accuracy

### Logical Consistency Check

Ask yourself:

- Do the conclusions follow from the premises?
- Are there hidden assumptions that don't hold up?
- Would the logic make sense if applied to a different context?

### Critical Details Check

For product-specific outputs like requirements or roadmaps:

- Are there technical dependencies not being addressed?
- Are timeline estimations reasonable?
- Are user scenarios comprehensive and realistic?

### Example of a Logic Check Prompt

```
I've just received this analysis about our product strategy. Before I use it, please help me sanity check the logic and accuracy:

1. Identify any claims that would benefit from data verification
2. Point out any logical leaps or assumptions
3. Check if the recommendations actually follow from the analysis
4. Note if any important stakeholder perspectives are missing
5. Highlight any implementation challenges that aren't addressed

Here's the analysis:
[LLM output you want to check]
```

## How to Chain Prompts to Validate Results

### The Chaining Technique

Prompt chaining means using the output from one prompt as input for another. This creates a multi-step workflow that can validate and improve results.

### Example Chain for a Product Roadmap

#### Step 1: Generate Initial Roadmap

```
Create a 6-month product roadmap for our fintech app focused on improving user engagement with investment features. Include timing, resource requirements, and expected impact.
```

#### Step 2: Critical Review

```
You are a skeptical but constructive product leader. Review this draft roadmap and identify:
1. Dependencies that might be overlooked
2. Resource constraints that seem unrealistic
3. Features that might not deliver the expected impact
4. Technical challenges that might be underestimated

Draft roadmap:
[Output from Step 1]
```

#### Step 3: Stakeholder Perspective Check

```
Review this draft roadmap from the perspective of these key stakeholders:
1. Engineering team concerned about technical debt
2. Sales team needing competitive features
3. Customer success team dealing with current pain points
4. Finance team focused on monetization

What concerns would each stakeholder likely raise?

Draft roadmap:
[Output from Step 1]
```

#### Step 4: Refinement Based on Feedback

```
Based on this feedback:
[Combined insights from Steps 2 & 3]

Please revise the original roadmap to address the most critical concerns while maintaining the focus on user engagement with investment features.
```

### Benefits of Chaining

- Uncovers blind spots in initial outputs
- Mimics real-world feedback processes
- Creates a paper trail of deliberation
- Results in more robust final deliverables

## Asking the Model to "Double-Check Itself" or Rephrase

### Self-Criticism Prompts

You can ask the LLM to evaluate its own responses:

```
You just provided this analysis of our user research:
[Previous LLM output]

Please critically evaluate your own analysis:
1. What assumptions did you make that might not be valid?
2. Which parts have the highest uncertainty?
3. What alternative interpretations of the data would be reasonable?
4. What additional information would make this analysis more robust?
```

### Rephrasing for Clarity

Sometimes the issue isn't accuracy but clarity. Ask for rephrasing:

```
Please rephrase the following product description to be:
1. More concise (reduce by 30%)
2. Clearer for non-technical stakeholders
3. More benefit-focused rather than feature-focused
4. Structured with bullet points for key advantages

Original description:
[LLM output to rephrase]
```

## Practice: Improve a Flawed Roadmap or Summary

### Exercise: Evaluating and Improving LLM Output

**Scenario**: An LLM has generated a product roadmap based on your initial prompt, but it has several issues. Your task is to identify the problems and iterate to create a presentation-ready version.

**The Flawed Roadmap**:

```
Q2 2023 Product Roadmap for HealthTrack App

Phase 1 (April 2023):
- Implement AI-powered health recommendations with 99.8% accuracy
- Complete overhaul of the user interface across all platforms (iOS, Android, web)
- Add integration with all major hospital EMR systems
- Launch premium subscription model ($5.99/month)

Phase 2 (May 2023):
- Release Apple Watch, Fitbit, and Garmin integrations simultaneously
- Add social sharing features for fitness achievements
- Implement telehealth consultation booking feature
- Complete HIPAA and GDPR compliance certification

Phase 3 (June 2023):
- Launch personalized nutrition planning powered by our proprietary ML algorithm
- Add support for 15 additional languages
- Implement AR feature for exercise form correction
- Release open API for third-party developers
```

#### Step 1: Identify the Issues

Create a prompt to help identify problems with this roadmap:

```
As an experienced product manager, please analyze this draft product roadmap for our health tracking app and identify potential issues:

1. Flag any timeline or resource assumptions that seem unrealistic
2. Identify features that may have dependencies not accounted for
3. Highlight any claims or metrics that seem questionable
4. Note any potential compliance or technical issues
5. Suggest what might be missing from this roadmap

Here's the draft roadmap:
[Insert the flawed roadmap]
```

#### Step 2: Request an Improved Version

After identifying the issues, create a prompt for an improved version:

```
Based on the issues identified with our draft roadmap, please create a revised version that:

1. Has a more realistic timeline with appropriate sequencing
2. Groups features into priority tiers (must-have, should-have, nice-to-have)
3. Acknowledges dependencies between features
4. Includes success metrics that are reasonable and measurable
5. Considers resource constraints (our team has 4 engineers, 2 designers, and 1 QA)
6. Addresses compliance requirements appropriately

Additional context:
- We're a startup with limited resources
- HIPAA compliance is essential before any health data features
- Our current focus is improving retention, which is currently at 20% after 30 days
```

#### Step 3: Make it Presentation-Ready

Finally, refine the improved version into something you could present to stakeholders:

```
Please transform this revised roadmap into a presentation-ready format with:

1. An executive summary highlighting key strategic goals
2. Clear quarterly milestones with measurable objectives
3. Resource allocation overview
4. Risk assessment and mitigation strategies
5. Expected business outcomes tied to company OKRs

Our company OKRs include:
- Increase monthly active users by 40% this year
- Improve 30-day retention to 35%
- Launch premium features that drive $100K MRR by Q4
```

### Sample Solution

After completing this exercise, you would have:

1. A critical analysis of the flawed roadmap
2. A more realistic, prioritized roadmap
3. A presentation-ready version aligned with business goals

This iterative process mirrors how you should work with LLMs in real product management scenarios.

## Additional Practice: Evaluating Different Types of LLM Output

### Exercise 1: Improving a Vague PRD

Take a poorly specified product requirements document and use evaluation techniques to identify gaps, then create prompts to fill those gaps.

### Exercise 2: Validating Competitor Analysis

Evaluate an LLM-generated competitive analysis for potential inaccuracies, then create a prompt chain to validate and improve the analysis.

### Exercise 3: Enhancing User Stories

Analyze a set of AI-generated user stories, identify quality issues, and iterate to create more useful, detailed stories.

## Tips

- **Trust but verify**: Always apply critical thinking to LLM outputs, no matter how confident they sound
- **Comparison helps**: Generate multiple versions and compare them to spot inconsistencies
- **External validation**: For critical decisions, triangulate LLM outputs with other sources
- **Documentation**: Keep a record of your prompt iterations and what improvements worked
- **Progressive refinement**: Don't try to fix everything at once; focus on the most critical issues first

## Homework

1. Take a real work product you created using an LLM (or create one now)
2. Apply at least two evaluation techniques we discussed
3. Create an improved version through prompt iteration
4. Document what improvements had the biggest impact

Tomorrow, we'll bring everything together with real-life use cases and develop your personal strategy for integrating these techniques into your daily PM workflow!

---
Up Next: [Day 5: Real-Life Use Cases and Prompt Strategy](05_use_cases/05_use_cases.md)
