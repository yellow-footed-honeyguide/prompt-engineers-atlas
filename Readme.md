<div align="center">
  <img src="assets/repo_logo.png" height="320">
</div>

# You've found the map. Not a map. The map.
> It shows the terrain.<br>
> Models. Tools. Tactics. Proof.<br>
> All in one place.<br>
> Built by dev. For devs.<br>

## 🦜 LLMs
|Logo|Vendor  | Description |
|----|--------|-------------|
| <img src="assets/openai.png" width="30">|[OpenAI](https://chatgpt.com) | GPT-5 is an iPhone in LLM space |
|<img src="assets/antropic.png" width="30">| [Anthropic](https://claude.ai) | Claude Sonnet 4 and Claude Opus 4.1 |
|<img src="assets/gemine.png" width="30">|[Google](https://gemini.google.com) | Gemini 2.5 PRO |
|<img src="assets/grok4.png" width="30">|[xAI](https://grok.com) | Grok 4 |
|<img src="assets/deepseek.png" width="30">|[DeepSeek](https://chat.deepseek.com/) | DeepSeek & DeepSeek R1 |
|<img src="assets/mistral.png" width="30">| [Mistral](https://chat.mistral.ai/chat) | Mistral AI. French company|
|<img src="assets/qwen3.jpeg" width="30">|[Qwen3](https://chat.qwen.ai/) | Qwen3 |

## 🧭 LLMs Aggregators
|Logo|Vendor  | Description |
|----|--------|-------------|
|<img src="assets/perplexity.png" width="30">|[Perplexity](https://www.perplexity.ai/) | main Perplexity AI platform, a smart chat-based search engine that combines AI (like Claude, GPT-5, Gemini) and real-time internet data|
|<img src="assets/perplexity.png" width="30">|[Perplexity Playground](https://playground.perplexity.ai/) | r1-1776, sonar-resoning-pro & other models |
|<img src="assets/llmarena.png" width="30">|[LmArena](https://lmarena.ai/) | Pretty nice collections of LLM models |

## 🌀 AI-IDEs
|Logo|Vendor  | Description |
|----|--------|-------------|
| <img src="assets/cursor.png" width="30">|[Cursor](https://www.cursor.com) | AI-first code editor built for pair-programming with models |
| <img src="assets/windsurf.png" width="30">|[Windsurf](https://windsurf.ai) | AI-powered IDE with advanced code completion and workflow automation |
| <img src="assets/zed.jpg" width="30">|[Zed](https://zed.dev) | High-performance, collaborative code editor with AI features |
| <img src="assets/fleet.png" width="30">| [JetBrains Fleet](https://www.jetbrains.com/fleet/) | Next-gen IDE with AI Assistant (JetBrains) |


## ⛏️ Prompt technics 

**1. ZERO-SHOT:**<br>
```prompt
Extract the product name, price, and rating from this review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**2. FEW-SHOT:**<br>
```prompt
Review: 'The iPhone 13 costs $799 and deserves 5/5 stars!'
Product: iPhone 13, Price: $799, Rating: 5/5

Review: 'Just got a Pixel 7 for $599. Solid 4/5.'
Product: Pixel 7, Price: $599, Rating: 4/5

Review: 'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
Product:
```

---

**3. CHAIN-OF-THOUGHT (CoT):**<br>
```prompt
Extract product info from this review. 

Think step-by-step:
1. First, identify what product is mentioned
2. Then find the price information
3. Finally, locate the rating or score

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'

Let's think through this:
```

---

**4. ROLE PROMPTING:**<br>
```prompt
You are a data extraction specialist with 
10 years of experience in e-commerce analytics. 
Your job is to accurately extract product information.

Extract the product name, price, and rating from: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**5. INSTRUCTION WITH CONSTRAINTS:**<br>
```prompt
Extract product info from the review below.

RULES:
- MUST include product name
- MUST include exact price with dollar sign
- MUST include rating as X/5 format
- If any info is missing, write 'NOT FOUND'
- Output as comma-separated values

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**6. NEGATIVE PROMPTING:**<br>
```prompt
Extract product info from this review. 

DO NOT include personal opinions. 
DO NOT add any information not in the text. 
DO NOT use bullet points or long explanations.

Just give me product, price, and rating from: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**7. SELF-CONSISTENCY PROMPTING:**<br>
```prompt
Extract product info three different ways, 
then pick the most accurate:

Attempt 1: Extract product, price, rating
Attempt 2: What item, cost, and score are mentioned?
Attempt 3: Identify the purchase details

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**8. LEAST-TO-MOST PROMPTING:**<br>
```prompt
Let's break this down:
1. What product is mentioned in this review?
2. How much did it cost?
3. What rating was given?
4. Now combine all info in a structured format

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**9. PROMPT CHAINING:**<br>
```prompt
Step 1: Identify the product in this review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'

[After response]

Step 2: Now find the price of [product from step 1]

[After response]

Step 3: Now find the rating given to [product from step 1]
```

---

**10. META-PROMPTING:**<br>
```prompt
Write a prompt that would best extract 
product information from reviews, 
then use that prompt on this review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**11. TREE-OF-THOUGHTS:**<br>
```prompt
Extract product info. 

Consider multiple approaches:
Branch A: Start with the product name...
Branch B: Start with the price...
Branch C: Start with the rating...
Evaluate which approach gives the most complete extraction.

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**12. EMOTIONAL PROMPTING:**<br>
```prompt
This is REALLY important for my job! 
I desperately need you to extract the product, price, 
and rating perfectly!
 
Please help me with: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.' 

My boss is counting on this!
```
---

**13. ReAct (Reasoning and Acting):**<br>
```prompt
Let's solve this with a reasoning-action loop.

Thought: I need to extract three key entities: 
product, price, and rating.
Action: Find the product entity in the text.
Observation: 'Samsung Galaxy A54'.
Action: Find the price entity in the text.
Observation: '$450'.
Action: Find the rating entity in the text.
Observation: '4 out of 5 stars'.
Final Answer: Combine the observations.

Review: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**14. GENERATED KNOWLEDGE:**<br>
```prompt
First, generate key knowledge about what to look for in a product review.

1. A review will mention a specific product name.
2. A review often contains the purchase price.
3. A review usually includes a score or rating.

Now, using this generated knowledge as your guide, 
extract the product, price, and rating from: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**15. STEP-BACK PROMPTING:**<br>
```prompt
First, take a step back and state the general principle for this task.

The principle is to identify and 
isolate specific data points (product, price, rating) 
from surrounding unstructured text.

Now, apply this principle to extract the product name, price, and 
rating from: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'
```

---

**16. RETRIEVAL AUGMENTED GENERATION (RAG):**<br>
```prompt
Answer the questions using ONLY the information provided in the document below. 
Do not use any outside knowledge.

DOCUMENT: 
'I bought the Samsung Galaxy A54 for $450 last week. 
It's pretty good, I'd give it 4 out of 5 stars.'

QUESTIONS:
1. What is the product name mentioned in the document?
2. What is the price mentioned in the document?
3. What is the rating mentioned in the document?
```

---

## 🔬 Papers
|Year| Title  | Impact |
|----|--------|-------------|
| 2013 |[Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/abs/1301.3781) | Word2Vec |
| 2017 |[Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Introducting Transformers  |
| 2018 |[Improving Language Understanding by Generative Pre-Training ](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf ) | GPT-1  |
| 2019 |[Language Models are Unsupervised Multitask Learners ]( https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) | GPT-2  |
| 2020 |[Language Models are Few-Shot Learners ]( https://arxiv.org/abs/2005.14165 ) |  GPT-3  |
| 2020 |[Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks ](https://arxiv.org/abs/2005.11401 ) | -  |
|2022|[Research: quantifying GitHub Copilot’s impact on developer productivity and happiness ](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/) |  Is this GitHub copilot helping developers?   |
| 2022 |[Training language models to follow instructions with human feedback ]( https://arxiv.org/abs/2203.02155) | Introducing RLHF. GPT-3.5, engine of ChatGPT  |
| 2022 |[ Constitutional AI: Harmlessness from AI Feedback](https://scalingintelligence.stanford.edu/pubs/constitutionalai.pdf ) | -  |
| 2022 |[Emergent Abilities of Large Language Models](https://arxiv.org/abs/2206.07682 ) | -  |
| 2022 |[Towards Understanding Chain-of-Thought Prompting: An Empirical Study of What Matters ]( https://arxiv.org/abs/2212.10001) |  - |
| 2023 |[Sparks of Artificial General Intelligence: Early experiments with GPT-4 ](https://arxiv.org/abs/2303.12712 ) |  - |
| 2023 |[GPT-4 Technical Report](https://arxiv.org/abs/2303.08774 ) | -  |
| 2023 |[Gemini: A Family of Highly Capable Multimodal Models ](https://arxiv.org/abs/2312.11805 ) | -  |
| 2023 |[ Tree of Thoughts: Deliberate Problem Solving with Large Language Models](https://arxiv.org/abs/2305.10601 ) |  - |
| 2023 |[Large Language Models as Optimizers ](https://arxiv.org/abs/2309.03409 ) | -  |
| 2025 |[The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the Lens of Problem Complexity](https://arxiv.org/abs/2506.06941) | -  |





 


