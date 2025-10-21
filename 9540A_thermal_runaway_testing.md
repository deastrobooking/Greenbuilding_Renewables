

# 🔢 UL 9540A / Thermal-Runaway Math Glossary

---

## ⚡ Heat and Energy Concepts

| Term                             | Symbol           | Units             | Meaning / Use                                                                                                                                  |
| -------------------------------- | ---------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Heat Release Rate**            | $$( \dot{Q}(t) )$$   | kW or MW          | The *power* of the fire — how fast energy is released as heat at a given moment in time. It’s like the wattage of a heater changing over time. |
| **Peak Heat Release Rate**       | ( \dot{Q}_{pk} ) | kW or MW          | The **maximum** heat output measured during the test. Used to design fire suppression systems and spacing.                                     |
| **Total Heat (Energy Released)** | ( E )            | MJ                | The total amount of heat energy released over time. Calculated by adding up (integrating) HRR:  [E = \int_{t_0}^{t_1} \dot Q(t) , dt]          |
| **Radiative Fraction**           | ( \chi_r )       | — (dimensionless) | Fraction of total heat radiated as light/heat waves (usually 0.2–0.35). Used to estimate radiant heating of nearby objects.                    |
| **Radiant Heat Flux**            | ( q''_{rad} )    | kW/m²             | Amount of radiant heat hitting a surface. [ q''_{rad} = \chi_r \frac{\dot Q}{4\pi R^2} ]                                                       |
| **Convective Heat Flux**         | ( q''_{conv} )   | kW/m²             | Heat transferred by hot air touching a surface. [ q''*{conv} = h(T_s - T*\infty) ]                                                             |
| **Heat Transfer Coefficient**    | ( h )            | W/m²·K            | Describes how efficiently heat moves from hot gas to a surface.                                                                                |
| **Surface Temperature**          | ( T_s )          | °C or K           | The temperature of the burning surface or object.                                                                                              |
| **Ambient Temperature**          | ( T_\infty )     | °C or K           | The temperature of the surrounding air (usually room temperature).                                                                             |

---

## 🌬️ Ventilation and Gas Behavior

| Term                            | Symbol                 | Units                 | Meaning / Use                                                                                                       |
| ------------------------------- | ---------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Room Volume**                 | ( V )                  | m³                    | Space where gases mix and accumulate (battery room, garage, etc.).                                                  |
| **Ventilation Flow Rate**       | ( Q )                  | m³/s                  | Rate of air movement (fresh air in or exhaust out). Larger (Q) = faster dilution.                                   |
| **Gas Generation Rate**         | ( G ) or ( \dot{m}_i ) | m³/s or kg/s          | How fast a certain gas (like hydrogen) is being produced during thermal runaway.                                    |
| **Gas Density**                 | ( \rho_i )             | kg/m³                 | Mass per volume of a gas. Hydrogen ≈ 0.084 kg/m³ at room temperature. Used to convert between kg/s and m³/s.        |
| **Concentration of Gas**        | ( C(t) )               | fraction (v/v) or ppm | How much gas is in the air, usually as a fraction or percent.                                                       |
| **Lower Flammable Limit (LFL)** | ( \text{LFL} )         | % (v/v)               | Lowest gas concentration that can ignite. For hydrogen, LFL ≈ 4 %.                                                  |
| **Upper Flammable Limit (UFL)** | ( \text{UFL} )         | % (v/v)               | Highest concentration that can burn (hydrogen ≈ 75 %).                                                              |
| **Percent of LFL**              | ( %\text{LFL} )        | %                     | How close you are to ignition level:  [ %\text{LFL} = 100 \times \frac{C}{\text{LFL}} ]                             |
| **Well-Mixed Room Model**       | —                      | —                     | A simplified model assuming gases mix evenly:  [ \frac{dC}{dt} = \frac{G}{V} - \frac{Q}{V}C ]                       |
| **Steady-State Concentration**  | ( C_\infty )           | fraction              | The final, constant gas concentration if release continues: ( C_\infty = G/Q ).                                     |
| **Purge Time Constant**         | ( \tau = V/Q )         | s                     | How long it takes for ventilation to replace the air in a room once.                                                |
| **Purge Time**                  | ( t_{purge} )          | s                     | Time to reduce gas concentration from (C_0) to (C_1):  [ t_{purge} = \frac{V}{Q} \ln!\left(\frac{C_0}{C_1}\right) ] |
| **Le Chatelier’s Mixing Rule**  | —                      | —                     | Calculates combined LFL for multiple gases:  [ \frac{1}{\text{LFL}_{mix}} = \sum_i \frac{y_i}{\text{LFL}_i} ]       |

