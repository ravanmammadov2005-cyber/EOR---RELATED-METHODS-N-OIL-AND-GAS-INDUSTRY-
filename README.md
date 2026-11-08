# EOR---RELATED-METHODS-N-OIL-AND-GAS-INDUSTRY-
Eor is one of the most important and cost-effective methods imposed by enginners on low pressure reservoirs to extract oil and improve the rate of production, as well as efficiency. There are too many sorts of EOR methods are applied according to given situation. 

Enhanced Oil Recovery (EOR) Screening & Analysis Tool 🛢️
​This project provides a straightforward methodology to evaluate, screen, and select the most effective Enhanced Oil Recovery (EOR) techniques based on fluid properties and reservoir characteristics.

​🎯 Project Purpose
​The primary objective is to streamline the initial screening phase of tertiary recovery. By analyzing key rock and fluid properties, this tool identifies technically viable EOR mechanisms to maximize ultimate oil recovery efficiency.

​💡 Supported EOR Methods & Mechanism Breakdown
​Gas Injection (CO2, Hydrocarbon, Nitrogen)
​Mechanism: Achieves miscibility or semi-miscibility with reservoir oil to reduce interfacial tension and swell the oil.
​Target: Light-to-medium oil reservoirs under high pressure.
​Chemical EOR (Polymer, Surfactant, Alkaline) 

​Mechanism: Increases displacing fluid viscosity (Polymer) or reduces capillary pressure and residual oil saturation (Surfactant/Alkaline).

​Target: Heterogeneous reservoirs with medium-viscosity oil.
​Thermal Recovery (Steam Flooding, SAGD, In-Situ Combustion)
​Mechanism: Introduces heat energy to drastically reduce heavy oil viscosity, improving mobilities and driving fluid movement.

​Target: Shallow reservoirs containing heavy or extra-heavy crude oil.
​📝 Practical Screening Examples

​Example 1: Medium Crude Reservoir
​Inputs: Viscosity = 25 cP | API Gravity = 24° API | Permeability = 150 mD
​Evaluation: The viscosity requires mobility control, while permeability is high enough to allow chemical injection.
​Recommended Method: Polymer Flooding

​Example 2: Deep Light-Oil Reservoir
​Inputs: Viscosity = 1.2 cP | API Gravity = 38° API | Depth = 2,800 m
​Evaluation: High pressure at depth combined with light crude creates ideal conditions for gas miscibility.
​Recommended Method: Miscible CO2 Injection

# Simple EOR Screening Tool 🛢️

A lightweight and clean Python script for quick **Enhanced Oil Recovery (EOR)** method screening based on oil viscosity.

---

## 📂 Project Structure

eor-tool/
├── main.py        # Single script containing the screening logic
└── README.md      # Project documentation

---

## 💻 Code (`main.py`)

Here is the entire code used in this project:

```python
def screen_eor(viscosity, api_gravity):
    print(f"--- Reservoir Parameters ---")
    print(f"Viscosity: {viscosity} cP")
    print(f"API Gravity: {api_gravity}° API\n")
    
    print("Recommended EOR Method:")
    if viscosity < 10 and api_gravity > 30:
        print("➡️ Gas Injection / Waterflooding")
    elif 10 <= viscosity <= 100:
        print("➡️ Polymer Flooding")
    else:
        print("➡️ Thermal Recovery (Steam / SAGD)")

if __name__ == "__main__":
    # Example: Medium-viscosity oil
    screen_eor(viscosity=25, api_gravity=24)
