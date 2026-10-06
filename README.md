# ml-first-principles

Build neural networks and computer vision from scratch, then ship two perception projects in their own repos.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python -c "import torch; print(torch.__version__, torch.backends.mps.is_available())"
```

PyTorch should report `True` for MPS on the M4 Pro. Jupyter:

```bash
python -m ipykernel install --user --name ml-first-principles --display-name "ml-first-principles"
jupyter lab
```

## How a session works

Each lesson folder has three files:

- `lesson.ipynb` is the working session
- `lesson.py` is the clean version, written after the notebook works
- `NOTES.md` is what you built, what broke, and what clicked

Commit at the end of the session, with a message about what you learned. A lesson is done when the code is committed and you can explain it with the laptop closed.

Project 1 (winter) and Project 2 (spring) get their own repos. This repo keeps the trunk: math notes, Karpathy, Kalman, and the CV curriculum.

## Progress

| Phase | What | Target | Status |
| --- | --- | --- | --- |
| 0 · Math | 3Blue1Brown and a short probability block | ~Oct 23, 2026 | not started |
| 1 · Karpathy | micrograd through a GPT you can explain. GPT-2 can slip into winter | mid-Dec 2026 | not started |
| 2 · Winter sprint | Project 1, its own repo: detect-and-track, tracker written by hand | mid-Jan 2027 | not started |
| 3 · CV + Kalman | Nayar, CS231n, then EKF / visual odometry | Feb–Apr 2027 | not started |
| 4 · Capstone | Project 2, its own repo | May 2027 | not started |

## Map

### `math/`

| Folder | Lesson |
| --- | --- |
| `01-linear-algebra` | 3Blue1Brown, Essence of Linear Algebra |
| `02-calculus` | 3Blue1Brown, Essence of Calculus |
| `03-neural-networks` | 3Blue1Brown, Neural Networks (backprop, transformers, attention) |
| `04-cross-entropy` | 3Blue1Brown, cross-entropy |
| `05-probability` | Bayes, Gaussians, maximum likelihood, expectation and variance |

### `karpathy/`

| Folder | Lesson |
| --- | --- |
| `01-micrograd` | Backprop from scratch |
| `02-makemore-bigram` | Bigram language model |
| `03-makemore-mlp` | MLP |
| `04-makemore-batchnorm` | Activations, gradients, batch norm |
| `05-makemore-backprop-ninja` | Manual backprop |
| `06-makemore-wavenet` | WaveNet |
| `07-gpt` | GPT from scratch |
| `08-tokenizer` | GPT tokenizer |
| `09-gpt2` | Reproduce GPT-2 (124M), scaled down or on a rented GPU |

### `kalman/`

| Folder | Lesson |
| --- | --- |
| `01-through-multivariate` | Labbe chapters 1–8, before the winter tracker |
| `02-ekf-ukf` | Labbe chapters 9–12 |

### `cv/`

| Folder | Lesson |
| --- | --- |
| `01-camera-and-imaging` | First Principles of Computer Vision, module 1 |
| `02-features-and-boundaries` | Module 2 |
| `03-3d-reconstruction` | Modules 3–4 |
| `04-cs231n` | Stanford CS231n, Spring 2025 lectures |
| `05-cs231n-assignments` | CS231n assignments |
| `06-hf-cv-course` | Hugging Face Community Computer Vision Course |
| `07-visual-odometry` | Visual odometry and state estimation |

### `stretch/`

| Folder | Lesson |
| --- | --- |
| `01-lerobot` | Hugging Face Robotics course / LeRobot |
| `02-nanochat` | Karpathy's end-to-end chat pipeline |

## Highlights

Nothing shipped yet. This section grows when a milestone lands: GPT from scratch, then the two projects.

## Credits

The explanations and assignments come from other people. The code in this repo is written from scratch, not forked.

- [Andrej Karpathy, Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero)
- [3Blue1Brown](https://www.3blue1brown.com/)
- [Stanford CS231n](https://cs231n.stanford.edu/)
- [Shree Nayar, First Principles of Computer Vision](https://fpcv.cs.columbia.edu/)
- [Roger Labbe, Kalman and Bayesian Filters in Python](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)
- [Hugging Face Community Computer Vision Course](https://huggingface.co/learn/computer-vision-course)
