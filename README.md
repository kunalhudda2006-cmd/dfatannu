# DFA Minimizer — Automata Simplification Engine

A gorgeous dark-themed, fully interactive DFA Minimization Visualizer built with vanilla HTML/CSS/JS.

## Features

- **Hopcroft's Algorithm** — Full step-by-step partition refinement
- **Graph Visualization** — SVG-rendered DFA with animated state groupings
- **Partition Steps** — Color-coded group evolution across iterations
- **Transition Table** — Side-by-side original vs minimized DFA tables
- **Equivalence Table** — Visual matrix of distinguishable/equivalent states
- **Result Summary** — Before/after comparison with merged state details
- **4 Built-in Presets** — Load example DFAs instantly
- **Export** — Download minimized DFA definition as text

## Deployment

### Vercel (Recommended)
```bash
npx vercel --prod
```

### Local
```bash
npx serve .
# or
python3 -m http.server 3000
```

## How It Works

1. Input your DFA: states, alphabet, initial/accepting states, transitions
2. Click **Run Minimization**
3. Navigate through steps using the stepper in Graph View
4. Explore Partition Steps to see each refinement iteration
5. Check the Equivalence Table to understand which states merged
6. View the Result for the final minimized DFA

## Algorithm

Uses **Hopcroft's partition refinement algorithm**:
1. Initial partition: accepting vs non-accepting states
2. Iteratively split groups based on transition targets
3. Stop when no more splits are possible
4. Build minimized DFA from final partition

## Input Format

- **States**: comma-separated (e.g., `q0, q1, q2`)
- **Alphabet**: comma-separated (e.g., `a, b`)
- **Transitions**: one per line, format `state,symbol→nextState`

## Tech Stack

- Pure HTML5 / CSS3 / Vanilla JavaScript
- SVG graph rendering (no dependencies)
- Google Fonts: Syne + Space Mono
