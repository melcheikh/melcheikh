# Martín el Cheikh

AI engineer working on model evaluation and behavior. I come from psychology (UBA), and that is the lens I bring to how models are measured, not just whether they run.

### What I'm working on

- **Evals.** I send measurement-validity fixes to [inspect_evals](https://github.com/UKGovernmentBEIS/inspect_evals) (UK AI Safety Institute): a grader failure counted as a real score instead of a missing value, a verdict parsed wrong, quietly biasing what the eval reports. [My PRs](https://github.com/UKGovernmentBEIS/inspect_evals/pulls?q=author%3Amelcheikh).

- **Inference.** I send fixes to [vLLM](https://github.com/vllm-project/vllm). I run models on consumer Blackwell (RTX 5090, SM120, NVFP4) and chase failures the project's CI does not cover. [My PRs](https://github.com/vllm-project/vllm/pulls?q=author%3Amelcheikh).

- **Models.** NVFP4 quantizations of Gemma 4 on [Hugging Face](https://huggingface.co/melcheikh).

### The angle

Most evals are written without experimental design: no control condition, no construct validity, no measure of uncertainty. A judge model that refuses the worst transcripts, or a scorer that reports zero when it measured nothing, makes a model look safer than it is. That gap, between "the number moved" and "the number means something", is where I work.

### Background

Psychology (UBA, in progress). Autodidact in AI since 2024. Buenos Aires.
