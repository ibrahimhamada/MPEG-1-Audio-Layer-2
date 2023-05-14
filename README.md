# MPEG-1-Audio-Layer-2
The project aims to implement the MPEG audio Layer 2 without the bitstream formatting using MATLAB.

My Project of the Digital Signal Processing Course Offered in Fall 2021 @ Zewail City.

In this project, I implemented the MPEG audio Layer 2 (Encoder and Decoder) without the bitstream formatting using MATLAB.


## MPEG-1-Audio Encoder-Decoder <a name="MPEG-1-Audio Encoder-Decoder"></a>
![image](https://user-images.githubusercontent.com/58476343/220171522-e007785d-f6a8-44cd-9686-2338bf77839a.png)

## Implementation Steps:

A) MPEG audio Encoder Layer 2

            1) Reading PCM-coded digital audio from standard Windows. WAV file.
            2) Designing the essentials of time-to-frequency filter bank to break the input signal into 32 equally spaced frequency subbands.
            3) Using the downsampler which reduces the amount of data required for each sub-band. 
            4) A psychoacoustic model is applied to the input signal with a 1024-point FFT to determine which frequency bands should be retained. 
            5) Comparing the total length of the encoded bits in both cases. 
            6) The Allocation and coding block uses the data provided by the model to determine how to encode the sub-band signals. 
            7) To achieve data compression, the encoder ignores subbands that are completely masked by other signal components.
            8) Additionally, subbands that are partially masked are encoded with less accuracy than the dominant subbands.

B) MPEG audio Decoder Layer 2

            1) Designing the decoder that restores the quantized spectral components of the signal.
            2) Reconstructing the time-domain representation of the audio signal from its frequency representation.
            
C) Performance Measure

            1) Compression ratio: it is defined as the ratio of the original signal to the compressed signal.
            2) Mean Opinion Score (Subjective evaluation): The audience would listen to the sound files and see the sound quality and score it. It has to grades from 5 to 1. 
            3) PEAQ (Perceptual Evaluation of Audio Quality) (Objective evaluation): measures the ODG (Objective Difference Grade) between the original and the reconstructed signal. In Objective testing five-level impairment for Perceptual Evaluation of Audio Quality (PEAQ).
