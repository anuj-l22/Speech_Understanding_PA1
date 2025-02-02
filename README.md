
# Audio‐Related Projects

This repository contains solutions for **Speech Understanding** tasks across two primary questions:  
- **Q1: AudioSeal** — Evaluating an audio watermarking system on different speech datasets.  
- **Q2: Audio Analysis** — Windowing and classification on UrbanSound8K (**Task A**), and comparing spectrograms of four songs (**Task B**).

---

## Q1: AudioSeal
- **Objective**: Experiment with a watermarking approach ([AudioSeal](https://github.com/facebookresearch/audioseal)) that embeds localized watermarks into generated speech.  
- **Files**:
  - `AudioSeal_on_NPTEL_English_data.ipynb`  
  - `AudioSeal_on_OpenSLR_Hindi_Data.ipynb`  
  - `B22AI061_Q1_AudioSeal_presentation.pdf`  
  - `B22AI061_Q1_Report_AudioSeal.pdf`  
- **Key Points**:  
  - Applied AudioSeal to **NPTEL Indian English** and **OpenSLR Hindi** datasets.  
  - Measured imperceptibility (PESQ, STOI) and detection resilience under random masking.  
  - Found cross‐lingual robustness in watermark detection, aligning with the AudioSeal paper.

---

## Q2: Audio Analysis

### Task A: Windowing & Classification (UrbanSound8K)
- **Goal**: Compare **Rectangular**, **Hann**, and **Hamming** windows for STFT; train a simple classifier (CNN) on resulting features.  
- **Files**:  
  - `B22AI061_Task_2A.ipynb` / `B22AI061_Task_2A_Report.pdf`  
- **Highlights**:  
  - 10‐fold cross‐validation on UrbanSound8K.  
  - Hann/Hamming reduce spectral leakage, yielding slightly better accuracy than Rectangular.

### Task B: Spectral Analysis of Four Songs
- **Goal**: Examine four songs (Rock, Electronic/Ambient, Classical, Jazz) by generating spectrograms (full track & 30‐second snippet).  
- **Files**:  
  - `B22AI061_Task_2B.ipynb` / `B22AI061_Task_2B_Report.pdf`  
- **Key Observations**:  
  - Each genre shows distinct frequency balance (centroid, bandwidth).  
  - “Retro City” (Rock) has strong midrange and highest loudness, “SCI-FI Background” (Electronic) is quieter with low‐frequency emphasis, etc.

---

## Further Details are present in README files for individual directories
