# X15-CM2350-Vortex-Delete
The official source for the X15 CM2350 emissions demandate delete.

*** This is the official Vortex Delete for the X15 CM2350 by zyNoT. ***

*** THIS OVERLAY IS INTENDED FOR USE ON BGT CM2350 ECMs ONLY, DO NOT USE ON BDR OR ANY OTHER CM2350 MODULE!!! ***

*** THIS IS NOT THE LATEST RELEASE OF THIS OVERLAY, THIS IS JUST A STARTING POINT FOR THOSE WILLING TO CREATE THEIR OWN! MANY CHANGES HAVE TAKEN PLACE SINCE THIS OVERLAY VERSION. THESE CHANGES INCLUDE: MISSING EMISSIONS PARAMETERS, CHANGES TO CHL, CHANGES TO TORQUE LOAD TO FUEL, CHANGES TO TURBO ACTUATION, CHANGES TO POST FUELING, CHANGES TO OFC, ETC. ETC. ***

WARNING! - These actions and steps should not be performed in countries that have laws against altering engine emissions!

WARNING! - This is only an example of how to go about editing the ECU and is not a final product or solution. Use at your own risk!!!

NOTICE! - No faults are added to blocking code tables as they are not needed when done correctly.

NOTICE! - This information may change over time. This delete hasn't been fully tested and therefor you are using at your own risk. 

Step 1) Verify you have overlay file included with this documentation.

Step 2) Obtain correct INCAL file for engine and fully unzip the calibration itself from it.

Step 3) Verify you have the correct ECFG file for your engine. If not, do not continue.

Step 4) Run overlay file included with this document using Calterm on the unzipped INCAL file.

Step 5) Zip modified INCAL file back up with ZIP utility. If you re-named it please re-name it back to original name and copy to correct place for INSITE to use it.

Step 6) Flash engine with INCAL modified in previous steps using INSITE, NOT CALTERM!

Step 7) Start  the truck up, run the truck for at least 30 minutes to allow ECM to populate all RAM data.

Step 8) Turn truck off, but make sure key switch is ON so you can connect back to ECM.

Step 9) “UPLOAD” the calibration FROM the truck TO the computer using Calterm.

Step 10) Make a copy of the pulled calibration. Open copy of the pulled calibration in Calterm. Modify fueling tables and VGT tables if needed. (They will be needed!) Save changes.

Step 11) “DOWNLOAD” the calibration you recently modified (hopefully you named it something like vortex_aftertablemodifications.cal), push this file to your trucks ECM using Calterm.

Step 12) Test truck and make sure there are no codes and engine runs good before hollowing out the DOC, DPF, SCR, and installing the blocking for EGR gas.


EXTRA NOTES:

* You may need to modify multiplexing settings in Paccar ESA to disable any after treatment messages or switches.

 * Once done, you may need to modify multiplexing settings in INSITE to disable any after treatment switches.

* You should set any after treatment module versions to all 0s in HEX. This cannot be done in the overlay as it can only be done on a full calibration file. It's recommended to do so when modifying tables in step 10.

* DO NOT block coolant or remove EGR cooler unless bypass water pipe is made to replace it.

* Drilling hole or leaving in SCR can is not good enough. Please also install a pyro gauge to keep an eye on exhaust temps.

* It is recommended to replace the crank case filter with Cummins Maintenance free filter for the X15 to reduce crank case pressure and back-pressure on the turbocharger oil return line. This filter is much smaller than the previous engine filters. 

* This engine unlike previous engine models does not have an after treatment doser injector. You don't need to block fuel leading to any as there won't be any. 

* Most X15 engines are using straight-through exhaust modules. The SCR will be in a different place and may be harder to reach. It is recommended to replace exhaust pieces that have inspection plates as you can see if DPF is drilled or if SCR mesh is missing during an inspection.
