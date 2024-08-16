# Noise Canceling Headphones - Analog Circuit Design

## Overview

This project focuses on designing a noise-canceling headphone system using analog circuitry. The objective was to achieve a 20 dB attenuation at a 100 Hz frequency for a given plant (headphones connected with a biasing circuit). The design and implementation include compensator design and stabilization of the headphone response using analog components.

## Objective

- Achieve attenuation of 20 dB at 100 Hz frequency using analog circuitry.
- Design an analog compensator to stabilize the response of the headphones.

## Approach

### 1. **Mathematical Modeling**
   - MATLAB was used to model the system, compensator circuit, and compensated system.
   - The data from the uncompensated system was analyzed in MATLAB, and a second-degree compensator transfer function was defined.
   - The final compensated system was evaluated to check if it met the requirements.

### 2. **Compensator Design**
   - A Lead-Lag compensator was designed, as a single pole-single zero compensator was insufficient.
   - A detailed circuit design with various components and parameters was implemented to compensate the system.

### 3. **Challenges Faced**
   - **Noise in Measurements**: External disturbances affected the measurement process, but compensatory measures were taken to mitigate noise.
   - **Instability of the Plant**: The phase margin was negative, which was resolved by using a second-order Lead-Lag compensator.
   - **Choosing the Right Compensator**: The compensator needed to be carefully chosen to ensure adequate phase compensation.
   - **Frequency Gain Issues**: A non-inverting amplifier was used to improve the 100 Hz frequency response, achieving a gain of 12-13 dB.

### 4. **Circuit Design**
   - Circuit parameters such as resistors and capacitors were selected to build the Lead-Lag compensator.
   - The compensator was implemented and tested using the designed circuit.

## Results

- The compensated system successfully achieved the desired gain at 100 Hz and stabilized the plant.
- The open and closed-loop responses were analyzed, and the system was tested for stability and performance.

## Observations and Inferences

- **Component Tolerances**: The large tolerance in passive components affected the overall circuit performance, but the roll-off behavior was still achieved.
- **System Tuning**: Critical analysis and tuning of the textbook circuit yielded improved results in the compensated system.
- **System Limitations**: Trade-offs were encountered during loop shaping, governed by the Bode Sensitivity Integral.
- **Closed-Loop Feedback**: The system stability was enhanced by implementing closed-loop feedback, with no gain crossover observed.
