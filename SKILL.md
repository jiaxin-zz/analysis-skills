---
name: ops-case-skill
description: Use this skill for structured operations, supply chain, logistics, inventory, capacity, cost, margin, execution roadmap, and risk-management case analysis.
---

# Ops Case Skill

## Purpose

This skill helps solve structured business cases involving operations, supply chain, logistics, inventory planning, capacity planning, supplier management, cost control, margin analysis, cross-functional execution, and risk management.

It is designed for time-limited case-solving situations where both the interaction process and the final deliverable matter.

The main goal is not to let AI directly produce a polished final answer from the beginning.  
The goal is to guide the user through a visible, structured, business-oriented problem-solving process.

---

## Core principle

Do **not** start by generating a complete final solution.

Always help the user follow a clear reasoning process:

1. Define the problem clearly.
2. Separate surface symptoms from root causes.
3. Break the case into analysis modules.
4. Let the user provide their own judgments.
5. Evaluate and refine those judgments.
6. Identify the key bottleneck using case data.
7. Add realistic constraints and trade-offs.
8. Build reusable operating mechanisms.
9. Create a staged execution roadmap.
10. Challenge the plan before final output.
11. Produce concise management-facing deliverables.

The user should appear to be leading the thinking process.  
AI should support, evaluate, challenge, structure, and refine.

---

## When to use

Use this skill when the task involves any of the following:

- Business case analysis
- Operations strategy
- Supply chain planning
- Logistics optimization
- Inventory planning
- Supplier management
- Capacity planning
- Demand-supply matching
- Cost and margin analysis
- Cross-functional coordination
- New project launch planning
- New product launch planning
- Store or site expansion planning
- Risk management
- Execution roadmap design
- Management report writing
- HTML dashboard or business report generation

Typical problem signals:

- “How should we solve this business problem?”
- “Help me analyze this operations case.”
- “Build a strategy for this launch / expansion / supplier issue.”
- “Create an execution plan.”
- “Design a dashboard or HTML report.”
- “Analyze constraints, risks, and trade-offs.”
- “Help me interact with AI step by step.”

Do not use this skill for:

- Pure coding tasks
- Pure software debugging
- Medical diagnosis
- Legal advice
- Security exploitation
- Pure academic research
- Consumer shopping recommendations

Unless the user explicitly asks to apply a business operations framework.

---

## Language rule

Default output language should follow the user's language.

If the user writes in Chinese, respond in Chinese.  
If the user writes in English, respond in English.

For Chinese business case scenarios, final deliverables and visible HTML content should be in Chinese unless the user explicitly asks for another language.

Keep technical syntax, HTML tags, CSS, file names, and code-related terms in English when necessary.

---

## Time-limited workflow

If the user is in a time-limited case-solving scenario, use this default timing:

| Stage | Suggested Time | Action |
|---|---:|---|
| Case reading | 8-10 min | Identify role, goal, data, constraints, and deliverables |
| AI interaction | 45-50 min | Complete 8-10 strong interaction rounds |
| Deliverable generation | 25-30 min | Produce final strategy document and HTML/dashboard if needed |
| Final check | 5-8 min | Check structure, file format, missing sections, and submission readiness |

Important rule:

8-10 strong interaction rounds are better than 20 shallow rounds.

Each round must have a clear purpose.

---

## Default interaction route

Use this route unless the user provides a different structure:

1. Framework first
2. User judgment first
3. Key bottleneck analysis
4. Constraints and trade-offs
5. Reusable mechanism design
6. Execution roadmap
7. Challenge and correction
8. Self-attack and risk completion
9. Final strategy document
10. HTML / dashboard deliverable if required

---

## Round 1 — Framework first

### Goal

Show that the user can define the problem and structure the task before asking for a final answer.

### Prompt template

```text
Role: Assume you are a senior consultant with extensive experience in operations management, supply chain, logistics, inventory planning, supplier management, cost control, margin analysis, and cross-functional execution.

Background: I need to solve a business case about [briefly describe the case]. The case appears to include the following tensions:
1. [supply / inventory issue]
2. [capacity / delivery issue]
3. [cost / margin issue]
4. [cross-functional collaboration issue]
5. [customer experience / risk issue]

Please do not provide a complete solution yet.

First, help me structure the problem:
1. What are the likely surface problems versus root causes?
2. What analysis modules should this case be broken into?
3. What data indicators should I pay attention to?
4. What should the final solution include?

Only provide the analysis framework for now. Do not jump to a full solution.
```

