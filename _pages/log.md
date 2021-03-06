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

### Week 28: Nov 29 - Dec 3, 2021
  - [ ] Add more documentation for radtest Scripts
  - [ ] Why are there OCM upsets?
  - [ ] Determine how many restarts were initiated by us, vs watchdog
  - [ ] Make some plans for next test
  - [ ] Learn more about kernel messages and where they come from
    - [ ] Try to find location in source code for each message (use oops codes?)

* **Monday**:
  - Added some notes about each message message with some links to kernel code
  - _TODO:_
    - Reclasify messages based on what I now know about the kernel source (die, panic, and fault messages)

### Week 26: Nov 15 - Nov 17, 2021
  - [ ] Add more documentation for radtest Scripts
  - [x] Make a note about each message chain
  - [x] Add a note about chains that cause timeout vs not
  - [ ] Why are there OCM upsets?
  - [ ] Determine how many restarts were initiated by us, vs watchdog
  - [ ] Make some plans for next test
  - [ ] Learn more about kernel messages and where they come from
    - [ ] Try to find location in source code for each message (use oops codes?)

* **Monday**:
  - Added some notes about each message chain
  - Grouped by chains that cause a timeout vs those that don't

* **Wednesday**:
  - Talked to Wes about generating confidence intervals for per-bit cross section.
  - _TODO:_
    - Change summaries script so that it generates all the tables from my docs
    - Add per-bit confidence intervals to the above
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test

* **Friday**:
  - Implement per-bit cross section
  - _TODO:_
    - Show confidence interval as a percent
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test


### Week 25: Nov 8 - Nov 12, 2021
  - [ ] Add more documentation for radtest Scripts
  - [ ] Make a note about each message chain
  - [ ] Add a note about chains that cause timeout vs not
  - [ ] Why are there OCM upsets?
  - [ ] Determine how many restarts were initiated by us, vs watchdog
  - [ ] Make some plans for next test
  - [ ] Learn more about kernel messages and where they come from
    - [ ] Try to find location in source code for each message (use oops codes?)

* **Monday**:
  - Add some more docs about message chains. Use the word message in place of events as it is more clear
  - Moved chain generation out to its own script
  - _TODO:_
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test

* **Friday**:
  - Spoke to Dr. Wirthlin about organizing results and future tests.
  - Added some notes about each chain
  - _TODO:_
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test


### Week 24: Nov 1 - Nov 5, 2021
  - [x] Redo the fluence to Failure table so it works on chains not events
  - [ ] Add more documentation for radtest Scripts
  - [ ] Determine how many restarts were initiated by us, vs watchdog
  - [ ] Learn more about kernel messages and where they come from
    - [ ] Try to find location in source code for each message (use oops codes?)

* **Monday**-**Thursday**:
  - *I was out sick*

* **Friday**:
  - Create a TOC on the main readme
  - Redo the fluence to Failure table
  - _TODO:_
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test


### Week 23: Oct 25 - Oct 29, 2021
  - [x] Document exact configuration for building the experiment so someone can recreate it
  - [ ] Add more documentation for radtest Scripts
  - [ ] Determine how many restarts were initiated by us, vs watchdog
  - [ ] Learn more about kernel messages and where they come from
    - [ ] Try to find location in source code for each message (use oops codes?)

* **Monday**:

* **Wednesday**:
  - Started sorting though sd cards to make sure I knew which configuration we were actually using for our test.
  - Need to confirm with Michael, but it seems we were using a new copy of the regular (sdcardfs) image
  - Started working on some docs for building the experiment

* **Thursday**:
  - Worked a bit more on the docs for the lansce test setup.

* **Friday**:
  - Finished the docs for the lansce test setup.
  - _TODO:_
    - Add docs for radtest scripts implementation
    - Add a note about which versions of the scripts were used in the real test

### Week 22: Oct 18 - Oct 22, 2021
  - [ ] Finalize experiment results for radiation beam test
    - [x] Finish responing to Dr. Wirthin's questions
    - [ ] Determine how many restarts were initiated by us, vs watchdog
    - [ ] Learn more about kernel messages and where they come from
      - [ ] Try to find location in source code for each message (use oops codes?)
    - [ ] Document exact configuration for building the experiment so someone can recreate it
    - [x] Make a script to generate chains
      - [x] Incorporate common events into chains
      - [x] Can we group chains into named groups?