---

## 💥 Explosion and Safety Ratios

| Term                            | Symbol                                  | Units    | Meaning / Use                                                             |
| ------------------------------- | --------------------------------------- | -------- | ------------------------------------------------------------------------- |
| **Flammable Limit Fraction**    | ( f )                                   | —        | Chosen safety fraction of LFL (e.g., 0.25 = 25 % LFL).                    |
| **Safe Concentration Limit**    | ( C_{limit} = f \times \text{LFL} )     | fraction | Target maximum gas concentration allowed by NFPA 69 (usually ≤ 25 % LFL). |
| **Required Airflow for Safety** | ( Q_{req} = G / C_{limit} )             | m³/s     | Minimum ventilation flow to keep gas below the limit.                     |
| **Hydrogen Release Mass Flow**  | ( \dot m_{H_2} )                        | kg/s     | Rate of hydrogen escaping from the cell/cabinet.                          |
| **Hydrogen Volumetric Flow**    | ( G_{H_2} = \dot m_{H_2} / \rho_{H_2} ) | m³/s     | Converts mass rate to gas volume rate for use in ventilation equations.   |

---

## 🌈 Fire Spread and Temperature

| Term                                  | Symbol             | Units | Meaning / Use                                                                                                                                                   |
| ------------------------------------- | ------------------ | ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Distance from Fire**                | ( R )              | m     | Distance between burning object and target. Affects radiant heating.                                                                                            |
| **Critical Heat Flux (for Ignition)** | ( q''_{crit} )     | kW/m² | Minimum radiant heat needed to ignite a nearby material (wood ≈ 12.5 kW/m²).                                                                                    |
| **Ceiling Jet Temperature Rise**      | ( \Delta T_{jet} ) | °C    | Hot-gas layer temperature rise under ceiling, predicted by **Alpert’s equation**:  [ \Delta T_{jet} = 16.9\frac{\dot Q^{2/3}}{H^{5/3}} ] (close to fire source) |
| **Ceiling Height**                    | ( H )              | m     | Vertical distance from fire to ceiling.                                                                                                                         |
| **Radial Distance (Ceiling Jet)**     | ( r )              | m     | Horizontal distance from fire center to ceiling detector.                                                                                                       |

---

## 😷 Toxic Gas Conversions

| Term                    | Symbol | Units | Meaning / Use                                                                      |
| ----------------------- | ------ | ----- | ---------------------------------------------------------------------------------- |
| **Parts per million**   | ppm    | —     | Number of gas molecules per million air molecules (1 ppm = 0.0001 %).              |
| **Mass Concentration**  | mg/m³  | —     | Amount of gas mass in air by volume.                                               |
| **Conversion**          | —      | —     | [ \text{mg/m}^3 = \frac{\text{ppm} \times \text{MW}}{24.45} ] (at 25 °C and 1 atm) |
| **Molecular Weight**    | MW     | g/mol | Used to convert between ppm and mg/m³ (e.g., HF = 20 g/mol).                       |
| **HF Safety Threshold** | —      | ppm   | Hydrogen fluoride limit ≈ 2 ppm (short-term exposure).                             |

---

## 🧮 Mathematical Tools You’re Using

