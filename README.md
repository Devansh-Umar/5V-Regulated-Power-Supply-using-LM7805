# 5V-Regulated-Power-Supply-using-LM7805
### *Simulating the circuit in LTspice & then implementing it through breadboard*

A regulated power supply is one of the first circuits many electronics students build, but while studying it I realised that simply connecting components together isn't enough to truly understand how it works.

When I first looked at the circuit, it appeared surprisingly simple - a transformer, four diodes, capacitors, and a 7805 regulator. But the more I studied each block, the more questions came to mind.

- Why do we need four diodes instead of one?
- Why is a large capacitor connected after the bridge rectifier?
- Why does the 7805 require additional capacitors even though it is already a voltage regulator?
- If the regulator is called **7805**, why doesn't every circuit produce exactly **5.00V**?

Instead of searching for my answers online, I decided to verify everything myself.

That decision turned this small circuit into one of my most enjoyable learning experiences.

Rather than directly assembling the hardware, I started with **LTspice**. It allowed me to observe waveforms, change component values, and understand the behaviour of each stage before blowing any physical components.

Only after I was satisfied with the simulation then, I moved to the breadboard and build the same circuit practically.

I’ve documented my whole observations - from understanding the theory, to simulation, to hardware implementation, and finally comparing the practical measurements with the expected results.

My goal isn't simply to show a working circuit. I also want to document the thought process behind it so that someone learning electronics can follow the same path and understand *why* each stage exists, not just *how* to connect it.

---

## Project Overview

**Software Used**
- LTspice

**Hardware Components**
- 230V / 9V Step-down Transformer
- 4 × 1N4007 Diodes (Bridge Rectifier)
- 1000µF Filter Capacitor
- 7805 Voltage Regulator
- 0.33µF Input Capacitor
- 0.33µF Output Capacitor *(Physical Build)*
- Breadboard & Connecting Wires

## My key Observation
One interesting observation during this project was that simulation and hardware never produce perfectly identical values.
During simulation I got almost ideal regulated output *5.003V*, whereas the practical circuit measured around **4.92V** & during hardware testing, the transformer secondary measured around **11.1V AC**, but I was using 9V so how?

Instead of assuming the circuit was incorrect or transformer as faulty, I googled & tried to understand why this difference existed. It became a good opportunity to learn about regulator tolerance, diode forward voltage drop, transformer regulation and the practical limitations that one cannot understand while studying only the theory.

That observation became one of the most valuable outcomes of this project.

---

## Repository Contents

[LTspice Circuit Schematic](Circuit_Connections/LTspice_Schematic.png)

[Different Stages of Output Waveforms](Output_Waveforms)

[Breadboard Connection Image](Circuit_Connections/Breadboard_Implementation.jpeg)

[Practical Demonstration Video](Physical_Measurement_Visuals.mp4)

[Detailed Project Report](Power_Supply_Project_Report.pdf)


---

## Detailed Understanding
For complete theory, circuit explanation, calculations, observations, LTspice analysis and hardware implementation details, see the **Project Report**.

 [**Power_Supply_Project_Report.pdf**](Power_Supply_Project_Report.pdf)

---

## What I’m thinking next

After this I’m going to extend this project using the **LM317 Adjustable Voltage Regulator** and then comparing the both **LM7805** and **LM317** in terms of voltage regulation, flexibility and practical applications.

---

### If you find this project useful, a star ⭐ on my repository would be memorable for me.

