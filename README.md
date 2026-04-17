# MorphoGenesis Lab

Interactive Reaction-Diffusion & Neural Cellular Automata Laboratory

Explore biological pattern formation through two complementary computational lenses: Alan Turing's 1952 reaction-diffusion theory (GPU-accelerated via WebGL) and modern Neural Cellular Automata that learn to grow and self-repair patterns.

## Features

### Reaction-Diffusion Engine
- Gray-Scott model running on GPU via WebGL 2.0 fragment shaders
- Real-time parameter controls (Feed rate, Kill rate, Diffusion rates)
- Click/drag to seed chemical concentrations
- 12 biological presets: Mitosis, Coral, Maze, Spots, Stripes, Worms, Bubbles, Waves, Spirals, Fingerprint, Solitons, Chaos

### Phase Diagram Explorer
- Interactive 2D heatmap of the F vs k parameter space
- Click any point to preview the pattern it produces
- Color-coded regions (extinction, spots, stripes, chaos, etc.)
- Apply parameters directly to the main simulation

### Neural Cellular Automata
- Train NCA in-browser with TensorFlow.js
- Watch patterns grow from a single seed cell
- Demonstrate self-repair: damage grown patterns and watch regeneration
- Multiple target shapes: Circle, Ring, Cross, Diamond, Gecko, Star
- Real-time loss curve visualization

### Perturbation Lab
- 5 perturbation tools: Seed, Erase, Barrier, Cut, Bomb
- Watch reaction-diffusion systems self-organize after damage
- Explore structural stability of different pattern types

### Mathematical Foundations
- Interactive PDE visualization
- Turing instability analysis
- Connection to real biology (zebrafish, leopards, coral, digit formation)

## Tech Stack

- WebGL 2.0 for GPU-accelerated simulation
- TensorFlow.js for Neural Cellular Automata
- Vanilla JS + HTML + CSS (no build step)
- Single-file architecture

## References

- Turing, A.M. (1952). "The Chemical Basis of Morphogenesis"
- Pearson, J.E. (1993). "Complex Patterns in a Simple System"
- Mordvintsev et al. (2020). "Growing Neural Cellular Automata"
- Mordvintsev et al. (2026). "BraiNCA: Brain-inspired NCA"

## License

MIT

Built by [Surya Midde](https://github.com/middesurya)
