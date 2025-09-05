# EPS Simulation

**Minimal CubeSat Electrical Power System (EPS)** simulated in CircuitJS1 (Falstad Circuit Simulator).

## Description of the challenge
This model simulates a CubeSat Power System with:
- Solar source + MPPT with the battery is the power source
- Battery (7.4 V) with 0.2 Ω internal R
- Sqaure wave source is used as the solar source here cause my version lacked PWL 
- Three nodes:BUS,LOAD and GND(Ground)
- EPS loss resistor (0.5 Ω) between BUS and LOAD
- Satellite Loads: OBC (2 W), ADCS (1 W), TT&C (4 W), Payload (2 W). ADCS/TT&C/Payload are time controlled.
- SPST switches in series with each load resistor
- Sqaure wave sources connected to the SPST control pins

## How I approached the problem 
- Before opening the simulator, I researched about it and what does it do
- Opened a new circuit on the browser
- Used the menus Draw and Inputs and Sources
- Configured the components 
- Tried to add scopes but was unable to due to the error(error was that the wire loop detected)
- I checked my connections again , i remember slightly overlapping the wire with the components which might be the reason why scopes were not generated 
- I tried to fix it but using just AI I couldnt, I looked up in youtube but found nothing and due to the lack of time I decided to just go with what I have .

## How to open and run( I have mentioned the general menthod but due to the error in mine you wont be able to see the scopes)
1. Open CircuitJS1 using this link: https://falstad.com/circuit/  
2. File → Import From Text → paste the contents of `src/eps_cubesat_circuit.txt` → OK.  
3. Set simulation period to ~180 s (two orbits).  
4. Click **Run**. Adjust Simulation Speed if the trace runs too fast.
5. Use the scopes to examine `Vbatt`, `Ibatt` and `SOC`.

## Links/Tools used
- [Chatgpt](https://chatgpt.com/)
-[Notebooklm](https://notebooklm.google.com/)