| Concept                  | Symbol / Equation                      | Plain-Language Explanation                                          |
| ------------------------ | -------------------------------------- | ------------------------------------------------------------------- |
| **Integration**          | ( \int \dot Q(t),dt )                  | Adds up small pieces of heat over time to find total energy.        |
| **Exponential Decay**    | ( C(t)=C_0 e^{-t/\tau} )               | Shows how gas concentration decreases as air flows in.              |
| **Inverse Square Law**   | ( 1/R^2 )                              | Heat intensity drops quickly as you move away from a fire.          |
| **Ratio / Proportion**   | ( C/V,, G/Q,, f=\frac{C}{\text{LFL}} ) | Relationships between flow, volume, and safety limits.              |
| **Dimensional Analysis** | —                                      | Making sure units match (e.g., converting kg/s → m³/s).             |
| **Logarithm**            | ( \ln(C_0/C_1) )                       | Used to find purge time — how long until gas falls to a safe level. |

---

## 🔍 Big-Picture Concepts

| Category                    | Description                                                                            |
| --------------------------- | -------------------------------------------------------------------------------------- |
| **Energy & Power**          | How much heat is released and how fast — determines fire size.                         |
| **Gas Dynamics**            | How gases spread and dilute in air — determines explosion risk.                        |
| **Heat Transfer**           | How fire heats up nearby materials — determines spacing.                               |
| **Safety Margins**          | Keeping concentrations below 25 % LFL ensures no ignition.                             |
| **Modeling Simplification** | “Well-mixed room” assumes gas spreads evenly — makes math manageable for early design. |

---

Perfect — here’s a **simple, high-school-level breakdown** of the math concepts used in **UL 9540A thermal-runaway testing** and the engineering design that comes from it.

---

## 🔥 1. What’s Being Measured

When a battery fails badly enough to **overheat and catch fire**, engineers need to know:

1. **How much heat** comes out.
2. **How fast** it comes out.
3. **What gases** are released (hydrogen, carbon monoxide, hydrofluoric acid).
4. **How big and hot** the fire might get.
5. **If it can spread** to other batteries.

These are measured in the UL 9540A test.
The test gives engineers **numbers** they can use to design **safe spacing, vents, and fire systems**.

---

## 🌡️ 2. Heat and Energy (Fire Power)

### Heat Release Rate (HRR)

* HRR is how fast energy is released as heat.
  Think of it like the **wattage of a heater**.
* Measured in **kilowatts (kW)** or **megawatts (MW)**.

Example:

```
If HRR = 1000 kW (1 MW)
→ that’s like 1000 space heaters running at once.
```

### Total Heat (Energy)

We add up the HRR over time to get total energy:
[
E = \text{(average heat rate)} \times \text{(time)}
]
This is measured in **megajoules (MJ)**.
It tells us how much total “fire energy” came out.

---

## 💨 3. Gas Release and Ventilation

When batteries burn, they release gases like **hydrogen (H₂)**.
Hydrogen is very light and **explosive at 4% concentration in air** (called the **LFL – Lower Flammable Limit**).

We calculate:
[
\text{Concentration} = \frac{\text{Gas released}}{\text{Room air volume}}
]
If that concentration is near 4%, it’s dangerous.
So we blow in fresh air to keep it below **25% of 4%**, or **1%**.

### Example:

* Room size: 300 m³ (like a big classroom)
* Hydrogen produced: 3 m³
  [
  \text{Concentration} = \frac{3}{300} = 0.01 = 1%
  ]
  ✅ Safe, right at the 25 % of LFL target.

---

## 🌬️ 4. How Much Ventilation Is Needed

We size fans or vents using:
[
\text{Airflow needed} = \frac{\text{Gas released per second}}{\text{Safe concentration}}
]
If the battery releases **0.002 m³ of hydrogen per second**
and we want to stay at **1 % (0.01)** concentration:
[
Q = \frac{0.002}{0.01} = 0.2\ \text{m³/s} \approx 425\ \text{CFM}
]
(That’s about what a small industrial fan can handle.)

---

## 🌈 5. Radiant Heat (How Fire Spreads)

Fires give off **radiation**—energy that can ignite nearby materials.

We use the **inverse square law** (like light and sound):
[
\text{Heat intensity} = \frac{\text{Fire power}}{4 \pi R^2}
]
Where (R) = distance from fire.

If the fire power doubles, the heat doubles.
If the distance doubles, the heat goes down by **four times**.

Engineers compare this heat to known ignition limits:

* Wood burns around **12 kW/m²**
* Plastic melts at **5–10 kW/m²**

