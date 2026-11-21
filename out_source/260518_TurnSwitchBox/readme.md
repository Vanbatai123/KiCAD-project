Summary
I need an experienced KiCad PCB engineer to repair an existing ESP32-S3 PCB project so it passes JLCPCB SMT/PCBA review.

This is not a full redesign. The PCB is already routed and mostly finished. JLCPCB found package/footprint mismatches during production review.

Required fixes:
1. U2 ESP32 module footprint/package mismatch
   - Current PCB pads do not match the selected ESP32-S3 module.
   - Replace/correct U2 footprint and BOM so the selected ESP32-S3 module matches the PCB pads.
   - Native USB support must remain.

2. D6 diode package mismatch
   - JLCPCB reported the selected D6 part does not match the PCB pads.
   - Correct footprint or select a compatible JLCPCB/LCSC part.

3. F1/F2 fuse footprint mismatch
   - JLCPCB reported pad/package mismatch.
   - Correct footprint or select matching fuse parts.

4. Review BOM, CPL/Pick-and-Place, and Gerber consistency.
   - All SMT parts must match the PCB footprints.
   - Exclude/DNP non-SMT parts if required.

Deliverables:
- Corrected KiCad project
- Corrected Gerber ZIP
- Corrected BOM CSV
- Corrected CPL/Pick-and-Place CSV
- Short confirmation that the files are ready for JLCPCB PCBA order

Important:
- KiCad 9 only
- Minimal necessary changes only
- Must have JLCPCB SMT/PCBA experience
- Must understand ESP32-S3 module footprints

Budget: 50 USD fixed price.