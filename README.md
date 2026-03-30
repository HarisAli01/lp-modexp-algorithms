# Advanced Algorithms Visualization Tool

Single-file interactive teaching tool for BSD 404 - Algorithms II.

The full application is implemented in `index.html` and runs offline with no external dependencies.

## Project Scope (CLO Coverage)

1. Part 1 (CLO-1): Linear Programming - Simplex Method
2. Part 2 (CLO-2): FFT / DFT Visualization
3. Part 3 (CLO-3): Modular Exponentiation + RSA Cryptosystem Lab

## Current UI Structure

- Homepage landing screen with cards for Part 1, Part 2, and Part 3
- Top tab selector for switching parts
- Home button to return to the landing screen
- Two-column layout on desktop (controls + visualization)
- Responsive layout under 980px
- Dark, readability-focused theme with per-part accent colors

## Shared Features in All Parts

- Control panel and visualization panel
- Playback controls in order: Build Steps, Step, Play, Pause, Reset
- Speed slider (0.25x to 4x)
- Step counter and status display (Idle, Ready, Playing, Paused, Done)
- Pseudocode with line highlighting and hover tooltips
- Plain-language step explanation box
- Scrollable history table with clickable rows (jump to step)
- Color legend near visualization
- Learning Objectives block in each part (placed below Key Insight)
- Collapsible educational sections:
  - Algorithm overview
  - Key concepts
  - Worked example
  - Lecture notes / roadmap

## Part 1 - Simplex Method

- Custom LP input: objective, constraints, bounds
- Pivot rule selection (largest coefficient / Bland's rule)
- Explicit problem-formulation section (input/output/objective/constraints/when to use and when not)
- Preset cases:
  - Basic feasible LP
  - Unbounded
  - Infeasible
  - Degenerate
- Stepwise tableau updates with pivot explanations
- 2D feasible-region drawing with:
  - Constraint lines
  - Feasible polygon
  - Current and visited simplex vertices
  - Vertex-to-vertex path
- Dual problem section with strong duality verification output

## Part 2 - FFT / DFT

- Preset sizes: N = 4, 8, 16
- Custom input signal
- Time-domain and frequency-domain views side by side
- DFT matrix view with phase-based coloring
- Cooley-Tukey decomposition stages (even/odd split and butterfly flow)
- Inverse reconstruction display
- Naive DFT vs FFT comparison:
  - Operation counts
  - Measured runtime
  - Numerical difference check
- Explicit recurrence/complexity explanation: T(n) = 2T(n/2) + O(n)
- Practical vs theoretical speedup discussion
- Dedicated "Complexity & Application Depth (CLO-2)" learning section

## Part 3 - Modular Exponentiation + RSA Lab

- Custom inputs: base, exponent, modulus
- Both variants:
  - Left-to-right
  - Right-to-left
- Binary exponent visualization with active-bit pointer
- Stepwise square / conditional multiply flow
- Live result updates
- Statistics:
  - Modular multiplication count
  - Bit length
- Preset examples including RSA-style example
- RSA cryptosystem lab:
  - Key generation from p, q, e (plus auto-key generation by bit size)
  - Encryption c = m^e mod n
  - Decryption m = c^d mod n
  - RSA status panel and generated key table (n, phi, e, d)
  - Correctness test suite across multiple messages
  - Number-theoretic checks: gcd(e, phi)=1 and e*d mod phi = 1
  - Security/efficiency notes and attack assumptions
- Dedicated "Cryptosystem Development & Testing (CLO-3)" learning section

## Tech Constraints

- HTML5
- CSS3
- Vanilla JavaScript (ES6+)
- SVG for visual rendering
- No external libraries or frameworks

## How to Run

### Option 1: Direct open

1. Open `index.html` in a modern browser.

### Option 2: Local server in VS Code

1. Open this folder in VS Code.
2. Start a static file server (for example Live Server).
3. Open `index.html`.

## File Structure

- `index.html`: complete app (HTML + CSS + JavaScript)
- `README.md`: project documentation