So we make sure the next battery or wall is far enough away.

---

## ⏱️ 6. Purging Gases Over Time

When fans are on, gases get flushed out:
[
C(t) = C_0 \times e^{-\frac{Qt}{V}}
]
This fancy-looking formula says:

* (C(t)): gas level after some time
* (C_0): starting gas level
* (Q): airflow rate
* (V): room size

The bigger the fan (Q) or smaller the room (V),
the faster gases go away (exponential decay).

---

## 😷 7. Toxic Gases (Safety Check)

Not all gases explode—some are **toxic**.
Hydrogen fluoride (HF), for example, is dangerous at low levels.

We use simple conversions:
[
1\ \text{ppm of HF} = 0.82\ \text{mg/m³}
]
Then compare to safe limits like **2 ppm short-term** exposure.

---

## ⚙️ 8. The Engineering Steps (Simplified)

| Step | What Engineers Calculate  | Why It Matters                     |
| ---- | ------------------------- | ---------------------------------- |
| 1️⃣  | Total energy released (E) | Size of fire or suppression system |
| 2️⃣  | Peak HRR ( \dot Q_{pk} )  | How fast the fire grows            |
| 3️⃣  | Radiant heat at distance  | Safe spacing                       |
| 4️⃣  | Gas concentration         | Ventilation sizing                 |
| 5️⃣  | % of LFL                  | Explosion safety                   |
| 6️⃣  | Purge time                | How long to clear the air          |
| 7️⃣  | Toxic ppm                 | Worker safety                      |

---

## 🧠 9. Why It Matters

All of these calculations are **the math behind safe energy systems**:

* Preventing explosions (by keeping hydrogen low)
* Preventing fires from spreading
* Ensuring firefighters and inspectors can enter safely

Here’s a compact, engineer-grade **math guide** for using UL 9540A report data to design ventilation, spacing, detection, and suppression around thermal-runaway hazards. I’ve kept it practical (plug-and-chug), with the governing equations and what each number comes from.

---

# 1) Know your inputs (from the UL 9540A report)

From the **unit/installation-level** sections pull:

* **Heat Release Rate vs. time** ( \dot Q(t)) [kW] and **peak HRR** ( \dot Q_{\text{pk}}). ([Sandia National Laboratories][1])
* **Gas species mass (or molar) release rates**: at least **H₂, CO, HF** vs. time ( \dot m_i(t)) or peak values. Fifth edition emphasizes **hydrogen** at unit level. ([shopulstandards.com][2])
* **Duration** of significant gas release (t_{\text{rel}}), **visible flame**, **droplets/projectiles**, key **surface/target temperatures**. ([Sandia National Laboratories][1])

Cross-link these data to **IFC/NFPA 855** requirements for HMA, ventilation/deflagration prevention, and protection features. ([ICC Digital Codes][3])

---

# 2) Fire size & energy: use the HRR curve

**Total heat (energy) released** over a window ([t_0,t_1]):
[
E=\int_{t_0}^{t_1}\dot Q(t),dt \quad [\text{MJ}] \quad\text{(numerically integrate the HRR trace)}
]
Use trapezoids on the tabulated HRR(t). This drives exposure, sprinkler expectations, and scenario selection. (HRR fundamentals: SFPE references.) ([SFPE][4])

---

# 3) Radiant/convective exposure to nearby targets

A simple, conservative **point-source radiation** check to estimate radiant flux at distance (R):
[
q''*{\text{rad}} ;=; \chi_r \frac{\dot Q}{4\pi R^2}\quad [\text{kW/m}^2]
]
where (\chi_r) (radiative fraction) is often 0.2–0.35 for hydrocarbon-like flaming; pick conservatively unless your 9540A report provides a better value. Compare (q''*{\text{rad}}) to **critical heat flux for ignition** of adjacencies (e.g., piloted ignition of wood often cited around **12.5 kW/m²**, with literature variability). ([Scribd][5])

