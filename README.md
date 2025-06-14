# Packaging---Fundamentals-and-testing

This repository contains the whole summary of the hands-on work done by Abhinav Prakash during the workshop on Packaging Fundamentals and testing. The workshop offered an in-depth exploration of the semiconductor packaging process, covering essential principles, the progression of packaging technologies, and cutting-edge 2.5D/3D architectures. It delved into interconnect methods, redistribution layers (RDLs), interposers, assembly techniques, and package reliability assessments. Participants also gained practical experience through hands-on sessions involving thermal simulations, package design, and modeling using ANSYS tools.

## *Table of Contents*

* [Module 1: Evolution of Semiconductor Packaging – From Fundamentals to Advanced Integration](#Module-1)
    + [Why do we need Packaging](#Why-do-we-need-Packaging)
    + [Requirement to Packaging](#Requirement-to-Packaging)
    + [Package Structure](#Package-Structure)
    + [Types of Packaging](#Types-of-Packaging)
    + [Anatomy of Packaging](#Anatomy-of-Packaging)
    + [Nomenclature of Packaging](#Nomenclature-of-Packaging)
    + [Comparative Packaging Evaluation](#Comparative-Packaging-Evaluation)
   
    
* [Module 2: From Silicon Wafer to Complete Package – Assembly and Fabrication Processes](#Module-2)
    + [Overview of Supply Chain and Assembly Facilities](#Overview-of-Supply-Chain-and-Assembly-Facilities)
    + [Wafer Preparation Grinding and Dicing](#Wafer-Preparation-Grinding-and-Dicing)
    + [Wire Bond Assembly Die to Molding Process](#Wire-Bond-Assembly-Die-to-Molding-Process)
    + [Flip Chip Technology Face-Down Die Integration](#Flip-Chip-Technology-Face-Down-Die-Integration)
    + [Wafer-Level Packaging (WLP)](#Wafer-Level-Packaging-(WLP))
   
 
* [Module 3: Thermal Simulations of Semiconductor Packages Using ANSYS](#Module-3)
    + [Introduction With ANSYS Electronics Desktop](#Introduction-With-ANSYS-Electronics-Desktop)
    + [Lab1-Designing Flip-Chip BGA Package](#Lab1-Designing-Flip-Chip-BGA-Package)
  
          
* [Module 4: Ensuring Package Reliability – Testing and Performance Evaluation](#Module-4)
    + [Testing at Different Stages](#Testing-at-Different-Stages)
    + [Package Testing ](#Package-Testing)
      
    
* [Module 5: Package Design and Modeling: Building a Semiconductor Package from Scratch](#Module-5)
    + [Package Cross-Section Modeling in ANSYS Electronics Desktop (AEDT)](#Package-Cross-Section-Modeling-in-ANSYS-Electronics-Desktop-(AEDT))
    + [Lab2 Designing QFN](#Lab2-Designing-QFN)
    + [Final QFN Design](#Final-QFN-Design)
 

* [Appendix](#Appendix)
* [References](#references)
* [Acknowledgement](#acknowledgement)
* [Accreditation](#Accreditation)
* [Inquiries](#inquiries)


## Module 1:
## Evolution of Semiconductor Packaging – From Fundamentals to Advanced Integration
---
### Why do we need Packaging
---
Semiconductor packaging is essential for transitioning delicate silicon dies from the controlled environment of a foundry to the harsh conditions of the real world. Initially, bare dies from manufacturers like TSMC or Intel are highly vulnerable. Packaging provides:

- Protection from corrosion, moisture, and physical damage.
- Connectivity to other components through structures like Ball Grid Arrays (BGA).
This process enables integration into complex systems, such as the iPhone 15 logic board, which includes chips from companies like Broadcom, SK Hynix, and Texas Instruments
  
![image](https://github.com/user-attachments/assets/797e8483-1067-400f-9fb3-04988d265c6c)

### Requirement to Packaging
---
Below hierarchical structure of electronic integration—from chip to package to board—highlighting the critical role of packaging in connecting and protecting semiconductor devices. The right side presents key factors in choosing the right package, including:

- Application type (logic, memory, power)
- Form factor
- Reliability and durability
- Cost
- Thermal dissipation
- Pin count (I/O pins)
  
These considerations ensure optimal performance, efficiency, and integration in electronic system

![Screenshot 2025-06-09 124959](https://github.com/user-attachments/assets/3e7a726a-800f-4929-b6ca-e75f8c3c109e)

### Package Structure
---
This diagram illustrates the typical structure of an electronic package, which serves as a bridge between the silicon die and the system board (PCB). Key components include:

- Mold compound: Protects the internal components from environmental damage.
- Die: The actual semiconductor chip performing the electronic functions.
- Die-to-carrier interconnections: Enable electrical connectivity between the die and the carrier.
- Carrier: Provides mechanical support and routing for signals.
- Carrier-to-board interconnections: Link the package to the system board.
- System Board (PCB): The final platform where the package is mounted and integrated into the device.

![Screenshot 2025-06-09 125253](https://github.com/user-attachments/assets/6fc9100a-08d4-4d8e-846c-8813e711b2b0)

### Types of Packaging
---
Electronic component packaging is essential for protecting semiconductor devices and enabling their integration into systems. Packaging types are broadly classified into Through-Hole Mounting and Surface Mount Technology (SMT). Each type offers unique benefits in terms of size, performance, and application.

#### Through-Hole Mounting
- DIP (Dual In-line Package): Rectangular package with two rows of pins for insertion into a PCB.
- TO (Transistor Outline): Cylindrical or flat package for transistors with leads extending from the bottom.
- PGA (Pin Grid Array): Package with a grid of pins underneath for socket or solder mounting.
#### Surface Mount Technology (SMT)
- QFN (Quad Flat No-lead): Leadless package with solder pads underneath for compact mounting.
- QFP (Quad Flat Package): Flat square package with leads on all four sides.
- CSP (Chip Scale Package): Ultra-compact package nearly the same size as the chip itself.
- PBGA (Plastic Ball Grid Array): BGA package using plastic substrate with solder balls underneath.
- LGA (Land Grid Array): Package with flat contact pads instead of pins for board connection.
- PoP (Package on Package): Stacked ICs in a single package to save space and enhance performance.
- MCM (Multi-Chip Module): Multiple chips integrated into one module for higher functionality.
- CoWoS (Chip-on-Wafer-on-Substrate): Advanced 2.5D packaging integrating chips on a silicon interposer.

![Screenshot 2025-06-09 125548](https://github.com/user-attachments/assets/1eaef90a-c68a-43a7-89f7-7da3706b0b55)

### Anatomy of Packaging 
---
Semiconductor packaging is categorized into Leadframe, Laminate, and Advanced package substrates, each offering different levels of complexity, performance, and integration. These packages protect the chip, provide electrical connections, and support thermal and mechanical stability.

#### Leadframe Packages
- DIP (Dual In-line Package): A rectangular package with two rows of pins for through-hole mounting.
- QFN (Quad Flat No-lead): A compact surface-mount package with no leads, using pads underneath.
- Leadframe-CSP: A chip-scale package built on a leadframe for minimal size and cost.
- Leadframe-QFP: A flat package with leads on all four sides, using a leadframe base.
#### Laminate Packages
- Wire bond PBGA: A plastic BGA package using wire bonding to connect the die to the substrate.
- Flip chip PBGA: A BGA package using flip-chip bonding for better electrical performance.
- PBGA (Plastic Ball Grid Array): A cost-effective BGA package with plastic encapsulation.
- LGA (Land Grid Array): A package with flat contact pads instead of pins for board-level connection.
- FC-CSP (Flip Chip Chip Scale Package): A compact package using flip-chip technology for high I/O density.
#### Advanced Package Substrates
- 2D FCBGA Substrate: A flat flip-chip BGA substrate for high-performance applications.
- 2.1D FCBGA with RDL: Adds a redistribution layer to enhance signal routing and connectivity.
- 2.3D FCBGA with Si Interposer: Uses a silicon interposer to connect multiple dies efficiently.
- 2.5D CoWoS: Integrates SoC and HBM on a silicon interposer for high bandwidth and performance.

![Screenshot 2025-06-09 130101](https://github.com/user-attachments/assets/dd1fb42d-21e6-4ffb-a891-988a208f2425)

### Nomenclature of Packaging 
---
Below Diagrams showing how chips are integrated with package substrates and PCBs. Illustrations of packaging types like COB, PBGA, FC CSP, 2D, 2.1D, 2.5D, and 3D. Cross-sectional views and 3D models of semiconductor components.

![Screenshot 2025-06-09 130459](https://github.com/user-attachments/assets/903a2887-64b2-426d-a558-f5ebdf750aa8)

### Comparative Packaging Evaluation
---
This section aids in evaluating package types based on key factors such as, Performance, Cost, Space limitations, Thermal performance and Reliability.
Selecting the most suitable package requires balancing these factors according to the specific needs of the application, system design, and business objectives.

![Screenshot 2025-06-09 130851](https://github.com/user-attachments/assets/f32640a7-aa3e-4549-9225-8fb8fd4a5c2b)



## Module 2:
## From Silicon Wafer to Complete Package – Assembly and Fabrication Processes
---
### Overview of Supply Chain and Assembly Facilities
---
The comprehensive supply chain involved in the production of integrated circuits (ICs), broken down into five key stages:

- Design House: This initial phase involves IC design using EDA tools and foundry PDKs, resulting in a GDSII layout and test programs.
- Wafer Fabrication: Silicon wafers are processed using specialized equipment, gases, chemicals, and materials to fabricate ICs.
- Package Assembly and Test: Individual ICs are packaged using substrates, tools, and materials, then tested for functionality.
- Board Assembly and Test: Packaged ICs are mounted on PCBs and tested as part of a larger circuit.
- Product Assembly and Test: Final electronic products are assembled using various components and tools, followed by rigorous testing.

![image](https://github.com/user-attachments/assets/0083890e-c2e2-47ed-8049-7019a91f2444)
 - [VIDEO](https://www.youtube.com/watch?v=hR5orrmpoeE)
### Wafer Preparation Grinding and Dicing
---

Wafer Preparation Steps are done in controlled cleanroom environment where the wafer processing begins. ISO Class 7 ensures minimal particle contamination, whcih invilve this steps
- Wafer Preparation Area – Cleanroom (ISO Class 7) for contamination-free processing.
- Incoming Wafer Carrier – Wafers arrive in protective carriers.
- Wafer Inspection – Visual/optical check for defects.
- Front Tape Lamination – Protective tape applied to wafer front.
- Backside Grinding – Wafer thinned using grinding tools.
- Tape Frame Mounting – Wafer mounted on tape frame for stability.
- Two-Step Dicing – Laser grooving followed by blade cutting to separate chips.
  
![image](https://github.com/user-attachments/assets/24f8798a-cea1-4fe1-9526-d36e3fc6cb6a)

### Wire Bond Assembly Die to Molding Process
---
- Die Attach : Epoxy is dispensed, the chip is picked and placed on Die Attach Film (DAF).
- Curing : Heat is applied to cure the epoxy and secure the die.
- Wire Bonding : Involves wire clamping, capillary tapping, EFO spark generation, ball and tail bond formation using ultrasound and heat, and wire loop creation.
- Molding (Transfer) : Resin is transferred into a mold to encapsulate the die and wires.
- Marking (Laser) : Laser marks identification or traceability info on the molded package.

![image](https://github.com/user-attachments/assets/1363a2ac-4194-44ba-9a73-4a9cd7ee52fb)

### Flip Chip Technology Face-Down Die Integration
---

- Bump Formation – Solder bumps are formed on the silicon chip.
- Solder Reflow – Bumps are melted and solidified.
- Chip Flipping – Chip is flipped face-down.
- Flux Dispensing – Flux is applied to the substrate.
- Chip Placement – Flipped chip is placed on the substrate.
- Solder Reflow – Electrical connections are formed.
- Flux Cleansing – Residual flux is cleaned.
- Underfill Dispensing – Underfill is applied around the chip.
- Underfill Curing – Underfill is cured with heat.
- Ball Mounting & Reflow – Solder balls are added and reflowed.
- Molding & Marking – Final encapsulation and laser marking.

![image](https://github.com/user-attachments/assets/c66467a8-9f9e-4300-8bd7-0b424f5aa12c)

### Wafer-Level Packaging (WLP)
---
#### Reconstitution Process
- Diced dies are picked and placed on a temporary carrier.
- Dies are molded to form a reconstituted wafer.
- Carrier is released.
#### Solder Ball Attach
- Solder balls are attached to the reconstituted wafer.
#### RDL (Redistribution Layer) Preparation
- Dielectric and metal layers are coated.
- Multiple rounds of RDL patterning are performed.
#### Final Steps
- Laser marking and singulation complete the Fan-out WLP.

  
![image](https://github.com/user-attachments/assets/c2332ca8-ad66-4cba-936a-efbc345bc563)

## Module 3:
## Thermal Simulations of Semiconductor Packages Using ANSYS
---
### Introduction With ANSYS Electronics Desktop
---
ANSYS Electronics Desktop (AEDT) is an integrated multi-physics simulation platform that combines tools for electromagnetic, signal integrity, thermal, and electro-mechanical analysis. It is extensively used for the design and evaluation of high-speed electronic circuits and systems.
### Lab1 Designing Flip-Chip BGA Package
---
#### Step 1 : Open AEDT and launch Icepak

- **NOTE** If Icepak is not visible then go to ```Tool -> Options -> General Options``` and change the Set Target Configurations to All
![image](https://github.com/user-attachments/assets/7249ad28-0a23-4b02-a79a-f9ad053f82b7)

#### Step 2 : Create a Flipchip BGA Package
- To generate Flipchip BGA Package ``` Icepak -> Toolkit -> Geometry -> Packages -> Flipchip_BGA```
- We configure the dimensions and various parameters of the package, substrate, die, die underfill, and solder balls here.
- Once all settings are adjusted, click OK to generate the package model.
![Untitled](https://github.com/user-attachments/assets/b079a79d-b467-420c-b096-ebd2003de508)

#### Package generated by Icepak
![image](https://github.com/user-attachments/assets/51a007f0-0b4f-4127-8c0d-37ad85f1d874)

#### Step 3 : Examine the 3D package model
- Below is the examine the 3D package model structure within Icepak.

#### Ball Group 
![Screenshot (3017)](https://github.com/user-attachments/assets/dda1b12c-97c0-4980-8919-1a5352d8e7aa)
#### Substrate
![Screenshot (3018)](https://github.com/user-attachments/assets/f4f4366e-c435-4c0d-9e03-7a077e7e4097)
#### Die Underfill 
![Screenshot (3019)](https://github.com/user-attachments/assets/e2f02480-0a47-4262-8343-9baec7075908)
#### Die
![Screenshot (3020)](https://github.com/user-attachments/assets/64143e4c-2763-49c4-a58e-4921d2ba33a5)

#### Step 4 : Add Source Thermal Model for Die
![Screenshot (3021)](https://github.com/user-attachments/assets/277c9bd0-66de-4dbb-8682-631e2994dd5b)

#### Step 5 : Add Source Thermal Model for Substrate
- In the sub-window that appears, select Temperature
- Repeat the same to add thermal monitors for the die and the die-underfill.
- 
![Screenshot (3022)](https://github.com/user-attachments/assets/0534aad3-5309-42da-a4df-50b60c4b561a)

#### Step 6 : Meshing And Running The Thermal Analysis
- Navigate to the Simulation tab and click on Generate Mesh.
- If prompted, save the project and wait for the mesh generation to complete.
- Make note of any errors or warnings that appear, and either ignore them if appropriate or take the necessary steps to debug and resolve the issues.

![Screenshot (3024)](https://github.com/user-attachments/assets/490e31e4-28b0-4481-9d37-cf8a4511790c)


#### Step 7 : Review Mesh Quality metrics
- After the mesh is generated, review its quality metrics, including Face Alignment, Skewness, and Volume.

![Untitled1](https://github.com/user-attachments/assets/1d920d29-4209-4e8f-af03-401413144d9e)

#### Step 8 : Thermal Analysis
- Under Project Manager, right click on ```Analysis -> Add Analysis Setup``` and configure the solver settings as required.

![Screenshot (3038)](https://github.com/user-attachments/assets/98f2c475-a515-42cf-a5cd-5e58bae654fe)

#### Step 9 : Viewing Results
- Next, validate the simulation setup:
- Click the Validate button in the top ribbon and confirm that all checks pass successfully.

![Screenshot (3039)](https://github.com/user-attachments/assets/bff91c03-534c-4ba5-b4fa-2364e72ff1c0)

#### Step 10 : Plot the temperature map
- Click on Analyze All button in the top ribbon
- After the simulation is complete, use the left mouse button to draw a selection rectangle in the 3D view and select the entire FC-BGA package.
- Right click and then select ```Plot Fields -> Temperature -> Temperature```
- Configure the different plot options:
    + Specify Name, Folder
    + Plot on Surface only
    + Surface Smoothing -> Enable Gaussian Smoothing
      
![Screenshot (3041)](https://github.com/user-attachments/assets/a1499e56-fdd5-438d-ab87-2b90d34ff8ff)
#### Field Plot
![Screenshot (3044)](https://github.com/user-attachments/assets/d564aecf-83e8-4d2b-acdc-28922dd9e666)

## Module 4:
## Ensuring Package Reliability – Testing and Performance Evaluation
---
This module emphasizes the quality assurance and testing phases of semiconductor packaging, which are crucial for detecting functional defects and ensuring long-term reliability.
### Testing at Different Stages
---
Here is the outlines the end-to-end process of semiconductor packaging and testing, involving both the Foundry and **OSAT (Outsourced Semiconductor Assembly and Test)** facilities. The journey begins with front-end manufacturing and wafer probe testing at the foundry, followed by wafer sorting to identify functional dies. These steps ensure only high-quality components proceed to packaging.

At the OSAT stage, sorted dies undergo package manufacturing, followed by package testing and **system-level tests (SLT)** to verify performance under real-world conditions. Throughout the entire process, there is continuous process development and in-depth diagnosis and failure analysis to maintain product quality, improve yield, and ensure long-term reliability.

![image](https://github.com/user-attachments/assets/6cd77fbd-b603-432f-9de9-b2c34225ae2d)

### Package Testing 
---
These are the three key stages in the post-assembly semiconductor testing process. The first stage, AOST (Assembly Open and Short Test), checks for electrical continuity issues such as open circuits or shorts caused during the assembly process. It ensures the basic integrity of the package before further testing.
Next is the Burn-in stage, where devices are subjected to elevated thermal and voltage conditions to simulate early-life operating stress. This helps identify and eliminate weak units. Finally, in the Final Test, devices undergo both cold and hot temperature testing to verify their functional, parametric, and reliability specifications, ensuring they perform correctly under various environmental conditions.

![image](https://github.com/user-attachments/assets/fda776d1-97f4-4137-8f48-e26c1b6ff682)

#### AOST (Assembly Open and Short Test)

![image](https://github.com/user-attachments/assets/df15b6eb-ac56-4110-8cc9-e19033d54183)

#### Burn-in Test

![image](https://github.com/user-attachments/assets/1906d914-2cc7-4763-ba73-fd338b978268)

#### Final Test

![image](https://github.com/user-attachments/assets/e40f5077-688d-46b3-8849-261d10fa4325)


## Module 5:
## Package Design and Modeling: Building a Semiconductor Package from Scratch
---
### Package Cross-Section Modeling in ANSYS Electronics Desktop (AEDT)
---
- Here we will primarily focuses on constructing the full cross-section of a wire bond package, incorporating elements such as the die, substrate, bonding wires, and mold compound, without involving any simulations or analyses.

![image](https://github.com/user-attachments/assets/c543ce72-77de-44d3-ba4d-55eb4a646677)

### Lab2 Designing QFN
---
The primary objective of this lab is to construct a full cross-sectional model of a QFN(Quad Flat No-lead) wire bond package—comprising the die, substrate, bond wires, and mold compound—without conducting any simulations or analyses.
Below table shows the detail about the design

| Component            | Properties                                                                 |
|----------------------|----------------------------------------------------------------------------|
| **Die**           | Material: Silicon  <br> Dimensions: 3mm x 3mm  <br> Die Height: 0.2 mm      |
| **Substrate**     | Material: FR4  <br> Dimensions: 5mm x 5mm  <br> Height: 0.5 mm              |
| **Die Attach**    | Material: Modified Epoxy  <br> Dimensions: 3mm x 3mm  <br> Thickness: 0.1 mm|
| **Die Bond Pads** | Material: Copper  <br> Dimensions: 0.2mm x 0.2mm  <br> Thickness: 0.005 mm  |
| **Substrate Bond Pads** | Material: Copper  <br> Dimensions: 0.2mm x 0.2mm  <br> Thickness: 0.005 mm |
| **Bond Wire**     | Material: Gold wire  <br> Type: JEDEC 4-point                              |
| **Mold Compound** | Material: Epoxy  <br> Dimensions: 5mm x 5mm  <br> Thickness: 1.2 mm         |

#### Step 1 : Launch Q3D
![Screenshot (3057)](https://github.com/user-attachments/assets/df8413dd-ac23-4d1f-a6fc-89523c871a12)

#### Step 2 : Creating the Die and Substrate
**Create the Die Geometry**
- Use the Rectangle tool from the ribbon or navigate through Menus ```Draw → Rectangle``` to draw a rectangle.
- Next, double-click on CreateRectangle Model → Rectangle1 to open its Properties dialog box.
- Set one corner at the origin (0, 0, 0) and define the dimensions as 3 mm × 3 mm.
- Then, select ```Model → Rectangle1``` and go to ```Modeler → Surface → Thicken Sheet...``` from the menu bar.
- Set the thickness to 200 microns (0.2 mm).

**Assign Material Properties**
- Open the Properties dialog box by double-clicking on ```Model → Rectangle1```
- Rename the geometry to Die and select Silicon as the material from the Material Library.

#### Die Geometry
![Screenshot (3063)](https://github.com/user-attachments/assets/2a00f482-8f9f-4604-bd82-e8bf31aa310f)
#### Die Material
![Screenshot (3062)](https://github.com/user-attachments/assets/3648013c-eba9-4052-aef6-220dacfda0ac)

- Similary Design the Substrate below the die

#### Step 3 : Die Attach Material and Bond Pads

- Draw a rectangle with the same dimensions as the die (3 mm × 3 mm) and position it at the same coordinates (0, 0, 0).
- Set its thickness to -100 microns (-0.1 mm), since the DAM layer is located beneath both the die and the substrate.
- Assign "Modified Epoxy" as the material.
- **Note:** Use distinct colors or shades for adjacent components to ensure clear differentiation in the 3D view.

![Screenshot (3070)](https://github.com/user-attachments/assets/b5479947-f3d5-4d5c-ba89-06a195235fd1)

#### Step 4 : Creating Bond pads 
- Draw 2 Bond pad on Die and Substarte 
- Draw a small rectangle and set its dimensions to match that of the die pad (0.2 mm × 0.2 mm).
- Position the first die pad at coordinates (0.2, 0.2, 0.2) so that it rests on top of the die and aligns with one of its edges.
- Set the thickness to 5 microns (0.005 mm).
- Similarly, create a small rectangle and set its dimensions to match the substrate bond pad size (0.2 mm × 0.2 mm).
- Position this substrate bond pad at coordinates (0.2, -0.7, -0.1), ensuring it is aligned with the previously created die bond pad and placed on top of the substrate.
- Set its thickness to 10 microns (0.010 mm).

![Screenshot (3075)](https://github.com/user-attachments/assets/b8856988-6514-4019-b6ba-f5a2fc7b5ec0)

#### Step 5 : Wire Bond Creation and Material Assignment
- Create bond wires using the Bondwire tool located under: ```Draw → Bondwire```.
- Connect the center of the die bond pad to the center of the substrate bond pad. For easier placement, switch to the Top view orientation.
- Set the bond wire type to JEDEC 4-point and assign Gold as the material.
![Screenshot (3079)](https://github.com/user-attachments/assets/b4f97b2a-dc79-42ea-b282-62eea1682eb2)

- Similary Crete all over the Die to get QFN(Quad Flat No-lead) Design

![Screenshot (3080)](https://github.com/user-attachments/assets/da613b54-e215-4463-9d51-da8df76e9d19)
![Screenshot (3082)](https://github.com/user-attachments/assets/1839a3ee-eb5d-48ad-89eb-ff63eefd5d79)

#### Step 6 : Applying the Mold Compound and Finalizing the Package Model
- Create a rectangular enclosure with dimensions 5 mm × 5 mm and a thickness of 1.2 mm to encapsulate the die and bond wires.
- Position it at coordinates (-1, -1, -0.1) so that it sits above the substrate, fully covering the top side.
- The 1.2 mm thickness ensures complete coverage of the die and bond wires while providing sufficient clearance for laser marking or other post-packaging processes.
![Screenshot (3095)](https://github.com/user-attachments/assets/a5b5ccd9-fa2e-4ebd-86c9-3b83d5985512)


### Final QFN Design
---
![Untitled4](https://github.com/user-attachments/assets/90e75398-648a-4cf8-937a-1c5f89770fa3)



## References
---
- [Amkor Manufacturing](https://www.youtube.com/watch?v=hR5orrmpoeE)
- [Ansys Electronics Desktop Student](https://www.ansys.com/en-in/academic/students/ansys-electronics-desktop-student)



## Acknowledgement
---
Finally, I would like to express my sincere gratitude to [Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/){Co-founder of VLSI System Design (VSD) Corp. Pvt. Ltd.} and Tarun Kumar Agrawal {Dept. of Electrical Engineering IIT Gandhinagar}   for help me in understanding the Packaging - Fundamentals-and-testing. The workshop was excellent and well-designed, this workshop taught about Packaging Design and Techniques 

## Accreditation
---
- To be added.....!
## Inquiries
---
- Connect with me at [LinkedIn](https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile)