* **Monday**:
  - Looked a bit more into memcard problem, added some notes
  - Added a table for MFTF, going to validate it some more

* **Wednesday**:
  - Reformated the docs from lansce
  - Added some info about root causes for kernel message chains

* **Thursday**:
  - Worked more on the root cause of FSBL messages

### Week 20: Oct 4 - Oct 8, 2021
  - [ ] Finalize experiment results for radiation beam test
    - [x] Adjust scripts to include fluence data from beam logs
    - [x] Create readme of all the error types encountered
    - [ ] Determine how many restarts were initiated by us, vs watchdog
    - [ ] Get to know reasons behind board restarts

* **Monday**:
  - Added Fluence data to log summaries
  - Went through and completed my list of log messages
  - _TODO:_
    - Figure out break down on board restarts, what faults happen before a restart?
    - Dive deeper on kernel error messages, what intersting data can we extract from an oops

* **Tuesday**:
  - Started looking at what events happen before a restart

### Week 19: Sep 27 - Oct 1, 2021
* **Goals**:
  - [ ] Finalize experiment results for radiation beam test
    - [x] Adjust scripts to include fluence data from beam logs
    - [ ] Determine how many restarts were initiated by us, vs watchdog
    - [ ] Get to know reasons behind board restarts
    - [ ] Create readme of all the error types encountered

* **Thursday**:
  - Scripts load fluence data from logs, still not formated right
  - Added some more fault types to the index.. getting pretty close on finding all faults
  - _TODO:_
    - Dive deeper on kernel error messages
    - Figure out break down on board restarts

* **Friday**:
  - Added kernel fault types and fixed bugs in cache matchers
  - _TODO:_
    - Merge markers and Faults
    - Add more flexible parsing for repeated lines
    - Clean up python code
    - Dive deeper on kernel error messages
    - Figure out break down on board restarts


### Week 19: Sep 20 - Sep 24, 2021
* **Goals**:
  - [ ] Finalize experiment results for radiation beam test
    - [x] Make some kind of python timeseries database of logs so we can query context
    - [ ] Adjust scripts to include fluence data from beam logs
    - [ ] Determine how many restarts were initiated by us, vs watchdog
    - [ ] Get to know reasons behind board restarts
    - [ ] Create readme of all the error types encountered

* **Monday**:
  - Created a new summary format that shows all data for each fault + counts for each run

* **Wednesday**:
  - Rewrote code for finding markers, added database for saving computed values

* **Friday**:
  - Finished cleaning up the python scripts
  - Started work on integrating Dr. Goeders MFTF calculations

### Week 18: Sep 13 - Sep 17, 2021
* **Goals**:
  - [ ] Finalize experiment results for radiation beam test
    - [ ] Create readme of all the error types encountered
    - [ ] Adjust scripts to resolve endtime
    - [ ] Adjust scripts to include fluence data from beam logs

* **Monday**:
  - Organized workspace a bit more 
  - Worked more on script for inferring end times
    - End time script kinda works, but there's a lot of rough edges in the data I want to iron out
    - Need to make a note of all the 'runs' and why they failed

* **Wednesday**:
  - Started writing a summary of experiment behavior in the test
  - Updated plot script
  - _TODO:_ 
    - Finish Updating Logs to create summary spreadsheets for each run

### Week 17: Sep 9 - Sep 10, 2021
* **Goals**:
  - [ ] Finalize experiment results for radiation beam test
    - [x] Add documentation to log processing scripts
    - [ ] Create readme of all the error types encountered
    - [ ] Adjust scripts to resolve endtime
    - [ ] Adjust scripts to include fluence data from beam logs

* **Wednesday**:
  - Spoke to Dr. Wirthlin about plans for interpreting logs
  - Added some more documentation to log parsings scripts

* **Friday**:
  - More incremental work with getting logs to compute failure to fluence data

### Week 16: Aug 30 - Sep 3, 2021
* **Goals**:
  - [ ] Finalize experiment for radiation beam test
    - [ ] Update logs to more readable format
    - [ ] Generate stats from logs, organize findings
    - [ ] MAYBE: update python scripts running the test to use a better log format
    - [ ] MAYBE: update the sdcard to make use of the test bitstream and confirm that errors are masked
    - [ ] Add documentation to log processing scripts