Add convection if you have local measurements:
[
q''*{\text{conv}} ;=; h\left(T_s-T*\infty\right)
]
then (q''*{\text{tot}}=q''*{\text{rad}}+q''*{\text{conv}}). Ceiling jet (for detection/sprinklers, damage checks) can use **Alpert** correlations with HRR and ceiling height (H):
[
\Delta T*{\text{jet}}=\begin{cases}
16.9,\dfrac{\dot Q^{2/3}}{H^{5/3}}, & r/H\le 0.18[6pt]
5.38\left(\dfrac{\dot Q}{r}\right)^{2/3}\dfrac{1}{H}, & r/H>0.18
\end{cases}
]
(with (r) = radial distance). ([NIST][6])

---

# 4) Gas hazard math (H₂/CO/HF): concentration, %LFL, and ventilation

**4.1 Well-mixed room model (transient)**
For a room of volume (V) ([m^3]) with ventilation (Q) ([m^3/s]) and a source (G) ([m^3/s]) (or mol/s) of a gas:
[
\frac{dC}{dt}=\frac{G}{V}-\frac{Q}{V}C \quad\Rightarrow\quad
C(t)=C_\infty\Big(1-e^{-\frac{Q}{V}t}\Big)+C(0),e^{-\frac{Q}{V}t}
]
Steady state: (C_\infty=\dfrac{G}{Q}). Use species molar/volumetric generation (G) from 9540A or convert mass to molar/volumetric. ([me.psu.edu][7])

**4.2 Purge/clear time**
If you start at (C_0) and exhaust to (C_{\text{target}}):
[
t_{\text{purge}}=\frac{V}{Q},\ln!\left(\frac{C_0}{C_{\text{target}}}\right)
]
(useful for post-event purge design). ([me.psu.edu][7])

**4.3 LFL checks and NFPA 69 criterion**
For **single gas**, percent of LFL:
[
%\text{LFL} = 100\times \frac{C}{\text{LFL}}
\quad\text{(H₂ LFL ≈ 4 % v/v in air at ambient)}
]
NFPA 69 practice keeps the **global** flammable gas below **25 % of LFL** (or up to 60 % with certain interlocked instrumentation). Use this as your **design limit** unless the AHJ dictates lower. ([AIChE][8])

For **fuel mixtures**, use **Le Chatelier’s mixing rule**:
[
\frac{1}{\text{LFL}*\text{mix}}=\sum_i \frac{y_i}{\text{LFL}*i}
\quad\Rightarrow\quad
%\text{LFL}*\text{mix}=100\times \frac{C*\text{tot}}{\text{LFL}_\text{mix}}
]
with (y_i) the volume (mole) fraction of each flammable species in the mixture. ([digitalcommons.mtu.edu][9])

**4.4 Unit conversions (ppm ↔ mg/m³) and toxic checks (HF)**
At 25 °C, 1 atm:
[
\text{mg/m}^3 = \frac{\text{ppm}\times \text{MW}}{24.45},\qquad
\text{ppm} = \frac{24.45\times \text{mg/m}^3}{\text{MW}}
]
**HF**: 1 ppm ≈ 0.82 mg/m³ (MW = 20.01). Compare to RELs/STELs if you’re documenting personnel exposure limits in an HMA. ([AIHA][10])

---

# 5) Ventilation sizing from 9540A gas data

Let (G_{H_2}) be the **peak** or **representative** volumetric generation rate of hydrogen (account for concurrent CO or other fuels via Le Chatelier if needed). To keep global concentration at or below a set fraction (f) of LFL (e.g., (f=0.25) for 25 % of LFL):
[
Q_{\text{req}} ;\ge; \frac{G_{H_2}}{C_{\text{limit}}}
\quad\text{with}\quad C_{\text{limit}}=f\times \text{LFL}*{H_2} ;=; f\times 0.04;\text{(v/v)}
]
If 9540A reports **mass** rate (\dot m*{H_2}) ([kg/s]), convert to volumetric at ambient:
[
G_{H_2}=\frac{\dot m_{H_2}}{\rho_{H_2}}\qquad
(\rho_{H_2}\approx 0.0838\ \text{kg/m}^3 \text{ @ 25 °C, 1 atm})
]
Then check **transient**: verify (C(t)) never exceeds (C_{\text{limit}}) for the measured release profile (\dot m(t)). Where installation-level data show multi-peak releases, size for the **worst credible 10–15 min window** or per AHJ direction. (IFC/NFPA 855 reference 9540A gas data for HMA; explosion prevention commonly follows NFPA 69 25 % LFL.) ([ICC Digital Codes][3])

