# Martín el Cheikh

I work with coding agents: I diagnose, verify on real hardware, and decide what gets sent upstream. My background is psychology (UBA) and twelve years in regulated pharmaceutical operations, so I care less about whether a number moved than about whether it measures what it says it measures.

### Merged upstream

- **[FlashInfer #7746](https://github.com/flashinfer-ai/flashinfer/pull/7746)**. The CuTe-DSL `bf16_fp4` split-K gate normalized wave count by `sm_count` instead of CTA slots (`sm_count * occupancy`), keeping multi-split tactics active on `occ=2` prefill shapes on SM120. Fixing it cut prefill split-K buffer allocations on an RTX 5090 (`M=2048, N=12288`: 1595 MiB to 361 MiB allocated; 3720 MiB to 1008 MiB reserved). Merged November 2026.
- **[supabase/auth #2802](https://github.com/supabase/auth/pull/2802)**. Excluded OAuth client sessions from MFA step-up invalidation (#2801). Merged November 2026.
- **[inspect_scout #679](https://github.com/meridianlabs-ai/inspect_scout/pull/679)** (Meridian Labs). The eval_awareness example rubric counted topic vocabulary such as "test" or "scenario" as evaluation awareness. I rewrote the definition around the model's stance toward its own situation and measured it against human labels and 400 real transcripts. With Gemini 3.1 Pro as judge, false flags on topical replies went from 32 of 200 to 0 with detection unchanged. Merged October 2026, closing issue #356.
- **[inspect_ai #5462](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5462)** (UK AISI). Quoted comma-separated values passed through `--env` were split into lists and corrupted environment variables. Merged September 2026.
- **[inspect_evals #2390](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2390)** (UK AISI). mind2web_sc loaded a subset of its 200 samples and reused sample ids. Merged September 2026.
- **[vLLM #48956](https://github.com/vllm-project/vllm/pull/48956)**. Fall back to native sampling when FlashInfer cannot target the GPU, found running on a consumer Blackwell card. Merged September 2026.
- **[Cap #2511](https://github.com/CapSoftware/Cap/pull/2511)**, **[omi #20744](https://github.com/BasedHardware/omi/pull/20744)** and **[local-ai-registry #293](https://github.com/sybil-solutions/local-ai-registry/pull/293)**: a tray stop fallback, a 409 handled on knowledge graph rebuild, and a validated RTX 5090 Laptop entry with four measured recipes.

### In review & approved

- **GPU inference and speculative decoding**:
  - [vLLM #55651](https://github.com/vllm-project/vllm/pull/55651) skip FlashInfer CUTLASS kernels when the local CUDA toolkit cannot JIT-compile for the GPU.
  - [stecasta/vllm#9](https://github.com/stecasta/vllm/pull/9) logit soft-capping support in `DraftVocab` (verified with `google/gemma-4-E2B-it` on RTX 5090).
  - [vllm-project/humming#214](https://github.com/vllm-project/humming/pull/214) bound Stream-K lock validation by merged wave.
- **inspect_evals**: judges whose parsing or failure handling biases the reported score.
  - [#2286](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2286) sciknoweval turns grader failures into fabricated grades (Approved by MattFisher).
  - [#2283](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2283) sycophancy reads any "y" in the judge's prose as a verdict.
  - [#2396](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2396) makemesay judge verdict parsing.
  - [#2438](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2438) agentharm refusal judge errors scored as results.
  - [#2471](https://github.com/UKGovernmentBEIS/inspect_evals/pull/2471) agent_threat_bench false security failures.
- **supabase/auth**: [#2894](https://github.com/supabase/auth/pull/2894) (RFC 8707 resource indicators), [#2895](https://github.com/supabase/auth/pull/2895) (Client ID Metadata Documents), and [#2897](https://github.com/supabase/auth/pull/2897) (request-bounded notification emails).
- **Research & hardware audits**:
  - [inspect_petri #174](https://github.com/meridianlabs-ai/inspect_petri/issues/174) shows that the auditor's stance changes how often clean models confess to hidden behavior.
  - [vLLM #52916](https://github.com/vllm-project/vllm/issues/52916#issuecomment-6937157965) hardware validation of Intel `WAITPKG` (`umonitor`/`umwait`) + ZMQ `SNDHWM=1` wakeup drops on Core Ultra 9 275HX + RTX 5090.

### Models & Verification

- **Hugging Face**: NVFP4 quantizations of Gemma 4 31B for Blackwell on [Hugging Face](https://huggingface.co/melcheikh), with more than 780,000 downloads as counted by the Hub.
- **YC Paxel**: [Audit Report](https://paxel.ycombinator.com/results/ybxjxk4r) analyzing 439 engineering sessions across 14 repositories, certifying deep focus, high-velocity coding with agents, and rigorous testing discipline.

### Background

Psychology at UBA, in progress. Twelve years at Roemmers in pharmaceutical logistics and operations under GMP. Buenos Aires.
