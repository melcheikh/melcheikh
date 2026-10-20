# Martín el Cheikh

I work with coding agents: I diagnose, verify on real hardware, and decide what gets sent upstream. My background is psychology (UBA) and twelve years in regulated pharmaceutical operations, so I care less about whether a number moved than about whether it measures what it says it measures.

### Merged upstream

- **[inspect_scout #679](https://github.com/meridianlabs-ai/inspect_scout/pull/679)** (Meridian Labs). The eval_awareness example rubric counted topic vocabulary such as "test" or "scenario" as evaluation awareness. I rewrote the definition around the model's stance toward its own situation and measured it against human labels and 400 real transcripts. With Gemini 3.1 Pro as judge, false flags on topical replies went from 32 of 200 to 0 with detection unchanged. Merged October 2026, closing issue #356.
- **[inspect_ai #5462](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5462)** (UK AISI). Quoted comma-separated values passed through `--env` were split into lists and corrupted environment variables. Merged September 2026.
- **[inspect_evals #2390](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2390)** (UK AISI). mind2web_sc loaded a subset of its 200 samples and reused sample ids. Merged September 2026.
- **[vLLM #48956](https://github.com/vllm-project/vllm/pull/48956)**. Fall back to native sampling when FlashInfer cannot target the GPU, found running on a consumer Blackwell card. Merged September 2026.
- **[Cap #2511](https://github.com/CapSoftware/Cap/pull/2511)**, **[omi #20744](https://github.com/BasedHardware/omi/pull/20744)** and **[local-ai-registry #293](https://github.com/sybil-solutions/local-ai-registry/pull/293)**: a tray stop fallback, a 409 handled on knowledge graph rebuild, and a validated RTX 5090 Laptop entry with four measured recipes.

### In review

- **inspect_evals**: judges whose parsing or failure handling biases the reported score.
  - [#2283](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2283) sycophancy reads any "y" in the judge's prose as a verdict.
  - [#2286](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2286) sciknoweval turns grader failures into fabricated grades.
  - [#2396](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2396) makemesay judge verdict parsing.
  - [#2438](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2438) agentharm refusal judge errors scored as results.
  - [#2471](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2471) agent_threat_bench false security failures.
- **Elsewhere**:
  - [vLLM #55651](https://github.com/vllm-project/vllm/pull/55651)
  - [supabase/auth #2802](https://github.com/supabase/auth/pull/2802)
  - [tscircuit/cli #5315](https://github.com/tscircuit/cli/pull/5315)
  - [Cap #2700](https://github.com/CapSoftware/Cap/pull/2700)
- **Research issue**: [inspect_petri #174](https://github.com/meridianlabs-ai/inspect_petri/issues/174) shows that the auditor's stance changes how often clean models confess to hidden behavior.

### Models

NVFP4 quantizations of Gemma 4 31B for Blackwell on [Hugging Face](https://huggingface.co/melcheikh), with more than 330,000 downloads as counted by the Hub.

### Background

Psychology at UBA, in progress. Twelve years at Roemmers in pharmaceutical logistics and operations under GMP. Buenos Aires.
