# SIM Image Simulation and Reconstruction in Python

##  Overview
This project demonstrates the principles of **Structured Illumination Microscopy (SIM)** using a Python-based simulation pipeline.  
SIM is an advanced imaging technique that surpasses the diffraction limit by projecting sinusoidal illumination patterns onto a sample, thereby shifting high-frequency details into the observable frequency band of a microscope.

The repository contains:
- Python scripts for simulation and reconstruction
- Figures generated during the workflow
- Final project report (PDF/Word)

---

##  Workflow
The simulation consists of the following steps:

1. **Ground Truth (GT) Image Generation**  
   Synthetic image with simple objects and a scale bar.  

2. **Low-pass Filtering**  
   Simulates microscope blurring due to diffraction.  

3. **Structured Illumination**  
   Multiplication of the blurred GT image with a sinusoidal grating pattern to simulate interference illumination.  

4. **Fourier Analysis**  
   FFT of GT and modulated images to visualize how sidebands (frequency shifts) appear.  

5. **Frequency Separation**  
   Filtering in Fourier space to separate low- and high-frequency components.  

6. **Reconstruction**  
   Combining frequency components to produce a higher-resolution image.  

7. **Noise Simulation**  
   Addition of Gaussian and Poisson noise to mimic real microscopy conditions, followed by reconstruction.  

---

##  Results
- SIM improves resolution by recovering high-frequency details lost in conventional microscopy.  
- Fourier domain analysis confirms the presence of **sidebands** caused by sinusoidal illumination.  
- Reconstruction yields sharper images compared to low-pass blurred ones.  
- Noise reduces clarity but SIM still provides resolution gains.  

| Step            | Observation |
|-----------------|-------------|
| GT              | Full frequency content |
| Low-pass        | High frequencies lost |
| Modulated       | Frequency shifted by grating |
| FFT             | Sidebands visible |
| Reconstruction  | Sharper than blurred |
| With Noise      | Degraded but still improved |

---

## ⚙ Installation & Usage
Clone the repo and install required Python packages:
```bash
git clone https://github.com/your-username/SIM-Simulation.git
cd SIM-Simulation
pip install -r requirements.txt
