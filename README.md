# EEXI Calculator

WPF application that estimates the Energy Efficiency Existing Ship Index (EEXI)
in line with the IMO MEPC guidelines.

## Overview

Enter the vessel particulars and its power installation - main engines,
auxiliary engines and shaft motors - and the tool computes the reference and
required speeds and the attained EEXI, using power/SFOC curves and the rule
formulae.

## Features

- Vessel particulars model
- Power systems: main engines, auxiliary engines, shaft motors
- Power (PME) and SFOC curve handling with polynomial fitting (MathNet)
- EEXI computation per rule expressions
- Charts (ScottPlot)
- Sample XML load cases

## Tech stack

- WPF, .NET 5.0-windows
- MathNet.Numerics, ScottPlot

## Repository layout

```
WPF_EEXI_Calculator/
  Model/            Vessel, EEXI, Fuel, Enums
  Model/PowerSystems  MainEngine, AuxiliaryEngine, ShaftMotor, PowerSystem
  MainWindow, UCurve
WPF_EEXI_Calculator.sln
Test.xml / Test1.xml   sample load cases
```

## Notes

The `Model/zNotes.txt` file keeps work-in-progress rule expressions for
reference.
