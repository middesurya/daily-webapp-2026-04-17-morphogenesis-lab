# BUILD REPORT — MorphoGenesis Lab
**Date:** 2026-04-17
**Build Time:** ~15 minutes
**Status:** DEPLOYED

## Links
- **Live:** https://morphogenesis-lab.vercel.app
- **GitHub:** https://github.com/middesurya/daily-webapp-2026-04-17-morphogenesis-lab

## Idea Selection
Analyzed 50+ existing repos on github.com/middesurya. Existing projects heavily cover ML theory visualization (superposition, grokking, MoE, speculative decoding, test-time compute, neuro-symbolic, Hopfield, chaos theory).

Chose to venture into computational biology + AI intersection — a completely new domain. Selected **Reaction-Diffusion + Neural Cellular Automata** because:
1. BraiNCA paper (April 2026) and ALICE workshop make NCA research hot right now
2. CRISPR trending on HN front page (217 points)
3. Zero overlap with existing repos
4. Visually spectacular and scientifically deep

## Architecture
- Single HTML file with embedded JS + WebGL 2.0 shaders
- Dual WebGL contexts (main simulation + perturbation lab)
- Gray-Scott reaction-diffusion on GPU via fragment shaders
- TensorFlow.js for Neural Cellular Automata training
- CPU fallback for phase diagram preview rendering

## Features Built
1. **Reaction-Diffusion Engine** — 512x512 WebGL GPU simulation with 12 biological presets
2. **Phase Diagram Explorer** — Interactive F vs k parameter space with live preview
3. **Neural Cellular Automata** — In-browser training, growth, damage & regeneration
4. **Perturbation Lab** — 5 tools (seed, erase, barrier, cut, bomb) for self-organization experiments
5. **Mathematical Foundations** — PDE explanations, Turing instability, biological connections

## Patterns Learned
- WebGL 2.0 ping-pong FBO technique for GPU compute shaders
- Float textures require EXT_color_buffer_float extension
- TF.js NCA training needs careful memory management (tf.tidy + manual dispose)
- Dual WebGL contexts work but each needs its own shader compilation pipeline
- Gray-Scott parameter space classification is approximate but visually useful

## Scoring
| Criterion | Weight | Score | Weighted |
|-----------|--------|-------|----------|
| Novelty | 3x | 9 | 27 |
| Feasibility | 3x | 8 | 24 |
| Wow Factor | 2x | 10 | 20 |
| Learning Value | 2x | 9 | 18 |
| Utility | 1x | 7 | 7 |
| **Total** | | | **96/110** |
