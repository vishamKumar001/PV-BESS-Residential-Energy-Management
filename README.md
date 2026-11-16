# PV-BESS Residential Energy Management System

**Design and Simulation of a Rule-Based Energy Management System for Peak Load Reduction in a Residential PV-Battery Hybrid System**

## Project Overview

This project focuses on the design and simulation of a rule-based Energy Management System (EMS) for a grid-connected residential solar PV and Battery Energy Storage System (BESS).

The system coordinates power flow between solar PV generation, battery storage, residential load demand and the utility grid to reduce peak grid dependency.

A MATLAB/Simulink-based model implements real-time power balancing and SOC-constrained battery charging and discharging strategies over a 24-hour operating cycle.

## System Specifications

| Parameter | Specification |
|---|---|
| Solar PV Capacity | 4 kW |
| Battery Storage Capacity | 10 kWh |
| Maximum Battery Charge/Discharge Power | 2 kW |
| Battery SOC Operating Range | 20–95% |
| Simulation Duration | 24 Hours |
| Simulation Platform | MATLAB/Simulink |
| EMS Strategy | Rule-Based Control |

## Key Features

- Residential grid-connected solar PV and BESS modelling.
- Rule-based Energy Management System development.
- Peak load shaving through controlled battery discharge.
- Surplus solar energy utilization through battery charging.
- SOC-constrained battery energy management.
- Grid power import and export monitoring.
- 24-hour simulation using solar irradiance, temperature and residential load profiles.
- Baseline versus EMS-controlled performance comparison.

## System Architecture

The system consists of four main energy components coordinated by a central EMS controller:

1. **Solar PV Array:** A 4 kW solar generation system supplying residential loads and battery charging.
2. **Battery Energy Storage System:** A 10 kWh battery with a maximum charge/discharge power of 2 kW.
3. **Residential Load:** A household demand profile with morning and evening peak consumption.
4. **Utility Grid:** Supplies the remaining demand and receives surplus energy when applicable.

The EMS regulates power flow between these components based on generation, demand and battery SOC.

## Energy Management Strategy

The proposed EMS operates in two primary modes:

### 1. Peak Shaving Mode (Load > PV)

When household demand exceeds PV generation, the EMS commands the battery to discharge and compensate for the power deficit, subject to battery power and SOC constraints.

### 2. Energy Storage Mode (PV > Load)

When PV generation exceeds household demand, surplus solar energy is used to charge the battery. Once the battery reaches its upper SOC limit, excess generation is exported to the grid.

## Simulation Results

The system was evaluated over a complete 24-hour operating cycle using MATLAB/Simulink.

The simulation examined:

- Solar irradiance and ambient temperature profiles.
- Residential household load variations.
- PV generation and grid power exchange.
- Battery charging and discharging behaviour.
- Battery State of Charge throughout the operating cycle.

### Key Performance Outcomes

- Reduced peak grid import from approximately 4.5 kW to 2.8 kW.
- Achieved approximately 38% peak demand reduction according to the report's summary results.
- Maintained battery SOC within the specified 20–95% operating range.
- Demonstrated coordinated utilization of solar generation and battery storage.

## Technologies Used

| Category | Technology |
|---|---|
| Simulation | MATLAB |
| System Modelling | Simulink |
| Energy Management | Rule-Based EMS |
| Renewable Energy | Solar PV |
| Energy Storage | Battery Energy Storage System |
| Control Strategy | Peak Shaving and SOC Constraints |

## Repository Structure

- `MATLAB/` – Simulation scripts and EMS control logic.
- `Simulink/` – PV-BESS system model.
- `Documentation/` – Detailed project report.
- `Figures/` – System architecture, flowchart and simulation plots.
- `Results/` – Simulation outputs and performance comparisons.

## Limitations

This project is based on simulation and mathematical component representations. It does not include physical hardware validation, detailed battery ageing or thermal degradation modelling.

## Future Improvements

- Implement the EMS algorithm on an embedded controller.
- Integrate real-time PV generation and household load measurements.
- Introduce solar and load forecasting.
- Evaluate advanced optimization-based energy management strategies.
- Validate the control strategy using a physical PV-BESS prototype.

## Contributors

- Dhivya R.
- Mahalakshmi I.
- Visham Kumar V.

Department of Electrical and Electronics Engineering  
Amrita Vishwa Vidyapeetham, Coimbatore, India
