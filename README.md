jupyter notebook

# Thermoelectric Energy Harvesting from Car Exhausts 

A majorly untapped source of energy in modern industries is heat lost in operations. As a countermeasure to amend this tremendous waste of potential, thermoelectric materials can be utilized to convert heat  into electricity,  improving energy efficiency and sustainability. While challenges in sourcing efficient materials, scalability and cost-effectiveness still pertain, further research in this field driven by the need to transform energy systems and reduce carbon emissions can open doors to innovative solutions to tackle these obstacles. 

This project simulates power generation from thermoelectric materials placed on a car exhaust system. Using real-world material properties (Bi₂Te₃, PbTe, SnSe), it models the output voltage, power, and cumulative energy over a dynamic 10-minute drive cycle. Results are scaled to a realistic 200-leg thermoelectric module and benchmarked using each material's figure of merit (ZT).

---

## Physics Background

Thermoelectric generators (TEGs) convert heat directly into electricity via the **Seebeck effect**, where a voltage is generated when a material experiences a temperature gradient. The output power depends on the:
- **Seebeck coefficient (S)**: How much voltage per °K
- **Electrical conductivity (σ)**
- **Thermal conductivity (k)**
- **Temperature difference (ΔT)**

Performance is benchmarked using the **dimensionless figure of merit**:
\[
ZT = \frac{S^2 \sigma T}{k}
\]

---

## What the Code Does

- Simulates a fluctuating exhaust temperature over 600 seconds
- Calculates voltage and output power for each material
- Computes cumulative energy harvested over time
- Scales results for a 200-leg thermoelectric module
- Outputs results as:
  - CSV data: `results/thermoelectric_module_results.csv`
  - Plots: `figures/plots.png`

---

## File Structure

```
thermoelectric-energy-harvesting/
│
├── Modelling Thermoelectric Energy Harvesting from Car Exhausts.ipynb     
├── README.md
│
├── results/
│   └── thermoelectric_module_results.csv
│
└── figures/
    └── plots.png
```

---

## Materials Simulated

| Material | ZT (avg) | Notes |
|----------|----------|-------|
| Bi₂Te₃   | ~0.87    | Common near-room-temperature material |
| PbTe     | ~0.50    | Older mid-temp material              |
| SnSe     | ~2.44    | State-of-the-art high ZT performer   |

---

## ▶How to Run

### Prerequisites

Install dependencies:
```bash
pip install numpy matplotlib tabulate pandas
```

### Run the script:
```bash
python thermoelectric_simulator.py
```
or use `Run All` in Jupyter Notebook.

---

## Sample Output Table (200-leg module)

| Material | Total Energy (Wh) | Avg Power (μW) | Max Power (μW) | ZT (avg) |
|----------|-------------------|----------------|----------------|----------|
| Bi₂Te₃   | 0.0499             | 299,667        | 899,996        | 0.87     |
| PbTe     | 0.0384             | 230,144        | 691,197        | 0.50     |
| SnSe     | 0.0562             | 337,125        | 1,012,495      | 2.44     |

---

## Future Work

- Add Carnot efficiency comparisons
- Introduce variable load matching
- Visualize waste heat recovery potential in fuel savings
- Build a Streamlit or web dashboard for interactivity

---

## License

MIT License. Free to use and modify.

---

## Author

Created by Zainab Mahmood. Reach me at zainab.mahmood.23@ucl.ac.uk or visit https://www.linkedin.com/in/zainab-mahmood-mirza/.
