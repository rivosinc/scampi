<!--
SPDX-FileCopyrightText: 2025 Rivos Inc.

SPDX-License-Identifier: CERN-OHL-P-2.0+
-->

# README

## SCaMPI: SCM for Platform Integration
Rivos-made BMC module adheres to DC-SCMv2 for dual-node HPM, this repo contains KiCAD schematic files and associated Allegro brd file. \
We also host [HTML-style schematics](https://rivosinc.github.io/scampi/#/) for those who don't want to set up KiCAD.

## DC-SCM mode vs. PCIe CEM mode
Besides the DC-SCI interface to go with HPM, CEM fingers are included for SCaMPI to serve as a PCIe x1 CEM card, with a 50pin FFC to jump over SPI, JTAG, I2C, etc. \
Once CEM mode is no longer needed, the CEM edge can be cut off and there're 0ohms to depop for proper isolation. \
Note that DC-SCM and CEM modes are deemed mutually exclusive, simultaneous support is out of scope for SCaMPI design.

## Acronyms / Definitions
 - HPM: Host Processor Module defined in OCP DC-MHS
 - DC-SCM: Datacenter Secure Control Module
 - DC-SCI: Datacenter Secure Control Interface refers to the connector interface between the DC-SCM and the HPM
 - Honeycrisp: a Rivos proprietary board, which connects to SCaMPI via CEM edge plus 50p FFC

[![REUSE status](https://api.reuse.software/badge/github.com/rivosinc/scampi)](https://api.reuse.software/info/github.com/rivosinc/scampi)
