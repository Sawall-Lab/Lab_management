<p align="center">
  <img src="../../images/ASU_BIOS_Logo.png" 
       alt="ASU-BIOS Logo"
       height="140">
</p>

---

# Quantifying Chlorophyll-*a* and Chlorophyll-*c2* concentrations in coral tissue
### Adapted from: Adapted from Dr. Hollie Putman’s protocol
**Author(s):** Dr. Chloe Carbonne  
**Lab:** Sawall Lab / MABEE Lab  
**Version:** v1.0  
**Date:** 2025-11-12

## Contents

- [Materials checklist](#Materials_checklist)
- [Protocol](#Protocol)
  - [Sample Preparation](#Sample_preparation)
  - [Plate Setup](#Plate_setup)
  - [Measuring Absorbance](#Measuring-absorbance)
  - [Calculating Chlorophyll Concentration](#Calculate_chl_concentration)
  - [Path Length Correction](#Path_length_correction)
- [References](#References)

<h2 id="Materials_checklist">Materials checklist</h2>

$\square$ 100% acetone  
$\square$ Flammable-safe fridge (4 °C)  
$\square$ Quartz 96-well plate  
$\square$ Glass plate lid (plastic lids will melt)  
$\square$ Refrigerated centrifuge  
$\square$ 10 mL glass syringe  
$\square$ 2 mL microcentrifuge tubes  
$\square$ Q-tips  
$\square$ Labeling tape  
$\square$ Microplate reader (λ 630, 663, 750 nm)  
$\square$ Homogenizer (Ultra-Turrax type)  
$\square$ Sonicator with adjustable amplitude  
$\square$ Vortex mixer  
$\square$ Parafilm (optional)

<h2 id="Protocol">Protocol</h2>

<h4 id="Sample_preparation">Sample Preparation</h4>

1. Prepare a **500 µL aliquot** of adult airbrush homogenate (coral slurry) in a **2 mL microcentrifuge tube**.

2. Add **1 mL of 100% acetone** to the slurry using a **10 mL glass syringe**.

3. Vortex tubes for **15 seconds**.

   - If the pellet does not dissolve or tissue chunks remain:
     - Sonicate **2 × 5 seconds**, **100% amplitude**
     - Keep tubes **on ice**
     - Avoid evaporation as much as possible

4. Place tubes **in the dark** at **4 °C** for **24 hours**.

5. After incubation, sonicate again:
   - **2 × 5 seconds**, **100% amplitude**, on ice

6. Centrifuge tubes at **2,000 rpm for 3 minutes** to pellet debris.

<h4 id="Plate_setup">Plate Setup</h4>

1. Use the plate template to **map sample positions**.

2. Pipette:
   - **200 µL** of each sample into **triplicate wells**
   - **200 µL acetone blanks** into:
     - First 3 wells
     - Last 3 wells

3. As you fill the plate:
   - Cover every ~3 columns with the **glass lid or parafilm**
   - Use another plate (or object of equal height) to support the lid and maintain balance

4. Once the plate is complete, **fully cover with the glass lid**.

<h4 id="Measuring absorbance">Measuring Absorbance</h4>

1. Measure absorbance at:
   - **630 nm**
   - **663 nm**
   - **750 nm**

2. Using Roger Lab’s plate reader:
   - Open **Gen5 software**
   - The **Task Manager** will open automatically
   - Select protocol: **“Chloe_Chla”**

<h4 id="Calculate_chl_concentration">Calculating Chlorophyll Concentration</h4>

1. Subtract **A750** from all absorbance measurements.

2. Calculate chlorophyll *a* and *c2* concentrations using equations from  
   **Jeffrey & Humphrey (1975)**.

<h4 id="Path_length_correction">Path Length Correction</h4>

Because well-plate path length differs from a 1 cm cuvette, apply a correction following **Warren (2007)**.

- Path length correction factor used here: **0.6 cm**
- This value may vary by instrument

#### Corrected Absorbance Calculations


data$c630.corr <- (data$c630 - data$c750) / 0.6
data$c663.corr <- (data$c663 - data$c750) / 0.6
Units of concentration: µg mL⁻¹

To calculate a plate-specific path length, follow the procedure described in Warren (2007).

<h2 id="References">References</h2>
References

Jeffrey, S. W. & Humphrey, G. F. (1975)
New spectrophotometric equations for determining chlorophylls a, b, c1 and c2

Warren, C. R. (2007)
Standards for chlorophyll measurement

Synergy HTX Operating Manual

Gen5 Software Manual