* **Monday**:
  - Things seem to be working over at the test

* **Tuesday**:
  - SD Card appears corrupted from test
  - Made backup images that use ramfs rather than sd card for file system
  - Using backup SD card at test, seems to work in the beam
  - Awaiting more logs from test

* **Wednesday**:
  - Awaiting more logs from test
  - Expermimenting with hybrid scrubber on mpsoc
  - Got logs back. seems to still be working good

* **Thursday**:
  - Made some log parsers for test

* **Friday**:
  - Wrote log results to csv files

### Week 15: Aug 25 - Aug 27, 2021
* **Goals**:
  - [ ] Finalize experiment for radiation beam test
    - [x] Add some kind of cpu benchmark + demo fpga design..
    - [x] Modify the Ultra96-v1 board to startup on power applied
  - [ ] Finish documentation for linux MPSoc in demo repo (maybe)

* **Wednesday**:
  - Just now getting back in town, reaching out to Dr. Goeders and Wes to finalize experiment
  - Made plan with wes to test integration with netbooter tomorrow
  - Finished test script and integrated with benchmarks on all cores
  - Modified board to start on powerup

* **Thursday**:
  - Integrated my board with rest of Ultra96 experiments
  - Add temp and voltage monitor
  - Fix CPU affinity so it actually works
  - _TODO:_
    - Create backup SD card

* **Friday**:
  - Finished packing up and testing final SD card images for test


### Week 12: Aug 2 - Aug 6, 2021
* **Goals**:
  - [ ] Add support code for radiation beam test
    - [x] Make fault injection configurable without re-compiling
    - [ ] Add some kind of cpu benchmark + demo fpga design..
    - [x] Make scrubber run automatically on startup
      - [ ] Figure out why the scrubber driver isn't loaded automatically (Maybe its due to the fpga manager being configured?)
    - [x] Enable ECC for kernel/memory/etc
  - [ ] Modify the Ultra96-v1 board to startup on power applied
  - [ ] Finish documentation for linux MPSoc in demo repo (maybe)

* **Monday**:
  - Work on breakout session presentation for this week

