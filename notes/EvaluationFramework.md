# Evaluation Framework

## 1. Qualitative Metrics

### 1.1. Sound Quality Assessment (Weight: 30%)

- **Clarity of Output Signal** (Score: 1-5)
  - How clear is the audio output compared to the original?
  - Measured subjectively through listening tests.
  
- **Word Intelligibility** (Score: 1-5)
  - How well can listeners understand spoken words?
  - Conduct listening tests with different speakers (male, female, child).
  
- **Similarity to Original Input** (Score: 1-5)
  - How similar is the processed signal to the original?
  - Compare the input and output using subjective measures.

### 1.2. Performance in Various Scenarios (Weight: 20%)

- **Different Sound Types** (Score: 1-5)
  - How does the design perform for male, female, and child speech?
  
- **Listening Environments** (Score: 1-5)
  - Test in quiet and noisy environments.
  
- **Multi-Speaker Scenarios** (Score: 1-5)
  - Evaluate performance in scenarios with overlapping speech.

## 2. Quantitative Metrics

### 2.1. Signal Processing Metrics (Weight: 30%)

- **Signal-to-Noise Ratio (SNR)** (Score: 1-5)
  - A measure of how much the signal stands out from background noise.
  
- **Frequency Response Accuracy** (Score: 1-5)
  - Compare the output frequency spectrum with the original input.

- **Envelope Extraction Accuracy** (Score: 1-5)
  - Compare the extracted envelope with the expected envelope of the original signal.

### 2.2. Computational Efficiency (Weight: 20%)

- **Processing Time** (Score: 1-5)
  - Measure the time taken to process each signal.
  
- **Memory Usage** (Score: 1-5)
  - Evaluate the memory consumption during processing.
  
- **Number of Channels** (Score: 1-5)
  - Higher channel numbers typically improve quality but increase computational load and power consumption.

## 3. Evaluation Process

### 3.1. Standardized Test Set

- Use a diverse set of audio samples (speech, music, environmental sounds) from **Task 2 of Phase 1**.
- Include male, female, and child voices, as well as different environments (quiet, noisy).

### 3.2. Listening Tests

- Conduct blind listening tests with participants.
- Use a rating scale (1-5) for each qualitative metric.
- Average scores across participants for each design.

### 3.3. Objective Measurements

- Use signal processing tools to measure **SNR**, **frequency response**, and **envelope accuracy**.
- Use a tool like MATLAB to compute these values directly from the audio data.

### 3.4. Computational Analysis

- Measure processing time and memory usage using system profiling tools.
- Adjust the number of channels to find the optimal balance between performance and computational load.

## 4. Weighted Scoring System

For each design, assign a score for each metric (1-5), multiply it by the corresponding weight, and sum these scores to generate a final **composite score**.

### Example Weighting

- **Qualitative Metrics**:
  - Sound Quality (30%)
  - Performance in Scenarios (20%)
  
- **Quantitative Metrics**:
  - Signal Processing (30%)
  - Computational Efficiency (20%)

### Final Score Calculation

```math
Final Score = (Sound Quality × 0.30) + (Performance in Scenarios × 0.20) + (Signal Processing × 0.30) + (Computational Efficiency × 0.20)
```

## 5. Comparative Analysis

- Create a **ranking matrix** comparing designs based on their final composite score.
- Use **graphs and charts** to visualize performance across different metrics.

## 6. Iterative Refinement

- Use evaluation results to make design improvements:
  - Adjust the number of channels, filter types, or envelope detection parameters.
  
- **Repeat the evaluation process** after refining each design to track improvements.

## 7. Bonus Task: Quantitative Evaluation Metric

To quantitatively assess the performance further, use an **intelligibility score** such as the **Short-Time Objective Intelligibility (STOI)**, which provides an objective measure of speech intelligibility.

**STOI Score** (Bonus Metric):

- **Weight: 10%**
- A value from 0 to 1 that measures how intelligible speech is after processing.
  
Integrating this metric:

```math
Adjusted Final Score = 0.9 × Final Score + 0.1 × STOI Score
```