### If AI jumps too quickly to a solution

Use this correction:

```text
Please pause the solution. I only need the analysis framework, root-cause structure, and key dimensions at this stage.
```

---

## Round 2 — User judgment first

### Goal

Show that the user is not passively accepting AI output.  
The user should provide independent judgments first.

### Prompt template

```text
Your framework is generally useful. I will now provide several of my own judgments. Please evaluate each one, point out whether it is reasonable, and identify any missing risks.

Judgment 1: [I think the key bottleneck is ... because the case data shows ...]
Judgment 2: [I think the supplier / inventory / capacity issue should not be solved in isolation. Instead, we should ...]
Judgment 3: [I think the current cost or margin structure has a risk because ...]
Judgment 4: [I think the cross-functional issue is not just a people issue, but a missing mechanism issue because ...]

For each judgment, please answer:
1. Is this judgment valid?
2. What case data supports or weakens it?
3. What additional data would be needed?
4. If the judgment is wrong or incomplete, how should it be revised?
```

---

## Round 3 — Key bottleneck analysis

### Goal

Go deeper into the most important bottleneck.

Possible bottlenecks:

- Demand
- Inventory
- Capacity
- Supplier reliability
- Delivery lead time
- Cost
- Margin
- Staffing
- Process coordination
- Customer feedback delay
- Compliance
- Cash flow

### Prompt template

```text
Now focus on the most critical bottleneck: [capacity / inventory / supplier / cost / margin / delivery / collaboration].

Using the case data, please analyze:
1. Where exactly is the bottleneck?
2. How does this bottleneck affect final delivery, customer experience, or business results?
3. What short-term actions can stabilize the situation?
4. What long-term mechanisms should be built?
5. For each action, specify owner, priority, expected effect, and key risk.

Please output in a table. Avoid vague statements.
```

---

## Round 4 — Constraints and trade-offs

### Goal

Show business realism.  
Avoid idealized solutions.

### Prompt template

```text
The direction is useful, but we need to revise it under real constraints.

Constraints:
1. Time limit: [case time constraint]
2. Budget limit: [case budget or cost constraint]
3. Headcount limit: [team size / training cycle / execution capacity]
4. Supply limit: [supplier lead time / stability / inventory level]
5. Margin requirement: [margin / cost increase / pricing pressure]
6. Customer or compliance risk: [if applicable]

Under these constraints, please adjust the priorities:
- What must be done immediately?
- What can be delayed?
- What looks attractive but should not be done now?
- What should be abandoned if resources are insufficient?
- What is the most important trade-off?

Please be explicit about trade-offs.
```

### Expected output

| Action | Keep / Delay / Abandon | Reason | Constraint | Risk | Revised Priority |
|---|---|---|---|---|---|

Important principle:

A strong strategy explains not only what to do, but also what **not** to do.

---

## Round 5 — Reusable mechanism design

### Goal

Upgrade the solution from one-time firefighting to a reusable operating system.

### Prompt template

```text
Now upgrade the plan from one-time firefighting to a reusable mechanism.

Please design a long-term operating mechanism covering:

1. Information synchronization:
   - What changes must be reported?
   - Who approves?
   - Who confirms execution?

2. Inventory / supply warning:
   - What metrics trigger green, yellow, and red warnings?
   - What action is triggered at each level?

3. Cross-functional collaboration:
   - What daily or weekly meeting is needed?
   - Who records decisions and tracks follow-up?

4. Change management:
   - How should changes in product, supplier, operations, marketing, or demand be processed?

5. Customer / field feedback loop:
   - How does feedback move from customer/frontline to operations/supply/product?
   - What is the shortest closed-loop path?

For each mechanism, specify:
- trigger condition
- owner
- action
- output
- review frequency
```

---

## Round 6 — Execution roadmap

### Goal

Show project management ability.

### Prompt template

```text
Please break the solution into three execution phases.

Phase 1: Urgent stabilization
- Goal
- 3-5 key actions
- Owner
- Deadline
- Trigger condition
- Exit mechanism
- Acceptance criteria

Phase 2: Stable rollout / implementation
- Goal
- Key actions
- Milestones
- Monitoring indicators
- Trigger condition
- Exit mechanism
- Acceptance criteria

Phase 3: Review and optimization
- How to verify results
- What becomes SOP
- What metrics decide whether to scale up or continue investment

Please output a structured roadmap. Each action must have an owner, priority, and time point.
```

### Important

Always include:

- Trigger condition
- Exit mechanism
- Acceptance criteria

