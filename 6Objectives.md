---
layout: page
title: Research Activities
---

### Data Formatter Installation and Commissioning

As the first stage of the Fast TracKer, the Data Formatter (DF) system arranges the data into conical regions to enable of the parallelization of the  pattern recognition engines.  It takes over 1000 input links from the pixel and silicon detectors, performs cluster finding in cluster finding mezzanine cards (FTK_IM), then routes the data to the processing engine.  Massive data sharing is necessary to perform this task, therefore ATCA crates with 40Gbps full mesh backplanes are utilized. There are 32 boards distributed over 4 crates.  Each board has one Xilinx Virtex7 FPGA which controls the data routing.

The DF boards and their initial firmware were designed by Fermi National Laboratory. Our group is responsible for the final firmware development, production, testing, installation and operation of the system.

### Fast Simulation for FTK

In addition to supporting FTK hardware, we are also developing a fast simulation of the FTK system.  FTK is custom designed to implement algorithms in hardware because they are too slow to implement in software, therefore a full simulation of the system in software is slow!  Our fast simulation captures the major aspects of the FTK performance so that we can develop new trigger selection algorithms and study the impact of FTK on analyses.

### Modeling g &#8594; bb and calibrating b-quark identification tools

Higgs bosons decaying to a pair of b and anti-b quarks is the most frequent Higgs decay path. To find Higgs in this decay mode, we usually rely on finding its daughter b-quarks with neural net-based tagging algorithms which look for the characteristic decay products of hadrons containing b-quarks.  When the Higgs boson carries large amount of momentum, the problem becomes difficult. Its daughter b quarks (and their subsequent decay products) tend to be collimated in their direction of flight and end up depositing energy in a small region of the calorimeter. The conventional tools of Higgs identification may lose power due to the proximity of the two b quarks.
 
Novel b-quark identification methods and techniques that can estimate the number of hadrons depositing energy in small regions on the calorimeter are developed to help better reconstruction of Higgs boson. The performance of such tools, however, needs to be understood well before we apply them. An environment very similar to high momentum h &#8594;bb is gluon splitting to bb, which is also a large but not so well modeled background to h&#8594;bb. Our group works on correcting the modeling of this process and calibrating the new tools in this environment.


### Searches for heavier Higgs bosons   

We are searching for the [heavier cousins](http://www.pbs.org/wgbh/nova/next/physics/higgs-boson-discovered/) of the Higgs boson which are theorized in many models of physics beyond the Standard Model of particle physics.  These heavy cousins can decay to two Higgs bosons, therefore we are searching for pairs of Higgs bosons decaying to b-quarks and tau-leptons.  This measurement is foundational for an eventual measurement of Standard Model processes producing two Higgs bosons, which tells us how the Higgs interacts with itself.




