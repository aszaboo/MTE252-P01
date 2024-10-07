# Filter Research Summary Table

| **Filter Type**          | **Description**                                                                 | **Benefits**                                               | **Drawbacks**                                             | **When to Use**                                         |
|--------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------|
| **Bandpass Filters (BPF)** | Divide input signal into frequency bands.                                      | - Efficient frequency separation<br>- Can use IIR or FIR  | - IIR can be unstable<br>- FIR requires more coefficients | For segregating frequency bands in cochlear implants    |
| **IIR Filters**          | Infinite impulse response filters that use feedback.                           | - Computationally efficient<br>- Sharp cutoffs possible   | - Can be unstable<br>- Non-linear phase response         | When efficiency is crucial and phase response is less important |
| **FIR Filters**          | Finite impulse response filters without feedback.                              | - Always stable<br>- Linear phase response possible        | - More coefficients needed for sharp cutoffs              | When linear phase is important or stability is a concern |
| **Lowpass Filters (LPF)**| Allow signals below a certain frequency to pass through.                      | - Simple design<br>- Useful for envelope extraction        | - Limited to low frequencies                               | For envelope extraction in cochlear implant processing  |
| **Rectifiers**           | Convert AC signals to DC by removing negative parts.                          | - Simple implementation<br>- Useful for envelope detection | - May introduce distortion                                 | For rectifying output signals from bandpass filters     |
| **Modulation Filters**   | Used to modulate signals for transmission or processing.                       | - Can encode information in a carrier wave                | - Complexity in design                                    | When combining signals for output                       |
| **Gammatone Filters**    | Mimic the auditory system’s response to sound.                                | - Close approximation of human hearing                     | - More complex to implement                               | For advanced auditory modeling                          |
| **Constant-Q Filters**   | Maintain a constant quality factor across frequency bands.                    | - Good for music processing                                 | - More computationally intensive                           | When precise tonal control is needed                    |
| **Sampling Rate Handling**| Techniques to manage different sampling rates during processing.              | - Ensures compatibility with various audio formats        | - Requires careful design to avoid aliasing               | When dealing with audio files of varying sampling rates |
| **Mono/Stereo Handling**  | Techniques for managing single vs. dual-channel audio files.                 | - Flexibility in audio output                               | - Stereo to mono conversion may lose spatial information   | When processing audio files with different channel formats |

### Important Features to Engineer Around

- **Frequency Band Division**: Essential for separating different pitches.
- **Number of Channels**: Affects the granularity of frequency representation.
- **Frequency Spacing**: Determines how closely spaced the frequency bands are.
- **Filter Design**: Choice between IIR and FIR based on application needs.
- **Envelope Extraction**: Critical for capturing the amplitude variations of signals.
- **Modulation**: Important for combining multiple signals effectively.
- **Signal Combination**: Necessary for generating the final output signal.
- **Sampling Rate Handling**: Ensures compatibility and fidelity across different audio sources.
- **Mono/Stereo Handling**: Important for maintaining audio quality and spatial characteristics.

This table provides a clear overview of the various filter types, their applications, benefits, drawbacks, and when they should be used, making it easier to make informed decisions during your project.

Citations:
[1] <https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/13836420/ff8b1606-baf9-4662-93bf-08dcf49617c3/paste.txt>
[2] <https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/13836420/9a6fd791-2b65-4649-841a-900bd7b48414/paste.txt>
