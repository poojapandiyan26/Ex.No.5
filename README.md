# EXP 5: Comparative Analysis of Different Types of Prompting Patterns

## Aim
To test and compare how different prompting pattern models respond to various prompts — broad or unstructured (Naïve prompts) versus clear and refined (Basic prompts) — across multiple scenarios. The experiment analyses the quality, accuracy, and depth of the generated responses.

---

## Objectives
- Define and distinguish between Naïve and Basic prompting patterns.
- Design matched prompt pairs for five diverse scenarios.
- Record and compare the AI model outputs for each prompt type.
- Evaluate outputs on Quality, Accuracy, and Depth dimensions.
- Derive insights and best practices for effective prompt engineering.

---

## Explanation of Prompt Types

### Naïve Prompt (Broad / Unstructured)
A naïve prompt is a vague, minimal instruction given to the model without specifying context, format, constraints, or expected output. These prompts rely on the model's defaults and often yield generic or incomplete results.

> **Example:** `"Write a story."` or `"Tell me about climate change."`

### Basic Prompt (Refined / Structured)
A basic prompt provides clear, detailed, and structured instructions that guide the model explicitly. It specifies context, audience, format, length, constraints, and the type of reasoning expected.

> **Example:** `"Write a 200-word fantasy short story about a young wizard who discovers a hidden library beneath her school. Include vivid descriptions, a moment of conflict, and a hopeful ending."`

---

## Test Scenarios Selected
1. **S1** — Creative Story Generation
2. **S2** — Factual Question Answering
3. **S3** — Summarising a Concept
4. **S4** — Advice / Recommendation
5. **S5** — Code Generation

---

## Master Comparison Table

| Scenario | Naïve Prompt | Basic Prompt | Quality (N) | Quality (B) | Accuracy (N) | Accuracy (B) | Depth (N) | Depth (B) |
|---|---|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Creative Story Generation | Write a story. | Write a 200-word fantasy short story about a young wizard who discovers a hidden library beneath her school. Include vivid descriptions, a moment of conflict, and a hopeful ending. | 3/5 | 5/5 | N/A | N/A | Low | High |
| Factual Question Answering | Tell me about climate change. | Explain the three primary causes of climate change, their approximate percentage contributions to global warming, and two evidence-based mitigation strategies supported by the IPCC. | 3/5 | 5/5 | Medium | High | Low | High |
| Summarising a Concept | Summarize machine learning. | In 150 words, summarize machine learning for a non-technical audience. Distinguish between supervised, unsupervised, and reinforcement learning, and give one real-world application for each. | 3/5 | 5/5 | Medium | High | Low | High |
| Advice / Recommendation | How do I be productive? | I am a college student struggling with procrastination during exam season. Recommend 5 science-backed productivity techniques, explain the cognitive reason each works, and estimate the time investment per day. | 2/5 | 5/5 | Low | High | Low | High |
| Code Generation | Write code to sort a list. | Write a Python function called `bubble_sort(arr)` that implements bubble sort on a list of integers. Include type hints, a docstring explaining time complexity (best/worst/average), and three assert-based test cases. | 2/5 | 5/5 | Medium | High | Low | High |

> **N** = Naïve Prompt &nbsp;|&nbsp; **B** = Basic Prompt &nbsp;|&nbsp; N/A = Not applicable (creative tasks)

---

## Detailed Scenario-wise Analysis

### S1: Creative Story Generation

| Attribute | Naïve Prompt | Basic Prompt |
|---|---|---|
| **Prompt Used** | Write a story. | Write a 200-word fantasy short story about a young wizard who discovers a hidden library beneath her school. Include vivid descriptions, a moment of conflict, and a hopeful ending. |
| **Model Response** | Once there was a boy who liked magic. He found a spell book and learned many spells. The end. | Detailed 3-paragraph story with named character (Lyra), sensory details (floating candles, enchanted maps), internal conflict when the library starts to vanish, and a hopeful resolution. |
| **Quality** | 3/5 | 5/5 |
| **Accuracy** | N/A | N/A |
| **Depth** | Low | High |
| **Observation** | Generic, vague, no character depth | Rich narrative, structured arc, on-theme |

---

### S2: Factual Question Answering

| Attribute | Naïve Prompt | Basic Prompt |
|---|---|---|
| **Prompt Used** | Tell me about climate change. | Explain the three primary causes of climate change, their approximate percentage contributions to global warming, and two evidence-based mitigation strategies supported by the IPCC. |
| **Model Response** | Climate change is the warming of the Earth due to greenhouse gases. It is caused by burning fossil fuels and deforestation. It leads to rising sea levels and extreme weather. | Identified fossil fuels (~73%), agriculture (~18%), and deforestation (~11%) with sourced figures; mitigation strategies included carbon pricing and renewable energy transition per IPCC AR6 report. |
| **Quality** | 3/5 | 5/5 |
| **Accuracy** | Medium | High |
| **Depth** | Low | High |
| **Observation** | Surface-level, no quantitative data | Precise, data-backed, structured |

---

### S3: Summarising a Concept

