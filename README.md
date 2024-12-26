# README: Induction Motor Drive with Frequency Inverter

## Overview

This project explores the implementation of induction motor drive systems, comparing **Direct Start** and **Frequency Inverter Start** techniques. It includes mathematical modeling, simulation results, and performance analysis. The implementation utilizes PWM (Pulse Width Modulation) control for the frequency inverter to achieve smooth motor operation, reduced inrush currents, and better performance control.

---

## Components and Methods

### Direct Start

Direct Start involves connecting the induction motor directly to the power supply. While straightforward, this method leads to high inrush currents, which can adversely affect the electrical network and mechanical components.

Key characteristics:
- **Voltage**: 220V RMS (line voltage)
- **High inrush current**: Up to \( 236\,\mathrm{A} \)
- **Limitations**: High torque and current peaks during startup

Mathematical analysis for this phase considers the synchronous speed:
$\omega_s = \frac{120 \cdot f}{N}$
Where:
- $\ f \$: Supply frequency (Hz)
- $\ N \$: Number of poles in the motor

### Frequency Inverter Start

Using a frequency inverter, this approach modulates the power supply frequency and voltage to ensure smooth motor acceleration. The PWM technique is applied, utilizing sinusoidal reference signals and a triangular carrier signal for pulse modulation.

Key components:
1. **PWM Modulation**:
   $V_f(t) = A \sin (\omega t), \quad A = \frac{m_a \cdot V_{CC}}{2}$
   Where:
   - $\ m_a \$: Modulation index
   - $\ V_{CC} \$: DC bus voltage

2. **Motor Torque and Power**:
   Mechanical torque is calculated as: $T_m = \frac{P_{\text{mec}}}{\omega_r}$
   Where:
   - $\ P_{\text{mec}} \$: Mechanical power
   - $\ \omega_r \$: Rotor angular velocity

---

## Results and Analysis

### Performance Metrics

1. **Current Reduction**:
   - Direct Start peak current: $\( 236\,\mathrm{A} \)$
   - Inverter Start peak current: $\( 59\,\mathrm{A} \)$ (75% reduction)

2. **Torque Stability**:
   During load application (\(59\,\mathrm{Nm}\)) and varying reference speeds (\(\pm 20\%\)), the system maintained stable torque levels.

3. **Efficiency**:
   The system achieved the desired mechanical power of \(10.8\,\mathrm{kW}\), with an electrical input of \(12\,\mathrm{kW}\) and an efficiency of 90%.

### Graphical Outputs

Key outputs include:
- Phase voltages and currents
- Torque and speed characteristics
- Power and efficiency metrics
- Harmonic analysis (FFT) of inverter output

---

## Project Parameters

### Simulation Settings

- **PWM Carrier Frequency**: $\(3\,\mathrm{kHz}\)$
- **Sampling Rate**: $180 kHz; T_s \approx 5.56,\mu s$
- **DC Bus Voltage**: $400 V$

### Motor Characteristics

- Synchronous speed: $1800 RPM$
- Slip: $4\%$ = $S = \frac{\omega_s - \omega_m}{\omega_s}$

---

## Conclusion

This project successfully demonstrated the advantages of using a frequency inverter for induction motor drives. The reduction in inrush current and the ability to control speed and torque dynamically highlight the benefits of modern motor control techniques.

For further insights, refer to the full report.pdf.
