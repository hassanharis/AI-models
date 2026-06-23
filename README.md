# AI-models

## Three Main Types of Language Models
Base vs. Chat & Instruct vs. Reasoning vs. Thinking

Specialised/Fine-Tuned LLMs

Code: Codex, Code Llama, CodeT5, StarCoder, WizardCoder
Math: WizardMath, MathGLM, Minerva
Science: Galactica, BioGPT, ChemBERTa
Legal: LexGPT, CaseLaw-GPT
Medical: Med-PaLM, BioBERT, ClinicalBERT
Finance: BloombergGPT, FinBERT
Translation: NLLB, mBART, OPUS-MT

1️⃣ Base Models
📚 The well-read student before exam practice.
- Trained only to predict the next word on massive datasets
- Encodes world knowledge in neural weights
- Smart… but not tuned to follow instructions (more hallucinations)
👉 Examples: Llama 3 (pretrained), Mistral 7B (base), Llama-3.1-Nanda-87B-Chat

2️⃣ Chat & Instruct Models
💬 The same student after coaching.
- Fine-tuned with SFT (Supervised Fine-Tuning) - instruction/response pairs
- Often improved further with RLHF (Reinforcement Learning from Human Feedback)
- More natural, safer, and better at tool use
- They’re usually fine-tuned with: Supervised fine-tuning (SFT), Instruction tuning, RLHF (Reinforcement Learning from Human Feedback)

Ideal use cases: General chat, Writing and editing, Summaries, Content generation, Customer support, Productivity tasks

👉 Examples: Llama 3 Instruct, Mistral 7B Instruct

3️⃣ Reasoning Models
🧩 The problem-solver who shows their work.
- Built on instruct models, but optimized with RL (Reinforcement Learning) + process supervision
- Trained to reason step-by-step, not just answer
- Excels at math, coding, planning
- multi-step reasoning, intermediate thoughts, chains of logic, internal reflections, step-by-step breakdowns, Chain-of-Thought (CoT) Prompting, Tree-of-Thought (ToT) / Graph-of-Thought (GoT),Program-Aided Language Models (PAL) / Tool-use Models: These models can generate code (e.g., Python) to solve problems, execute that code, and then use the results to formulate their final answer.
- Reasoning models excel at: Math and logic, Code reasoning, Troubleshooting, Planning, Analytical tasks, Anything requiring structured thought

👉 Examples: OpenAI o3, Claude Sonnet 4

<img width="1100" height="651" alt="image" src="https://github.com/user-attachments/assets/13c7f0e6-5afd-466d-b930-0db47a2d38fc" />


Takeaway:
 👉 Base = knowledge
 👉 Instruct = directions
 👉 Reasoning = problem-solving

 <img width="1100" height="414" alt="image" src="https://github.com/user-attachments/assets/7ddc1807-cfdf-4556-90f1-43029b3a276c" />

Thinking Models
While closely related to reasoning, “thinking models” or models with enhanced planning often emphasise planning, self-correction, and deliberation. These models might involve iterative processes where the LLM refines its understanding, generates multiple drafts, or seeks external information to improve its output. This often involves an “inner monologue” or an “agentic” approach.

Goal: To achieve higher quality, more nuanced, and more robust outputs by allowing the model to engage in a more deliberate and potentially iterative internal process.

Example: An LLM drafting an essay, then identifying weaknesses and revising paragraphs for better flow and coherence, or an agentic LLM browsing the web to gather information before answering a complex query.

How they “think”:

Self-Correction/Self-Refinement: The LLM evaluates its own generated output against certain criteria or internal “critics” and then attempts to revise and improve it. This is akin to a human reviewing their work.
Iterative Generation: The model generates initial thoughts, then elaborates, refines, and expands on them in multiple passes.
“Inner Monologue” / Scratchpad: The LLM generates internal thoughts or plans (which might not be shown to the user) to guide its final output. This allows for more deliberate processing before committing to a response.
Agentic LLMs: LLMs that can act as “agents” by setting goals, breaking them into sub-goals, executing tools, observing results, and correcting their course. This embodies a more active and thoughtful process.




| Model Type      | What It Does                         | Best For                                                                                             | Primary Function                            | Performance Trade-offs                                                          |   |   |   |
|-----------------|--------------------------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------|---|---|---|
| Base            | Predicts next token                  | Custom fine-tuning, complex embeddings, RAG architectures.                                           | Pattern completion / Text prediction        | Not conversational. Lacks instruction formatting; requires complex prompting.   |   |   |   |
| Chat / Instruct | Follows instructions, chats fluently | Everyday tasks, writing, conversation, Customer-facing chatbots, quick API tasks, simple extraction. | General chat, summarization, classification | Fast and cheap, but poor at deep logic or multi-step calculations.              |   |   |   |
| Reasoning       | Produces intermediate thought steps  | Hard problems, coding, Logic puzzles, legal analysis, competitive programming, agent workflows.      | Deliberate problem-solving, math, coding    | Highly accurate, but much slower and significantly more expensive.              |   |   |   |
| Hybrid          | Chooses how much to reason           | General-purpose intelligent agents                                                                   |                                             | Balances speed and depth                                                        |   |   |   |
|                 |                                      |                                                                                                      |                                             |                                                                                 |   |   |   |
|                 |                                      |                                                                                                      |                                             |                                                                                 |   |   |   |



## When to use which?

Chat models tend to produce more natural, expressive writing
Reasoning models can feel more structured or analytical
Base models → perfect for training or teaching new skills
Chat models → great for writing, conversation, creativity
Reasoning models → ideal for tough, multi-step challenges
Hybrid models → the best general-purpose solution today

If you are building an AI feature, you now have three architectural choices:

The “App” (90% of use cases): Use an Instruct Model with Tool Calling (e.g. MCP, function calls, Skills). You want a conversational assistant that can look up data or do stuff. It’s fast, cheap, and lagom (Swedish for balanced/optimal) for most text tasks.

The “Operator” (5% of use cases): Use a Thinking Model. If the task involves vague requests, math, strict constraint satisfaction, or complex coding, you pay the latency penalty for the reasoning capability.

The “Domain Expert” (5% of use cases): Fine-tune a Base Model. Use this only if you need the model to speak a completely novel language (e.g., a proprietary legacy query language) where the “helpful assistant” training of Instruct models actively interferes with the syntax.

<img width="777" height="1236" alt="image" src="https://github.com/user-attachments/assets/7dc6c1d6-99d6-4fca-806c-befcfb37760f" />



 
