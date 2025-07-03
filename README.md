# Simulink Model README

## Overview
This model implements a comprehensive simulation of an air conditioner based on vapour compression refrigeration cycle. The major focus is to control temperature and humidity within specified limits by varying compressor rpm and fan speeds. The model is designed in simulink. The deliverables include:
- Simulink Model (.slx file)
- Matlab File(.mat file)
- Documentation (.pdf file)
- Markdown File (.md file)

---

## Features 

- **Temperature and Humidity Control**: Ensures that dry bulb temperature is maintained at 27 degree celsius and wet bulb temperature is maintained at 19 degree celsius.

- **PID Control**: Dynamically varies the compressor RPM and indoor fan speed based on load conditions.

- **Simscape Fluids**: Uses the Simscape Fluids library for modelling of compressor, evaporators, condensers and expansion valve.

---

## Files and Directory Structure

- **hvac_l2_albatrossenergetics.slx**: The Simulink file containing the model and control logic.

- **matlab.mat**: The matlab.mat file where all the variables are defined.

- **30_l2_albatrossenergetics.pdf**: Detailed documentation of the model.

- **README.md**: This file, giving an overview and usage instructions.

- **Superheat_Subcool.m**: After running the model, run this file to plot superheat and subcool.

---

## Installation and Requirements

### **Software** 

- **Matlab** : 2024a or later (compatible with Simulink and Simscape Fluids)
- **Simulink** : Required for dynamic system modelling.
- **Simscape Fluids** : Necessary for component-based modelling.

### **Dependencies**
Ensure the following MATLAB toolboxes are installed:
- **Simulink**
- **Simscape**
- **Simscape Fluids**

---

## Usage Instructions

1. Open the **Simulink Model**:
   - Open hvac_l2_albatrossenergetics.slx in MATLAB.
   - Open matlab.mat and save all the variables defined in your MATLAB workspace.
   - Run the simulation to observe system performance under varying load conditions.

2. Read the **Report**:
    - Refer to 30_l2_albatrossenergetics.pdf for detailed explanation of model and simulation results.

3. In each subsection mentioned below in the model, there are scope blocks. By clicking on scope block of respective subsystem, you will get the desired plot.

---

## Subsystem Descriptions

### 1. COP and EER Data Subsystem
This subsystem calculates the Coefficient of Performance (COP) and Energy Efficiency Ratio (EER) of the system based on input parameters. It includes a dedicated section for efficiency calculations.

### 2. Superheating and Subcooling Plot Subsystem
Provides a visual representation of superheating and subcooling trends in the system. This helps in analyzing the thermal performance and safety limits.

### 3. Saturation Pressure/Temperature and Mass Flow Subsystem
Computes and displays the saturation pressure, temperature, and mass flow rate for the refrigerant used in the system.

### 4. Results Subsystem
Outputs key results such as temperature, pressure, and enthalpy data. Includes P-H diagrams for thermodynamic analysis.

### 5. Power Parameters Subsystem
Calculates and displays power consumption and other energy parameters to evaluate system performance.

### 6. Work Function Subsystem
Contains functions for calculating the fan's work, which contributes to the cooling system's overall performance.

### 7. Cooling Load Data Subsystem
Computes and visualizes the cooling load of the system in kilowatts, along with the corresponding cooling power.

### 8. External Environment Subsystem
External Environment contains the condenser fan and fan drive. 

### 9.House Subsystem
House subsystem contains the evaporator fan and fan drive. It also contains measurement properties block which measures specific humidity. There is one another block which measures relative humidity.There is moisture gain and occupant heat gain blocks which are the sources of latent and sensible heat load respectively.

### 10. Verification Subsystem
Includes tools to verify the system's functionality and ensure all components are performing as expected.

### 11. Safety System Subsystem
Contains safety protocols to prevent damage to the system under extreme operating conditions.

### 12. Compressor Drive Subsystem
Manages the compressor's operation and drive signals to optimize refrigerant flow and energy efficiency.





## Highlights

- The model ensures optimal system performance while adhering to constraints such as:
  - Time to reach target conditions: **<10 minutes**
  - Energy Efficiency
  - Environmental Consideration

  
- The system dynamically varies **compressor RPM** and **fan speeds** based on the indoor conditions, outdoor conditions and heat load.

---

