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

<br>

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
<details>

---

## 🧭 **How to Contribute**

This repository will grow as lab members add manuals, update SOPs, and upload new documents.  
To keep everything consistent, please follow the guidelines below.

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



