# Safe Multi-Agent Reinforcement Learning for Persistent Surveillance

**MADDPG agents wrapped with control barrier functions so battery-driven agents never enter unsafe, unrecoverable states during long-duration surveillance.**

📄 [**Report — view in browser**](https://docs.google.com/viewer?url=https%3A%2F%2Fraw.githubusercontent.com%2FLokesh97Bansal%2FSafe-Learning-MADDPG-with-Barrier-Certification%2Fmain%2FReport.pdf) · 🎞 [**Slides — view in browser**](https://docs.google.com/viewer?url=https%3A%2F%2Fraw.githubusercontent.com%2FLokesh97Bansal%2FSafe-Learning-MADDPG-with-Barrier-Certification%2Fmain%2FSlides.pdf) · 🎬 [Full-quality video (MP4)](./video.mp4) · [PPTX](./PPT.pptx)

![Demo](./preview.gif)

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
