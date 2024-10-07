# Project Outline

## Project Background

This project involves designing a signal processor for cochlear implants, where audio signals are split into frequency bands and processed. This mimics the natural stimulation of auditory nerves by a cochlear implant, with the final output differing from the original input due to the filtering and modulation processes.

Your project will involve:

- Reading and processing audio files.
- Designing filter banks to divide audio into frequency bands.
- Modulating and reconstructing audio for output.
- Iterating and evaluating your design using established metrics.

## Phase 1: Data Exploration

### Input (Audio File)

- **Parameters**:
  - **Sampling rate (Hz)**: Number of samples per second. Higher sample rates capture more detail but result in larger file sizes.
  - **Input Channels (n)**: Number of channels capturing audio data:
    - **Mono**: Single audio channel, used for simpler recordings like voice.
    - **Stereo**: Two channels (Left and Right) for more dynamic audio such as music.
    - More channels (e.g., 6 for surround sound) capture complex sound dynamics.
  - **Length (s)**: Duration of the audio file.

## Phase 2: Filter Design

### Parameters

- **Frequency Range**: The range of frequencies in the input signal.
- **Number of Input Channels (N)**: Number of channels/frequency bands to divide the audio signal.
- **Filter Types**:
  - **IIR Filters (Infinite Impulse Response)**:
    - Uses both current input and previous outputs in calculations.
    - Efficient with fewer parameters but has non-linear phase response and can be unstable due to feedback.
    - Applications: Audio equalization, biomedical sensor processing, telecommunications.
  - **FIR Filters (Finite Impulse Response)**:
    - Uses only current input, always stable, and can have a linear phase response.
    - Requires more memory to match IIR filter performance.
    - Applications: Communication systems requiring precise phase preservation.
  
  - **Other Filters**:
    - **Bandpass Filter (BPF)**: Passes frequencies within a certain range.
    - **Lowpass Filter (LPF)**: Passes low frequencies and attenuates higher frequencies.

### Process Workflow

1. **Filter the audio**: Use a bandpass filter bank to divide the signal into multiple frequency bands.
2. **Plot signals**: Visualize the output of the lowest and highest frequency channels.
3. **Envelope extraction**:
   - Rectify the filtered signals.
   - Detect the envelope of the rectified signals using a lowpass filter with a 400 Hz cutoff.
4. **Plot envelopes**: Display the envelope of the lowest and highest frequency channels.

### Deliverables for Phase 2

- A short report (≤6 pages) documenting filter design activities.
- Include plots from Tasks 6 and 9 in the report.
- Submit code files.

## Phase 3: Generating Audio Output

### Inputs

- **Bandpass Filter Outputs (n)**: Combine the outputs from each frequency band to reconstruct the signal.
- **Normalization Parameters**: Use the absolute maximum value to normalize the combined signal.

### Processing Workflow

1. Generate a signal using a cosine function at the central frequency of each bandpass filter.
2. Modulate the amplitude of each cosine signal using the rectified signal from each bandpass filter.
3. Combine the modulated signals.
4. Normalize the combined signal.
5. Play the output sound and write it to a new file.

## Phase 4: Evaluate the Design

1. Use the evaluation metrics from Phase 1 to assess the performance of the signal processor.
2. Iterate by adjusting parameters and refining design choices.

## Phase 5: Design Iteration

### Parameters to Explore

- Linear vs. other spacing types between subbands (100 Hz - 8 kHz).
- Overlapping subbands.
- IIR vs. FIR filters.
- Different filter types.
- Effects of varying the cutoff frequency of the lowpass filter in envelope detection.

### Architecture Modifications

- Consider hardware limitations and design trade-offs such as channel count vs. power and complexity.

## Phase 6: Bonus Task

- Add a new evaluation metric to quantitatively assess the design.

## Phase 7: Report Writing

### Must-Have Sections

- Discussion of Tasks 14, 15, and 16 (and Bonus Task).
- Recommendation of the best design based on evaluation and iteration.
- Comparison of advantages and trade-offs between filtering techniques.

## Phase 8: Final Submission

### Deliverables

- Final report (≤6 pages).
- Code files.
- Input and output audio files.
