<p align="center">
  <img src="../images/ASU_BIOS_Logo.png" 
       alt="ASU-BIOS Logo"
       height="140">
</p>

---

# Protocol for SeapHOx Deployment and Retrieval
**Author(s):** Roderick Bakker, Xinya Calhoun  
**Lab:** Sawall Lab / MABEE Lab  
**Version:** v1.2  
**Date:** 2025-02-19

## Overview

This protocol is used for deploying and retrieving the SeapHOx in the field.

## Contents

- [Materials](#Materials)
- [Software Setup](#Software_Setup)
- [Deployment](#Deployment)
- [Retrieval](#Retrieval)

<h2 id="Materials">Materials</h2>

- [SeapHOx Box](       )
    - Tool bag
        - Small, broad, flat head screwdriver
        - Square head screwdriver
        - 5/32 hex driver
        - Adjustable wrench/spanner
        - SeapHOx copper tubing
        - [Stirrer magnets](     )
    - Plastic tubing with weight attached
    - SeapHOx communication cable (8-pin)
    - Grease
- Bucket
- Durabook field laptop with UCI software
- Filtered seawater (preferably 0.1µm) 
- MilliQ

<h2 id="Software_Setup">Software Setup</h2>

1. Attach the communications cable to port 1 on the back of the field laptop.
2. Connect the cable to the SeapHOx.
3. Open the UCI software on the field laptop and press “Connect”.
4. Select: 
    - Instrument type: SeaFET
    - Baud rate: 115200, check try all baud rates
    - Port: COM1
    - Press connect 
5. Make sure data from the previous deployment is offloaded before proceeding!
6. In the Seafet dashboard click deployment wizard.
    a. Set operating mode to Autonomous Sampling.
    b. Synchronize SeaFET clock to computer, check the “clear SeaFET data” box
       - Important: Make sure data from previous deployment is offloaded.
    c. Set the desired start time (UTC) for deployment.
        - Important: set the start time several hours past the deployment time to make sure the SeaFET doesn’t run whilst at the surface. 
    d. Real-time data transmission can be on or off during autonomous deployment. Header format should already be set correctly.
    e. Check the “Enable External Pump” box. 5 seconds is sufficient at low sampling intervals (2-30 min), for longer intervals pump time should be increased to clear previous water masses and fouling. 
    f. Set the sampling interval in seconds (Eddy Reef JSB = 300 seconds).
    g. Input minimum expected water temperature. Set sampling interval in seconds.
7. The SeapHOx is now programmed for deployment.
8. Swipe a magnet over the [switch](   ) at the bottom to confirm the SeapHOx is ready for deployment.
    a. If the light flashes green: SeapHOx is ready.
    b. Flashes red: The Seaphox did not disconnect correctly
        i. Open the command terminal in the UCI software.
        ii. Type “startlater” and press enter.
        iii. The command terminal should now show the logging start and interval.
        iv.	Check the magnetic switch again, it should now flash green. 
        v. Press disconnect in the SeaFET dashboard.
9. Disconnect the communications cable from the computer and the SeapHOx.
10.	Grease the dummy plug and attach to the SeapHOx.


<h2 id="Deployment">Deployment</h2>

1. Remove the wet cap from the SeaoHOx using the 5/32 hex driver.
    - Water will come out of the wet cap.
    - Important: the wet cap needs to be installed and flowing with water within 15 minutes or the ISFET sensor will dry out and may be permanently damaged.
2. Remove the [plastic seals](../images/SeapHOx_Deployment_&Retrieval/WetCap_Plastic_Seals.png) from the wet cap using an adjustable spanner.
3. Place the [copper tubes](../images/SeapHOx_Deployment_&Retrieval/WetCap_Copper_Tubing.png) on the wet cap and tighten firmly with the adjustable spanner.
    - Ensure that the black, plastic adapter piece is oriented towards the CTD inlet so that it will [fit into the hole](../images/SeapHOx_Deployment_&Retrieval/Copper_Tubing_Connection.png).
4. Attach the wet cap back onto the SeapHOx using the 5/32 hex driver.
    - Pressure will have to be maintained towards the CTD inlet to replace the screws.
5. Place the SeapHOx in water, or maintain flow using the plastic tubing. 
    - **Important**: do not let the SeapHOx run dry.
6. Deploy the SeapHOx with the wet cap facing upward.
    - If deploying with the [frame](../images/SeapHOx_Deployment_&Retrieval/SeapHOX_Frame.png), deploy the X base first by laying it down on a flat part of the reef, and reinforcing each arm of the X onto the reef with rope. Attach the SeapHOx afterwards.
7. Check that the [purge hole](../images/SeapHOx_Deployment_&Retrieval/SeapHOX_Purge_Hole.png) on the top of the SeapHOx is clear from fouling or debris.


<h2 id="Retrieval">Retrieval</h2>

1. Fill the bucket with seawater. 
2. Detach the SeapHOx from the X base of the frame (if necessary) and bring the SeapHOx back to the surface.
3. Immediately start [water flowing through the SeapHOx](       ) by starting a siphon with the plastic tubing, with the non-weight end attached to the open copper tube and the weight end in the bucket.
    - **Important**: ensure water is flowing consistently. The SeapHOx pump does not have a minimal conductivity sensor and will run dry, damaging both the pump and the ISFET sensor.
4. Attach the communications cable to port 1 on the back of the field laptop.
5. Dry the data connector plug. Remove the dummy plug from the SeapHOx and connect the data cable.
    - Important: make sure no water gets into the plugs.
6. Open the UCI software on the Durabook and press “Connect”.
7. Select: 
    - Instrument type: Seafet
    - Baud rate: 115200, check try all baud rates
    - Port: COM1
    - Press connect
8. Select “Transfer Data” and import to the field laptop.
9. Swipe a magnet over the switch at the bottom to confirm the SeapHOx is off.
10. Take off the wet cap and remove the copper tubing.
11. Rinse off any debris with filtered seawater and remove fouling around the wet cap area.
12. Insert one of the plastic seals (the once facing the CTD) and reinstall the wet cap.
13.	Fill the wet cap with filtered seawater and install the second plastic seal.
14.	Rinse the CTD with MQ.

