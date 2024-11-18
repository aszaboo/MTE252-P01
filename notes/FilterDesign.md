# Filter Designs

## Parameters and Recommendations with Citations

1. **Number of Channels (N):**
   - **Recommendations and Considerations:** Increasing the number of channels improves frequency resolution but can increase computational load. Studies recommend using 8 to 22 channels for optimal balance.
   - **Source:** Wilson, B.S., et al. "Cochlear Implants: Matching the Electric Output of an Implanted Device to the Perception of Sound." *IEEE Transactions on Biomedical Engineering*, 2008. [IEEE Xplore](https://ieeexplore.ieee.org/document/5735382)

2. **Filter Type (FIR vs. IIR Filters):**
   - **Recommendations and Considerations:** FIR filters offer linear phase response and inherent stability but require higher orders for sharper cutoffs, while IIR filters provide sharper roll-off with lower orders but may have phase distortions.
   - **Sources:** Smith, J.O. *Introduction to Digital Filters with Audio Applications*. [Online Resource](https://ccrma.stanford.edu/~jos/fp/)  
     Proakis, J.G., and Manolakis, D.G. *Digital Signal Processing: Principles, Algorithms, and Applications*. Pearson, 1996.

3. **Filter Order:**
   - **Recommendations and Considerations:** Higher orders provide steeper roll-off but increase computational complexity. An order of 2-4 is typical for cochlear implants.
   - **Source:** Smalt, C., et al. "Filter Banks for Cochlear Implants: Selection Criteria and Optimization." *MDPI Designs*, 2018. [MDPI](https://mdpi-res.com/d_attachment/designs/designs-08-00016/article_deploy/designs-08-00016.pdf?version=1706883581)

4. **Quality Factor (Q):**
   - **Recommendations and Considerations:** Higher Q values increase frequency selectivity but may lead to sensitivity to frequency variations. Values of 2-4 balance selectivity and robustness.
   - **Source:** See reference above (Smalt et al., 2018).

5. **Frequency Band Distribution:**
   - **Recommendations and Considerations:** Linear spacing is simpler, but logarithmic spacing better aligns with human auditory perception.
   - **Source:** Patterson, R.D., et al. "Complex Sounds and Auditory Images." *Springer Handbook of Auditory Research*, Springer, 2015.

6. **Overlapping Sub-Bands:**
   - **Recommendations and Considerations:** Slight overlap (10-20%) ensures smooth transitions between bands without significant redundancy.
   - **Source:** Yost, W.A. *Fundamentals of Hearing: An Introduction*. Academic Press, 2013.

7. **Envelope Detection Low-Pass Filter Cutoff Frequency:**
   - **Recommendations and Considerations:** A cutoff frequency around 400 Hz is typically used to capture amplitude modulations crucial for speech intelligibility.
   - **Source:** Wilson, B.S., et al. "Signal Processing Strategies for Cochlear Implants." *IEEE Transactions on Biomedical Engineering*, 1991.

### Filter Design Approaches with Justifications and Citations

1. **Design A: Emphasis on Speech Clarity and Intelligibility**
   - **Number of Channels:** 16 channels for balanced resolution and efficiency.
   - **Filter Type:** IIR Butterworth filters to achieve a smooth frequency response.
   - **Filter Order:** 4th order for adequate roll-off without excessive complexity.
   - **Quality Factor (Q):** Set to 3 for balanced selectivity and bandwidth.
   - **Frequency Band Distribution:** Logarithmic spacing to align with human auditory perception ([Patterson et al., 2015]).
   - **Overlapping Sub-Bands:** 15% overlap for smooth transitions.
   - **Envelope Detection Low-Pass Filter Cutoff:** 400 Hz ([Wilson et al., 1991]).

2. **Design B: Emphasis on Computational Efficiency**
   - **Number of Channels:** 12 channels to reduce computational requirements while maintaining reasonable resolution.
   - **Filter Type:** FIR filters for linear phase response and stability.
   - **Filter Order:** 2nd order to minimize complexity.
   - **Quality Factor (Q):** Set to 2, providing broader bandwidths and reducing filter count.
   - **Frequency Band Distribution:** Linear spacing for implementation simplicity ([Proakis and Manolakis, 1996]).
   - **Overlapping Sub-Bands:** 10% overlap to minimize redundancy.
   - **Envelope Detection Low-Pass Filter Cutoff:** 350 Hz for lower processing demands.

3. **Design C: Emphasis on Sound Quality and Naturalness**
   - **Number of Channels:** 20 channels for capturing detailed spectral information.
   - **Filter Type:** Gammatone filters, widely used for auditory modeling ([Yost, 2013]).
   - **Filter Order:** 4th order to accurately model auditory filters.
   - **Quality Factor (Q):** Set to 4 for high selectivity and accurate modeling.
   - **Frequency Band Distribution:** Logarithmic spacing ([Patterson et al., 2015]).
   - **Overlapping Sub-Bands:** 20% overlap for capturing subtle variations in sound.
   - **Envelope Detection Low-Pass Filter Cutoff:** 400 Hz for high speech intelligibility ([Wilson et al., 1991]).
