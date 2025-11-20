<p align="center">
  <img src="../images/ASU_BIOS_Logo.png" 
       alt="ASU-BIOS Logo"
       height="140">
</p>

---

# Protocol for Chlorophyll-A Measurement 
**Author(s):** Roderick Bakker  
**Lab:** Sawall Lab / MABEE Lab  
**Version:** v1.0  
**Date:** 2023-12-07

## Overview 

This protocol is used for the measurement of Chlorophyll-A after the water samples have been collected and filtered, and the filters have been put in the freezer. The protocol for the collection and filtration process can be found [here](). 

## Contents

- [Risk Assessment](#Risk_Assessment)  
- [Solution Preparation](#Solution_Preparation)  
- [Sample Extraction](#Sample_Extraction)  
    - [Materials](#SE_Materials)
    - [Methods](#SE_Methods) 
- [Sample Preparation](#Sample_Preparation)  
    - [Materials](#A_Materials)
    - [Methods](#A_Methods)  

<h2 id="Risk_Assessment">Risk Assessment</h2>

| Substance | CAS | Hazards | Prevention |
|--------|----------------|--------|----------------|
| Acetone (90%) | 67-64-1 | H225: Flammable, H319: Eye irritant | Keep in ventilated space |
| Hydrochloric Acid (HCl, 1M) | 7647-01-0 | H314: Skin corrosion, H318: Eye damage | Wear gloves and eyewear |

<h2 id="Solution_Preparation">Solution Preparation</h2>

-	Acetone 90%: 1 : 9, MQ : Acetone (100%, HPLC grade)
-	HCl 1M: 11.1 : 1, MQ : HCl (12.1M, reagent grade)

<h2 id="Sample_Extraction">Sample Extraction</h2>

To be done the day before measurements.

<h4 id="SE_Materials">Materials</h4>

-	12mm culture tubes
-	Parafilm or reusable caps
-	Aluminium foil
-	Acetone (90%)
-	Chl-a samples 

<h4 id="SE_Methods">Methods</h4>

Note: perform in low light conditions.

1. Retrieve samples from the -80°C freezer.
2. Label a clean glass tube for each chl-a sample.
    - Don’t write on the tubes, use tape to label tubes or label their positions in the rack.
3. Transfer each filter to a glass tube, labelled with the corresponding sample ID.
4. Add 3mL 90% acetone and seal the tube with parafilm or a reusable cap.
5. Vortex for 5 seconds. 
    - Make sure the filter is fully submerged in acetone afterwards.
6. Cover the sample rack in aluminium foil.
7. Leave the samples overnight at -20°C (no more than 24 hours).

<h2 id="Sample_Preparation">Sample Preparation</h2>

<h4 id="A_Materials">Materials</h4>

-	Trilogy + Chl-a Acid module + 12mm tube adapter
-	Extracted chl-a samples from previous day
-	12mm culture tube
-	90% Acetone
-	Secondary chl-a standard
-	Spatula
-	1M HCl
-	Pasteur pipet
-	[“chlorophyl-a_trilogy_raw_fluorescence” datasheet](../Chlorophyll-A/chlorophyl-a_trilogy_raw_fluorescence_template.xlsx)

<h4 id="A_Methods">Methods</h4>

Note: perform in low light conditions.

1. Turn on the trilogy to allow it to warm up whilst samples are being prepared.
2. Remove extracted samples from the -20°C freezer.
3. Vortex each tube for 5 seconds.
4. Remove the 12mm tube adapter from the trilogy and measure the secondary standard, note value in excel sheet (B2).
5. Place the 12mm tube adapter back in the trilogy.
6. Add 3mL acetone to a 12mm culture tube and measure, note value in excel sheet (B3).
7. To measure samples: remove filter from the tube with a blunt tip spatula and discard.
    - If using a reusable spatula, rinse with MQ and dry in between samples.
8. Place the sample in the trilogy.
9. Measure raw fluorescence and note value as F0 (column C).
10. Take the tube from the trilogy and add 3 drops of 1M HCL and gently shake the tube.
11.	Place the sample back in the trilogy.
12.	Measure raw fluorescence and note value as FA (column D).
13.	Repeat steps 7-12 for all samples.
14.	Input sample and solvent volumes, the sheet will calculate concentrations.
15.	Dispose of samples and blank in acetone waste bottle, leave tubes overnight in fumehood and dispose with regular glassware.
