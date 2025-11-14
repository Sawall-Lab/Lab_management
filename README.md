<p align="center">
  <img src="images/MABEE_Logo_Wide.png" 
       alt="MABEE Lab Logo"
       height="140">
</p>

---

# 🧪 **Sawall Lab / MABEE Lab — Lab Management Repository**  
### *Field Manuals • Lab Equipment Guides • Sampling Protocols • Analysis SOPs*

This repository serves as the central hub for **protocols**, **equipment manuals**, and **lab SOPs** used across the Sawall Lab / MABEE Lab at **ASU BIOS**.  
It is designed to maintain **standardization**, **reproducibility**, and **training consistency** across all field and laboratory workflows.

All lab members are encouraged to contribute to this repository by uploading new materials or updating existing documents.

---

## 📁 **Repository Structure**

The repository is organized into the following subdirectories.  
Each folder contains manuals, SOPs, or reference documents relevant to field research, laboratory analyses, and coral ecology work.

| Folder | Name | Description | Examples of Contents |
|--------|-------|-------------|------------------------|
| **0_Onboarding** | Onboarding Materials | Safety, orientation, and introductory documents for new lab members. | Lab welcome guide, onboarding checklists, safety forms |
| **1_Field_Manuals** | Field Equipment Manuals | Manuals and operational guides for field instruments. | ADCP manuals, SeapHOx setup, McLane RAS documentation |
| **2_Lab_manuals** | Lab Equipment Manuals | Operating manuals and usage guides for laboratory instruments at BIOS and ASU Tempe. | TA titrator, OXY-12 system, freeze dryer, sonicator |
| **3_Water_quality_sampling** | Water Quality Sampling Protocols | SOPs for collecting seawater samples for biogeochemical analysis. | Nutrients, DIC/TA, Chl-a pigments, particulate matter, RAS prep |
| **4_Water_quality_analyses** | Water Quality Analysis Protocols | Laboratory SOPs for analyzing seawater samples. | Ammonium, TA analyses, Chl-a, particulate matter |
| **5_Live_coral_measurements** | Live Coral Measurements | Protocols for measuring coral physiology, performance, and metabolism. | Coral surface area (Agisoft/ImageJ), grayscale scoring, incubations |
| **6_Coral_tissue_analyses** | Coral Tissue Analyses | SOPs for processing coral tissue and symbionts. | Tissue stripping, zoox density counts, chlorophyll extraction, protein/lipid assays |

---

## 🌳 **Repository Folder Structure (Collapsible)**

<details>
<summary><strong>Click to expand folder tree</strong></summary>

````md
📁 Lab_management/
│
├── 📁 0_Onboarding/
│   ├── 📄 Welcome_documents/
│   ├── 📄 Safety/
│   └── 📄 Checklists/
│
├── 📁 1_Field_Manuals/
│   ├── 📄 ADCP/
│   ├── 📄 SeapHOx/
│   ├── 📄 RAS/
│   └── 📄 Other_instruments/
│
├── 📁 2_Lab_manuals/
│   ├── 📁 BIOS/
│   │   ├── 📄 Titrator/
│   │   ├── 📄 OXY-12/
│   │   └── 📄 Incubators/
│   └── 📁 ASU_Tempe/
│       ├── 📄 Freeze_dryer/
│       └── 📄 Sonicator/
│
├── 📁 3_Water_quality_sampling/
│   ├── 📄 Nutrients/
│   ├── 📄 DIC_TA/
│   ├── 📄 Pigments/
│   ├── 📄 Particulates/
│   └── 📄 RAS_preparation/
│
├── 📁 4_Water_quality_analyses/
│   ├── 📄 Ammonium/
│   ├── 📄 TA/
│   ├── 📄 Chl-a/
│   └── 📄 Particulate_matter/
│
├── 📁 5_Live_coral_measurements/
│   ├── 📄 Surface_area/
│   ├── 📄 Grayscale/
│   ├── 📄 Incubations/
│   └── 📄 Calcification_TA/
│
└── 📁 6_Coral_tissue_analyses/
    ├── 📄 Tissue_stripping/
    ├── 📄 Zoox_density/
    ├── 📄 Chl-a/
    ├── 📄 Proteins/
    └── 📄 Lipids/
````
</details> 

---

## 🧭 **How to Contribute**

This repository will grow as lab members add manuals, update SOPs, and upload new documents.  
To keep everything consistent, please follow the guidelines below.

<details>
<summary><strong>Click to expand</strong></summary>

<br>

### 🟦 **Adding New Files**
1. Navigate to the correct folder  
2. Click **Add file → Upload files**  
3. Use clear filenames:  
   - `TA_sampling_protocol_v1_2024.md`  
   - `SeapHOx_manual_v3.pdf`  
   - `Coral_tissue_stripping_v2.docx`  
4. Add a descriptive commit message

---

### 🟧 **Writing New SOPs (Markdown Preferred)**

When creating new SOPs, use **Markdown (.md)** so GitHub renders them clearly.

Include:

