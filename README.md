**1. Place & Route design flow**

**1.1 Goals**

This directory aims to explain the physical design in more detail. In this tutorial, the physical design is developed for a small single-core RISC-V SoC called PULPino.

I am going to exercise the following steps:

Floorplanning

Placement

Clock Tree Synthesis

Routing

Verification

The general view of the flow is shown in the following picture:

![Screenshot 2024-12-15 204756](https://github.com/user-attachments/assets/8b71626f-c8dc-4de6-b2a3-389d8891ccbb)


**1.2 Orginize your data and setup the tool**

Before I start, it is a good idea to organize data by creating a set of directories where I will put the data generated during the design flow. Go to the directory of pulpino_soc and create the following directories:

cd pulpino_soc/do_pr

mkdir results

mkdir reports

mkdir cmd

mkdir log

mkdir tool

For the lab, you are going to use the INNOVUS tools from Cadence. Create a sourceme.csh file to do the setup and copy the following commands into your file.

setenv LM_LICENSE_FILE "28211@item0096"
source /eda/cadence/2017-18/scripts/INNOVUS_17.11.000_RHELx86.csh

Now you can source that file.

**source sourceme.csh**

And then, I can start the tool

**innovus -log log/**


