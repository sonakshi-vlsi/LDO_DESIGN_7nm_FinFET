# LDO_DESIGN_7nm_FinFET
Custom LDO design in a 7nm FinFET process: two-stage OTA error amplifier driving a PMOS pass transistor, with feedforward capacitor compensation. Achieves 72.75° phase margin, 15.18 dB gain margin, and -52 dB PSRR at 2 MHz, simulated in Cadence Virtuoso.

## LDO Specifications ( After DC analysis and test of regions of transistor )

| Parameter | Value |
|------------|------------|
| Technology | TSMC 7nm (gate length of all transustors is 8nm) |
| Input Voltage | 1 V to 1.2V |
| Reference Voltage | 550mv |
| Feedback Voltage | 498mv - 501mV |
| Output Voltage | ~700 mV |
| Load Current Range | 100 µA – 6mA |
| Output Capacitor | 100 pF |
| FeedForward Capacitor | 50 fF |
| Output Resistor (in series with output cap to increase stability) | 50 ohms |
