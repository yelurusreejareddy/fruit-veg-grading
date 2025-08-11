# Fruit & Veg Grading (Classical imageprocessing, A/B)

A small, fast image processing pipeline that grades produce freshness into **two classes**:
- **A** = good  
- **B** = bad
Color + texture features + a light classifier (k-NN / SVM).

---

## Repo contents

- [`projectcode.ipynb`](projectcode.ipynb) — end-to-end notebook (load → features → model → eval → predict)
- [`dataset/`](dataset/) — sample images organized by class  
  - `Mango__good`, `Mango__bad`, `lemon__good`, `lemon__bad`
- [Short paper](Sreeja%20Reddy,%20Yeluru%20final%20paper.pdf) — PDF with method and results
- `README.md` — this file
- `LICENSE` — MIT

---

## Quick start

# Open the notebook
jupyter notebook projectcode.ipynb

## Expected data layout
dataset/
- Mango__good/
- Mango__bad/
- lemon__good/
- lemon__bad/

Add your own fruit the same way, e.g. apple__good, apple__bad.
