# fruit-veg-grading

Classical image processing pipeline that grades produce as good or bad without deep
learning or a GPU, using color, edge, and texture features with a rule-based classifier.

## Files Included

- fruit_veg_grading_cv.ipynb - end-to-end notebook: loading, background removal, features, classification, evaluation
- dataset/ - sample images in four folders: Mango__good, Mango__bad, lemon__good, lemon__bad
- final_paper.pdf - paper with method and results

## Pipeline

1. Load images and resize to 128x128
2. Split into training, validation, and test sets (60/20/20)
3. Remove the background with gamma correction, HSV thresholding, morphological opening and closing, and a convex hull mask around the largest contour
4. Extract features: HSV color histograms, Sobel edge density, and Shannon entropy
5. Classify with a rule: high edge density or high entropy means bad, otherwise good
6. Evaluate with accuracy, a classification report, and a confusion matrix

## Results

| Split | Accuracy |
|---|---|
| Training | 64.33% |
| Validation | 65.04% |
| Test | 63.44% |

## Stack

Python, OpenCV, scikit-image, scikit-learn, NumPy, pandas, Matplotlib, seaborn

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

