Deep Learning-Based Detection and Classification of White Blood Cells

A research project on classifying five types of white blood cells (WBCs) from microscopic images using transfer learning and convolutional neural networks.

Project Overview

This project explores five-class WBC image classification using three ImageNet-pretrained CNN architectures:

\- EfficientNetB0

\- ResNet50

\- MobileNetV2

The five classes are Basophil, Eosinophil, Lymphocyte, Monocyte, and Neutrophil.

Scope: This project classifies cropped WBC images. It does not perform full-smear object detection, cell localization, cell counting, or clinical diagnosis.



Dataset

The experiment used 10,298 valid JPG images.

Class	Images

Basophil	1,218

Eosinophil	3,117

Lymphocyte	1,214

Monocyte	1,420

Neutrophil	3,329

Total	10,298





Stratified data split:

Split	Images

Training	7,208

Validation	1,545

Testing	1,545





The dataset is not included in this repository. Keep the original dataset and large backups in Google Drive, and add the verified dataset source/link here when ready.

Model Performance

Results transcribed from the test outputs in the research notebook:

Model	Test Accuracy	Macro Precision	Macro Recall	Macro F1-score	Test Loss

EfficientNetB0	94.76%	93.35%	94.86%	94.03%	0.1636

ResNet50 (final run)	93.59%	92.63%	93.54%	92.92%	0.2116

MobileNetV2	96.05%	95.07%	95.75%	95.38%	0.1305





Best result in this experiment: MobileNetV2, with 96.05% test accuracy, 95.38% macro F1-score, and 0.1305 test loss.

Experimental limitation

This is a preliminary comparison, not a fully controlled architecture-only comparison. EfficientNetB0 was fine-tuned, while ResNet50 and MobileNetV2 were trained with frozen pretrained backbones. The notebook also contains a duplicate ResNet50 training run; the table reports the later run used in the final comparison. Use consistent training configurations before making strong claims about architecture superiority.

Repository Structure

WBC-Classification-Research/

├── README.md

├── Notebooks/

│   └── WBC\_Classification\_Research\_Mysha22.ipynb

├── Results/

│   ├── Model\_Comparison.csv

│   ├── Accuracy\_Comparison.png

│   ├── Validation\_Accuracy.png

│   ├── Validation\_Loss.png

│   ├── Confusion\_Matrices/

│   └── Classification\_Reports/

├── Reports/

├── Models/

├── requirements.txt

└── .gitignore

This is the intended organization; only add files that actually exist. Keep large datasets, extracted image archives, checkpoints, and large trained model files in Google Drive or suitable external storage. Add shareable links here when available.

Technologies Used

\- Python

\- Google Colab

\- TensorFlow / Keras

\- NumPy and Pandas

\- Matplotlib and Seaborn

\- Scikit-learn

\- Pillow (PIL)

How to Run

1\. Open the notebook in Google Colab.

2\. Make the dataset available in Google Drive.

3\. Update the dataset path in the notebook.

4\. Run the notebook cells in order.

5\. Review the classification reports, confusion matrices, and comparison plots.

Record the exact package versions from the working Colab environment in requirements.txt before attempting a reproducible local run.

Researcher

Samira Sultana Mysha

Department of Computer Science and Engineering

Premier University

Research Track Internship — Authentic Four Technology

Notes

\- Metrics are experimental results from the notebook, not clinical performance claims.

\- Do not use this model for medical diagnosis or treatment decisions.

\- Add the verified dataset publication citation and dataset source URL before final academic submission.

