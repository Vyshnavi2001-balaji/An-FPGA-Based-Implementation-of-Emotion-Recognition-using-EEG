# An-FPGA-Based-Implementation-of-Emotion-Recognition-using-EEG
An FPGA-Based Implementation

An electroencephalograph (EEG) is a device used to record electrical activity in the human brain through wearable metal electrodes placed on the scalp. Brain cells communicate via electrical impulses, which remain active even when the brain is at rest. This electrical activity is visualized as squiggly lines in EEG recordings.

In the processing phase, gaze-related EEG data is pre-processed within a frequency range of 0 to 75 Hz and sampled at 200 Hz, forming a new matrix. A finite impulse response (FIR) low-pass filter is applied to eliminate higher frequency components, as a band-pass filter could distort the EEG signals.

Each pre-processed EEG signal undergoes feature extraction, followed by feature reduction using Principal Component Analysis (PCA). PCA is an analytical technique based on singular value decomposition (SVD), which transforms correlated features into a set of uncorrelated principal components. The steps involved in PCA include:
(a) Mean normalization of features
(b) Calculation of the covariance matrix
(c) Extraction of eigenvectors
(d) Selection of principal components (reduced features)

These reduced features are then passed to a Support Vector Machine (SVM) classifier to predict sentiment.

For hardware implementation, VHDL code and a testbench were written for 2×2 matrix operations. Corresponding waveforms and RTL schematics were generated using Xilinx ISE 14.5. Additionally, a Simulink model was developed for FPGA implementation, where eigenvalues were pre-calculated using a System Generator.

## PROPOSED SOFTWARE METHODOLOGY:
![image](https://github.com/user-attachments/assets/08f018b4-2119-4c3b-87f7-a6b37c74cbf7)

## PROPOSED HARDWARE METHODOLOGY:
![image](https://github.com/user-attachments/assets/225ce1ad-5f17-45a9-8ed2-2442c8c86942)

## EXPERIMENTAL RESULTS
![image](https://github.com/user-attachments/assets/5ce923b0-3902-4659-9bfa-715ed7b8d9b3)

#### Simulation waveform of eigenvector calculation
![image](https://github.com/user-attachments/assets/5fa9fa75-00eb-4003-9ac9-ce4e44ebaf5d)

#### Schematic diagram of eigenvector calculation
![image](https://github.com/user-attachments/assets/8e360d00-8d35-4afe-b8f5-36aaa1e711e9)

#### RTL Schematic
![image](https://github.com/user-attachments/assets/36f3126f-cd5a-4f64-a216-48203fdd5f57)

#### Device utilization summary
![image](https://github.com/user-attachments/assets/462a5bd2-9c27-46df-ba97-a85c5ff10ded)

#### Simulink model for computing eigenvectors
![image](https://github.com/user-attachments/assets/b168c33e-887e-4f88-8683-06d9984f7a14)

#### Simulink generates a hardware model.
![image](https://github.com/user-attachments/assets/352963a0-b2be-4a16-8cf2-1f975604d6fd)

## CONCLUSION
This novel approach focuses on recognizing human emotions using EEG signals and implementing the system on an FPGA. The process begins with a preprocessing stage that filters the EEG signal within a frequency range of 0–75 Hz and applies a sampling rate of 200 Hz. After preprocessing and feature extraction, the EEG data is reduced to 620 features.

Principal Component Analysis (PCA) is then applied to reduce dimensionality by transforming the data into a set of uncorrelated principal components. These components are subsequently fed into a Support Vector Machine (SVM) classifier to predict the corresponding emotional state.

For hardware implementation, VHDL code and a testbench were developed for 2×2 matrix operations. Waveforms and RTL schematics were generated using Xilinx ISE 14.5. Additionally, a Simulink model was created for FPGA implementation, with eigenvalues pre-determined using the System Generator.








