# Awesome LLM Evaluation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**A curated list of tools, benchmarks, frameworks, and research for evaluating large language models.**

Maintained by [Jake Meany](https://github.com/jakemeany523), marketing at [LayerLens](https://layerlens.com) (continuous evaluation infrastructure for AI).

## Contents

- [Evaluation Platforms](#evaluation-platforms)
- [Coding Benchmarks](#coding-benchmarks)
- [Reasoning Benchmarks](#reasoning-benchmarks)
- [Agent Benchmarks](#agent-benchmarks)
- [Safety and Alignment](#safety-and-alignment)
- [Instruction Following](#instruction-following)
- [Multimodal Benchmarks](#multimodal-benchmarks)
- [Evaluation Frameworks](#evaluation-frameworks)
- [LLM-as-Judge](#llm-as-judge)
- [Datasets and Data Tools](#datasets-and-data-tools)
- [Research Papers](#research-papers)
- [Blog Posts and Articles](#blog-posts-and-articles)
- [Community](#community)

## Evaluation Platforms

Platforms that provide infrastructure for running, managing, and analyzing LLM evaluations.

- **[LayerLens Stratix](https://layerlens.com)** : Continuous evaluation infrastructure. 200+ models, 6 benchmarks, vendor-neutral. Evaluation that generates, judges, and learns.
- **[Arize AI](https://arize.com)** : ML observability platform with LLM evaluation capabilities.
- **[Braintrust](https://braintrust.dev)** : Evaluation and logging platform for AI products.
- **[LangSmith](https://smith.langchain.com)** : Tracing, evaluation, and monitoring for LangChain and beyond.
- **[Weights & Biases](https://wandb.ai)** : ML experiment tracking with LLM evaluation integrations.
- **[Humanloop](https://humanloop.com)** : Evaluation and prompt management platform.
- **[Patronus AI](https://patronus.ai)** : Automated evaluation for LLM applications.
- **[Galileo](https://rungalileo.io)** : LLM evaluation with purpose-built judge models.
- **[DeepChecks](https://deepchecks.com)** : Testing and validation for AI systems.

## Coding Benchmarks

Benchmarks focused on code generation, debugging, and software engineering capabilities.

- **[SWE-bench](https://swebench.com)** : Real GitHub issues requiring multi-file code changes. The gold standard for agent-level coding evaluation.
- **[SWE-bench Lite](https://swebench.com)** : Curated subset of SWE-bench. 300 representative instances.
- **[LiveCodeBench](https://livecodebench.github.io)** : Continuously updated coding benchmark from competitive programming. Resistant to contamination.
- **[HumanEval](https://github.com/openai/human-eval)** : 164 Python function completion problems. Widely cited, largely saturated.
- **[MBPP](https://github.com/google-research/google-research/tree/master/mbpp)** : 974 crowd-sourced Python programming problems.
- **[Terminal-Bench](https://github.com/terminal-bench/terminal-bench)** : Evaluates models on real terminal/CLI tasks.
- **[BigCodeBench](https://bigcode-bench.github.io)** : Comprehensive code generation benchmark with practical programming tasks.
- **[Aider Polyglot](https://aider.chat/docs/leaderboards/)** : Multi-language coding benchmark from the Aider project.

## Reasoning Benchmarks

Benchmarks testing logical reasoning, math, and problem-solving.

- **[ARC AGI 2](https://arcprize.org)** : Abstract reasoning corpus. Tests genuine generalization, not pattern matching on training data.
- **[MATH-500](https://github.com/hendrycks/math)** : 500 competition-level math problems. Widely cited but approaching saturation for top models.
- **[MMLU Pro](https://github.com/TIGER-Lab/MMLU-Pro)** : Harder version of MMLU with more complex multi-step questions.
- **[GPQA Diamond](https://github.com/idavidrein/gpqa)** : Graduate-level science questions. PhD-level difficulty.
- **[GSM8K](https://github.com/openai/grade-school-math)** : Grade school math. Effectively saturated (top models >95%).
- **[BIG-Bench Hard](https://github.com/suzgunmirac/BIG-Bench-Hard)** : 23 challenging tasks from BIG-Bench that remain difficult.

## Agent Benchmarks

Benchmarks evaluating autonomous agent capabilities: tool use, multi-step planning, real-world task completion.

- **[BFCL v3](https://gorilla.cs.berkeley.edu/leaderboard.html)** : Berkeley Function Calling Leaderboard. Tests structured tool/function calling accuracy.
- **[BIRD-CRITIC](https://bird-bench.github.io/)** : Database interaction benchmark. Tests SQL generation and result interpretation.
- **[WebArena](https://webarena.dev)** : Autonomous web browsing and task completion across realistic websites.
- **[OSWorld](https://os-world.github.io)** : Computer use benchmark. Tests ability to operate desktop environments.
- **[Tau-bench](https://github.com/sierra-research/tau-bench)** : Real-world agent tasks across airline and retail domains.
- **[ToolBench](https://github.com/OpenBMB/ToolBench)** : API tool usage across 16,000+ real-world APIs.
- **[AgentBench](https://github.com/THUDM/AgentBench)** : Multi-dimensional agent benchmark across 8 environments.

## Safety and Alignment

Benchmarks and tools for evaluating harmful outputs, bias, and safety properties.

- **[HELM](https://crfm.stanford.edu/helm/)** : Stanford's holistic evaluation including toxicity, bias, and fairness.
- **[TruthfulQA](https://github.com/sylinrl/TruthfulQA)** : Tests whether models generate truthful answers vs. common misconceptions.
- **[BBQ](https://github.com/nyu-mll/BBQ)** : Bias Benchmark for QA across 9 social categories.
- **[RealToxicityPrompts](https://allenai.org/data/real-toxicity-prompts)** : 100K prompts for measuring toxic generation risk.
- **[WildGuard](https://github.com/allenai/wildguard)** : Safety classification benchmark for identifying harmful requests and responses.

## Instruction Following

Benchmarks testing how precisely models follow complex instructions.

- **[IF-Evals](https://github.com/google-research/google-research/tree/master/instruction_following_eval)** : Google's instruction following evaluation. Tests constraint adherence across formatting, length, content requirements.
- **[MT-Bench](https://huggingface.co/spaces/lmsys/mt-bench)** : Multi-turn conversation benchmark with human preference alignment.
- **[AlpacaEval](https://github.com/tatsu-lab/alpaca_eval)** : Automated evaluation of instruction-following using LLM judges.
- **[Arena Hard](https://github.com/lm-sys/arena-hard-auto)** : Automated version of Chatbot Arena using challenging real-world queries.

## Multimodal Benchmarks

Benchmarks for vision, audio, and multi-modal capabilities.

- **[MMMU](https://mmmu-benchmark.github.io)** : Massive multi-discipline multimodal understanding. College-level visual reasoning.
- **[MathVista](https://mathvista.github.io)** : Mathematical reasoning with visual context.
- **[RealWorldQA](https://huggingface.co/datasets/xai-org/RealWorldQA)** : Real-world image understanding questions.

## Evaluation Frameworks

Open-source tools for building and running your own evaluations.

- **[LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness)** : EleutherAI's standardized evaluation framework. Supports 200+ tasks.
- **[OpenAI Evals](https://github.com/openai/evals)** : OpenAI's evaluation framework for LLMs.
- **[promptfoo](https://github.com/promptfoo/promptfoo)** : Test and evaluate LLM outputs. CI/CD integration.
- **[DeepEval](https://github.com/confident-ai/deepeval)** : Unit testing framework for LLMs with 14+ evaluation metrics.
- **[ragas](https://github.com/explodinggradients/ragas)** : Evaluation framework focused on RAG pipelines.
- **[Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)** : UK AISI's evaluation framework for AI safety.

## LLM-as-Judge

Research and tools for using LLMs to evaluate other LLMs.

- **[Judging LLM-as-a-Judge](https://arxiv.org/abs/2306.05685)** : Foundational paper on using LLMs as evaluators. Documents position bias, verbosity bias, and self-enhancement bias.
- **[Agent-as-Judge](https://arxiv.org/abs/2410.10934)** : Judges that read execution traces, not just outputs. >90% agreement with human experts vs. ~70% for standard LLM-as-Judge.
- **[GEPA (Generative EPA)](https://arxiv.org/abs/2504.01495)** : Judge optimization framework. Closes human-judge agreement gap by 10% average.
- **[PandaLM](https://github.com/WeOpenML/PandaLM)** : Automated LLM evaluation with reference-free judgment.
- **[JudgeLM](https://github.com/baaivision/JudgeLM)** : Fine-tuned models for scalable LLM evaluation.

## Datasets and Data Tools

Resources for building custom evaluation datasets.

- **[Hugging Face Datasets](https://huggingface.co/datasets)** : Largest collection of ML datasets. Filter by task type for evaluation sets.
- **[LMSYS Chatbot Arena](https://chat.lmsys.org)** : Crowdsourced human preference data from 1M+ pairwise comparisons.
- **[Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard)** : Hugging Face's aggregated benchmark results.
- **[Artificial Analysis](https://artificialanalysis.ai)** : Model comparison across price, speed, and quality dimensions.

## Research Papers

Key papers on LLM evaluation methodology.

- [Holistic Evaluation of Language Models (HELM)](https://arxiv.org/abs/2211.09110) : Stanford's comprehensive evaluation framework paper
- [Chatbot Arena: An Open Platform for Evaluating LLMs](https://arxiv.org/abs/2403.04132) : The Elo-based crowdsourced evaluation methodology
- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) : Position bias, verbosity bias, self-enhancement bias analysis
- [Can LLMs Follow Simple Rules?](https://arxiv.org/abs/2311.04235) : Instruction following evaluation methodology
- [Agents of Chaos](https://arxiv.org/abs/2502.17407) : Multi-agent failure modes (124 internal emails with PII, circular loops, false completion reports)

## Blog Posts and Articles

Practical writing on LLM evaluation.

- [The Rise of Judgment Engineering](https://github.com/jakemeany523/judgment-engineering) : Why evaluation must generate, judge, and learn (not just score outputs)
- [Evaluation is All You Need](https://www.anthropic.com/research/evaluations) : Anthropic's perspective on evaluation-driven development
- [A Survey on Evaluation of Large Language Models](https://arxiv.org/abs/2307.03109) : Comprehensive survey of evaluation methods

## Community

- **[LMArena (Chatbot Arena)](https://lmarena.ai)** : Live crowdsourced model comparison
- **[r/LocalLLaMA](https://reddit.com/r/LocalLLaMA)** : Active community for LLM discussion and evaluation
- **[r/MachineLearning](https://reddit.com/r/MachineLearning)** : Academic ML community with benchmark discussions
- **[Hugging Face Discord](https://huggingface.co/join/discord)** : Evaluation-focused channels

---

## Contributing

Found a tool, benchmark, or paper that should be here? Open a PR. Requirements:

- Must be publicly available (open-source preferred)
- Include a one-line description of what it does
- Place it in the correct category

## Maintainer

Built by [Jake Meany](https://github.com/jakemeany523) at [LayerLens](https://layerlens.com). I work at the intersection of AI evaluation and marketing, and maintain several related projects:

- **[JakeOS](https://github.com/jakemeany523/jake-os)** : AI-augmented operating system for solo marketing
- **[AI Marketing Skills](https://github.com/jakemeany523/ai-marketing-skills)** : Production-tested skill library for AI agents
- **[DevPulse](https://github.com/jakemeany523/devpulse)** : Developer community research tool
- **[Judgment Engineering](https://github.com/jakemeany523/judgment-engineering)** : AI evaluation methodology

## License

CC0 1.0 Universal
