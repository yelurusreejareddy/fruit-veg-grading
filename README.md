# Fruit & Veg Grading (Classical imageprocessing, A/B)

A small, fast image processing pipeline that grades produce freshness into **two classes**:
- **A** = good  
- **B** = bad
using color, texture, and edge features with a lightweight classifier.

---

## Repo contents

- [`fruit_veg_grading_cv.ipynb`](fruit_veg_grading_cv.ipynb) — end-to-end notebook (load -> features -> model -> eval -> predict)
- [`dataset/`](dataset/) — sample images organized by class  
  - `Mango__good`, `Mango__bad`, `lemon__good`, `lemon__bad`
- project_report.pdf - PDF with method and results
- `README.md` - this file
- `LICENSE` - MIT

---

## Quick start

## Open the notebook
jupyter notebook projectcode.ipynb

## Expected data layout
dataset/
- Mango__good/
- Mango__bad/
- lemon__good/
- lemon__bad/

Add your own fruit the same way, e.g. apple__good, apple__bad.

## How it works (short)
- Load image and convert to HSV (stable color space for produce).
- Color features — compact HSV histograms / masks to capture ripeness + discoloration.
- Texture features — edge/entropy or simple local patterns to catch bruising/shriveling.
- Classifier — small k-NN or SVM.
- Metrics — accuracy, precision/recall/F1, confusion matrix.
- Predict — pass a path -> get A or B.

## Reproduce (inside the notebook)
- Set DATA_DIR = "dataset" (or your path).
- Run Pre-processing cells (resize if needed, HSV conversion).
- Run Feature extraction cells to build the feature matrix.
- Pick the k-NN or SVM block and train.
- Run Evaluation to see metrics + confusion matrix.
- Use the Predict cell to grade a single image.

## Tips

- Keep lighting/background consistent when collecting images.
- If classes are imbalanced, use stratified splits and report macro-F1.
- To support more than two grades, add folders like fruit__gradeC and update the label map.
- Easy upgrades: histogram equalization, better texture descriptors, tiny CNN baseline for comparison.

## Paper / citation
If you cite:
Yeluru, Sreeja Reddy. "Fruit & Vegetable Grading using Classical Computer Vision."
GitHub, 2025. https://github.com/yelurusreejareddy/fruit-veg-grading

## License
MIT — see LICENSE.

