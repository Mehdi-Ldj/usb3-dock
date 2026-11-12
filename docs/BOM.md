# Bill of materials

One row per designator: the value the schematic asks for, the manufacturer part
number that meets it, and the LCSC code the assembler orders. This table is the
input to the assembly file — a part on the board with no row here, or a row that
disagrees with the board on value or footprint, stops the BOM from being written.

**182 designators, 174 of them placed.** R22 is marked do-not-populate (CONFIG1
recovery), and seven board features — three fiducials, four mounting holes — are
fabrication options rather than parts. The orderable files, `jlc-bom.csv` (47
lines after identical parts are collapsed) and `jlc-cpl.csv`, ship in the
fabrication package attached to the release.

Policy applied to the passives: **0402 for every 100 nF**, in two lines —
`C1525` 16 V for the 50 positions at 5 V or below, `C307331` 50 V for the two
on +12 V — 0603 for other signals and decoupling, 0805 for the current-sense
shunts and for 10 uF, 1210 for bulk, C0G for anything under 1 nF and for the
crystals' load caps, X5R/X7R elsewhere, 1 % on every resistor including the
CC dividers.

| Ref | Value | MPN | LCSC | Part class / footprint |
|---|---|---|---|---|
| C1 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C2 | 100p | 0402CG101J500NT | C1546 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C4 | 4u7 | CC0603KRX5R8BB475 | C326580 | 0603 X5R 25 V; footprint Capacitor_SMD:C_0603_1608Metric |
| C10 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C11 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C12 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C13 | 100n | CL05B104KB54PNC | C307331 | 0402 X7R 50 V ±10 %; on the 12 V rail; footprint Capacitor_SMD:C_0402_1005Metric |
| C20 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C21 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C30 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C31 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C40 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C41 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; 1.2 V buck output, 2 × 10 µF in parallel (SLVSDG1C §8.2.2.5: Cout 10–47 µF, 22 µF standard for 2.2 µH at 1.2 V); footprint Capacitor_SMD:C_0805_2012Metric |
| C50 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C51 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C52 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C58 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; U25 decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C53 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C54 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C55 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C56 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C65 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C66 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C67 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C68 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C69 | 100u | CGA1210X5R107M160RT | C6120014 | 1210 X5R 16 V ±20 %; footprint Capacitor_SMD:C_1210_3225Metric |
| C70 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C71 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C72 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C73 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C74 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C75 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C76 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C77 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +3V3 (U2) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C80 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C81 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C82 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C83 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C84 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C85 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C86 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C87 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C88 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C89 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C90 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; +1V2 (U2 core) decoupling; footprint Capacitor_SMD:C_0402_1005Metric |
| C91 | 1u | TCC0603X5R105K160CT | C696901 | 0603 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0603_1608Metric |
| C92 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C93 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C105 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C106 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C107 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C108 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C109 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C110 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C111 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C120 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0805_2012Metric |
| C121 | 1u | TCC0603X5R105K160CT | C696901 | 0603 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0603_1608Metric |
| C122 | 1u | TCC0603X5R105K160CT | C696901 | 0603 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0603_1608Metric |
| C123 | 1u | TCC0603X5R105K160CT | C696901 | 0603 X5R 16 V ±10 %; footprint Capacitor_SMD:C_0603_1608Metric |
| C124 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C125 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C126 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C127 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C128 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C129 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C130 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C131 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C132 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C133 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C134 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C136 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C137 | 18p | 0402CG180J500NT | C1549 | 0402 C0G 50 V ±5 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C138 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; footprint Capacitor_SMD:C_0402_1005Metric |
| C139 | 1u | 0805B105K250NT | C89190 | 0805 X7R 25 V ±10 %; CH224A VHV decoupling, 25 V gives 48 % derating on the 12 V rail; footprint Capacitor_SMD:C_0805_2012Metric |
| C140 | 100n | CL05B104KB54PNC | C307331 | 0402 X7R 50 V ±10 %; on the 12 V rail; U1 VIN second bypass (pin 11 side, TI: equal caps each side); footprint Capacitor_SMD:C_0402_1005Metric |
| C141 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; U1 VIN bulk, 4th of four (TI recommends 40 µF); footprint Capacitor_SMD:C_0805_2012Metric |
| C142 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C143 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C144 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C145 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C146 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C147 | 100n | CL05B104KO5NNNC | C1525 | 0402 X7R 16 V ±10 %; USB 3.2 AC coupling (0402 chosen for pair fan-out); footprint Capacitor_SMD:C_0402_1005Metric |
| C148 | 10u | TCC0805X5R106K160FT | C380332 | 0805 X5R 16 V ±10 %; 1.2 V buck output, second of the 2 × 10 µF pair with C41; footprint Capacitor_SMD:C_0805_2012Metric |
| D1 | SMBJ15A | SMBJ15A | C113988 | SMB TVS 15 V; footprint Diode_SMD:D_SMB |
| D2 | LED | KT-0603R | C2286 | 0603 LED; footprint LED_SMD:LED_0603_1608Metric |
| D3 | LED | KT-0603R | C2286 | 0603 LED; footprint LED_SMD:LED_0603_1608Metric |
| F1 | 3A | 0468003.NRHF | C41342 | 1206 slow fuse 3 A; footprint Fuse:Fuse_1206_3216Metric |
| J1 | USB_C PWR | 12401610E4#2A | C5119948 | USB-C 24P receptacle, Amphenol; 6330 in stock; footprint Connector_USB:USB_C_Receptacle_Amphenol_12401610E4-2A |
| J2 | USB_C UFP | 12401610E4#2A | C5119948 | USB-C 24P receptacle, Amphenol; 6330 in stock; footprint Connector_USB:USB_C_Receptacle_Amphenol_12401610E4-2A |
| J3 | USB3_A | U231-091N-4BLRA00-S | C2880618 | USB 3.0 A receptacle, right-angle, SMD contacts + TH shell; footprint dock:USB_A_Receptacle_XKB_U231-091N-4BLRA00-S |
| J4 | USB3_A | U231-091N-4BLRA00-S | C2880618 | USB 3.0 A receptacle, right-angle, SMD contacts + TH shell; footprint dock:USB_A_Receptacle_XKB_U231-091N-4BLRA00-S |
| J5 | USB3_A | U231-091N-4BLRA00-S | C2880618 | USB 3.0 A receptacle, right-angle, SMD contacts + TH shell; footprint dock:USB_A_Receptacle_XKB_U231-091N-4BLRA00-S |
| J6 | USB_C DFP | 12401610E4#2A | C5119948 | USB-C 24P receptacle, Amphenol; 6330 in stock; footprint Connector_USB:USB_C_Receptacle_Amphenol_12401610E4-2A |
| J7 | RJ45 MagJack | HR911130A | C54408 | RJ45 gigabit magjack, Bob Smith to chassis; footprint dock:RJ45_Hanrun_HR911130A |
| J8 | USB_A | 67643-2910 | C564920 | USB 2.0 A receptacle, Molex; 2055 in stock; footprint Connector_USB:USB_A_Molex_67643_Horizontal |
| J9 | SWD | PZ254V-11-04P | C2691448 | 2.54 mm 1x4 pin header; footprint Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical |
| L1 | 4u7 | CMLO0650H4R7MTT | C439009 | shielded 4.7 µH ≥ 8 A, 7 × 6.6 mm; footprint dock:L_7.1x6.6mm_CMLO0650H |
| L2 | 2u2 | PNR4020-2R2M | C54620130 | shielded 2.2 µH ≥ 2 A, 4 × 4 mm; footprint dock:L_4x4mm_PNR4020 |
| L3 | 3u3 | FNR4030S3R3MT | C167870 | shielded 3.3 µH ≥ 2 A, 4 × 4 mm; footprint dock:L_4x4mm_FNR4030 |
| R2 | 73k2 | 0603WAF7322T5E | C14890 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R3 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R4 | 56k | 0603WAF5602T5E | C23206 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R5 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; U1 PGOOD pull-up to VREG5 (TI: 10 kΩ to VREG5); footprint Resistor_SMD:R_0603_1608Metric |
| R10 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R11 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R20 | 12k | 0603WAF1202T5E | C22790 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R21 | 200k | 0603WAF2003T5E | C25811 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R22 | 200k | 0603WAF2003T5E | C25811 | 0603 ±1 %, DNP (CONFIG1 recovery); footprint Resistor_SMD:R_0603_1608Metric |
| R23 | 200k | 0603WAF2003T5E | C25811 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R24 | 200k | 0603WAF2003T5E | C25811 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R25 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R28 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R29 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R30 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R31 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R32 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R33 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R34 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R40 | 5k1 | 0603WAF5101T5E | C23186 | 0603 ±1 % (CC, 1 % required by USB-C); footprint Resistor_SMD:R_0603_1608Metric |
| R41 | 5k1 | 0603WAF5101T5E | C23186 | 0603 ±1 % (CC, 1 % required by USB-C); footprint Resistor_SMD:R_0603_1608Metric |
| R42 | 330 | 0603WAF3300T5E | C23138 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R43 | 56k | 0603WAF5602T5E | C23206 | 0603 ±1 % (CC, 1 % required by USB-C); footprint Resistor_SMD:R_0603_1608Metric |
| R44 | 56k | 0603WAF5602T5E | C23206 | 0603 ±1 % (CC, 1 % required by USB-C); footprint Resistor_SMD:R_0603_1608Metric |
| R45 | 330 | 0603WAF3300T5E | C23138 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R46 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R47 | 100k | 0603WAF1003T5E | C25803 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R50 | 0R1 | RL10FTNR100 | C160917 | 0805 0.1 Ω ±1 % 250 mW, 81 mW dissipated; footprint Resistor_SMD:R_0805_2012Metric |
| R51 | 0R1 | RL10FTNR100 | C160917 | 0805 0.1 Ω ±1 % 250 mW, 81 mW dissipated; footprint Resistor_SMD:R_0805_2012Metric |
| R52 | 0R1 | RL10FTNR100 | C160917 | 0805 0.1 Ω ±1 % 250 mW, 81 mW dissipated; footprint Resistor_SMD:R_0805_2012Metric |
| R53 | 0R1 | RL10FTNR100 | C160917 | 0805 0.1 Ω ±1 % 250 mW, 81 mW dissipated; footprint Resistor_SMD:R_0805_2012Metric |
| R54 | 0R1 | RL10FTNR100 | C160917 | 0805 0.1 Ω ±1 % 250 mW, 81 mW dissipated; footprint Resistor_SMD:R_0805_2012Metric |
| R55 | 4k7 | 0603WAF4701T5E | C23162 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R56 | 4k7 | 0603WAF4701T5E | C23162 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R70 | 2k | 0603WAF2001T5E | C22975 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R71 | 12k | 0603WAF1202T5E | C22790 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R72 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R80 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R81 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R82 | 1k | 0603WAF1001T5E | C21190 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R83 | 1k | 0603WAF1001T5E | C21190 | 0603 ±1 %; footprint Resistor_SMD:R_0603_1608Metric |
| R85 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; U1 EN divider lower leg; footprint Resistor_SMD:R_0603_1608Metric |
| R86 | 5k1 | 0603WAF5101T5E | C23186 | 0603 ±1 %; CC1 pull-down, power port; footprint Resistor_SMD:R_0603_1608Metric |
| R87 | 5k1 | 0603WAF5101T5E | C23186 | 0603 ±1 %; CC2 pull-down, power port; footprint Resistor_SMD:R_0603_1608Metric |
| R88 | 330 | 0603WAF3300T5E | C23138 | 0603 ±1 %; green magjack LED series resistor, J7 pin 11 to +3V3, LED0 sinks; footprint Resistor_SMD:R_0603_1608Metric |
| R89 | 330 | 0603WAF3300T5E | C23138 | 0603 ±1 %; yellow magjack LED series resistor, J7 pin 14 to +3V3, LED1 sinks; footprint Resistor_SMD:R_0603_1608Metric |
| R90 | 200k | 0603WAF2003T5E | C25811 | 0603 ±1 %; U1 MODE divider upper (RM_H to VREG5), FCCM/ILIM/400 kHz per TPS56C215 Table 6-3; footprint Resistor_SMD:R_0603_1608Metric |
| R91 | 10k | 0603WAF1002T5E | C25804 | 0603 ±1 %; U1 MODE divider lower (RM_L to AGND); footprint Resistor_SMD:R_0603_1608Metric |
| U1 | TPS56C215 | TPS56C215RNNR | C473372 | VQFN-18-HR 3.5x3.5; footprint dock:Texas_RNN0018A_TPS56C215 (TI RNN0018A)|
| U2 | USB5807C | USB5807CT/KD | C628616 | VQFN-100 12x12 |
| U3 | TLV76133 | TLV76133DCYR | C7527500 | SOT-223 |
| U5 | TLV62569 | TLV62569DBVR | C141836 | SOT-23-5 |
| U6 | LAN7800 | LAN7800T-I/VSX | C625080 | SQFN-48 6x6 |
| U7 | HD3SS3212 | HD3SS3212IRKSR | C544517 | VQFN-20; footprint dock:DHVQFN-20-1EP_2.5x4.5mm_P0.5mm_EP1x3mm_TI |
| U25 | HD3SS3212 | HD3SS3212IRKSR | C544517 | VQFN-20; upstream SS orientation mux for J2, mirrors U7; footprint dock:DHVQFN-20-1EP_2.5x4.5mm_P0.5mm_EP1x3mm_TI |
| U8 | STM32F072C8 | STM32F072C8T6 | C80488 | LQFP-48 |
| U9 | TPS2065 | TPS2065DBVR | C133792 | SOT-23-5 |
| U10 | TPS2065 | TPS2065DBVR | C133792 | SOT-23-5 |
| U11 | TPS2065 | TPS2065DBVR | C133792 | SOT-23-5 |
| U12 | TPS2065 | TPS2065DBVR | C133792 | SOT-23-5 |
| U13 | TPS2065 | TPS2065DBVR | C133792 | SOT-23-5 |
| U14 | INA219 | INA219AIDCNR | C87469 | SOT-23-8 |
| U15 | INA219 | INA219AIDCNR | C87469 | SOT-23-8 |
| U16 | INA219 | INA219AIDCNR | C87469 | SOT-23-8 |
| U17 | INA219 | INA219AIDCNR | C87469 | SOT-23-8 |
| U18 | INA219 | INA219AIDCNR | C87469 | SOT-23-8 |
| U19 | TMP112 | TMP112BIDRLR | C3019123 | SOT-563; UMW second source. TI TMP112AIDRLR (C28927) is short at the fab; the TI fallback is TMP102AIDRLR (C99269), same pinout and register map |
| U20 | TMP112 | TMP112BIDRLR | C3019123 | SOT-563; UMW second source. TI TMP112AIDRLR (C28927) is short at the fab; the TI fallback is TMP102AIDRLR (C99269), same pinout and register map |
| U21 | TLV7031 | TLV7031DBVR | C2869832 | SOT-23-5 |
| U26 | TLV7031 | TLV7031DBVR | C2869832 | SOT-23-5; compares UP_CC1/UP_CC2, drives U25 SEL (upstream plug orientation) |
| U22 | SRV05-4 | SRV05-4.TCT | C13612 | 4-channel TVS array SOT-23-6, 5 V, < 5 pF; footprint Package_TO_SOT_SMD:SOT-23-6 |
| U23 | SRV05-4 | SRV05-4.TCT | C13612 | 4-channel TVS array SOT-23-6, 5 V, < 5 pF; footprint Package_TO_SOT_SMD:SOT-23-6 |
| U24 | CH224A | CH224A | C42459160 | ESSOP10; USB PD sink controller, strapped to 12 V; footprint Package_SO:SSOP-10-1EP_3.9x4.9mm_P1mm_EP2.1x3.3mm |
| Y1 | 25 MHz | X322525MMB4SI | C70582 | 3225 |
| Y2 | 25 MHz | X322525MMB4SI | C70582 | 3225 |
| Y3 | 8 MHz | X50328MSB2GI | C115962 | 5032 |