* **Tuesday**:
  - Work on breakout session presentation for this week
  - Continued looking for a way to bypass the push on/off switch (Dr. Goeders seems to know.. We'll wait to see what he says)

* **Wednesday**:
  - Fix Module autoload
  - Gave breakout session presentation
  - Adapted python script to program bitstream and run scrubber

* **Thursday**:
  - ~~Looks like ECC is already enabled (should talk to wes and Dr. Goeders though)~~
  - ECC must be enabled in vivado project or the ecc driver doesn't load
  - Added dhrystone benchmark to project
  - Added example fpga counter to the project
  - _TODO:_
    - Create final test driver that runs the scrubber + demo programs and records output

### Week 12: July 26 - July 30, 2021
* **Goals**:
  - [x] Learn more about Linux drivers
    - [ ] Figure out why the scrubber driver isn't loaded automatically (Maybe its due to the fpga manager being configured?)
  - [ ] Add support code for radiation beam test
    - [ ] Make fault injection configurable without re-compiling
    - [x] Add watchdog script that can restart the board over jtag/uart
    - [ ] Add some kind of cpu benchmark + demo fpga design..
    - [ ] Make scrubber run automatically on startup
    - [ ] Enable ECC for kernel/memory/etc
  - [ ] Modify the Ultra96-v1 board to startup on power applied
  - [ ] Finish documentation for linux MPSoc in demo repo (maybe for next week)

* **Monday**:
  - Read through some of the 427 documentation and studied the scrubber code to get a better understanding of how it works

* **Tuesday**:
  - Studied the code some more and wrote some documentation on how we interface with the pcap through the pmu
  - Read some of the docs for the Ultra96-v1, looking for a way to bypass the push button power on (I think its different from the v2)

* **Friday**:
  - Used python scripts from the DTRA-URA repo to build my own test driver for this experiment
  - Still need to make the script startup automatically on the petalinux side and/or make the driver script run the test

### Week 12: July 19 - July 23, 2021
* **Goals**:
  - [x] Keep trying to get petalinux working
  - [x] Email sebastian to inform him of my schedule and ask if there are any followup things to do
  - [x] Adapt Linux readback scrubber to build in a petalinux project:
    - [x] Build an app to use the existing FPGA manager API and get familiar with how it works

* **Monday**:
  - I think some of my problems were due to UART not working right, I'm going to slow it down, check the cable carefully and see what happens
  - Discovered that one of my SD Cards was having trouble. Petalinux now starts up correctly

* **Tuesday**:
  - Started working on vitis project to build pmu firmware [DONE: PMU Firmware built]
  - Discussed with Dr. Wirthlin our goals regarding upcoming radiation test
  - Going to work more on familiarizing myself with FPGA Manager API

* **Wednesday**:
  - Added Scrubber to petalinux project. Seems to build and work ok!

### Week 11: July 12 - July 16, 2021
* **Goals**:
  - [ ] Test William's files to see if I can build Petalinux for Ultra96

* **Thursday**:
  - Returned to office from vacation
  - Applied the board files for William to see if they resolve the issues I'm having with building petalinux

### Week 9: June 28 - July 2, 2021
* **Goals**:
  - [ ] Get Petalinux working for Ultra96

* **Monday**:
  - Config team meeting
  - Continued working on petalinux build for Ultra96
  - Still Stuck.. William is going to share his project with me so I can compare the differences

* **Tuesday**:
  - Helped with chip camp

### Week 8: June 21 - June 25, 2021
* **Goals**:
  - [ ] Start building Petalinux for Ultra96
  - [x] Continue debugging the baremetal MPSoc scrubber

* **Monday**:
  - Worked more on disecting my example bitstream for the Ultra96. 
  - I should be able to correleate the bitstream with non-zero frames here soon

* **Tuesday**:
  - Talked to Wesley about his experince. Offered a few tips.
  - Read up on Williams documentation on Petalinux build for Ultra96. Shouldn't be too bad.
  - Thought more about problems with the scrubber. My Frads list is significantly larger than the one in use by DTRA project.
  Maybe there was something wrong with the fradlist I created.
  - _TODO:_
    - Check out how the scrubber code masks the frame types and compare with my Fradlist Gen
    (Was my hypothisis correct about extending the frame lengths)
    - Try throwing in the fradlist from the DTRA repo and seeing what that does
    - Try commenting out that pl reset line that is removed in the DTRA repo
    - Try getting rid of the watchdog and see if anything changes
    - Adjust the printouts and see what frames are incorrect

    - Create an example Ultra96 petalinux project in the new pcap_scrubbing repo

* **Wednesday**:
  - Ran the scrubber again, and aparently it works today? I think I might have been using the wrong fradslist by mistake.
  - Documented everything up to this point, merged code changes back to repo
  - Added petalinux and Vivado demo projects to repo
  - Generated a test project for building petalinux for ultra96. It almost works.
  - _TODO:_ 
    - Test demo petalinux projects, clean up old project directories


### Week 7: June 14 - June 18, 2021
* **Goals**:
  - [ ] Create example repo for proposed pcap scrubber organization

  - [ ] Test scrubber for PR 
  - [x] Add file logging for scrubber

  - [x] Aquire an Ultra96
  - [ ] Start building the MPSoc scrubber

* **Monday**:
  - Created a basic example repo for pcap scrubbers [here](https://github.com/rjsmith1999/pcap_scrubbing)
  - Copied docs from hybrid_scrubber repo to demo repo
  - Added file logging to scrubber
  - Squashed more bugs in the hybrid scrubber

* **Tuesday**:
  - Fixed potential memory leak in hybrid scrubber
  - Discovered that my Vitis2019.2 installation is broken, yay.
  - Reinstalled Vitis.. something is still wrong?
  - But was able to make an example bare metal project for the Ultra96
  - _TODO:_
    - Add CSU/PCAP to the example project and test the scrubber
    - Finish Documenting the Bare Metal Scrubber

* **Wednesday**:
  - Figured out the the bare metal scrubber isn't working on the ultra96 because the fradslist is wrong
  - Made a baremetal fradslist gen program
  - _TODO:_
    - Fixup the fradslist gen program
    - Compare the fradlist with the new fradslist (are all the frame types the same)
    - Add my code changes back to the repo (including fradslist)
    - Maybe incorporate an example project?
    - Finish Documenting the Bare Metal Scrubber

* **Thursday**:
  - Spent some time studying the bitstream format to understand why the readback scrubber isn't working


### Week 6: June 7 - June 11, 2021
* **Goals**:
  - [x] Fix bug in crc_latch
  - [x] Finish testing new scrubber and ship to Sebastian
  - [x] Take inventory of exisiting scrubbers

* **Monday**:
  - Found the bug in crc_latch logic. I was dumb, and put a bit in the wrong place in a multi-bit wire. After opening up the project in simulation it became obvious what I did.
  - Seems to be working good on the zc706. Unfortunatly there is some bug causing fault injection to not work on the zedboard. The old scrubber works fine, but the new code with the srvcli stuff breaks things. (but only on the zedboard)
  - _TODO:_
    - Finish updating both projects to use the patched ip
      - Write hardware zed
      - Gen Project zed
      - Write TCL Script and delete IP project for now
      - Run petalinux-config get-hw on petazed
      - Commit
    - Test with fault injection _on both boards_
      - It seems faults (at least multi-bit even faults) are not detected on zedboard yet?
    - Verify with Sebastian it meets all of his requirements
    - Update Documentation to match new file structure

* **Tuesday**:
  - Oops.. At some point I gave the zedboard code the wrong device id.. it works now
  - Found another bug.. right now trying a full readback scrub after disabling/enabling the scrubber on the zed board breaks the whole board
  - Need to check: Can I replicate on zc706, can I replicate in readback only mode, what data might be left around between enabling/disabling the scrubber 
  - Fixed the above bug.. but now something else is causing random errors, only on the zc706.. need to look into it later
  - _TODO:_
    - Verify with Sebastian it meets all of his requirements
    - Update Documentation to match new file structure

* **Wednesday**:
  - Went back and realized it didn't really fix the enable/disable bug.. should be good now..
  - _TODO:_
    - Verify with Sebastian it meets all of his requirements
    - Update Documentation to match new file structure

* **Thursday**:
  - Discussed with Dr. Wirthlin future goals for pcap scrubbers and linux
  - Took inventory of exisiting scrubbers, developed plan for organization

* **Friday**:
  - Did some work on outreach project for the ELC

### Week 5: June 1 - June 4, 2021
* **Goals**:
  - [x] Apply updated ip to sebastians example projects for the zedboard and zc706
  - [x] Test on zedboard
  - [ ] Update c application to run as a client server program

* **Tuesday**:
  - Emailed Sebastian over the weekend, we discussed further changes to the scrubber we could make to support the CASPR project.
  - Quickly tested new ip on zedboard, seems to work ok
  - Finished testing the device id parameter, doesn't seem to be neccessary, probably don't need to instance the icap at all? (unless its for clocking purposes)
  - Recreated project scripts for vivado 2019.2, everything seems to be good there
  - Added some more documentation about the updated ip core. 
  - _TODO:_
    - Going to create a new version of the c code, formated like sebastians example, maybe break things out into more files

* **Wednesday**:
  - Restructured the c app in preparation for srvcli version (WIP on srv-cli branch)
    - Way more files now, but hopefully easier to maintain and adapt to the srvcli format
  - _TODO:_
    - Finish adapting code to work as srvcli

* **Thursday**:
  - Finished updated c code to work in srvcli format
  - _TODO:_
    - Figure out why the usleep delay doesn't work
    - Test with fault injection
    - Get rid of the weird 10sec delay

* **Friday**:
  - Fixed some of the timing bugs, should be pretty close to finishing now
  - Check for infinite loops (add a simulated watchdog and alert in the status message)
  - _TODO:_
    - Test with fault injection _on both boards_
    - Verify with Sebastian it meets all of his requirements
    - Update Documentation to match new file structure

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
 - Discovered that the new project I created didn't configure the processing system correctly, and that broke the petalinux config as well. After importing the zc706 preset to the new project I created, and reverting the petalinux config file to the original version, I was able to deploy my new project onto the zc706 board. 
 - New project works! Changing the ip to only write to the fifo when fecc_eccerr goes high seemed to help the zc706 board to work correctly. I should probably go back and check to make sure that was really the fix, or if other changes might be neccesary. Maybe I can discover why the frame_ecce2 does weird things on the zc706 in the first place.
 - Now: report findings to dr wirthlin and sebastian, clean up projects, etc.


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

## Rainy day TODO:
- Fix my readback only scrubber or delete it
