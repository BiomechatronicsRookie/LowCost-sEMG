## LowCost-sEMG
This repository contains files for a simple surface electromyography sensor designed for the Arm2U team (https://arm2u-etseib.upc.edu/wp/). The PCB was designed using ALTIUM.

# sEMG
Surface elegromyography is a non-invasive technique used to measure muscular electrical activity. These signals related to motor commands can be used as a signal input for the control of robotic devices such as prosthetics. 
Signal processing such as band-pass filtering, notch-filtering and envelope detection must be performed in order to adapt the signal for a suitable control strattegy.

- Schematics: This systems consists of a series of cascaded stages. First, raw EMG signal is obtained with an instrumentation Amplifier. For simplicity the raw signal obtained is biased between 0 and Vcc, i.e. the signal wil fluctuate around Vcc/2V.
Aferwards a series of filtering stages come where a bandpass second order active RC filter is applied to suppress frequencies below and avobe 10 and 300 Hz respectively. Then the bias is subtracted and the signal is rectified. 
The final stage consists on a low-pass filter with cutoff frequency of 1Hz to obtain the envelope of the signal. The schematic attached is the implementation of all these stages.

![EGM sch](https://user-images.githubusercontent.com/67059763/121668370-84bb0700-caab-11eb-9eb0-0c6db804259a.PNG)
