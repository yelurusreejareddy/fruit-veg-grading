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

```bash
## (optional) new virtual env
python -m venv .venv && source .venv/bin/activate   # macOS/Linux
# .venv\Scripts\activate                             # Windows

pip install -U pip
pip install numpy opencv-python scikit-image scikit-learn matplotlib tqdm jupyter

# open the notebook
jupyter notebook projectcode.ipynb
---
