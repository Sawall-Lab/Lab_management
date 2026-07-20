<p align="center">
  <img src="../../images/ASU_BIOS_Logo.png" 
       alt="ASU-BIOS Logo"
       height="140">
</p>

---

# Coral Protein Assay Protocol - Plate Reader
### Adapted from: Coral Reef Ecology Course
**Author(s):** Katelyn Saric  
**Lab:** Sawall Lab / MABEE Lab  
**Version:** v2.0  
**Date:** 2026-07-13  

## Contents

- [Materials checklist](#Materials_checklist)
- [Protocol](#Protocol)
  - [Coral Host and Zoox Tissue Preparation](#Coral_Host_and_Zoox_Tissue_Preparation)
  - [BSA Protein Standards Preparation](#BSA_Protein_Standards_Preparation)
  - [BCA Working Reagent Preparation](#BCA_Working_Reagent_Preparation)
  - [Microplate Procedure for Pierce BCA Protein Assay Kit](#Microplate_Procedure_for_Pierce_BCA_Protein_Assay_Kit)
  - [Plate Reader Program](#Plate_Reader_Program)
  - [Data Analysis](#Data_Analysis)

<h2 id="Materials_checklist">Materials checklist</h2>

$\square$ Pierce BCA Protein Assay Kit from Thermo Scientific  
$\square$ 96-well flat-bottom plastic plate  
$\square$ Incubator at 37°C  
$\square$ Plate reader Spectrophotometer  
$\square$ 1% and 5% SDS in MilliQ water  
$\square$ P1000 and P200 pipettes and tips  
$\square$ Clean 1.5ml microfuge tubes (Eppendorf cups)  
$\square$ Clean 50 mL Falcon tubes  
$\square$ MilliQ water  

<h2 id="Protocol">Protocol</h2>

<h4 id="Coral_Host_and_Zoox_Tissue_Preparation">Coral Host and Zoox Tissue Preparation</h4>

1. Thaw the **1 mL homogenate aliquot**. Turn on incubator and start preheating to 37°C.

2. Shake well to resuspend settled material. Keep samples on **ice**.

3. Centrifuge at **1500 rcf for 5 min** to separate zooxanthellae from host tissue. 

4. Carefully transfer the supernatant (host tissue) to a new **1.5 mL Eppendorf cup** labelled with coral ID, host/zoox, and undiltuted (e.g. P1a H undil). Try to get all the supernatant without disturbing the zooxanthellae pellet. Mix by pipetting, then add **900 µL** of the host slurry to a new **1.5 mL Eppendorf cup** labelled with coral ID and host/zoox (e.g. P1a H). Add **225 µL** of **5% SDS** to the host tissue to get a final concentration of 1% SDS.  

5. Add **400 µL of 1% SDS** to each zooxanthellae pellet and shake vigorously to resuspend the pellet.

6. Incubate the host tissue and zooxanthellae samples at **37 °C** for **15 mins**, shaking at **200 rpm**, to lyse the cells.
7. Centrifuge at **6000 rcf** for **5 min** to collect/remove cell debris from proteins in suspension.

<h4 id="BSA_Protein_Standards_Preparation">BSA Protein Standards Preparation</h4>

**Principle:** Measure the colour change that occurs when the BCA working reagent is added to the samples. The more protein in a sample (or standard), the stronger the colour change -- this is measured as absorbance on a plate reader. Create a standard curve with the concentrations below using the BSA standard provided by the kit.

- Standards are prepared in **1.5 mL microcentrifuge tubes**.
- Label the cap of each tube with the **Vial ID** ("A", "B", "C", etc.).

| Vial | Volume of MilliQ H₂O (µL) | Volume of BSA (µL) | [BSA] (µg / mL) |
|------|---------------------------|--------------------|-----------------|
| A | 0 | 300 of stock | 2000 |
| B | 125 | 375 of stock | 1500 |
| C | 325 | 325 of stock | 1000 |
| D | 175 | 175 of vial B dilution | 750 |
| E | 325 | 325 of vial C dilution | 500 |
| F | 325 | 325 of vial E dilution | 250 |
| G | 325 | 325 of vial F dilution | 125 |
| H | 400 | 100 of vial G dilution | 25 |
| I | 400 | 0 | 0 (blank) |
| SDS blank | 320 | 80 of 5% SDS | 0 (blank with SDS) |

<h4 id="BCA_Working_Reagent_Preparation">BCA Working Reagent Preparation</h4>

1. Use the following formula to determine the total volume of working reagent (WR) required for standards and samples. In the example above, **9 standards** are needed, and each sample and standard is run in **triplicate**.

   ```
   (9 standards + # samples) * (3 replicates) * (200 µL of WR) = total volume of WR required
   ```

2. Prepare WR by mixing **50 parts BCA Reagent A** with **1 part BCA Reagent B** (50:1, Reagent A:B) in a sterile 50 mL Falcon tube. The WR should be **green** in colour, and stored **in the dark** until you are ready to load it into your plate. The ratio is 50:1, so there are 50 + 1 = **51 total parts**.

   ```
   total WR volume / 51 parts = µL per part
   µL per part * number of parts = µL per reagent
   ```

3. Round up the volume to account for pipetting error.

<h4 id="Microplate_Procedure_for_Pierce_BCA_Protein_Assay_Kit">Microplate Procedure for Pierce BCA Protein Assay Kit</h4>

1. Pipette **25 µL** of each standard, blank or unknown sample into the microplate **in triplicate**.

2. Add **200 µL of the working reagent (WR)** to each well.

3. Cover the plate to keep it dark and incubate at **37 °C for 30 minutes at ~125 rpm**.

4. Remove the plate and allow it to cool to room temperature for **10 minutes** (keep it **covered / in the dark**).

5. Measure the absorbance at **562 nm** on a plate reader spectrophotometer **without the plate cover**. Before reading, make sure there are no bubbles in the wells. Pop them with a paperclip, wiping with a Kim wipe between wells. 

<h4 id="Plate_Reader_Program">Plate Reader Program</h4>

- **Plate reader:** SpectraMax M2
- **Software:** SoftMax Pro 7.1
- **Software Product Key:** 3338329450633820971

**1.** Start a new project: **Plate icon** in the top left-hand corner → **"New"**.
*Note: inside the project you can have different experiments, and different plates within each experiment.*

<p align="center">
  <img src="../../images/Protein_plate_reader/step1_new_project.png"
       alt="Step 1 — start a new project"
       width="500">
</p>

**2.** Change absorbance in **"Settings Information"**: change the value in the box to **562 nm** → **"OK"**.

<p align="center">
  <img src="../../images/Protein_plate_reader/step2_settings_information.png"
       alt="Step 2 — select "Settings Information""
       width="500">

<p align="center">
  <img src="../../images/Protein_plate_reader/step2_wavelength.png"
       alt="Step 2 — set wavelength to 562 nm"
       width="500">
</p>

**3.** Set the plate map in the **"Template Editor"**.

<p align="center">
  <img src="../../images/Protein_plate_reader/step3_template_editor.png"
       alt="Step 3 — open the Template Editor"
       width="500">
</p>

&nbsp;&nbsp;&nbsp;&nbsp;**a.** Set concentration units to **µg/mL** by clicking **"Edit"** and changing the units in the drop-down.

<p align="center">
  <img src="../../images/Protein_plate_reader/step3a_edit_units.png"
       alt="Step 3a — select "Edit" button"
       width="500">

<p align="center">
  <img src="../../images/Protein_plate_reader/step3a_units.png"
       alt="Step 3a — set concentration units to µg/mL"
       width="500">
</p>

&nbsp;&nbsp;&nbsp;&nbsp;**b.** Set standards.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**i.** Click **"Standards"** in the groups legend on the right-hand side.

<p align="center">
  <img src="../../images/Protein_plate_reader/step3b_i_click_standards.png"
       alt="Step 3b-i — click Standards in the groups legend"
       width="500">
</p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**ii.** Select the first triplicate of standards (click and drag) and enter the concentration of BSA (e.g. 2000 for A, 1500 for B, 1000 for C, etc.).

<p align="center">
  <img src="../../images/Protein_plate_reader/step3b_ii_enter_concentration.png"
       alt="Step 3b-ii — enter BSA concentration for each standard triplicate"
       width="500">
</p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**iii.** Continue until all standards are assigned their appropriate values.

<p align="center">
  <img src="../../images/Protein_plate_reader/step3b_iii_all_standards.png"
       alt="Step 3b-iii — all standards assigned"
       width="500">
</p>

&nbsp;&nbsp;&nbsp;&nbsp;**c.** Set unknowns.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**i.** Label the SDS blank triplicate and all samples with their coral ID on the plate map.

<p align="center">
  <img src="../../images/Protein_plate_reader/step3c_i_label_unknowns.png"
       alt="Step 3c-i — label SDS blank and samples with coral ID"
       width="500">
</p>

**4.** Place the plate in the plate reader **uncovered** and click the green **"Read"** icon in the top bar.

**5.** Export the data as an Excel file: **Plate icon** in the top left-hand corner → **"Export"** → **Export to XML XLS TXT** → export as an Excel file to a known location on the computer.

<p align="center">
  <img src="../../images/Protein_plate_reader/step5_export.png"
       alt="Step 5 — export data as Excel"
       width="500">
</p>

**6.** Save the project: **Plate icon** in the top left-hand corner → **"Save as"** → save to a known location on the computer.

<h4 id="Data_Analysis">Data Analysis</h4>

1. Subtract the average 562 nm absorbance of the **Blank** standard replicates from the 562 nm measurement of all other individual standard and unknown sample replicates. Take care to use the appropriate blank for the standard curve and for the samples. That is, subtract the mean of the **SDS blank** from the unknown samples, and the standard blank (**standard I**) from the other standards. 

<p align="center">
  <img src="../../images/Protein_plate_reader/Data_analysis/step1_blanks.jpg"
       alt="Step 1 — normalize data with blanks"
       width="500">

2. Check for outliers amoung both the standard and unknown triplicates. Remove necessary outliers to lower the SD, and calculate the mean absorbance for all samples. 

3. Prepare a **standard curve** by plotting the average blank-corrected 562 nm measurement for each BSA standard versus its concentration in µg/mL.

<p align="center">
  <img src="../../images/Protein_plate_reader/Data_analysis/step2_standardcurve.jpg"
       alt="Step 2 — plot standard curve"
       width="500">

4. Use the equation from the standard curve to calculate the protein concentration of each unknown sample in each well. 

<p align="center">
  <img src="../../images/Protein_plate_reader/Data_analysis/step3_concentration.jpg"
       alt="Step 3 — calculate protein conc per well"
       width="500">
  
5. Multiply the protein concentration per well by the **dilution factor** to get the corrected protein concentration for each unknown **host** sample. The dilution factor is equal to the total volume of host tissue plus the volume of SDS added (e.g. 900 µL host + 225 µL SDS = 1,125), divided by the volume of host tissue (e.g. 1,125 µL total / 900 µL host = 1.25). 

<p align="center">
  <img src="../../images/Protein_plate_reader/Data_analysis/step4_dilutionfactor.jpg"
       alt="Step 4 — calculate corrected host protein conc per well using dilution factor"
       width="500">

6. Divide the protein concentration per well by **2.5** to get the corrected protein concentration for each unknown **zoox** sample.

<p align="center">
  <img src="../../images/Protein_plate_reader/Data_analysis/step5_dilutionfactor.jpg"
       alt="Step 4 — calculate corrected zoox protein conc per well using dilution factor"
       width="500">

7. Multiply the corrected protein concentration by the **total slurry volume** measured in the tissue air picking protocol for each fragment ID to get the **total protein (μg)**. Then divide the total protein (μg) by the surface area of the coral fragment to get the protein per surface area (μg/cm^2). Divide by 1000 to get mg/cm^2. 

8. Calculate the mean protein concentration across all three replicates for each unknown sample.
