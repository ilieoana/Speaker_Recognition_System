# Speaker Recognition System

A comprehensive speaker verification system using statistical methods and identity vectors, developed as part of my Bachelor's degree project. This system implements custom algorithms for speaker verification on a Romanian speakers corpus, resulting in a published IEEE paper.

## 🎓 Published Research
**📄 IEEE Publication**: [Speaker Verification Experiments using Identity Vectors, on a Romanian Speakers Corpus](https://ieeexplore.ieee.org/document/9587396)

This project has been peer-reviewed and published in IEEE Xplore, demonstrating its academic and technical merit.

## 🎯 Project Overview
This project implements a speaker verification system using statistical methods and identity vectors, specifically designed for Romanian speakers. Unlike black-box deep learning approaches, this system builds all core algorithms from scratch, providing full control over the mathematical foundations and feature extraction processes.

**🔬 Academic Context**: Developed as a Bachelor's degree thesis project focusing on statistical signal processing, identity vector computation, and speaker verification algorithms - all implemented from first principles.

## ✨ Key Features

- **Custom Statistical Algorithms**: All core functions implemented from scratch
- **Identity Vector Computation**: Statistical approach to speaker modeling
- **Romanian Corpus Optimization**: Specifically tuned for Romanian language characteristics
- **Mathematical Foundation**: Complete control over underlying mathematics
- **Verification System**: Speaker verification (1:1 matching) implementation
- **Forensic Applications**: Suitable for legal and security applications
- **Performance Analytics**: Comprehensive statistical evaluation metrics

## 🛠 Technologies & Implementation

### Core Technologies
- **Python 3.x** - Primary programming language
- **NumPy** - Numerical computations and matrix operations
- **SciPy** - Statistical functions and signal processing
- **Matplotlib** - Visualization and analysis plots
- **Wave/Audio Libraries** - Basic audio file handling

### Custom Implementations
- **Statistical Feature Extraction** - Hand-coded feature computation
- **Identity Vector Algorithms** - Custom statistical modeling
- **Distance Metrics** - Implemented similarity measures
- **Verification Algorithms** - Custom speaker verification logic
- **Performance Evaluation** - Statistical significance testing

### Mathematical Foundations
- **Statistical Modeling** - Gaussian distributions, covariance matrices
- **Linear Algebra** - Matrix operations, eigenvalue decomposition
- **Signal Processing** - Spectral analysis, windowing functions
- **Probability Theory** - Likelihood estimation



## 📊 Speaker Verification System Architecture

### Training

```
        Background Speakers
                │
                ▼
    [Speaker Speech Detection]
                │
                ▼
        [Feature Extraction]
                │
                ├───► [Train GMM-UBM Model]
                │               │
                ▼               ▼
            [Statistics Calculation] 
                    │
                    ├───► [Train Total Variability Space (T-Matrix)]
                    │                │
                    ▼                ▼
                   [i-vector Extraction] 
                            │
                            ├───► [Compute Projection Matrix]
                            │                   │
                            │                   │
                            ▼                   ▼
                         [Train GPLDA Speaker Model]
```
**Outputs:**
- UBM Model
- T-Matrix
- Projection Matrix
- GPLDA Model

---

### Enrollment

```
         Known Speaker
              │
              ▼
    [Speaker Speech Detection]
              │
              ▼
     [Feature Extraction]
              │
              ▼
    [Statistics Calculation] ◄────────── Uses UBM Model
              │
              ▼
       [i-vector Extraction] ◄────────── Uses T-Matrix
              │
              ▼
    [Session Compensation] ◄──────── Uses Projection Matrix
  ```
---

### Verification

```
         Known Speaker
              │
              ▼
    [Speaker Speech Detection]
              │
              ▼
     [Feature Extraction]
              │
              ▼
    [Statistics Calculation] ◄────────── Uses UBM Model
              │
              ▼
       [i-vector Extraction] ◄────────── Uses T-Matrix
              │
              ▼
    [Session Compensation] ◄──────── Uses Projection Matrix
              │
              ▼
      [Score Calculation] ◄─────────── Uses GPLDA Model
              │
              ▼
         [Decision] ◄──── Threshold
```

### Statistical Pipeline
1. **Audio Preprocessing Module**: Handles audio loading, noise reduction, and normalization
2. **Feature Extraction**: Extracts audio features (MFCC, spectral and temporal features)
3. **Statistical Modeling**: Identity vector computation using statistical methods
4. **Verification**: Distance-based speaker verification
5. **Evaluation Module**: Assesses model performance with various metrics

## 🔬 Scientific Approach

### Identity Vector Method
The system uses a statistical approach to create identity vectors that capture speaker-specific characteristics:
- **Statistical Feature Modeling**: Custom algorithms for feature distribution analysis
- **Dimensionality Reduction**: Mathematical techniques for efficient representation
- **Speaker Modeling**: Identity vectors as compact speaker representations
- **Verification Metrics**: Statistical distance measures for speaker comparison

### Romanian Corpus Considerations
- **Language-Specific Tuning**: Optimized for Romanian phonetic characteristics
- **Corpus Analysis**: Statistical analysis of Romanian speech patterns
- **Cultural Adaptation**: Accounting for Romanian accent variations
- **Forensic Applications**: Suitable for legal proceedings in Romanian courts

### Dataset

This project uses the  “RoDigits – a Romanian connected-digits speech corpus for automatic speech and speaker recognition” for speaker recognition training and evaluation.

#### Citation:
```bibtex
@article{georgescu2018rodigits,
  title={Rodigits-a romanian connected-digits speech corpus for automatic speech and speaker recognition},
  author={Georgescu, Alexandru Lucian and Caranica, Alexandru and Cucu, Horia and Burileanu, Corneliu},
  journal={University Politehnica of Bucharest Scientific Bulletin, Series C},
  volume={80},
  number={3},
  pages={45--62},
  year={2018}
}
```

## 🚀 Usage

There is a demo version of the application in the demo directory that allows enrolling a new speaker in the system, as well as verification. For creating models, all methods are provided in the code directory.


## 🔬 Technical Implementation Details

### Custom Feature Extraction
- **Spectral Features**: Hand-implemented FFT-based spectral analysis
- **Cepstral Analysis**: Custom cepstral coefficient computation
- **Temporal Features**: Statistical temporal pattern analysis
- **Normalization**: Custom normalization techniques for Romanian speech

### Identity Vector Computation
- **Statistical Modeling**: Gaussian mixture parameter estimation
- **Dimensionality Reduction**: Principal component analysis implementation
- **Vector Quantization**: Custom clustering algorithms
- **Model Adaptation**: Speaker-specific model adaptation techniques

## 📚 Academic Contributions

### Research Contributions
- **Novel Statistical Approach**: Custom implementation of identity vector methods
- **Romanian Language Focus**: Specialized optimization for Romanian speakers
- **Mathematical Rigor**: Complete mathematical foundation and proof of concepts
- **Forensic Applications**: Practical applications in legal contexts

### Learning Outcomes
- **Advanced Statistics**: Deep understanding of statistical modeling
- **Signal Processing**: From-scratch implementation of audio processing
- **Algorithm Design**: Custom algorithm development and optimization
- **Research Methodology**: Scientific approach to problem-solving
- **Academic Writing**: Peer-reviewed publication skills

## 📄 Publications & Citations

O. -M. Novac, S. -A. Toma and E. Bureaca, "Speaker Verification Experiments using Identity Vectors, on a Romanian Speakers Corpus," 2021 International Conference on Speech Technology and Human-Computer Dialogue (SpeD), Bucharest, Romania, 2021, pp. 162-166, doi: 10.1109/SpeD53181.2021.9587396.
keywords: {Training;Forensics;Speaker recognition;Testing},

### Citation Format
```bibtex
@INPROCEEDINGS{9587396,
  author={Novac, Oana-Mariana and Toma, Stefan-Adrian and Bureaca, Emil},
  booktitle={2021 International Conference on Speech Technology and Human-Computer Dialogue (SpeD)}, 
  title={Speaker Verification Experiments using Identity Vectors, on a Romanian Speakers Corpus}, 
  year={2021},
  volume={},
  number={},
  pages={162-166},
  keywords={Training;Forensics;Speaker recognition;Testing},
  doi={10.1109/SpeD53181.2021.9587396}}
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Academic use encouraged with proper citation of the IEEE publication.

⭐ **If you find this research useful, please star the repository and cite our IEEE paper!**

📄 **IEEE Publication**: This work has been peer-reviewed and published in IEEE Xplore Digital Library, demonstrating its academic rigor and technical merit.