# Change Log
All notable changes to this project will be documented in this file.

## 2022-10-09

Updating GNU Radio and HackRF versions. Integrating a few more links, tools, and fixes.
 
### Added

- Software Defined Radio with HackRF in Lessons menu
- GNU Radio Tutorials in Lessons menu
- Sample rate and frequency edit boxes for IQ data
- Gqrx IQ data button for loading a file into Gqrx when sample rate and frequency is supplied
- SigDigger to installer, menu, CREDITS.md, SoftwareAndConflicts for Python3 branches (Python2 branch avoids PyQt5 programs)
- ham2mon for Python3 branches in installer, menu, CREDITS.md, SoftwareAndConflicts
- Links in README to GRCon22 slides, paper, video and AIS page
- HackRF to CREDITS.md and SoftwareAndConflicts
   
### Changed

- Moved PySDR menu item to Lessons menu
- Updated GNU Radio versions for each branch (3.7.11.0->3.7.13.5, 3.8.1.0->3.8.5.0, 3.10.1.1->3.10.4.0)
- Updated SoftwareAndConflicts help page with GNU Radio versions
- Removed old copy of HackRF release, downloading the latest as part of the install
- Edited Updating HackRF Firmware instructions in the help menu
 
### Fixed

- Launch Wireshark button in the Sniffer tab did not work for Python3 branches
- Added python-qwt5-qt4 to installer for enabling GNU Radio Filter Design Tool in Python2 branch
- Added RX1 antenna option for X3xx devices with TwinRX daughterboards to: TSI Wideband Detector settings, IQ Record settings

## 2022-09-25

Disabling IIO-Oscilloscope for Python2_maint-3.7 branch.
   
### Changed

- Disabled IIO-Oscilloscope for Python2_maint-3.7 due to its failure to install

## 2022-09-23

Adding support for bladeRF 2.0 micro and updating existing bladeRF content.
 
### Added

- bladeRF 2.0 micro support (Dashboard, Hardware Selection GUI, TSI Detector, Inspection flow graphs, IQ record/playback, Archive playback, adding attacks to library)
- adsb_parser block in gr-ainfosec for Python2_maint-3.7, Python3_maint-3.8 branches
- Added more bladeRF firmware support to the installer for: 40, A4, A9
- Guess button functionality for original bladeRF, serial number passed to flow graphs
- Added bladeRF 2.0 micro to hardware list in README
   
### Changed

- Moved gain variables for osmocom source/sink blocks to IF gain location for bladeRF flow graphs
- Installing bladeRF and gr-osmocom software from source for Python2_maint-3.7 branch to support bladeRF 2.0
- Resized bladeRF probe button window size
 
### Fixed

- Added missing ".py" for USRP N2xx TSI wideband detector name
- Resized hardware selection GUI for Python2_maint-3.7 branch
- Added missing hardware types in combobox for adding new demodulation flow graphs to library
- Changed bladeRF icon from a bladeRF 2.0 image

## 2022-09-18

USRP2 and USRP N2xx support was added but not tested against real devices. Please report any issues.
 
### Added

- USRP2, USRP N2xx support (Dashboard, Hardware Selection GUI, TSI Detector, Inspection flow graphs, IQ record/playback, Archive playback, adding attacks to library)
- Added more USRP daughterboards for hardware selection
   
### Changed

- Removed openHAB as a default option for DragonOS until further examination is completed
- Listed new hardware in the README
 
### Fixed

- Added a missing package in the DragonOS install for Viking

## 2022-09-13

The DragonOS Focal install has only a few more tools that need to be examined.
   
### Changed

- Updated installer for DragonOS Focal with more tools
- Formatted Credits.md
- Updated README with branch information
 
## 2022-09-10

Ubuntu 22.04 and the 3.10 OOT modules have been moved to a new branch: Python3_maint-3.10.
 
### Added

- Python3_maint-3.10 branch with 3.10 flow graphs, OOTs, and submodules
- Discord link to README
- Python3_maint-3.10 installer image to README
- Discord link to Help menu
   
### Changed

- Removed 3.10 OOT modules and submodules from Python3_maint-3.8 branch
- Python3_maint-3.8 installer image in README
- Branch information throughout the README
- Removed Ubuntu 22.04 from Python3_maint-3.8 installer
- Python2_maint-3.7 installer warnings and checks for other operating systems
- Disabled broken 22.04 tools in the Dashboard menu for Python3_maint-3.10 branch
 
### Fixed

- Removed attack history debug messages in Python3_maint-3.8 branch
- Check for KDE neon/Ubuntu 22.04 in the initial install script in Python3_maint-3.8 branch
- Updated commands for 802.11 Monitor Mode Tool for Ubuntu 22.04 in Python3_maint-3.10 branch
- Converted Monitor Mode Tool to Python3/PyQt5 for 3.8, 3.10 branches

## 2022-09-07