| Attribute | Naïve Prompt | Basic Prompt |
|---|---|---|
| **Prompt Used** | Summarize machine learning. | In 150 words, summarize machine learning for a non-technical audience. Distinguish between supervised, unsupervised, and reinforcement learning, and give one real-world application for each. |
| **Model Response** | Machine learning is when computers learn from data without being explicitly programmed. It is a branch of artificial intelligence. | Clear 3-part explanation: supervised (spam detection), unsupervised (customer segmentation), reinforcement (game-playing AI). Used analogies like "teaching by example". Word count ~148. |
| **Quality** | 3/5 | 5/5 |
| **Accuracy** | Medium | High |
| **Depth** | Low | High |
| **Observation** | Incomplete, no sub-types mentioned | Complete, audience-appropriate, well-structured |

---

### S4: Advice / Recommendation

| Attribute | Naïve Prompt | Basic Prompt |
|---|---|---|
| **Prompt Used** | How do I be productive? | I am a college student struggling with procrastination during exam season. Recommend 5 science-backed productivity techniques, explain the cognitive reason each works, and estimate the time investment per day. |
| **Model Response** | Make a to-do list. Wake up early. Avoid distractions. Take breaks. | 5 strategies: Pomodoro Technique, spaced repetition, implementation intentions, sleep scheduling, and the 2-minute rule — each with a cognitive rationale and daily time estimate. |
| **Quality** | 2/5 | 5/5 |
| **Accuracy** | Low | High |
| **Depth** | Low | High |
| **Observation** | Generic bullet points, no reasoning | Tailored, evidence-based, actionable |

---

### S5: Code Generation

| Attribute | Naïve Prompt | Basic Prompt |
|---|---|---|
| **Prompt Used** | Write code to sort a list. | Write a Python function called `bubble_sort(arr)` that implements bubble sort on a list of integers. Include type hints, a docstring explaining time complexity (best/worst/average), and three assert-based test cases. |
| **Model Response** | `my_list = [3,1,2]`<br>`my_list.sort()`<br>`print(my_list)` | Full `bubble_sort(arr: list[int]) -> list[int]` with docstring (O(n²) worst, O(n) best), nested-loop implementation, and 3 assertions covering empty, sorted, and reverse lists. |
| **Quality** | 2/5 | 5/5 |
| **Accuracy** | Medium | High |
| **Depth** | Low | High |
| **Observation** | Used built-in sort, no explanation | Custom algorithm, documented, tested |

---

## Evaluation Analysis: Impact of Prompt Clarity

| Evaluation Dimension | Naïve Prompts | Basic Prompts |
|---|---|---|
| **Response Quality** | Often generic, vague, and incomplete. Avg: 2.6/5 | Consistently detailed, well-structured, and relevant. Avg: 5/5 |
| **Accuracy** | Factually surface-level; may miss specifics | High accuracy with specific facts, data, and domain-appropriate detail |
| **Depth of Analysis** | Low — single-layer answers, no sub-categories | High — multi-layer reasoning, examples, evidence |
| **Consistency** | Highly variable; depends on model defaults | Reliable and reproducible results across runs |
| **Usability of Output** | Requires significant post-processing | Ready-to-use; minimal revision needed |
| **Where Naïve Works** | Simple yes/no questions, basic definitions, casual brainstorming | Not applicable — basic prompts always match or exceed naïve results |

---

## Key Findings and Insights

### 1. Basic prompts consistently outperform naïve prompts
Across all five scenarios, structured prompts produced significantly higher-quality, more accurate, and deeper responses. Average quality: **5/5 (Basic)** vs **2.6/5 (Naïve)**.

### 2. Naïve prompts: when they are acceptable
Naïve prompts can be acceptable for simple, closed-ended queries such as basic definitions or yes/no questions. However, even in these cases, a slightly refined prompt yields better results.

### 3. The role of context and constraints
Specifying audience, length, format, and reasoning requirements dramatically improved response usability. Context-setting converted vague outputs into purpose-fit, audience-appropriate content.

### 4. Domain specificity matters
In technical scenarios (Code Generation), naïve prompts caused the model to use shortcuts (built-in functions) rather than implementing the requested algorithm. Structured prompts enforced the correct approach and added testability.

---

## Summary: Prompt Engineering Best Practices

| # | Principle | Example Application |
|:---:|---|---|
| 1 | Specify the output format | "Respond in a numbered list of 5 items" |
| 2 | Define the target audience | "Explain to a 10-year-old" vs "Explain to a data scientist" |
| 3 | Set word or length limits | "In 150 words" or "in 3 paragraphs" |
| 4 | Provide context or background | Include role, problem statement, or constraints |
| 5 | Ask for reasoning or evidence | "Explain why" or "cite evidence for each point" |
| 6 | Use role-play framing | "You are an expert nutritionist. Advise..." |
| 7 | Break complex tasks into steps | Multi-step prompts produce structured outputs |

---

## Result

 **The prompt for the above said problem executed successfully.**

---

## Conclusion

This experiment validated that prompt quality is a decisive factor in the usefulness of AI-generated outputs. Naïve prompts produce generic, surface-level responses that often require significant additional work. In contrast, well-structured basic prompts that specify context, format, audience, and constraints consistently unlock the full capability of AI language models.

For students, researchers, and professionals, investing time in prompt design — even a few additional seconds — yields dramatically better outputs and reduces post-processing effort. **Effective prompt engineering is not optional; it is foundational to productive human-AI collaboration.