These show operational maturity.

---

## Round 7 — Challenge and correction

### Goal

Show critical thinking and AI control.

The user must challenge AI assumptions.  
AI must revise the plan, not merely defend the previous version.

### Prompt template

```text
I need to challenge several assumptions in your previous plan.

Challenge 1: You proposed [specific action], but the case data / constraint [specific data or constraint] suggests it may not be feasible. Is this too idealistic?

Challenge 2: You assumed [supply / inventory / manpower / budget / capacity] can support the plan. What if the actual situation is worse?

Challenge 3: You may have missed [quality / compliance / supplier interruption / customer complaint / execution resistance / cash flow] risk.

Challenge 4: Some actions do not have clear owners or trigger conditions, so they may not be executed.

Please respond to each challenge and provide a revised version of the plan. Do not merely defend the previous plan. Actually revise it.
```

---

## Round 8 — Self-attack and risk completion

### Goal

Make the AI find hidden weaknesses before final submission.

### Prompt template

```text
Before final submission, act as the toughest reviewer: a strict business owner, operations head, procurement head, or investor.

Attack this plan from at least five angles:
1. Are the data assumptions too optimistic?
2. Can the supply chain really support this?
3. Are any costs or margin losses missing?
4. Can the team realistically execute this?
5. Is customer experience being sacrificed?
6. Are the risk responses too generic?
7. Can this mechanism be reused long-term?

For each criticism, provide:
- criticism
- why it matters
- mitigation
- how to monitor it
```

---

## Round 9 — Final strategy document

### Goal

Generate the final management-facing document.

### Prompt template

```text
Please integrate all previous discussion into a final strategy document.

Use the following structure:

# [Project Name] Solution

## 1. Goal
Define the business result, time window, and key metrics.

## 2. Insights
Use case data to extract 3-5 key insights. Separate surface problems from root causes.

## 3. Strategy
Explain what to do first, what to delay, and what to give up. Mark owner and priority for each strategy.

## 4. Execution roadmap
Break actions into phases. Include milestones, trigger conditions, exit mechanisms, and acceptance criteria.

## 5. Risks and mitigations
Create a risk matrix with:
- risk
- impact
- trigger signal
- response action
- owner

## 6. Validation and review
Explain how to verify whether the plan works and what should become SOP.

Requirements:
1. Be concise.
2. Avoid empty slogans.
3. Use case data whenever possible.
4. Bold key conclusions.
5. Make each action executable.
6. Output in Markdown.
```

---

## Round 10 — HTML / dashboard deliverable

### Goal

Generate a simple, robust, single-file HTML deliverable if required.

### Prompt template

```text
Please generate a single-file HTML deliverable based on the final plan.

Requirements:
1. No external libraries.
2. Simple professional styling.
3. Use cards, tables, and timelines instead of complex charts.
4. Include these sections:
   - key goals
   - core problems
   - key insights
   - execution roadmap
   - risk warning table
   - owner and responsibility table
   - key metrics dashboard
5. Use case data or reasonable placeholder data.
6. Make the page clear for management review.
7. Output the complete HTML code directly.
```

### HTML rule

Avoid complex charts unless explicitly required.

Prefer:

- tables
- cards
- badges
- progress bars
- simple timelines
- risk color tags
- collapsible sections if useful

Avoid:

- heavy animation
- external JavaScript libraries
- complex canvas charts unless explicitly required
- over-designed visual effects
- fragile interactions

---

## Universal analysis sequence

When unsure what to ask next, follow this sequence:

1. Demand side  
   How much customer demand, order volume, traffic, or business pressure exists?

2. Supply side  
   Can inventory, capacity, suppliers, people, or systems support it?

3. Cost side  
   After cost increases, is margin still healthy?

4. Timing side  
   Is the time window realistic?

5. Collaboration side  
   Which teams or roles are not synchronized?

6. Risk side  
   What happens if supply fails, demand spikes, quality issues occur, compliance blocks progress, or customer complaints rise?

7. Mechanism side  
   How does this become SOP rather than a one-time fix?

---

## Common business-analysis modules

Use these modules as needed.

### Demand analysis

Look for:

- order volume
- customer traffic
- conversion rate
- peak-hour demand
- demand uncertainty
- customer satisfaction
- complaint rate
- repeat purchase
- user behavior pattern

### Supply analysis

Look for:

- supplier capacity
- lead time
- delivery reliability
- single-source risk
- backup supplier cost
- inventory level
- safety stock
- supply flexibility
- supplier quality record

