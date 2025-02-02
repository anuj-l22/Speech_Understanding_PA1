
---

# Q2: Audio Analysis Tasks

This repository contains two related tasks for **Speech Understanding** (Q2). Task A focuses on **windowing techniques** and **classification** using the UrbanSound8K dataset, while Task B examines **spectrograms** of four different genres of music from Pixabay.

---

## Task A: Windowing & Classification on UrbanSound8K

### Overview
- **Goal**: Compare **Rectangular**, **Hann**, and **Hamming** windows for STFT spectrogram generation, then train a **CNN** (or another simple model) to classify the resulting features.
- **Dataset**: [UrbanSound8K](https://urbansounddataset.weebly.com/urbansound8k.html), which comprises 8,732 audio samples across 10 classes.

### Files
- **`B22AI061_Task_2A.ipynb`**  
  - Implements:
    1. Window demonstration (Rectangular vs. Hann vs. Hamming).  
    2. Spectrogram/feature extraction (Mel-spectrogram or MFCC).  
    3. CNN training & 10-fold evaluation on UrbanSound8K.
- **`B22AI061_Task_2A_Report.pdf`**  
  - Discusses:
    1. Window theory & spectral leakage.  
    2. Visual spectrogram comparisons.  
    3. Accuracy results across folds.

### Usage
1. **Unzip UrbanSound8K** in the same directory:
   ```
   Q2/
    ├─ UrbanSound8k/
    │   ├─ audio/
    │   │   ├─ fold1/
    │   │   ├─ ...
    │   │   └─ fold10/
    │   └─ metadata/UrbanSound8k.csv
    ├─ B22AI061_Task_2A.ipynb
    ├─ B22AI061_Task_2A_Report.pdf
    └─ ...
   ```
2. **Install dependencies** (e.g., `librosa`, `numpy`, `matplotlib`, `PyTorch`).
3. **Open** `B22AI061_Task_2A.ipynb` and **run** each cell to:
   - Load audio and generate spectrograms under each window.  
   - Train a CNN with 10-fold cross-validation.  
   - Compare performance metrics for each window.

### Highlights
- Rectangular introduces more **spectral leakage**.  
- Hann/Hamming produce smoother high-frequency regions.  
- Modest accuracy gains (a few percentage points) often favor Hann overall.

---

## Task B: Comparative Spectral Analysis of Four Songs

### Overview
- **Goal**: Select **four songs** (each from a different genre) and analyze their **spectrograms**—both the entire track and a 30-second snippet.  
- **Sources**: [Pixabay](https://pixabay.com/music/) (free music under the Pixabay license).

### Files
- **`B22AI061_Task_2B.ipynb`**  
  - Loads `.wav` files from four genres (Rock, Electronic/Ambient, Classical, Jazz).  
  - Generates **full** and **snippet** spectrograms.  
  - Computes basic metrics (Spectral Centroid, Bandwidth, Rolloff, RMS).
- **`B22AI061_Task_2B_Report.pdf`**  
  - Describes:
    1. Methodology for generating spectrograms (STFT with Hann window).  
    2. Comparative analysis of each genre’s time–frequency content.  
    3. Observations linking these differences to fundamental speech/audio analysis.

### Usage
1. **Download** the four `.wav` files from [Drive ( Downloaded as mp3 from Pixabay then converted to wav](https://drive.google.com/drive/folders/1ijCBT2TTh6xypSrqfIC_XdHw9VBil9XB?usp=sharing) 
2. **Open** `B22AI061_Task_2B.ipynb` in Jupyter.  
3. **Run** each cell to:
   - Plot **full spectrogram** and **30–60 s snippet** spectrogram for each song.  
   - Print metrics and highlight differences in frequency balance, amplitude, etc.

### Key Observations
- **Retro City (Rock)**: Strong midrange energy, highest RMS.  
- **SCI-FI Background (Electronic)**: Subdued amplitude, emphasis on low frequencies.  
- **Spring Mood (Classical)**: Extended high‐frequency content, high centroid.  
- **Vinyl (Jazz)**: Balanced brightness, moderate loudness.

---

## References

1. **UrbanSound8K Dataset**  
   [https://urbansounddataset.weebly.com/urbansound8k.html](https://urbansounddataset.weebly.com/urbansound8k.html)
2. **Pixabay Music**  
   [https://pixabay.com/music/](https://pixabay.com/music/)
3. **GitHub code from where manual stft implementation was adopted**  
   [GitHub](https://github.com/aluchies/stft)
4. **Librosa Docs**  
   [https://librosa.org/doc/latest/](https://librosa.org/doc/latest/)
5. **Spectral Leakage Explanation** (YouTube)  
   [https://youtu.be/tCWU9C-LdJQ](https://youtu.be/tCWU9C-LdJQ)
6. **Matplotlib**  
   [https://matplotlib.org/](https://matplotlib.org/)


---

**End of README**
