---
layout: default
title: IMMERSE Log
---

## Weekly schedule:

|  Monday - Wednesday |   Friday   |
| ------------------- | ---------- |
|    9AM - 1PM        | 9AM - 1PM  |
|    2PM - 5PM        | 2PM - 5PM  |


-------------------
## Log:

### Week 5: May 24 - May 28, 2021
* **Goals**:
  - Figure out why the FrameECC/byu hybrid scrubber ip isn't working on the zc706 (could be DEVICE_ID)
  - Comunicate findings to Sebastian and Dr. Wirthlin
  - If we can't get it working, look at adapting the code for readback and/or blind scrubbing. (Done)
  - Test Readback scrubber on zc706..
  - Ask around for the source design of the hybrid-scrubber for better debuging
  - Get another microsd -> sd card adapter so I can run both boards at once (DONE)

* **Monday**:
  - More testing.. Still not working on zc706
  - Made a modified version of the scrubber that only uses the crc and not the ecc checks.. basically a readback only scrubber
  - Simplified git history and pushed all my work to github under the two branches zc7045-updates (main code) and debug-fault-inject (WIP code)

* **Tuesday**:
  - Going to test crc only scrubber on the z7045
  - Need to summarize current probelem on github issues
  - Document the expected behavior of the hybrid scrubber registers, use them to recreate the ip?
  - Translated the hybrid scrubber ip to verilog by hand (almost, still need to recreate the block design)
  - Discovered that both the PCAP and the ICAP take a specific device ID, added code to generate the device id from the frad-gen-app
  - Accidentally deleted the hybrid scrubber ip project I wrote in verilog. I'll have to recreate it later (and add it to the github project)

* **Wednesday**:
 - Tried to make a new project for zc706 board, it didn't work
 - Going to try a different way of modifying the exisiting project, we'll see what that does..

* **Friday**:
 - Tried to make a new project for zc706 board, it didn't work
 - Going to try a different way of modifying the exisiting project, we'll see what that does..


### Week 4: May 17, 2021
* **Goals**:
  - Get scrubber reference projects running on all boards
  - Run scrubber and generate FRAD's list
  - Understand the process of creating those projects from scratch (using William's documentation)
  - Document in detail how to use the example projects

* **Monday**:
  - Downloaded Sebastian's referce project, attempting to build for zedboard
  - Installed petalinux tools
  - After lots of trial and error, I understand better the process for building petalinux for the zedboard.
  - Successfully booted petalinux on zedboard

* **Tuesday**:
  - Confirmed Scrubber runs on zedboard and zc706
  - Spent some time studying the scrubbing app code
  - Something is causing the scrubber on the zc706 to detect errors, maybe its just the frads list, need to investigate more..

* **Wednesday**:
  - Worked on outreach stuff
  - Played around with fault injection in the scrubbing code
  - Started a basic frad list generator using the pcap
  - Used frad list generator to modify code for zc706, awaiting more testing

* **Thursday**:
  - Worked on outreach stuff
  - Played around with fault injection in the scrubbing code
  - Made a change to scrubber, fault injection now works correctly on zedboard, FRAME_ECC still returns meaningless data on zc706, need to understand why

### Week 3: May 10, 2021
* **Friday**: 
  - Met with Dr. Wirthlin to discuss personal goals for scubber on SSP
  - Updated ccl website with my info

  - Downloaded the hybrid scrubber code from github, and added it to the premade projects for the zedboard and ZC706.. was able to generate a bitstream successfully for Zedboard.. however I don't have a license to run sythesis for the ZC706 part..
  - Some notes about the hybrid_scrubber repo and premade projects:
  -  It looks like the hybrid scrubber (hardware) from the repository is packaged as a Vivado IP block.
  - The projects are just simple block projects that generate the hybrid scrubber IP and connect it to the processor

### Break: Apr 30 - May 13
  - Read thesis on FPGA scrubbers
  - Met with Dr. Wirthlin and Sebastian about CSP/SSP Project


### Week 1: April 26, 2021

* **Monday**: 
  - Setup workstation
  - Install linux
* **Tuesday**: 
  - Located Pynq board
  - Completed 427 lab1
  - Improved Lab website
* **Wednesday**: 
  - Finished installing Vitis
  - Wrote basic buttons driver for lab2
  - Talked with Michael Eyler from the shop about outreach pulse ox project

* **Thursday**: 
  - Finished drivers for lab2

### Week 0: April 19, 2021

* **Friday**: 
  - Read labs
  - Xilinx configuration guide
  - Ultrascale+ Reference manual

-------------------
## Docs to make:
 - deploy.sh to package and copy the petalinux build
 - How to format the sd card
 - How to make a new app for petalinux

## TODO:
- Try deploying current version to board and see what happens
- Try adding new ip to sebastians project
- Try generating the hardware definition again and see if that works
- Check to see turning off the undocumented flags does anything?
- Try a different way of reading the frame ecc device (kernel module?)
- Try going back to sebastians initial project and see if that works with a new frads list?
- Document the expected behavior of the hybrid scrubber registers, use them to recreate the ip?

- Maybe look at a tutorial for block designs in Vivado?
- Clean up the readback only scrubber for better printouts

- Finish 427 Lab 2 (and maybe look at the other Kernel labs)
- Read linux on MPSoc documentation from William

- Read documentation for PulseOx project
- Make presentation for Linux on MPSoc