---

# 6) Example (numerical, ready to adapt)

**Given (9540A unit-level):**

* Peak HRR ( \dot Q_{\text{pk}}=1.2\ \text{MW}); integral over event (E=900\ \text{MJ}).
* Peak **hydrogen** mass rate (\dot m_{H_2}=0.010\ \text{kg/min}=1.67\times10^{-4}\ \text{kg/s}) for 12 min.
* Indoor room (V=300\ \text{m}^3); target (f=25%) of LFL (H₂ LFL = 4 % v/v).

**Ventilation (steady-state minimum):**
[
G_{H_2}=\frac{1.67\times10^{-4}}{0.0838}=1.99\times10^{-3}\ \text{m}^3/\text{s}
]
[
C_{\text{limit}}=0.25\times0.04=0.01\ \text{(v/v)}
]
[
Q_{\text{req}}=\frac{1.99\times10^{-3}}{0.01}=0.199\ \text{m}^3/\text{s}
;=; 422\ \text{cfm}
]
Round up and add margin/interlocks per NFPA 69; if mixture includes CO/HCs, compute (\text{LFL}_\text{mix}) with Le Chatelier and re-solve. ([ammoniaknowhow.com][11])

**Transient check:** with (Q=500\ \text{cfm}=0.236\ \text{m}^3/s),
[
\frac{dC}{dt}=\frac{G}{V}-\frac{Q}{V}C
\quad\Rightarrow\quad
\tau=\frac{V}{Q}=1271\ \text{s}\ (\approx21.2\ \text{min})
]
Peak occurs before steady-state; verify (C(t)) numerically using the measured (G(t)). If peak exceeds 1 % v/v, increase (Q) or add emergency purge on high H₂. ([me.psu.edu][7])

**Separation via radiation (screening):**
With (\chi_r=0.25), (\dot Q=1.2\ \text{MW}), at (R=2.5\ \text{m}):
[
q''_{\text{rad}}=0.25\times\frac{1200}{4\pi(2.5)^2}\approx3.8\ \text{kW/m}^2
]
Well below 12.5 kW/m² → unlikely piloted ignition of wood-like combustibles from **radiation alone**; still check **convection/ceiling jet** if overhead items are vulnerable. ([Scribd][5])

**Ceiling jet (detector/sprinkler screening):**
Ceiling height (H=4.0\ \text{m}), (r=2.0\ \text{m}\Rightarrow r/H=0.5>0.18):
[
$$\Delta T_{\text{jet}}=
5.38\left(\frac{1200}{2}\right)^{2/3}\frac{1}{4}
\approx 5.38,(600)^{2/3}/4 \approx 5.38\times71.1/4\approx95\ ^\circ\text{C}$$
]
Use this to sanity-check thermal device activation predictions (DETACT/LAVENT) if needed. ([NIST][6])

---

# 7) What to show in the HMA/permit math section (bullet template)

* **Standard & edition** of test: e.g., *ANSI/CAN/UL 9540A (5th Ed., Mar 12 2025)*. Summarize any hydrogen-measurement details that affect your calcs. ([shopulstandards.com][2])
* **HRR summary**: (\dot Q_{\text{pk}}), (E), and notes on flames/droplets. Map to separation/suppression rationale. ([Sandia National Laboratories][1])
* **Gas analysis**: mass→molar/volumetric conversions; **well-mixed** transient and steady state; **%LFL** (single or mixed using **Le Chatelier**); compute (Q_{\text{req}}) for (f=25%) of LFL per **NFPA 69**. ([ammoniaknowhow.com][11])
* **Purge time** from alarm setpoint to safe level. ([me.psu.edu][7])
* **Toxicity check** for **HF** (ppm↔mg/m³ conversions and comparison to REL/STEL if required by AHJ/owner). ([EPA][12])
* **Overhead effects**: ceiling-jet ∆T screening (Alpert) and detector/sprinkler implications. ([NIST][6])

---

