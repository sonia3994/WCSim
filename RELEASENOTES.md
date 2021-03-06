This file contains the release notes for each version of WCSim. Release notes can also be found at https://github.com/WCSim/WCSim/tags. 

*************************************************************
01/21/2014: Notes for v1.2.0        
*************************************************************
Bug Fixes
* Missing HK variables added so that the HK geometry could be specified as the default and the code won't crash. 
* HasSubEvents() function now returns the proper Boolean value. 
* Dark noise is now added between the start of the trigger window and the start of the signal. 

Structural Changes
* All of the different detector setups were moved into a file called WCSimDetectorConfigs.cc.
* WCSimPMTQE.cc was created and all quantum efficiency info was put there.
* WCSimWCDigitizer was split into a PMT collection (in the newly created WCSimWCPMT file) and a digitizer collection.
* The PMT information was put into a single file called WCSimPMTObject.cc. PMTs now inherit from the newly created WCSimPMTObject class. 
* WCSimWCConstructWC is now named WCSimConstructCylinder to explicitly show that this function builds cylinderical geometries and should not be used to construct the HK geometry. 

New Features
* Python script was added to generate kinematics files for simple particles. 
* A (very) basic validation script was added in a new directory called verification-test-scripts. The verification_HitsChargeTime.C script checks the hits, charge, and timing of events against a clean copy of the WCSim code. 
* HPDs were added to the list of possible tubes allowed in WCSim.
* Hyper-K with HPDs was added as a new detector configuration. 
* Updated the dark rate parameters for normal PMTs.
* Added the dark rate comands to novis.mac. Uncommented out the dark rate commands in novis.mac and vis.mac.
* Included the dark rate parameters for the HPDs in vis.mac and novis.mac.
