# Battery Simulation Project

### 1. Installations  
To run this project, you need to have Python installed along with the following libraries:  
- `pandas`  
- `numpy`  
- `os`  

You can install the required libraries using pip:  
```bash
pip install pandas numpy
```

Ensure that the folder `pv_data` contains the CSV files for the simulation, as described below.  

---

### 2. Project Motivation  
The purpose of this project is to simulate the charging and discharging of a battery storage system over a year, using real photovoltaic (PV) generation and consumption data. By analyzing the energy flow between the PV system, battery, and grid, this project aims to:  
- Evaluate how much energy is stored in the battery.  
- Determine how much energy is discharged to power consumption.  
- Calculate the surplus energy fed into the grid.  
- Quantify the dependency on grid power.  

This project allows homeowners, businesses, or researchers to assess the performance of battery storage systems and identify potential energy savings over time.  

---

### 3. File Descriptions  
The project consists of the following files and folders:  

#### Python Code  
- **main.py**: The main program that runs the simulation. It includes the following components:  
  - Validates and corrects the CSV files (if necessary).  
  - Simulates the battery behavior based on PV generation, consumption, and grid interaction.  
  - Generates a summary report (`simulation_report.txt`) with key statistics.  

#### Data Files  
- **pv_data/**: A folder containing daily CSV files of PV and consumption data. Each file represents one day and includes columns such as:  
  - `PV-Erzeugung / Mittelwerte [W]` (or `[kW]`) – PV generation data.  
  - `Eigenverbrauch / Mittelwerte [W]` – Power consumption data.  
  - `Netzbezug / Mittelwerte [W]` – Grid power usage data.  

#### Output  
- **simulation_report.txt**: A text file summarizing the simulation results, including stored energy, discharged energy, grid feed-in, grid draw, and battery status at the end of the simulation.  

---

### 4. How to Interact with Your Project  

1. **Prepare the Data:**  
   - Ensure the daily PV data files are stored in the `pv_data` folder.  
   - Each file must follow the correct structure, with timestamps and relevant columns for PV generation, consumption, and grid usage.  

2. **Run the Simulation:**  
   - Execute the Python script using the following command:  
     ```bash
     python main.py
     ```  

3. **Validation and Correction:**  
   - The script automatically checks if any files have inconsistent units (e.g., `[kW]` instead of `[W]`) or incorrect column names. If issues are found, the script corrects and overwrites the files.  

4. **View Results:**  
   - After the simulation, open the `simulation_report.txt` file to review the results. This file will provide key metrics like:  
     - Total energy stored in the battery.  
     - Total energy discharged from the battery.  
     - Energy fed into the grid.  
     - Energy drawn from the grid.  

---

### 5. Licensing, Authors, Acknowledgements, etc.  

**Licensing:**  
This project is open-source and released under the MIT License. Feel free to use and modify the code as needed for personal or commercial use.  

**Authors:**  
This project was developed by Yannick Gorda

--- 

Feel free to customize this Reader file further to reflect specific project details or additional contributors.