# 8) Quick reference values & equations (copy-paste box)

* **H₂ LFL** ≈ **4 % v/v** (air, ambient). Range ≈ 4–75 %. ([AIChE][8])
* **NFPA 69 design criterion**: keep **global** combustible gas ≤ **25 % LFL** (unless enhanced interlocks allow up to 60 %). ([ammoniaknowhow.com][11])
* **Well-mixed room**: $$(C(t)=C_\infty(1-e^{-Qt/V})+C(0)e^{-Qt/V}), (C_\infty=G/Q)$$. ([me.psu.edu][7])
* **Purge time**: $$(t=(V/Q)\ln(C_0/C_1))$$. ([me.psu.edu][7])
* **Le Chatelier (mixture LFL)**: $$(1/\text{LFL}_\text{mix}=\sum y_i/\text{LFL}_i)$$. ([digitalcommons.mtu.edu][9])
* **ppm↔mg/m³** at 25 °C, 1 atm: $$(\text{mg/m}^3=\text{ppm}\times \text{MW}/24.45)$$. **HF**: 1 ppm ≈ 0.82 mg/m³. ([AIHA][10])
* **Point-source radiation**: $$(q''=\chi_r \dot Q/(4\pi R^2))$$. Compare to ~**12.5 kW/m²** piloted-ignition screen for wood-like materials (literature range). ([Scribd][5])
* **Ceiling jet (Alpert)**: $$(\Delta T_{\text{jet}}=16.9,\dot Q^{2/3}/H^{5/3})$$ (near-axis) or (5.38(\dot Q/r)^{2/3}/H) (farther out). ([NIST][6])

---

If you give me the **specific ESS model** and a couple of numbers straight from its 9540A report (peak H₂ mass rate, release duration, HRR(_\text{pk}), room (V)), I’ll plug them into these equations and return a ready-to-paste **HMA calculation page** with assumptions and code line-ups.

[1]: https://www.sandia.gov/app/uploads/sites/163/2022/02/3c_Barowy_UL9540A_Sandia_Mar2019.pdf?utm_source=chatgpt.com "UL 9540A"
[2]: https://www.shopulstandards.com/ProductDetail.aspx?productId=UL9540A_5_S_20250312&utm_source=chatgpt.com "UL 9540A | UL Standards & Engagement"
[3]: https://codes.iccsafe.org/content/IFC2024P1/chapter-12-energy-systems?utm_source=chatgpt.com "CHAPTER 12 ENERGY SYSTEMS - ICC Digital Codes"
[4]: https://www.sfpe.org/FPEeXTRAIssue63?utm_source=chatgpt.com "FPEeXTRA Issue 63"
[5]: https://www.scribd.com/document/336828351/05-1-Heat-Flux-Calculations-Wind-Free?utm_source=chatgpt.com "05.1 Heat Flux Calculations Wind Free | PDF | Combustion"
[6]: https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=916864&utm_source=chatgpt.com "Ceiling Jet Flows"
[7]: https://www.me.psu.edu/cimbala/me405web_Fall_2006/Lectures/Chapter_05_Sections_7_to_10.pdf?utm_source=chatgpt.com "General Ventilation and the Well-Mixed Model"
[8]: https://www.aiche.org/sites/default/files/docs/pages/the_elemental_-_hydrogen_flammability.pdf?utm_source=chatgpt.com "Hydrogen Flammability"
[9]: https://digitalcommons.mtu.edu/michigantech-p/3870/?utm_source=chatgpt.com "Derivation of Le Chatelier's mixing rule for flammable limits"
[10]: https://www.aiha.org/ih-calculator-app/calcs/conversion-concentration.html?utm_source=chatgpt.com "Conversions: Concentration - AIHA Calculator"
[11]: https://www.ammoniaknowhow.com/wp-content/uploads/attachments/NFPA-69.pdf?utm_source=chatgpt.com "NFPA 69 - Standard on Explosion Prevention Systems ..."
[12]: https://www.epa.gov/sites/default/files/2016-10/documents/hydrogen-fluoride.pdf?utm_source=chatgpt.com "Hydrogen Fluoride (Hydrofluoric Acid)"
