# Hard-Techno Subgenre Classification Using CNNs & ML Methods

## Group Members
- Georgopoulos Panagiotis
- Verykokidis Apostolos

## Project Summary
The project aims to build a model that classifies 8-second audio clips into five subgenres of hard-techno. We extracted mel-spectrogram images from audio clips and experimented with several ML algorithms and CNN architectures to achieve the best performance.

## Contents
- **Code:** Python notebooks and scripts used for data preprocessing, feature extraction, ML experiments, CNN training, and transfer learning.
- **Report:** Detailed PDF documentation explaining the methodology, results, and discussion, available in `report.pdf`.
- **Presentation:** PowerPoint slides for the project presentation, available in `presentation.pptx`.
- **Mel-spectrograms:** PNG images of mel-spectrograms used for training and transfer learning experiments.

## Dataset
- The entire dataset used can be found in this public link: `https://drive.google.com/drive/folders/1Wtcmi4grjVQK8G2KAdINsqbb7Qm0VIGg?usp=sharing`
- Clips extracted from hard-techno tracks (8 seconds each).
- Total clips: 1772.
- Labels correspond to five subgenres: bouncy, tekno, warzone, industrial, non-techno-drop.
- Train/Validation/Test split of 70% / 15% / 15%, with clips from the same track kept in the same split to avoid data leakage.

## Methodology

### Machine Learning Approach
- Feature extraction using Librosa for chroma, spectral, zero crossing, and MFCCs features.
- Experiments with SVM, XGBoost, LightGBM, and voting classifiers.
- Achieved moderate performance, highlighting the challenging nature of the classification task.

### Deep Learning Approach
- Conversion of audio clips into mel-spectrogram images.
- CNN architectures tested with various configurations.
- Best model reached an average validation accuracy of ~83.8% and test F1 score of ~78.4%.
- Applied class weights to balance dataset classes.

### Transfer Learning
- Used the trained model on the GTZAN dataset (10 genres) for transfer learning experiments.
- Achieved a test F1 score of ~62.6% over 5 runs, demonstrating model adaptability.

## How to Run
1. Clone the repo
2. Install dependencies:  
   `pip install -r requirements.txt`
3. Open and run the notebook in Jupyter

- Explore notebooks for feature extraction, model training, evaluation, and transfer learning.
- Refer to the report for comprehensive details.
- See presentation slides for summary and key insights.

## Including Mel-Spectrograms
We have included the mel-spectrogram PNG files in the melgrams/ folder. These represent the transformed audio data used as CNN inputs. We excluded raw audio clips due to copyright and size considerations.
