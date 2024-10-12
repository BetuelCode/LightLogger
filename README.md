# Overview
This repository contains the Light Logger project, which involves the acquisition of calibration data with an emphasis on spectral and directional analysis. You will find both the raw sensor and spectrometer data within this repository. The provided code is intended for data visualization and analysis, and is accessible under the MIT license (see `LICENSE.md` file).

If you have any comments or queries, please reach out to us at b.kayacik@web.de and manuel.spitschan@tum.de.

# Dependency Management
This Python project utilizes **pip** for package management. Use `pip install -r requirements.txt` to download the correct package versions (the given version or higher) and ensure computational reproducibility. When running the Python code files, make sure to use a virtual environment (e.g., created with venv or conda) to avoid issues with package dependencies and working directories.

# Workflow description 
Here we explain the Python script processing for analyzing 
- Characterization of UV channels
- Spectral sensitivity
- Directional dependance of the novel light logger and
- Diffuser testing.

Each step includes the corresponding raw data, along with the data preparation and calculations necessary for visualization.

### Step 1: Characterization of UV channels

#### Spectrometer
Folder: `01_UV` <br>
Input: `file1 - file12.csv`  <br>
Output: `UV_spectrometer_code.ipynb` <br>
Code: `UV_spectrometer_code.ipynb`

For the calibration of the UV channels, the corresponding data from the OceanOptics spectrometer can be found in this folder `01_UV`. The data file containing all acquired spectrometer data is in `01_UV/spectrometer_data`. Hereby, the CSV files in the `filtered` folder were used, which contain only the relevant information obtained from the raw data.

**Note:** We have also included the raw data with all acquired data from the OceanOptics spectrometer, which can be found in the folder `rawdata`.  


#### Sensor
Folder: `01_UV` <br>
Input: `sensor_parameter.csv` <br>
Output: `UV_sensor_code.ipynb` <br>
Code: `UV_sensor_code.ipynb`

In order to develop an algorithm that automatically adjusts the parameters to changing light conditions, data with varying parameters were tested. The corresponding data can be found in this folder: `sensor_data`.

#### Algorithm
Folder: `01_UV` <br>
Input: `sensor_algorithm.csv` <br>
Output: `UV_algorithm_code.ipynb` <br>
Code: `UV_algorithm_code.ipynb`

After developing the algorithm, sensor data was collected (see folder `sensor_data`).

### Ste 2: Spectral sensitivity
Folder: `02_Spectral` <br>
Input (sensor): `spectral_sensor_10% - 100%.csv` <br>
Input (spectrometer): `spectral_Jeti_10% - 100%.csv`, `spectral_Jeti_all intensities.csv`, `total_irradiance.csv` <br>
Output: `spectral_code.ipynb` <br>
Code: `spectral_code.ipynb`

The data required to run the code is organized into separate folders (`sensor_data` and `jeti_data`) containing sensor data and spectrometer data.

### Step 3: Directional dependance
Folder: `03_Directional`<br>
Input (sensor): `direc_sensor_450-550nm.csv`, `normalized_sensor_450-550nm.csv` <br>
Input (spectrometer): `direc_450-550nm.csv` <br>
Output: `directional_code.ipynb`<br>
Code: `directional_code.ipynb`

### Step 3: Diffuser testing
Folder: `03_Directional`<br>
Input: `directional_pure_sensor+truebungskon0,5%-2%.csv`, `trübungskon0,5%-2%_normalized.csv` <br>
Output: `directional_code.ipynb`<br>
Code: `directional_code.ipynb`



