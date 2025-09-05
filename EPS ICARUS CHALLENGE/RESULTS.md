# RESULTS

## Figures/Screenshots 
- `figures/full circuit.png` — Shows the full connections of all the components.
- `figures/error while producing scope.png` — Overlap of the connections made by the wires which caused the error I think.
- `figures/scope produced.png` — The waveform is just a single line
- `figures/ ai generated image.png`- shows how to connect SPST to the resistors/load
- `figures/ ai generated image 2.png` - shows the basic connection of BUS and LOAD
- `figures/ numerical calculations.png`- shows the calculation of load resistances 

## Mapping between model elements and EPS functions
- Solar source → solar panels (time-varying current injection)
- Battery + 0.2 Ω → onboard battery and internal impedance
- 0.5 Ω EPS resistor → wiring/converter losses between BUS and loads
- Resistive loads (27.38 Ω, 54.76 Ω, 13.69 Ω) → OBC, ADCS, TT&C (calculated via R = V²/P)
- VCS (SPST) + square-wave drivers → software/hardware-controlled switching of payloads and bursts

## Key quantitative numbers (example)
- Maximum total load: 9 W → max current ≈ 1.216 A
- Voltage drop across EPS resistor (0.5 Ω) at full load ≈ 0.61 V
- Power lost in EPS resistor at full load ≈ 0.74 W

## Conclusions/ Observation / Expected output 
- These would have been the expected observation/outcome
- Battery Voltage (Vbatt): Should remain relatively stable or slightly increase during sunlight if the battery is charging, You'll notice slight voltage droops during high load bursts (like TT&C) due to the battery's internal resistance, Vbatt will be generally lower and show a more noticeable droop during eclipse, as the battery alone powers all loads.
-Battery Current(Ibatt): During sunlight, if total load is less than solar input, the battery will be charging (current flowing into the battery, potentially indicated by a negative sign), If total load demand exceeds solar input (e.g., during ADCS or TT&C bursts), the battery will discharge (current flowing out of the battery, likely positive current), During eclipse, the solar input is 0A, so the battery supplies all loads, and Ibatt will consistently show positive current (discharging).
- State Of Charge: This plot should generally trend upward during sunlight (indicating charge) and trend downward during eclipse (indicating discharge). This pattern should repeat consistently each orbit

## Errors and how to fix them
- Scope was not produced and when it was , it was just a straight line.
- To fix it :make the connections again and make sure when the connections are made there are no red dots at the end terminals.