## Where the parts depart from the class the schematic asked for

Two lines are not what the sheet says, each for a reason that is a fact about
the catalogue, not a preference:

- **C4, 4.7 uF.** There is no 4.7 uF 0603 part at 50 V in any dielectric in
  the catalogue: 0603 X7R stops below that at every stocked maker. C4 sits on
  `VREG5`, the 5 V converter's own LDO output, so 25 V is 5× headroom. It ships
  as 0603 X5R 25 V.
- **L1, 4.7 uH.** 6045 cannot carry 8 A; the smallest case that does is
  7 × 6.6 mm. The inductor ships as Cybermax CMLO0650H4R7MTT, 8 A saturation,
  6.5 A RMS, 24 mΩ.

The three inductors were first picked out of the fab's own library and then
swapped: Sunlord's SWPA and MWSA ranges are stocked for assembly but have no
LCSC listing, so their C-numbers resolve to nothing a person can look up. Every
code in this file now opens on LCSC.


## Board features

No MPN, not ordered — fabrication options on the panel, not assembly parts.

| Ref | Value | MPN | LCSC | Note |
|---|---|---|---|---|
| FID1 | Fiducial | — | — | PCB feature, not ordered; footprint Fiducial:Fiducial_1mm_Mask2mm |
| FID2 | Fiducial | — | — | PCB feature, not ordered; footprint Fiducial:Fiducial_1mm_Mask2mm |
| FID3 | Fiducial | — | — | PCB feature, not ordered; footprint Fiducial:Fiducial_1mm_Mask2mm |
| H1 | Mounting hole M3 | — | — | PCB feature, not ordered; footprint MountingHole:MountingHole_3.5mm_Pad_Via |
| H2 | Mounting hole M3 | — | — | PCB feature, not ordered; footprint MountingHole:MountingHole_3.5mm_Pad_Via |
| H3 | Mounting hole M3 | — | — | PCB feature, not ordered; footprint MountingHole:MountingHole_3.5mm_Pad_Via |
| H4 | Mounting hole M3 | — | — | PCB feature, not ordered; footprint MountingHole:MountingHole_3.5mm_Pad_Via |
