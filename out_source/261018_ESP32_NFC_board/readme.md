Summary
Hi there,

I have a nearly-complete 4-layer KiCad 7 PCB (55×55mm, ESP32-S3 + NFC + USB-C). An AI autorouter finished ~90% of the routing. I need a human to do the final cleanup before fab.
What needs to be done:

Fix 13 DRC clearance violations (grid-resolution artifacts, no rerouting needed — just nudge)
Route 4 remaining connections (CC1, BOOT, redundant USB-C D+ contact)
Confirm GND plane L2 and 3V3 plane L3 are filled correctly
DRC to zero errors
Export Gerbers + drill file for JLCPCB (4-layer)

I provide:

.kicad_pcb with all components placed and 35/39 nets routed
.kicad_sch schematic
Custom footprint library (fp_lib/)
DRC status report listing every issue with location and suggested fix

Requirements:

KiCad 7 (not older)
Experience with 4-layer EMC-conscious boards
Deliver: fixed .kicad_pcb + Gerbers ZIP ready for JLCPCB

I am not a PCB designer myself and I cannot evaluate the AI's work. If you open the files and find issues beyond the DRC report — wrong footprints, bad routing decisions, schematic errors, anything that would cause problems at fab or in the field — please tell me before fixing anything. I'd rather know and discuss than get a clean DRC with hidden problems.