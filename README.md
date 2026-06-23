# AI-models

## Three Main Types of Language Models

Base vs. Instruct vs. Reasoning

1️⃣ Base Models
📚 The well-read student before exam practice.
- Trained only to predict the next word on massive datasets
- Encodes world knowledge in neural weights
- Smart… but not tuned to follow instructions (more hallucinations)
👉 Examples: Llama 3 (pretrained), Mistral 7B (base)

2️⃣ Instruct Models
💬 The same student after coaching.
- Fine-tuned with SFT (Supervised Fine-Tuning) - instruction/response pairs
- Often improved further with RLHF (Reinforcement Learning from Human Feedback)
- More natural, safer, and better at tool use
👉 Examples: Llama 3 Instruct, Mistral 7B Instruct

3️⃣ Reasoning Models
🧩 The problem-solver who shows their work.
- Built on instruct models, but optimized with RL (Reinforcement Learning) + process supervision
- Trained to reason step-by-step, not just answer
- Excels at math, coding, planning
👉 Examples: OpenAI o3, Claude Sonnet 4

Takeaway:
 👉 Base = knowledge
 👉 Instruct = directions
 👉 Reasoning = problem-solving
