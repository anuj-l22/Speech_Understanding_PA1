

---

# **AudioSeal (Q1)**

## **Overview**

This folder contains code, reports, and presentation materials for **Question 1**, where we explore and evaluate **AudioSeal**—a state-of-the-art audio watermarking system designed to embed an imperceptible watermark into generated speech. The detector can then localize whether (and where) the audio was AI-generated, even after real-world edits. 

**Reference Paper:**  
> **Proactive Detection of Voice Cloning with Localized Watermarking**  
> R. Schmucker, H. Elsahar, and P. Faure. 2024.  
> [arXiv:2401.17264](https://arxiv.org/abs/2401.17264)  
> Code: [https://github.com/facebookresearch/audioseal](https://github.com/facebookresearch/audioseal)

## **Contents of This Folder**

1. **`AudioSeal_on_NPTEL_English_data.ipynb`**  
   - Jupyter notebook demonstrating how we apply the pretrained AudioSeal generator/detector to **NPTEL** (Indian English) data.  
   - Covers sample extraction, watermark embedding, random masking (to simulate partial watermark removal), and metric computation (PESQ, STOI, SI-SNR, detection scores).

2. **`AudioSeal_on_OpenSLR_Hindi_Data.ipynb`**  
   - Similar to the above notebook, but focuses on **OpenSLR Hindi** dataset.  
   - Evaluates whether AudioSeal retains high imperceptibility and detection accuracy cross-lingually in Hindi data.

3. **`B22AI061_Q1_AudioSeal_presentation.pdf`**  
   - A concise slide deck summarizing **AudioSeal** and our experiments.  
   - Highlights the main motivations, methodology, and results of applying AudioSeal to the NPTEL and Hindi datasets.

4. **`B22AI061_Q1_Report_AudioSeal.pdf`**  
   - A detailed report covering:
     - The **task** of speech watermarking and its real-world importance.
     - An **analysis** of AudioSeal vs. other SOTA watermarking approaches.
     - **Experiments** (NPTEL, Hindi) with results in PESQ, STOI, SI-SNR, detection accuracy.
     - **Discussion** of open problems, limitations, and future directions.

5. **`README.md`**  
   - This README file, containing an overview of the contents, dataset links, and references.

## **Datasets**

We used **two main datasets** to test AudioSeal:

1. **NPTEL Indian English**  
   - A collection of Indian English speech from lecture recordings.  
   - Download link or GitHub reference:  
     \[
       \text{NPTEL Indian English Speech Dataset (NPTEL2020):} 
       \url{https://github.com/AI4Bharat/NPTEL2020-Indian-English-Speech-Dataset}
     \]

2. **OpenSLR Hindi**  
   - A Hindi speech dataset from the OpenSLR initiative.  
   - Available at:  
     \[
       \text{OpenSLR Hindi_test:}
       \url{http://www.openslr.org/}
     \]



## **Results Summary**

- **NPTEL**:  
  - Watermarked speech maintains PESQ ~4.44, STOI=0.998, with Detector Score ~1.0.  
  - Even after partial masking, detection remains >0.68, indicating partial robustness.
- **Hindi**:  
  - Watermarked PESQ ~4.45, STOI=0.998, with Detector Score ~1.0.  
  - Similarly, partial masking yields ~0.68 detection, confirming cross-lingual resilience.

These results align with the **AudioSeal** paper’s claims of high imperceptibility and robust detection under multiple edits.

## **References**

- **AudioSeal Paper**:  
  R. Schmucker, H. Elsahar, and P. Faure.  
  “Proactive Detection of Voice Cloning with Localized Watermarking.” 2024.  
  [arXiv:2401.17264](https://arxiv.org/abs/2401.17264).

- **AudioSeal Official Code**:  
  [https://github.com/facebookresearch/audioseal](https://github.com/facebookresearch/audioseal)

- **NPTEL Indian English Speech Dataset**:  
  [https://github.com/<YourNPTELrepo>](https://github.com/AI4Bharat/NPTEL2020-Indian-English-Speech-Dataset)

- **OpenSLR Hindi\_test**:  
  [http://www.openslr.org/](http://www.openslr.org/)

## **License / Acknowledgements**

- AudioSeal is published by [Meta AI Research](https://github.com/facebookresearch/audioseal).  
- Datasets are owned by their respective publishers (NPTEL, OpenSLR).  

---


