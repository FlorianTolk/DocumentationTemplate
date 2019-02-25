# Project Name
A brief description of the project and its intended purpose

## Hardware requirements
### Computational Resource Requirements
CPU Cores
CPU Clock Speed
RAM requirements
### Minimal Phuysical Storage
Drive Space
HHD or SSD if required
NAS or SAN if required

## Operating System Requirements
### Drivers and other software
Required Kernal Divers (including version)
SDKs/JDKs (including version)
Libraries (including version)
### System Setup
Required Operating System (including build version)
Required user permissions
Required credentials
### Additional Requirements
Third party libraries (including version)
Third Party applications (including version)
URL and download or ordering instructions for above libraries and applications
Licensing information for above libraries and applications
 - Full license needs to be included in the repository

## Application Documentation
### Deployemnt Description
Default network topology
Default IP addresses
Default Port usage
Assignment of servers and each HW
### Deployemnt Instructions
Build/Cold start/Installation Procedure from a clean system that meets all listed operating system requirements.
Installation testing instructions
Troubleshooting tips

## Licensing Information
The Licensing information must include transfer to the ADL (Dr Schatz) and a copy of or location of all licenses for all software used in vendor’s software delivery.
Software developed under this contract must have a statement of release of data rights as defined in the contract.
Any software developed under a Gnu Public License (GPL) that has been modified must be disclosed as defined in the license agreement by the vendor.

*The following information does not need to be included in teh README, but needs to included in all PR's*
## Update Documentation
Every time a new update needs to be pushed to the ADL GitHub, the vendor will push to their branch initially, including all below information.
### New version number in the push title
Version format is #.#.#
Version updating #.#.X is minor, non breaking changes
Version updating #.X.# is major, potentially breaking changes
Version updating X.#.# is a new version change of the project.
### Detailed Summary
What Software Trouble Reports(STR) or GitHub Issues are being addressed
What additional functionality are being made
What services are being changed (if multiple services are being used, Github automatically trackes what files aree being changed)

*The following do not need to be included in the README, but aims to detail how code should be documented*
## Code Documentation
The first line(s) of each file should be a comment clearly stating the purpose of the file
Each function should include a comment clearly stating its purpose within the file
License headers and copywrite statements must be included (where applicable)
Variable, operation, and arguments names should be intuative, if not they must include comments that explain their purpose
Use Camel Case when naming variables
Use white spaces consistently
Use overloaded functions conservatively
