# Applied Machine Learning: Coursework Portfolio

Labs and problem sets from **INFO 251: Applied Machine Learning** at the UC Berkeley School of Information: a course covering the full applied ML pipeline, from causal inference and regression through tree-based models, neural networks, and unsupervised learning.

Each notebook below is my own submitted work, implementing methods from scratch (gradient descent, k-nearest neighbors, cross-validation) alongside applied use of scikit-learn, Keras/TensorFlow, and folktables, on real-world datasets spanning economics, housing, income, images, and faces.

## Syllabus: topics, techniques, and datasets

| # | Mini projects | Topics | Techniques | Dataset |
|---|---|---|---|---|
| 1 | [Python & Pandas Fundamentals](problem-sets/01-python-pandas-fundamentals) | Data exploration | Pandas, descriptive statistics | California Housing |
| 2 | [Causal Inference](problem-sets/02-causal-inference-did) | Differences-in-differences, fixed effects, spillover effects | Linear regression, panel data methods | PROGRESA (Mexican conditional cash transfer program) |
| 3 | [KNN & Cross-Validation](problem-sets/03-knn-cross-validation) | Prediction fundamentals, model evaluation | RMSE from scratch, k-nearest neighbors from scratch, k-fold and nested cross-validation | California Housing |
| 4 | [Gradient Descent & Regularization](problem-sets/04-gradient-descent-regularization) | Optimization, overfitting | Gradient descent from scratch, ridge regularization, AdaGrad | California Housing |
| 5 | [Trees, Forests & Fairness](problem-sets/05-trees-forests-fairness) | Tree-based models, algorithmic fairness | Decision trees, random forests, ROC curves, error-parity analysis across demographic groups | ACS PUMS income data (via `folktables`) |
| 6 | [Neural Networks](problem-sets/06-neural-networks-image-classification) | Deep learning, image classification | Feedforward neural networks, CNNs, transfer learning | CIFAR-10 (car vs. truck classification) |
| 7 | [Unsupervised Learning & Facial Recognition](problem-sets/07-facial-recognition-pca) | Clustering, dimensionality reduction | k-means clustering, PCA/eigenfaces, k-means++ | Labeled Faces in the Wild (LFW) + my own photos |

## Labs

Shorter, guided exercises done in class. 

| Lab | Topics | Dataset |
|---|---|---|
| [Computational Efficiency in NumPy](Labs/03-numpy-computational-efficiency) | Vectorization vs. loops, broadcasting | Synthetic matrices |
| [ML Experiments in Python](Labs/04-ml-experiments-python) | Vectorized nearest-neighbor search, train/test splitting, cross-validation (numpy, pandas, and scikit-learn approaches) | Auto dataset |
| [Gradient Descent](Labs/05-gradient-descent) | Implementing gradient descent | Synthetic data |

## Repository structure

```
INFO201_AppliedMachineLearning/
├── README.md
├── problem-sets/
│   ├── 01-python-pandas-fundamentals/
│   ├── 02-causal-inference-did/
│   ├── 03-knn-cross-validation/
│   ├── 04-gradient-descent-regularization/
│   ├── 05-trees-forests-fairness/
│   ├── 06-neural-networks-image-classification/
│   └── 07-facial-recognition-pca/
│       ├── ps7_facial_recognition_pca.ipynb
│       ├── lfw_funneled/       # Labeled Faces in the Wild dataset
│       └── my_photos/          # personal test images for the "classify yourself" exercise
└── Labs/
    ├── 03-numpy-computational-efficiency/
    ├── 04-ml-experiments-python/
    └── 05-gradient-descent/
```

Each project folder contains one notebook with all analysis, code, and written answers inline, plus any small supporting dataset it needs to run standalone.

## Notes on this repo

A few things worth knowing if you're browsing this:

- **Instructor material is excluded from the public repo.** 
- **Redundant exports were cleaned up.** The two Lab notebooks whose `.ipynb` cell outputs were cleared (Lab 4, Lab 5) keep their PDF alongside them, since that's currently the only place the rendered plots/results are visible.
- **The LFW face dataset is large.** `problem-sets/07-facial-recognition-pca/lfw_funneled/` is about 266MB across 13,000+ image files, already part of this repo's git history. Cloning this repo will be slower than the others as a result. Shrinking that would mean rewriting git history (e.g. with `git filter-repo`), which is a bigger, riskier operation worth deciding on separately rather than doing automatically here.

## Author

Laura Gomez ([neurogomez](https://github.com/neurogomez))
