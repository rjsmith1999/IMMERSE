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
## TODO:
- Learn the process of building linux for Zynq/MPSoc (how and where do I apply the xdevconfig patch)
- Maybe look at a tutorial for block designs in Vivado?

- Finish 427 Lab 2 (and maybe look at the other Kernel labs)
- Read linux on MPSoc documentation from William

- Read documentation for PulseOx project
- Make presentation for Linux on MPSoc