# Wearable-fNIRS-Headband-PCB
End-to-end design and implementation of a 4-layer, high-density PCB for a wearable functional Near-Infrared Spectroscopy (fNIRS) system. The module is engineered for high-precision neural activity monitoring by measuring hemodynamic changes via multi-wavelength optical sensing.

![fNIRS 3D Render](Assets/PCB Front View.png)

**Engineering Design Considerations:**
•	**Component Selection & Specification:** Conducted rigorous datasheet analysis to select ultra-low noise, precision Operational Amplifiers with minimal Input Bias Current . These parameters were critical for implementing the high-gain Transimpedance Amplifier (TIA) stages required to convert low-level photodiode currents into measurable voltage signals.

•	**Stackup Strategy & PDN Optimization:** Developed a 4-layer PCB stackup featuring dedicated internal Power (VCC) and Ground (GND) planes. This architecture was chosen to ensure a low-impedance Power Delivery Network (PDN) and to provide robust electromagnetic interference (EMI) shielding for sensitive analog nodes.

•	**Signal Integrity & Noise Mitigation:**
o	Mixed-Signal Isolation: Employed strategic layout partitioning to physically isolate "noisy" high-current LED driver paths on the Top Layer from ultra-sensitive analog sensing circuitry on the Bottom Layer.
o	Crosstalk Mitigation: Optimized trace routing to minimize inductive and capacitive coupling between digital switching signals and the high-impedance analog front-
end.

•	**Strategic Floorplanning:**
o	Optical-to-Electrical Optimization: Calculated and implemented optimal source-detector separation to maximize cortical light penetration depth while preventing detector saturation.

o **Parasitic Minimization:** Executed tight placement of feedback networks in immediate proximity to the Op-Amp inverting inputs to minimize parasitic capacitance and prevent stability issues or increased noise floors.

•	**Verification & DFM (Design for Manufacturing):**
o	Managed complex layout tasks under strict spatial constraints.
o	Performed comprehensive DRC (Design Rule Check) suites to ensure 100% netlist connectivity and clearance compliance.
o	Delivered a DFM-compliant design, optimized for high-yield manufacturing and reliable assembly.