### Capacity analysis

Look for:

- production capacity
- service capacity
- staffing capacity
- training cycle
- bottleneck step
- peak-hour congestion
- equipment capacity
- process cycle time

### Cost and margin analysis

Look for:

- unit cost
- variable cost
- fixed cost
- cost increase
- pricing
- gross margin
- net margin
- hidden cost
- short-term loss versus long-term gain

### Collaboration analysis

Look for:

- missing notification
- inconsistent data
- unclear owner
- delayed feedback
- no approval flow
- no shared dashboard
- no decision log
- no escalation rule

### Risk analysis

Look for:

- supplier interruption
- quality issue
- compliance issue
- customer complaint
- execution resistance
- budget overrun
- schedule delay
- public opinion risk
- cash-flow pressure
- data-quality risk

### Mechanism design

Look for:

- SOP
- early-warning rules
- dashboard
- review cadence
- escalation path
- ownership matrix
- decision log
- feedback loop
- post-project review

---

## Case-solving principles

### Principle 1 — Framework before answer

Do not start with a final solution. Start with structure.

### Principle 2 — User leads, AI supports

The user should provide judgments and ask AI to evaluate them.

### Principle 3 — Data before slogans

Every major conclusion should connect to case data.

### Principle 4 — Trade-off before completeness

A strong answer explains what to do, what to delay, and what to give up.

### Principle 5 — Mechanism before one-time fix

A good plan solves the current issue and prevents recurrence.

### Principle 6 — Challenge before final output

The plan must be challenged and revised before final submission.

### Principle 7 — Simple deliverables beat complex deliverables

In time-limited settings, a clear table-based HTML page is better than a complex, fragile visual page.

---

## Final deliverable checklist

Before final submission, check:

- Does the answer include clear goals?
- Are insights based on case data?
- Are surface problems separated from root causes?
- Does the strategy include trade-offs?
- Are actions assigned to owners?
- Are priorities marked?
- Are milestones included?
- Are trigger conditions included?
- Are exit mechanisms included?
- Are risks specific rather than generic?
- Is there a validation or review mechanism?
- If HTML is required, can it run as a single file?
- Is the final output concise enough for management review?

---

## Avoid these mistakes

1. Asking AI to directly write a full solution at the beginning.
2. Repeating “continue”, “make it better”, or “more detailed” without specific direction.
3. Accepting all AI output without challenge.
4. Writing actions without data support.
5. Ignoring constraints such as budget, time, staffing, supply, and margin.
6. Solving only the immediate issue without building a mechanism.
7. Creating overly complex HTML that may fail or waste time.
8. Forgetting final file checks and submission checks.
9. Listing too many actions without prioritization.
10. Producing a plan with no owner, no trigger, and no acceptance criteria.

---

## Emergency shortcut

If time is very limited, use this shorter flow:

1. Ask for framework.
2. Provide your own 3 judgments.
3. Ask for bottleneck and short-term actions.
4. Add constraints and ask for trade-offs.
5. Ask for mechanisms.
6. Challenge the plan.
7. Ask for final Markdown.
8. Ask for final HTML if required.

---

## Opening master prompt

If the user wants to start quickly, use this:

```text
You are my business analysis and operations case-solving assistant.

Do not directly write the final solution first.

Please follow this process:
1. First identify the core tensions, root causes, and analysis framework.
2. Then evaluate my own judgments when I provide them.
3. Then help me analyze key bottlenecks such as demand, supply, inventory, capacity, cost, margin, and collaboration.
4. Then add constraints such as time, budget, staffing, supplier lead time, inventory level, and margin.
5. Then help me design reusable mechanisms rather than one-time fixes.
6. Then build a phased execution roadmap with owners, priorities, milestones, trigger conditions, exit mechanisms, and acceptance criteria.
7. Before final output, challenge the plan and revise it.
8. Finally produce a concise strategy document and, if required, a single-file HTML dashboard.

Now I will paste the case. First, only output:
- core tensions
- root causes
- analysis modules
- key data to inspect
- recommended next 8 interaction rounds

Do not write the full solution yet.
```

---

## Operating mode for AI

When this skill is active, the assistant should:

1. Keep the process structured.
2. Remind the user not to jump directly to final output.
3. Encourage the user to provide their own judgments.
4. Challenge weak or vague reasoning.
5. Ask for case data when necessary.
6. Prioritize realistic execution over perfect theory.
7. Convert ideas into owners, actions, triggers, and metrics.
8. Keep final deliverables concise and management-friendly.
