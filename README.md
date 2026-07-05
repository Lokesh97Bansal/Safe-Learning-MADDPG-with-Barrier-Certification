# Safe Multi-Agent Reinforcement Learning for Persistent Surveillance

**MADDPG agents wrapped with control barrier functions so battery-driven agents never enter unsafe, unrecoverable states during long-duration surveillance.**

▶ [**Watch the demo video**](./video.mp4) · 📄 [**Project report (PDF)**](./Report.pdf) · 🎞 [**Slides (PPTX)**](./PPT.pptx)

![Result](./featured.PNG)

## Overview
A reinforcement-learning agent tasked with long-duration ground surveillance can learn policies that drive it into states it cannot recover from — the canonical example being **battery die-out** far from a charging point. This project combines **multi-agent deep deterministic policy gradient (MADDPG)** with **control barrier functions (CBFs)** so that exploration and the learned policy are both constrained away from unsafe, unrecoverable regions of the state space, while surveillance performance is preserved.

## Method
- MADDPG for cooperative multi-agent surveillance policies.
- Control barrier functions as a safety layer: actions are filtered so barrier conditions on battery/state constraints are never violated.
- Long-horizon episodes evaluating persistent coverage under the safety constraint.

## Result
- Safe surveillance executed across full episodes with **zero entries into the unsafe (battery-die-out) region**, versus unconstrained MADDPG baselines that fail.

## Context
Graduate research project, Robotics & Autonomous Systems, **IISc Bengaluru** (Jan–Apr 2022).
