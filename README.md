
# Ring Oscillator for Timing Applications 


This project simulates the designed ring oscillator circuit to analyze its timing performance and stability in various conditions.

Note:Note: Circuit requires further optimization to improve performance. Design yet to be modified.

## A Glance at the Ring Oscillator for Timing Applications

The ring oscillator is a vital component for generating stable oscillations without relying on an external clock source, making it indispensable for various timing, clock generation, and frequency synthesis applications, including phase-locked loops (PLLs) and clock recovery systems. Its design, often based on inverters or NAND gates, provides flexibility and precise frequency control through adjustable stages. Designing a ring oscillator with a high power supply rejection ratio (PSRR) and stable frequency characteristics is crucial for consistent performance across varying operating conditions. This project explores the principles of ring oscillator operation, its implementation, the design challenges encountered, and potential improvements to enhance its performance and reliability.


## Block Diagram of the Ring Oscillator for Timing Applications

 ![image alt](https://github.com/ansariasmi01/RO/blob/9cbdac6bae896ea371accd4a8989f908d5866e6f/Block%20Diagram.jpg)


## Circuit Diagram of the Ring Oscillator for Timing Applications
![image alt](https://github.com/ansariasmi01/RO/blob/ddf1eacce8eab92efb141f6da4ecf5d1be1e2256/Circuit%20Diagram.jpg)

## Ring Oscillator Performance Parameters

| Parameter                  | Description                                       | Min     | Typical           | Max   | Unit           | Condition                      |
|----------------------------|---------------------------------------------------|---------|-------------------|-------|----------------|--------------------------------|
| **Average Power**          | Average power consumption                         | -       | 10.15 x 10^-6    | -     | W              | -                              |
| **Frequency**              | Oscillation frequency                             | -       | 5.63             | -     | GHz            | -                              |
| **Phase Margin**           | Stability phase margin                            | -       | 180              | -     | Degrees        | -                              |
| **Bandwidth**              | Oscillator bandwidth                              | -       | 684.0 x 10^-12   | -     | b/s            | -                              |
| **Frequency Jitter**       | Frequency stability jitter                        | -       | 100              | -     | MHz            | @800 ps                        |
| **Period Jitter**          | Timing stability jitter per period                | -       | 0                | -     | s              | @933.5 ps                      |
| **Voltage**                | Supply voltage                                    | -       | 3.85             | -     | mV             | @734.7 ps                      |
| **Harmonic Frequency**     | Second harmonic frequency                         | -       | 2.0              | -     | GHz            | -                              |
| **Phase Noise**            | Noise in phase                                    | -7.0    | -6.4             | -6.0  | k dBc/Hz       | at 2 GHz                       |
| **Input Noise**            | Input noise spectral density                      | -       | 3.083            | -     | kV/sqrt(Hz)    | at 2 GHz                       |
| **Output Noise**           | Output noise spectral density                     | -       | -6.4             | -     | kV/sqrt(Hz)    | at 2 GHz                       |
| **Total Harmonic Distortion (THD)** | Measure of distortion                   | -       | 3.586 x 10^-4    | -     | %              | at -3.649 dB                   |
| **Noise Factor**           | Factor of noise in the system                     | -       | 1                | -     | V²/Hz          | at 2 GHz                       |
| **Transfer Function**      | Output-to-input transfer characteristic           | -       | 0.0              | -     | V/V            | at 2 GHz                       |
| **Power Added Efficiency** | Efficiency of power usage                         | -       | 91.424 x 10^3    | -     | %              | at -3.694 point                |
| **Compression Point**      | Power at which gain drops by 1 dB                 | -       | 3.712            | -     | dB             | at 6.056 dBm                   |
| **IPN Curves**             | Intermodulation Product Nonlinearity curve slope  | 0.5     | 1                | 1.5   | dB/dB          | First order                    |



## Pre-Layout Performance Characteristics

### Layout of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/cd427a753980366ec0a95909d68420f1bfcd979e/Layout%20of%20Ring%20Oscillator.jpg)


### Waveform for Transient Analysis of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/53f755c0909f7e1233ad8938bcdf64ff1ea27d2c/Waveform%20for%20Transient%20Analysis%20of%20Ring%20Oscillator.jpg)


### Waveform for Power consumption of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/3a3501fdcc766131db901cd8fd7dde76fcafc3b8/Waveform%20for%20Power%20consumption%20of%20%20Ring%20Oscillator.jpg)


### Waveform for Voltage of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/17e54efa43e744370824d8875eb2331f5c3d36a4/Waveform%20for%20Voltage%20of%20Ring%20Oscillator%20.jpg)


### Waveform for THD of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/01c21d03d2fee96dfaf33a806397526538b987db/Waveform%20for%20THD%20of%20%20Ring%20Oscillator.jpg)


###  Waveform for Compression Point of Ring Oscillator 
![image alt](https://github.com/ansariasmi01/RO/blob/a0dafd039aa3d1688806105265f0cc2020b3438a/Waveform%20for%20Compression%20Point%20of%20Ring%20Oscillator%20.jpg)

### Waveform for Power Added Efficiency of Ring Oscillator
![image alt](https://github.com/ansariasmi01/RO/blob/86fdba7b808af338e0d3f47f8feb72e7c8469987/Waveform%20for%20Power%20Added%20Efficiency%20of%20Ring%20Oscillator.jpg)



## Tools used and steps to reproduce all waveforms (Tools allowed are xschem/eSim/ngspice) 
Ngspice is an open source mixed-signal circuit simulator.

### Installing Ngspice

#### For Ubuntu

Open your terminal and type the following to install Ngspice
```
$  sudo apt-get install -y ngspice
```

## Running the Simulation


To enter the Ngspice Shell, open the terminal & type:
```
$ ngspice
```
To simulate a netlist, type:
```
ngspice 1 ->  source <filename>.cir
```

You can exit from the Ngspice Shell by typing:
```
ngspice 1 ->  exit
```
 <p align="center"> or </p>
 
```
ngspice 1 ->  quit
```

There are several waveforms that need to be obtained to observe the performance of the Bandgap reference circuit.

### Pre-Layout Simulation

To clone the Repository and download the Netlist files for Simulation, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/sherylcorina/avsdbgp_3v3
$  cd avsdbgp_3v3/Simulation/Ngspice_Simulation/Final_Simulation/PreLayout
```

### Future Work

1. **Improved Layout Techniques**: Use better layout methods like Common Centroid and Interdigitisation to enhance the matching of components in the ring oscillator.

2. **Post-Layout Testing**: Perform post-layout simulations to check if the ring oscillator works as expected and meets the required frequency.

3. **Supply Voltage Testing**: Analyze how the oscillator performs under different supply voltage levels to ensure it remains stable.

4. **Power Optimization**: Look for ways to reduce power consumption in the ring oscillator by adjusting the biasing currents or resizing transistors.

5. **Temperature Testing**: Test how the oscillator’s frequency changes with temperature and implement fixes to keep it stable across different temperatures.

6. **Integration with Other Circuits**: Explore combining the ring oscillator with other circuits like phase-locked loops (PLLs) to create a complete timing solution.

7. **Prototype Development**: Build a prototype of the ring oscillator and test it in real-world conditions to confirm that it performs as expected.

8. **Stability Improvement**: Research ways to make the ring oscillator more stable, such as adding feedback or redesigning certain components.

9. **Alternative Designs**: Investigate different ring oscillator designs to see if they perform better than the current one.

10. **Application Customization**: Modify the ring oscillator design for specific uses, like low-power communication or high-speed digital applications.

## Contributors 

- **Almas Ansari** 
- **Kunal Ghosh** 
- **Nibha Desai** 



## Acknowledgments

- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Nibha Desai, HoD. Professor, SAKEC, India

## Contact Information

- Almas Ansari, Undergraduate Student, SAKEC, Mumbai  almas.18219@sakec.ac.in
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Nibha Desai, HoD. Professor, SAKEC, India nibha.desai@sakec.ac.in


