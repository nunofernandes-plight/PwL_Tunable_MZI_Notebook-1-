# Tunable MZI in PhotonForge: the Precision with Light version
## Precision with Light, PhotonForge Series, Episode 3 (companion notebook)

Based on the PhotonForge documentation example Tunable MZI (Flexcompute), using the open-source LNOI400 PDK from Luxtelligence. This version adds three things the original does not: design numbers before simulation (Vπ, fringe voltages), a phase and transmission check against the analytic MZI, and a bandwidth check of the null (what limits extinction across the C-band).

What differs from the documentation example. The original loads a phase shifter from phase_shifter.gds, produced in another example (Quantum Chip). So that this notebook runs on its own in Colab, we build a 100 µm heated waveguide with the PDK component heated_straight. Length and port specification match; the heater geometry does not, and since the heater law here is a placeholder anyway (see section 3), nothing downstream depends on it.

Requirements. A Flexcompute/Tidy3D account and API key. The mode solve and the 2x2 MMI run on the Tidy3D cloud and consume a small number of FlexCredits. Everything else is local.

Status of this notebook: the structure, the PDK calls, the netlist assembly and every NumPy cell were checked offline against the installed packages. The cloud-dependent cells follow the documentation example's calls; run it once top to bottom and compare your plots with the text of the article before publishing results.
