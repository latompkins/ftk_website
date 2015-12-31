---
layout: post
title: Data Formatter Board Production Testing
---
<em> By Rex Brown </em>

We recently finished testing 37 FPGA-based boards that will be used to augment the triggering system of the ATLAS experiment at LHC. What do these boards allow us to do, you ask? They allow us to organize a high-speed stream of data, 800 Gbps, into an easily readable and accessible format for downstream usage. ATLAS collects raw data at a rate of 1 petabyte, or 1000 terabytes, per second! It is impossible to write all of this data to disk due to this astronomical rate, so triggering (rapidly deciding which events in a particle detector should be kept) becomes very important. We want to save the most interesting events, so this need be done carefully. Currently, the job that these boards will do is done with software. This is great, except for the fact that the software can’t run quite fast enough to keep up with the flow of data. Therefore, implementing our software algorithms into hardware allows us to be able to keep up with a data rate that increases as as the LHC increases the collision rate and the experiment makes modifications. This forces us to be on the cutting-edge of technology, since the boards will need to remain current for many years.

<figure>
<img src="pictures/posts/DFPic.jpg">
<figcaption>The Data Formatter (DF) board and attached Rear Transition Module (RTM). Note the four uninhabited areas of the board where the Input Mezzanines (IMs) usually live. The large black area near the center of the board is the heat sink for the Virtex-7 FPGA.</figcaption>
</figure>

Testing such high-performance hardware takes great care. A visual inspection upon receiving the boards rules out obvious issues such as incorrect capacitor polarity or warped circuit boards. After passing this test, the boards are labeled to prevent any confusion that arises from having 37 identical pieces of hardware. Next, we attempt to program the Field-Programmable Gate Array (FPGA) after inserting the board into our crate. FPGAs offer unparalleled flexibility in processing data exactly the way that we want to. Different firmware fundamentally alters how the FPGA operates, making it maximally customizable. At this point, we start more intense testing of the individual transceivers of the FPGA and their connections. Data Formatter (DF) boards are connected to each other within a single crate by what’s called a backplane, that allows communication speeds of up to 40 Gbps per transceiver quad, of which there are 20 total on the FPGA. Connections between the total of four crates is accomplished through QSFP cables that are made of optical fibers. This allows for reliable, high-speed communication over longer distances. One final test is a check of the communication between the DF and the Input Mezzanines (IMs) that the data comes in through. 
The network topology used in the Data Formatter system is somewhat beautiful. It consists of 32 boards, spread across four crates of 8 boards each, and is illustrated below in Figure 1.

<figure>
<img src="pictures/posts/df_network_topology.png">
<figcaption>The fabric interface connections in 14-slot full mesh ATCA backplane. Each line represents a multi-lane bidirectional channel rated for up to 40 Gbps. A graphical depiction of the 32 boards (in green) and high speed interconnect lines in four crate system. Blue lines represent backplane data paths. Orange lines represent inter-crate fiber links.</figcaption>
</figure>

As you might imagine, challenges are encountered along the way. Mechanical issues and improper soldering of various components caused some Rear Transition Modules (RTMs) to be unusable. The RTM connects to the back of the DF, and provides the means to connect to either downstream, for further processing, or other crates of boards. New RTMs were being tested in parallel with new DFs, so test results often required in-depth interpretation to find what the issue was. In the end, the vast majority of the boards and RTMs were tested to be fully-functioning, and were shipped off to CERN!

The board which the DF system uses are Pulsar IIb boards, which were designed at Fermilab.  More on the Pulsar IIbs can be found at [ATCA@FNAL](http://www-ppd.fnal.gov/ATCA/). 