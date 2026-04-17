# MorphoGenesis Lab — SPEC

## Concept
An interactive laboratory for exploring biological pattern formation through two complementary computational lenses:
1. **Classic Reaction-Diffusion** (Gray-Scott model) — Alan Turing's 1952 morphogenesis theory, GPU-accelerated via WebGL
2. **Neural Cellular Automata (NCA)** — Modern differentiable self-organizing systems that learn to grow patterns

Users can create leopard spots, zebrafish stripes, coral growth, and labyrinthine patterns in real-time, then watch Neural Cellular Automata learn to reproduce and regenerate those patterns from scratch.

## Why This Matters (April 2026)
- BraiNCA paper (April 2026) advancing NCA for motor control & morphogenesis
- ALICE 2026 workshop exploring artificial life + NCA
- CRISPR breakthroughs trending on HN — biology + computation intersection is hot
- Unique niche: NO existing webapp combines reaction-diffusion + NCA interactively

## Features

### Tab 1: Reaction-Diffusion Engine
- Gray-Scott model running on GPU via WebGL fragment shaders
- Real-time parameter controls: Feed rate (F), Kill rate (k), Diffusion rates (Du, Dk)
- Click/drag to seed chemical concentrations
- 12+ biological presets (mitosis, coral, maze, spots, stripes, waves, worms)
- Speed control (steps per frame)
- Resolution control (256x256 to 1024x1024)

### Tab 2: Phase Diagram Explorer
- 2D interactive heatmap of F vs k parameter space
- Click any point to see the pattern it produces
- Color-coded regions (extinction, spots, stripes, chaos, etc.)
- Animated transitions between parameter regimes

### Tab 3: Neural Cellular Automata
- Train NCA to grow a target pattern from a single seed cell
- Visualize training progress (loss curve, intermediate states)
- Demonstrate self-repair: damage the grown pattern and watch it regenerate
- Architecture visualization showing the local update rule
- Compare NCA-grown vs reaction-diffusion patterns

### Tab 4: Perturbation Lab
- Apply perturbations to running simulations: cut, inject, erase, barrier
- Watch self-healing and pattern reorganization
- Measure recovery time and structural stability
- Side-by-side comparison of perturbation responses

### Tab 5: Mathematical Foundations
- Interactive PDE visualization: du/dt = Du∇²u - uv² + F(1-u)
- Animated explanation of diffusion, reaction, and feeding terms
- Turing instability analysis with dispersion relation plots
- Connection to real biological morphogens (Shh, BMP, Wnt)

## Tech Stack
- Single HTML file with embedded JS + WebGL shaders
- WebGL 2.0 for GPU-accelerated reaction-diffusion
- TensorFlow.js for NCA training
- Canvas 2D for charts and phase diagrams
- No external dependencies except TF.js CDN
- Vercel deployment with cleanUrls

## Architecture
```
index.html
├── WebGL Shaders (Gray-Scott compute + render)
├── NCA Module (TF.js model definition + training loop)
├── Phase Diagram Generator (pre-computed + interactive)
├── Perturbation System (mouse interaction + barrier placement)
├── Math Visualizations (animated PDE terms)
└── UI Framework (tab system, controls, presets)
```

## Scoring
| Criterion | Weight | Score | Weighted |
|-----------|--------|-------|----------|
| Novelty | 3x | 9 | 27 |
| Feasibility | 3x | 8 | 24 |
| Wow Factor | 2x | 10 | 20 |
| Learning Value | 2x | 9 | 18 |
| Utility | 1x | 7 | 7 |
| **Total** | | | **96/110** |
