# ATM Anomaly Detection Model

An AI-based ATM monitoring system that analyzes CCTV video footage to detect unusual or potentially fraudulent activity, using a Convolutional Neural Network (CNN) trained to classify normal vs. abnormal behaviour.

## Problem Statement

ATMs are a common target for fraud and tampering, and manual CCTV monitoring is slow, inconsistent, and hard to scale. This project explores whether a CNN trained on frame-level image data can automatically flag abnormal activity in ATM surveillance footage, reducing reliance on manual review and lowering false positives.

## Approach

The pipeline is broken into four stages, each handled in a dedicated notebook:

1. **Dataset Creation** — collects and organizes labelled video/image data representing normal and abnormal ATM activity.
2. **Frame Extraction** — extracts individual frames from the source video footage so they can be fed into the CNN as image data.
3. **Model Training** — trains a CNN on the extracted frames to classify each one as normal or abnormal behaviour.
4. **Testing** — runs the trained model against unseen footage/frames to evaluate real-world performance.

## Results

- Achieved **98.5% detection accuracy** in classifying normal vs. abnormal ATM activity.
- Reduced false positives through careful data preprocessing and feature extraction before training.

## Tech Stack

- **Language:** Python
- **Deep Learning:** CNN (Convolutional Neural Network)
- **Libraries:** Scikit-learn, Pandas, NumPy
- **Environment:** Jupyter Notebook

## Project Structure

```
ATM-Anomaly-Detection-Model/
├── 1_create_dataset.ipynb       # Builds and labels the dataset
├── 2_extract_frames.ipynb       # Extracts frames from CCTV video input
├── 3_train_cnn_model.ipynb      # Trains the CNN (5 epochs)
├── 4_test_model.ipynb           # Runs inference and evaluates results
├── data/
│   └── train_data.csv           # Training data / labels
├── requirements.txt
└── README.md
```

> Note: rename your existing notebook files to match the structure above (drop the typo "Anomoly" → "Anomaly" and "Creat" → "Create") and move loose files like `train_path.txt` and any `.pyc` files into appropriate subfolders or remove them if they're not needed.

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/shrikardesai2020/ATM-Anomaly-Detection-Model.git
   cd ATM-Anomaly-Detection-Model
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks in order:
   - `1_create_dataset.ipynb`
   - `2_extract_frames.ipynb`
   - `3_train_cnn_model.ipynb`
   - `4_test_model.ipynb`

## Future Improvements

- Add real-time video stream support instead of static frame extraction.
- Experiment with deeper architectures (ResNet, EfficientNet) for improved accuracy.
- Deploy as a lightweight API or dashboard for live monitoring demos.

## Author

**Shrikar V. Desai**
[GitHub](https://github.com/shrikardesai2020) · [LinkedIn](https://linkedin.com/in/shrikar-desai) · [Portfolio](https://shrikardesai2020.github.io/Shrikar-Portfolio/)