- Title & version  
- Purpose  
- Materials & reagents  
- Equipment  
- Procedure (numbered steps)  
- QC & calibration  
- Troubleshooting  
- Safety notes  
- References  

A template is provided below.

---

### 🟥 **Updating Existing Materials**

For small edits:  
- Use GitHub’s built-in editor.

For larger updates:

```bash
git pull
git checkout -b update-protocol-name
git add .
git commit -m "Updated TA analysis protocol"
git push
```
</details>

## 📄 **Standard Lab Protocols Template**

<details>
<summary><strong>Click to expand SLP Template</strong></summary>

<br>

````md
<p align="center">
  <img src="images/ASU_BIOS_Logo.png" 
       alt="ASU-BIOS Logo"
       height="140">
</p>

---

# Protocol Title
### Adapted from: Cite original authors if applicable.
**Author(s):**  Your Name
**Lab:** Sawall Lab / MABEE Lab  
**Version:** v1.0  
**Date:** YYYY-MM-DD

## Purpose
Describe what the protocol does, its context, and why it is needed.

## Materials & Reagents
List all required materials with details that support reproducibility.

- Chemical name, grade, purity  
- Supplier & catalog number  
- Storage conditions  
- Shelf life  
- Working concentrations and how to prepare them  

Example:
- **99.5% Ethanol**, Molecular Grade (Sigma-Aldrich, Cat. #459844)  
- **Pierce BCA Protein Assay Kit** (ThermoFisher, Cat. #23255)

## Equipment
Include all instruments, software, and hardware.

- Model, manufacturer, and serial number  
- Calibration notes  
- Required settings (e.g., temperature, speed, gain, cycle time)  
- Software version numbers    

## Sample Preparation
Describe any pre-processing steps:

- Sample preservation  
- Filtration or homogenization  
- Storage temperatures  
- Incubation time before measurement  
- Subsampling strategy  

You may refer to other protocols here using Markdown links, e.g.:  
`[See Tissue Homogenization Protocol](../6_Coral_tissue_analyses/Air_picking.md)`

## Procedure
Provide steps **exactly as performed**, using numbered lists for clarity.

1. Step-by-step instructions.  
2. Include as much detail as possible. 
3. Add notes for optional steps or troubleshooting as necessary.  

**Important:**  
- Specify **units**, **temperatures**, **volumes**, **incubation times**, and **rates**.  
- Include stopping points where the procedure may be paused.

## Quality Control & Calibration
Document all required QC checks:

- Calibration curves  
- Standard acceptance criteria (e.g., ±2%)  
- Blanks, technical replicates, and internal standards  
- Frequency of calibration (daily, per batch, per instrument start)  
- These are just a few examples.

## Troubleshooting (Optional)
Provide actionable solutions to likely issues.

| Problem | Possible Cause | Solution |
|--------|----------------|----------|
| Low signal | Dirty cuvette | Clean thoroughly with kimwipe + RO water |
| High blank | Reagent contamination | Prepare fresh reagents |
| Drift | Temperature instability | Allow longer equilibration | 

## Safety Notes
- Required PPE (gloves, eye protection, lab coat, etc.)  
- Chemical hazards (corrosive, toxic, carcinogenic, etc.)  
- Spill response  
- Waste disposal instructions (solid vs. liquid waste)  
- Biosafety considerations  

## Data Logging & Record-Keeping
Specify where the outputs go.

- **Raw data file format:** (e.g., `.csv`, `.txt`, `.xlsx`)  
- **Metadata requirements:** date, operator, temperature, instrument settings  
- **Naming convention:**  
  - `SampleID_AnalysisType_YYYYMMDD_operator.csv`
  
## Versioning Notes
- v1.0 — Initial protocol  
- v1.1 — Minor edits, formatting improvements  
- v2.0 — Major methodological update  

## References
- Papers 
- Manuals  
- GitHub Repositories  
- Related SOPs
- DOI links if applicable  

---

# 📸 **Embedding Images in SOPs**
Use the following Markdown format:

```md
<p align="center">
  <img src="images/my_image.png" alt="Description" width="400">
</p>
```

You can also reference images inside subfolders:

```md
<img src="../images/Instrument_Diagram.png" width="350">
```

---
````
# 📊 **Making Tables in Markdown**
Basic table:

```md
| Sample ID | Volume (mL) | Result (µmol/L) |
|-----------|-------------|------------------|
| A01       | 5           | 3.22             |
| A02       | 5           | 3.10             |
```

Multi-line formatting:

```md
| QC Step | Acceptable Range | Notes |
|--------|------------------|-------|
| CRM | ±2% | Batch-specific |
| Blank | < 0.05 | Reprepare if greater |
```

---

# 🔗 **Links**
Link to other protocols:

```md
[See related Air Picking SOP](../6_Coral_tissue_analyses/filename.md)
```

Link to external resources:

```md
[Putnam Lab Chl a Protocol](https://emmastrand.github.io/EmmaStrand_Notebook/Chlorophyll-A-Protocol/)
```
---
</details> 
