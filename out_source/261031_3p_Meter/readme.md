I need a custom PCB that integrates a microcontroller with several onboard sensors. The goal is to move from a breadboard prototype to a compact, production-ready board. I will supply the current schematic and pinout, along with preferred component part numbers; you will refine the circuit, lay out the board, and prepare fabrication-ready Gerber, BOM, and pick-and-place files.

Please create a two-layer design unless you can justify more layers for signal integrity or size constraints. All components should be surface-mount where practical so assembly can be automated later. I’m comfortable with KiCad, Altium, or Eagle—use whichever you prefer but provide the editable source files.

Before we call the job done, I’d like a brief design review over a shared screen, confirmation that all footprints match the manufacturer datasheets, and DRC/ERC reports showing no outstanding errors.

-Divide the PCB into two clearly marked areas: ESP/external DC side and mains-referenced metering side.
-Keep GND_IN, 5V_ESP, 5V_IN and 3V3_ESP on the ESP/external DC side.
-Keep RN7302, PY32, voltage dividers, CT input circuits, 3V3_O and GND_O on the metering side.
-GND_O is connected to Y phase (MY). Treat this entire metering section as live, including its 3.3V supply.
-Place U10 (CA-IS3115AW) and U13 (CA-IS3742HW) across the isolation boundary, with their respective input/output sides facing the correct areas.
-Do not connect GND_IN to GND_O. Keep copper pours, tracks and vias from bridging the isolation gap on any PCB layer.
-Maintain clearance and creepage suitable for 440VAC operation, the required insulation level and installation environment. Add PCB slots where needed.
-Keep the CT connector and SWD debug connector within the live metering area. Mark the debug connector “LIVE—Y-PHASE REFERENCED.”
-Keep mains terminals, fuses and MOVs together. Separate high-voltage tracks from sensitive CT, reference and crystal tracks.