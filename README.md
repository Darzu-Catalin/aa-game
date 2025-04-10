# OK Boomerang – Iterated Prisoner’s Dilemma Strategy

## How it works (quick overview)

1. **Opens with cooperation.**
2. Keeps a **sliding window** (≈10 % of total rounds, 1–20 moves) of the opponent’s last actions.
3. Computes the opponent’s **defection ratio** (`dr`) in that window.  
   * `dr ≤ 30 %` → cooperate  
   * `dr ≥ 70 %` → defect  
   * otherwise copy the opponent’s last move, but if both defected last round and overall `dr < 50 %`, forgive and cooperate.
4. In Stage 2 it **chooses the next opponent** with the highest long‑term cooperation ratio, skipping anyone already played 200 times.

The strategy is **deterministic, uses no external libraries, never defects first** → classified as **neat**.

## Why “OK Boomerang”?

Defections “come back” to the opponent like a boomerang—but only after repeated misuse, and the boomerang can be caught and reset through cooperation.

## Author & contact

* **Catalin Darzu**, FAF‑231 
* **E‑mail:** catalin.darzu@isa.utm.md
