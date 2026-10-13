# EEXI Calculator

Windows desktop application that estimates the **Energy Efficiency Existing Ship
Index (EEXI)** following the IMO MEPC guidelines.

---

## At a glance

| | |
| --- | --- |
| **Type** | Windows desktop app (WPF) |
| **Built with** | C# · .NET 5 (`net5.0-windows`) |
| **Status** | Stable: no recent changes (published May 2022) |

---

## Features

- **Vessel particulars** input.
- **Power installation:** main engines, auxiliary engines and shaft motors.
- **Power and SFOC curves** with polynomial fitting (MathNet.Numerics).
- **EEXI calculation:** reference speed, required EEXI and attained EEXI from the rule formulae.
- **Charts** of the curves (ScottPlot).
- **Load cases stored as XML**; two samples are included.

---

## Requirements

| | |
| --- | --- |
| Operating system | Windows 10 or 11 |
| Build | Visual Studio 2019 or 2022 with the **.NET desktop development** workload and the .NET 5 SDK |

> .NET 5 is out of support. To build with a current SDK, change `TargetFramework`
> in `WPF_EEXI_Calculator.csproj` to `net8.0-windows`.

---

## Building and running

1. Open `WPF_EEXI_Calculator.sln` in Visual Studio.
2. NuGet packages restore automatically on the first build.
3. Build and run with **F5**, then open `Test.xml` or `Test1.xml` to see an example.

---

## Project structure

```
WPF_EEXI_Calculator.sln
WPF_EEXI_Calculator/
├─ Model/                   Vessel, EEXI, Fuel, Enums
│  └─ PowerSystems/         MainEngine, AuxiliaryEngine, ShaftMotor, PowerSystem
├─ Helpers/                 converters and helpers
├─ UCurve.xaml(.cs)         curve editor control
└─ MainWindow.xaml(.cs)     main window
Test.xml, Test1.xml         sample load cases
```

---

## Dependencies

| Package | Used for |
| --- | --- |
| MathNet.Numerics | Curve fitting |
| ScottPlot.WPF | Charts |
| MoralesLarios.Utilities | UI helpers |

---

## Notes

`Model/zNotes.txt` keeps work-in-progress rule expressions for reference.

---

## Related projects

- [EEOI Calculator 2.0](https://github.com/JRouss1975/EEOI_Calculator_v2): the operational indicator calculated per voyage.

---

## License

Copyright © JRouss1975. All rights reserved.

No license is granted to use, copy, modify or distribute this code without written permission.
