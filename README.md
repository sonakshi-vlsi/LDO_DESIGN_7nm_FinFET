# LDO_DESIGN_7nm_FinFET
Custom LDO design in a 7nm FinFET process: two-stage OTA error amplifier driving a PMOS pass transistor, with feedforward capacitor compensation. Achieves 72.75° phase margin, 15.18 dB gain margin, and -52 dB PSRR at 2 MHz, simulated in Cadence Virtuoso.

## Components Used

**MOSFETs:** Low-threshold (LVT) FinFET devices throughout  
**Capacitors:** Ideal capacitors for simulation  
**Resistors:** Ideal resistors for simulation  
**Technology:** TSMC N7 FinFET PDK
## LDO Specifications ( After DC analysis and test of regions of transistor )

| Parameter | Value |
|------------|------------|
| Technology | TSMC 7nm (gate length of all transistors is 8nm) |
| Input Voltage | 1 V to 1.2V |
| Reference Voltage | 550mv |
| Feedback Voltage | 498mv - 501mV |
| Output Voltage | ~700 mV |
| Load Current Range | 100 µA – 6mA |
| Output Capacitor | 100 pF |
| FeedForward Capacitor | 50 fF |
| Miller Capacitor | 100 fF |
| Output Resistor (in series with output cap to increase stability) | 50 ohms |
| DC Load regulation @1v:VDD @iLOAD: 100uA - 6mA | 0.661 mV/mA |
| DC Load regulation @1.2v:VDD @iLOAD: 100uA - 6mA | 0.390 mV/mA|
| DC Line regulation @iLOAD: 500uA | 2.574 mV/V|
| DC Line regulation @iLOAD: 6mA | 7 mV/V|

## LDO Specifications ( After AC and STB analysis, with AC at VDD )
iLoad: 500uA, Vdd: 1V, Vref: 550mV

| Parameter | Value |
|------------|------------|
| Phase Margin | 72.75 degree |
| Gain Margin | 15.10dB |
| UGW | 128.5MHz |
| Gain Margin Frequency | 2.407GHz |
| PSRR @10kHz | -52.28dB |
| PSRR @2M | -52.20dB |
| PSRR @10M | -50.66dB |
| PSRR @100M | -37.40dB |

## LDO Specifications ( After Transient analysis )

| Parameter | Value |
|------------|------------|
| Transient Load regulation @1.2v:VDD @iLOAD: 100uA - 6mA | 2.525mV/mA |
| Transient Load regulation @1v:VDD @iLOAD: 100uA - 6mA | 2.525mV/mA |
| Transient Line regulation @iLOAD: 500uA | 3 mV/V |
| Transient Line regulation @iLOAD: 6mA | 14.3 mV/V|

## LDO Specifications ( After NOISE analysis )

| Frequency | Value |
|------------|------------|
| 100 Hz | 10.57 µV/√Hz |
| 1 kHz | 3.534 µV/√Hz |
| 10 kHz | 1.188 µV/√Hz |
| 1 MHz | 139.3 nV/√Hz |
| 10 MHz | 55.95 nV/√Hz |

## LDO Specifications Worst Case ( After VT analysis, and varying load current along with Line Voltage and Temperature )


Worst PM        →  52.77°   
Worst GM        →  6.874 dB (At T = -40°, Vdd= 1.2V, Iload = 5mA)  
Worst PSRR      →  −29.59 dB  
Worst Noise     →  4.217 µV/√Hz @ 1kHz  
Worst UGF       →  422.1 MHz  