The new KDE neon install follows the same steps as Ubuntu 20.04.4. The GUIs look a little wonky due to the differences in Qt.

### Added

- Added KDE Neon (User - 5.25/20.04) option to the installer for the Python3 branch. Will be the same steps as 20.04.4 until a difference is found.

### Fixed

- Modified ESP32 Bluetooth Classic Sniffer installation to work with Wireshark 3.6.5.

## 2022-09-05

Ubuntu 22.04 is still not fully supported. The 3.10 flow graphs need to be integrated and tested. There are also a few issues remaining with the install.

### Changed

- Set installer checkbox defaults to False/unchecked for 22.04 tools that are known to not install properly
 
### Fixed

- "Verify" checks for 22.04 OOTs (Python3 imports)
- Clone command in README was not capitalized (changed fissure to FISSURE)
- PlutoSDR blocks with 'int' errors for Python2 branch
- Grip "Verify" check runs a different command

## 2022-09-04

Run these commands to download the Git submodules for the GNU Radio out-of-tree modules:
```
cd ./FISSURE
git submodule update --init
```
 
### Added

- Submodules to FISSURE repository for most of the out-of-tree modules
- Initial PlutoSDR support:
  - PlutoSDR installation with IIO Oscilloscope
  - ZWAVE PlutoSDR attack for testing
  - PlutoSDR Inspection flow graphs
  - PlutoSDR TSI Detector flow graph
  - PlutoSDR IQ Recording and Playback flow graphs
  - PlutoSDR Archive Playback flow graph
- IIO Oscilloscope and gr-iio to CREDITS.md, SoftwareAndConflicts.md
- IIO Oscilloscope to menu (SDR)
- Fork locations for OOTs to Credits.md
- 3.10 OOTs: gr-ainfosec, gr-fuzzer, gr-bluetooth, gr-limesdr, gr-tpms
   
### Changed

- Inserted command to download submodules (Out-of-Tree Modules) prior to installation in README.md
- Removed OOT modules to replace with submodules
- Made dashboard.py executable
- Moved install location for libbtbb (gr-bluetooth)
- Updated OOT folder names in the installer
 
### Fixed

- Python3 error when adding a new attack to the library
- A couple install issues and some of the missing items with the DragonOS install (not complete yet)
- OOT Versions in Ubuntu 22.04 SoftwareAndConflicts.md

## 2022-08-28

We are grateful to all developers whose software is installed and accessed with FISSURE.

### Added

- CREDITS.md
   
### Changed

- baudline install, removing local software copy
- Bless website in Software list
- Credits section to README
- Credits in About page

## 2022-08-27

DragonOS and Ubuntu 22.04 are still in beta status. They are under development and several features are known to be missing. Several items in the installer might conflict with existing programs or fail to install until the status is removed.
 
### Added

- maint-3.10 out-of-tree modules in Custom Blocks folder and the installer; still missing: gr-ainfosec, gr-fuzzer, gr-bluetooth, gr-limesdr(?)
- Ask to proceed before installing PyQt4/5 and other programs with the first installer program
- DragonOS Focal install option, software items are still being tested, check back later for a full verified list
   
### Changed

- SoftwareAndConflicts 22.04 OOT status
- README to expand on beta status for operating systems
 
### Fixed

- Updated Python2 branch to the latest gr-tpms_poore for better error handling
- Fixed 20.04 variable for Enscribe in 22.04 section of the installer

## 2022-08-25
 
### Added

- LTE-ciphercheck in installer, menu, software list, example ciphercheck.conf copied from Tools folder during install
- unihedron Electromagnetic Radiation Spectrum Poster v2 in menu
 
### Fixed

- Attack/Fuzzing Apply buttons were causing errors when adding entries to Attack History for the Python3 branch
- Link in README for Discussions and Issues pages
- Commented out `drb_config = drb.conf` in enb.conf for srsRAN in Python2 branch

## 2022-08-21

Impacts the Dashboard, Hardware Select UI, and flow graph library.
 
### Added

- Shortcut to Open-weather.community in the Tools Menu
- Serial number option for HackRFs in flow graphs (does not work with Inspection flow graphs) and Hardware Select UI, added Guess and Probe button functionality
   
### Changed

- Updated the Tab Help to better reflect all the tabs
- Serial number variable to HackRF flow graphs, requires `"hackrf=" + str(serial)` in source/sink blocks
- Hardware Selection UI width to show longer serial numbers and interface names
 
## 2022-08-15

Pull the latest *dashboard.py* to access future archive IQ files at a new address (https://fissure.ainfosec.com).
 
### Added

- CHANGELOG.md file
- Standalone flow graphs for generating J2497 signals with gr-j2497
- *Enscribe* to installer, menu, and Supported Software 
   
### Changed

- Archive file location moved to https://fissure.ainfosec.com
 
### Fixed

- Packet Crafter "Open" button was looking for a "Custom" protocol to populate. Now it only fills in the "Constructed Sequence" text edit box.

