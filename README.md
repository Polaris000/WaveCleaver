# WaveCleaver


### About
The aim of this project is to build a deep learning system that identifies the human voice and isolates the other sources of sound from a single waveform. The application of this technology is extensive, with potential benefits including improved performance of noise-canceling systems and enhanced quality of audio communications.

### Results

| Experiment            | SDR Metric  |
|-----------------------|--------|
| Bandpass Filter       | 7.8    |
| Spectral Gating       | 7.2    |
| Sepformer             | 10.4   |
| Conv-TasNet           | 8.53   |
| Waveform AutoEncoder  | -3.1   |
| Spectogram AutoEncoder| 13.77  |
---


### Usage

#### Environment Setup
1. **Install Conda**: If you haven't already, install Conda by following the instructions on the [official Conda documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html).

2. **Create a New Environment**: Open your terminal or command prompt and run the following command to create a new Conda environment. Replace `myenv` with your desired environment name.

    ```bash
    conda create --name myenv
    ```

3. **Activate the Environment**: Once the environment is created, activate it using the following command:

    ```bash
    conda activate myenv
    ```


4. **Install Dependencies**: Once you have your `requirements.txt` file ready, you can install all the dependencies listed in it using `pip`. Run the following command in your terminal:

    ```bash
    pip install -r requirements.txt
    ```


#### Running the experiments
The experiments above were run via notebooks. Simply follow the general setup steps, then run the notebooks top-down.


---
### Files
- In `/data` we have all the relevant files for the custom test dataset, our model inferencing results as .csv files, and the .csv files for all of our loss and accuracy curves
- In the `/notebooks` path we have the notebooks for all of our experimentation.
- Our from scratch model can be found in `notebooks/spectogram_autoencoder.ipynb` and `notebooks/autoencoder.ipynb`
- Our non-ml methods can be found in `notebooks/Python_Noise_Reduction_Methods.ipynb`
- Our experiments for inferencing can be found in `notebooks/pretained_sound_separation.ipynb` and `notebooks/sepformer.ipynb`
- Our attempt at transfer learning on demucs can be found in `notebook/finetuning-demucs.ipynb`
