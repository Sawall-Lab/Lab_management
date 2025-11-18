---
title: "Metrohm_Titrator_&_Tiamo_Software"
author: "Xinya Calhoun"
date: "2025-11-13"
output: html_document
---

# Standard protocol for total alkalinity sampling 

Original: 20251113    
Last Revised: 20251113

Overview: This protocol is used for the estimation of carbonate (CO3) and/or total alkalinity (TA) through a 2-step titration process. A sample volume of 30-50mL is required; protocols are available for different volumes, but the different protocols cannot be mixed during a single run. 

Gloves for machine and sample handling! This lab sometimes uses HgCl2 so there could be traces.

No gloves for computer handling! 

Contents
- [**Materials**](#Materials)
    - ##Making titrant 
    - ##Samples
    - ##Purchasing new materials
- [**Making Titrant**](#Making Titrant)  
- [**Tiamo Software**](#Tiamo Software) 
    - ##Databases
    - ##Methods 
    - ##Export Templates
- [**Machine Preparations**](#Machine Preparations)  
- [**Bubble Removal**](#Bubble Removal)    
- [**Sample Preparation**](#Sample Preparation)  
    - ##Notes
    - ##Adding sample data directly into the machine  
    - ##Adding sample data using an CSV spreadsheet sample table 
- [**Conducting Titrations**](#Conducting Titrations)  
- [**End of Day**](#End of Day)  
- [**Waste Disposal**](#Waste Disposal)  
    - ##Clean Waste 
    - ##Spiked Waste  
    - ##Gloves, Aluminum foil, etc. 
- [**Data Processing**](#Data Processing)  
- [**Storage**](#Storage)  
- [**Troubleshooting**](#Troubleshooting) 
    - ##Calibration  
    - ##Volume 
    - ##System was shut down 
    - ##Broken equipment 

1. <a name="Materials"></a> **Materials**

Materials are mostly stored in room 305. Note that not all materials on this list need to be used each time samples are run.

Making titrant: 
    -	Balance/scale
    -	HCl
    -	Reagent+ grade NaCl
    -	MilliQ water (aka MQ)
    
Samples:
    -	Collected samples
    -	LNSW + bottles
    -	Titrant
    -	Styrofoam stands (if using falcon tubes)
    -	Aluminum foil cut into small squares
    -	White lids
    -	MQ
    -	HCl
    -	pH testing strips
    -	3mol KCl solution
    -	CRMs
    
Purchasing new materials: 
    -	Aluminum foil and pH testing strips can be purchased at stores on-island and reimbursed.
    -	HCl and HgCl2 can be ordered through Lab Operations (Yasah Pitcher, ypitcher@bios.asu.edu; Jess Godfrey, Jessica_Godfrey@bios.asu.edu).              
    -	Metrohm solutions and parts (KCl solution, etc.) can be purchased through their website.

2. <a name="Making Titrant"></a> **Making Titrant**

Note: use fresh MQ and clean glassware. 

    1. Mix 900mL MQ with 38.5g Reagent+ grade NaCl (located in a Ziploc bag in a drawer) in a 1L beaker. Mix occasionally over the course of 1-2 hours until the NaCl is fully dissolved. 
    2. Add 2.78mL Reagent grade HCl (located in a bottle in the cabinet under the fume hood). 
    3. Add more MQ so the total volume of the titrant solution is 1L (should add ~97.22mL of MQ).

For absolute TA measurements: use RM or CRM measurements to back calculate precise acid concentration. Adjust concentration in tiamo software and R templates. 

Note: If running a lot of samples (eg. over the summer field season) it’s best to make 4L at once in the big 4L amber bottle (blue label) and top up the smaller amber titrant bottle (green label) as needed. This avoids having to restandardize.


3. <a name="Tiamo Software"></a> **Tiamo Software**

Note: DO NOT close the Tiamo software application on the computer, it will reset the rack which may prevent the instrument from working (see Troubleshooting).

Databases: locations to group data/records produced by analyzed samples

    -	To find: Database -> File -> Database manager
       o	To create a new Database (if necessary): Database Manager -> right-click empty space and select “New”.
    -	Databases are used to organize and group produced sample files together
    -	Multiple Methods can be saved in one Database
    -	Saving a method in a Database is done by modifying the method (see below).

Methods: step-by-step procedure that the instrument takes each time it analyzes 1 sample.

    -	To find: Methods -> File -> Methods Manager
    -	Methods can be created and customized for exactly what steps the user wants the instrument to do (eg. How many MilliQ rinses, how many mm the tower is lowered)
    -	The general Method that is used for the titration of seawater samples in the MABEE Lab is “TA_CO3_20mL_AU_2024”. 
    -	Each Method has its own export templates for the “res” and “mp” files.
    -	If a new Method needs to be made in order to have different export templates but the same steps are desired, an old Method can be duplicated.
        o	Within the duplicated Method, find the EXPORT command labeled “Export Measuring Points” for exporting the “mp” files, and “Export Results” for exporting the “res” files, and modify them by selecting their respective export templates (see below to create export templates).
        o	Within the duplicated Method, find the DATABASE command, selecting the appropriate database to save the data in and labeling it as the database name.
    -	Be sure to save the Method after any changes are made, or else they may not be applied.

Export Templates: outlines for where the produced “res” and “mp” files from each analyzed sample will be saved in the computer’s File Explorer, and what metadata will be included in the produced “res” files from each analyzed sample.

    -	To find: Database -> Tools -> Templates -> Export Templates…
    -	Two files are exported for each titration reaction, one containing the raw measuring points (labeled “mp”; larger file ~20KB) and one containing the results: derived values (CO3, TA) and quality control metrics (temperatures & pH EP) (labeled “res”; smaller file ~1KB)
    -	“Mp” file: 
        o	“File type” should be under “*csv. (Measuring point list)”
        o	“File name” should be under “Sample identification” and “ID1”
    -	“Res” file:
        o	“File type” should be under “*csv. (Comma Separated)”
        o	“File name” should be under “Sample identification” and “ID1”
        o	The metadata included in the “res” file can be modified based on the metadata that is input into the IDs of the sample tables, as well as the results that need to be included
            	When creating/editing a “res” export template, click “Select fields”
            	There can be as many or as few “selected fields” as desired
            	Each value from the “available field” can be given a simplified/clearer “displayed name”

4. <a name="Machine Preparations"></a> **Machine Preparations**

Start of week (or when machine has not run for 2 or more days)

    1. Fill the rinse water jerry can with 10L FRESH MQ.
    2. Mix titrant in amber bottle by swirling the bottle gently.
    3. Perform a 3-point calibration.

Start of day (every day)

    1. Check that the titrant bottle is at least half full (500mL = ~150 runs).
    2. Check that the MQ reservoir has 5L or more (5L = ~30 runs).
    3. Check/empty the waste water reservoirs (see Waste Disposal).
    4. Attach the top of pump 2. 
        Note: black mark on the tube goes flush with the right-hand side of the base of the clip.
        Note: tube should be within the large groove on the metal part of the holder.
    5. Open the electrode and top up with KCL (3-mol) by squeezing liquid from the KCl bottle into the hole.
    6. Start the computer (login is written on tape on the computer).
    7. Open the Tiamo software.
    8. Check for bubbles in both Dosinos (aka Dosing devices) and the blue tube coming from the titrant bottle. 
    9. If bubbles are present, proceed to “Bubble Removal”, if not, proceed to “Sample Preparation”.

5. <a name="Bubble Removal"></a> **Bubble Removal**

Note: bubble removal process only uses MQ so the waste line of pump 2 can be in the waste bottle with the green label for the duration of the process.

    1. Put a 50mL Falcon tube into the position directly under the injection needle.
    2. In the Tiamo software: 
        a.	“Manual -> Tower 1 -> Move
        b.	Lower the “Lift position” until the injection needle is lowered to ~150mm in the Falcon tube.
    3. In “Tower 1”, start pump 2. 
        Note: pump 2 drains the sample beaker - if the sample beaker isn’t draining, adjust the spring tension on pump 2 by twisting the silver knob on the clasp.
    4. In “Dosing Devices”, start “prepare” commands for both dosinos.
    5. Wait until prepare commands have finished and liquid is fully drained out of the sample beaker.
    6. Stop pump 2 and run pump 1 until sample beaker is full to ~25mL.
    Note: don’t run pump 1 for too long or else the sample beaker will overflow.
    7.	Check that air had been removed from the dosinos and the line coming from the titrant bottle. 
        Note: The line should be free of bubbles. For the dosinos: small air bubbles (1mm or smaller) are okay, but bigger bubbles should be removed by now. If not, repeat prepare commands as many times as required.
        -	If there is still a concerning amount of bubbles despite multiple prepare commands, the Dosino device can be taken apart to remove the bubbles (see Storage for instructions). 
    8. In “Lift position”, raise the injection needle back to home position (0mm).
    9. Empty Falcon tube into waste bottle with green label or into sink.

6. <a name="Sample Preparation"></a> **Sample Preparation**

Notes:

    1. Each sample takes ~10-12 minutes.
    2. Low-nutrient seawater (LNSW) must be collected at the start of each group of samples being run (eg. samples collected at the same time for the same purpose) – collect a bucket half-full of water and then completely fill four or five 500mL plastic LMSW bottles.
        -	Each LNSW bottle should only be used for one day of titrations – once open the exposure to air will influence their TA.
    3. The system usually takes 5-10 junk (LNSW) samples to prime all the lines and settle the electrode. If the machine has been run the previous day then 5-6 samples is sufficient, but if it has been sitting inactive for a couple days then more samples may be needed (8 or more).
        -	The system is ready for real samples if the TA value of 3 consecutive junk samples are (ideally) no more than ~3µmol apart (eg. 2185.59, 2184.01, 2186.44). A spread of 5µmol is acceptable.
    4. The titrator takes a maximum of 24 samples at a time.
    5. Samples can be added for a run into the Tiamo software directly, or a sample table can be made beforehand (as a CSV spreadsheet) and uploaded to the software.
    6. More samples can be added to runs as the titrator is running, both into the software directly and as sample tables. 
    7. Each sample requires (at minimum) a method, sample position, sample ID and salinity (in that order!).
    8. Depending on the type of vial the sample is in as well as how full the vial is, the “Special position” will have to be changed to ensure enough sample is taken up:
        -	Falcon tubes (with Styrofoam stand): special position = 180mm
        -	Sample vials and 30mL threaded glass vials: special position = 187mm
    9. 2 junk samples should be run between every ~12 real samples to ensure the system is still stabilized or to determine drift.

Adding sample data directly into the machine:

    1. Go to the “Workplace” tab in the Tiamo software (top left corner).
    2. Expand the “run” window (top right corner).
    3. Clear the sample data tab if old samples are present (select any line of sample data and right-click -> delete).
    4. Double-click the first line.
    5. Select the desired method.
    6. Add sample ID in the ID1 field.
    7. Add sample salinity in ID2 field.
    8. Other metadata can be added in ID3-ID8 fields.
    9. Click “Apply” to add the sample to the table.
    10. Use the arrows at bottom left hand corner to move to the next line and add more samples.
    11.	Proceed to “Starting Titrations”.

Adding sample data using an CSV spreadsheet sample table:

Note: if samples are collected by another researcher, a template table can be sent to them for them to fill out and returned for running the titrations. Example templates are provided in the “Templates” folder.

    1. Copy the sample table template (or a previous sample table) to a daily folder (yyyyymmdd).
    2. Add the correct date (yyyymmdd) to the template file and append with titration run number.
    3. Add method name in column A (Method).
    4. Add sample positions in column B (Sample Position).
        Note: for duplicates or triplicates, samples should not be run one after the other – alternate duplicates or triplicates with each other to account more for drift.
    5. Add sample IDs in column C (ID1).
    6. Add sample salinities is column D (ID2).
        Note: LNSW salinity is 36.6, sample salinity is dependent on water quality measurements.
    7. Other metadata can be added in columns E-J (ID3-ID8).
    8. Add titration volume in column K (Sample Size).
    9. Add sample unit in column L (Sample Size Unit) (unit will be mL unless specified otherwise). 
    10. Two vials of LNSW should be placed at the start and end of every batch of samples (every ~6 samples). For these only the method, position, salinity and vial number should be added (columns A-D). All other columns can be put as “NA”. 
        a. Method: same as for samples
        b. Position: position on sample rack
        c. Vial: junk-# (number junks continuously throughout a day)
        d. Salinity: 36.6
    11. Delete the row with header information (row 1).
    12. Store sample table as csv file.
    13. Go to the “run” window in the Tiamo “workplace” tab.
    14. Press “Sample table” at the bottom of the run window. 
    15. Press “Import data”.
    16. Find the stored sample table and open it to upload samples to the Tiamo software. 
        Note: If header information wasn’t deleted earlier this line should be deleted in the “run” window.
    17. Proceed to “Starting Titrations”.


7. <a name="Conducting Titrations"></a> **Conducting Titrations**

Recall that at the beginning of the day the LNSW junks need to be run first! The following describes real  samples but the steps for junks are relatively the same.

    1. Un-spiked samples are kept in the fridge until they are run (for a week at most since they are un-spiked), but must be room temperature before titration. Take them out of the fridge and let them sit before analyzing.
    2. Methods are available for 30mL and 50mL samples. 30mL samples go in threaded sample vials or falcon tubes and can be placed directly on the titrator. Larger samples and LSNW junks will have to be transferred to 50mL vials. 50mL falcon tubes must be placed in Styrofoam stands to keep them upright.
    3. For 50mL samples, aliquot samples to sample vials to reach just under the blue fill line (fill line indicates ~40-50mL).
    4. Cover sample vials lids, first with aluminum foil, then with a white lid.
    5. Place samples on the titrator carousel in their appropriate positions.
    6. Ensure waste line on pump 2 is in the waste bottle with the green label for un-spiked samples, and the red label for spiked (HgCl2) samples.
    7. Place the white foam 50mL falcon tube holder in front of the sensor of the tower. 
        Note: Machine will not run without covering the sensor, unless official Metrohm beakers and beaker covers are used.
    8. Import the desired sample table.
    9. Double-check samples are in their proper positions on the carousel and match the sample positions in the sample table.
    10. In the Tiamo workplace tab, press “Start”. 
    11. Monitor the machine’s process of first titration as well as the results (under “Database”) to ensure (1) the samples are located properly on the carousel, (2) the waste pump is fully draining the sample beaker and (3) the titration reaction is running properly and produced reasonable results.
        Note: ensure that the determination overview shows the correct database, or the results of each sample will not be shown: under “Database” go to File -> Open -> select the appropriate database -> Open.
    12. After samples are run, the remaining sample liquid can be disposed of depending on the type (see Waste Disposal). 
        a.	Vials containing LNSW or un-spiked samples: dump remaining liquid into the sink, rinse 3x with MQ and set to dry.
        b.	Vials containing samples spiked with HgCl¬2: dump remaining liquid into the glass bottle with the yellow lid (located under the sink), rinse once with MQ and dump that rinse into the glass bottle, then rinse 3x with MQ and set to dry.

8. <a name="End of Day"></a> **End of Day**

    1. Top up electrode with KCl and close it.
    2. Unlatch top of pump 2.
    3. Move waste line on pump 2 back to waste bottle with green label. 
    4. Discard remnants from sample vials into the appropriate waste bottle, wash each 3x with MQ and leave to dry.
    5. Proceed to “Data Processing”.

9. <a name="Waste Disposal"></a> **Waste Disposal**

Clean waste water:

    1. Nalgene bottle with green label that says “Waste Water (clean)”
        -	Located on the counter
    2. Used for junk samples and un-spiked seawater samples
    3. Contains seawater, MQ, and Titrant
    4. Can be dumped down the sink with running tapwater

Spiked waste water (two containers):

    1. Rectangular jerry can with red label that says “Waste Water (spiked/HCl)”
        -	Located on the counter
    2. Glass bottle with yellow lid and red label that says “HgCl2 Mercury Chloride HgCl2”
        -	Located under the sink
        -	Used for the leftovers in sample vials, as well as rinse #1 with MilliQ
    3. sed for samples spiked with HgCl2
    4. Contains seawater, MQ, Titrant, and HgCl2
    5. Needs to be treated with HCl to lower the pH to ~3 (TEST WITH PH PAPER)
        - Jerry can full to 10L needs ~15ml of HCl
    6. Bring wastewater to the mercury filter in the DIC Lab (discuss beforehand with Becky Garley, Rebecca.Garley@bios.asu.edu)

Gloves, aluminum foil, etc:

    1. All things that come in contact with regular samples can be disposed of in the regular waste bins.
    2. All things that come in contact with HgCl¬2 (gloves, aluminum foil, etc.) should be disposed of in a double-bagged biohazard bag that can be obtained from Lab Operations (Yasah Pitcher, ypitcher@bios.asu.edu; Jess Godfrey, Jessica_Godfrey@bios.asu.edu).              
        -	Once biohazard bag is full, seal and return bag to Lab Operations.

10. <a name="Data Processing"></a> **Data Processing**

Note: see “Methods -> Export locations for data” to find exact locations for file exports. 

    1. The files containing raw measuring points (mp) should be transferred to a date labelled folder (yyyymmdd) at the end of each day.
    2. The files containing derived values (res) are used for the calculation of the calcification rates. As with the measuring points these files should be transferred to a folder labeled with the date (yyyymmdd).
    3. The folder from step 3 should be copied to the appropriate dropbox or Google Drive folder for processing. 

11. <a name="Storage"></a> **Storage**

Storage refers to when the system and the instrument will not be running samples for ~3+ weeks.

    1. Swap amber titrant bottle with the clear Dosino storage bottle (contains MQ) and rinse the Dosino 3x.
    2. Flush all lines with MQ using the machine commands (do not try to take off the lines and do it manually). After switching Titrant bottle for the Storage bottle, all inflows come from MQ - running prepare commands for both Dosinos is enough.
        -	Bonus: not necessary, but both Dosino units can be taken apart and rinsed with MQ to flush out any salt build up: follow Metrohm instructional videos for the sample Dosino but the titrant Dosino is the same process, and after reassembly run the “Prepare” command once or twice to ensure proper function. Tools required for disassembly are found in the drawer in room 305 marked “Metrohm”, in a Ziploc bag labeled “Tools”.
    3. Place electrode in a storage tube with the Metrohm 3M KCl solution. Seal the storage tube with Parafilm to prevent the solution from desiccating.
    4. Discard leftover waste and rinse out waste containers with MQ. 
    5. Download a backup of the Tiamo results database, and upload the backup as well as all .csv result files to the Dropbox.
        -	Must do this before the computer is shut down long-term as it can take a while for the computer and Tiamo software to boot up again once they've been down for a while.
    6. Acid wash and MQ wash all 50mL vials and 30mL threaded vials before storage.
        -	50mL vials can remain in the cupboard.
        -	30mL threaded vials go back in their cardboard boxes.

12. <a name="Troubleshooting"></a> **Troubleshooting**

Calibration:

If values seem off, the lab has batches of Certified Reference Material (CRM) solution that have been prepared by the Scripps Institution, with each respective batch’s salinity, TA and CO2 values published online. Run some samples of an UNOPENED bottle of solution (if already opened then the values will not be accurate due to air exposure) using their salinity, and if the CO2 and TA results do not match those published by Scripps (be sure to correspond the batch number to the number on the website) then there is something off with the system’s readings and offset must be accounted for.

Note: the Scripps solutions are spiked with HgCl¬2!

If new CRMs need to be purchased, email co2crms@ucsd.edu and they will provide an order form.

Volume:

The titrator needs to take up a certain amount of volume depending on the Method, and depending on the vial (50ml glass vials, 30ml threaded vials, falcon tubes, etc.), the tower needs to lower more to take up enough volume of the sample. If it does not, the TA values may be much lower or will read “invalid”. See Sample Preparation -> Notes -> step 8.

Software was shut down:

If the computer is shut down or the application is closed, the software will reset and may give error messages when trying to move the tower for bubble removal, as it will not be able to read the rack position: “Current position” (under Manual -> Tower 1 -> Move -> Rack position) will read “-----" instead of the number value that corresponds to the rack position directly under the tower.

To fix: set up one junk sample in the Workplace and start it. The system should begin running as usual – you can press “Stop” once the tower begins to lower as though to take up the sample. When “Stop” is pressed, everything will stay as it was while “Stop” was pressed, so go into “Manual”, stop the stirrer and move the Lift position back to 0. “Current position” should now read the number value that corresponds to the rack position directly under the tower. Proceed with bubble removal.

Broken equipment:

Broken parts can simply be replaced – there are spare parts in the drawer in room 305 marked “Metrohm”, in a Ziploc bag labeled “Spare Parts”. If parts required are not in the drawer, they can be replaced by ordering from the Metrohm website.

