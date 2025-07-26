# 📘 Module 3  – Labs : Thermal simulation of semiconductor analysis with ANYSYS 

## 🗂️ Lecture 10 :  Introduction And Getting Started With ANSYS Electronics Desktop

In this lecture, we were introduced to **Ansys Electronics Desktop – Student Version**, which integrates several electromagnetic, thermal, and circuit-level simulators under one umbrella. Our primary focus was on **Icepak**, a specialized tool within this environment used for **thermal management simulations** in electronics, especially in **semiconductor packaging** workflows.

---

## 🧰 Getting Started with Ansys Electronics Desktop

Once the software was installed and launched, we were presented with the main toolbar showing various modules:

<img width="343" height="115" alt="image" src="https://github.com/user-attachments/assets/13ac49dc-8c57-4d65-8f04-be4eca5b27ea" />


- **HFSS**: High-Frequency Structure Simulator, used for RF and microwave electromagnetic simulations.
- **Q3D Extractor**: Used for parasitic inductance and capacitance extraction in 3D structures.
- **Circuit**: For circuit-level analysis.
- **Icepak** ✅: The module we use for thermal simulations.
- **Maxwell**: Electromagnetic field simulation.
- **Simplorer**: System-level multiphysics simulation.

Here, **Icepak** was selected, which opens up a powerful and intuitive environment tailored for simulating heat flow, airflow, and thermal characteristics of complex IC packages and systems.

---

## 🗂️ Project Setup in Icepak

Once Icepak is selected, a **Project Manager** panel appears on the left:

<img width="251" height="334" alt="image" src="https://github.com/user-attachments/assets/b0dc7f73-ca1b-47be-8ad7-39f015baefbf" />


A new project titled `IcepakDesign1 (SteadyState)` was created. It includes:
- **3D Components**: Allows importing and managing external components.
- **Model**: Geometry building section.
- **Thermal**: Assign temperature sources, heat loads, and boundary conditions.
- **Monitor**: Used to track specific values during simulation (e.g., temperature at a point).
- **Solar Loading**: Optional solar heating configuration.
- **Mesh**: Finite volume meshing to discretize the geometry.
- **Analysis**: Defines simulation type (steady/transient), convergence criteria, and solves.
- **Optimetrics**: For parametric studies and design optimization.
- **Results / Field Overlays**: Used to visualize simulation outcomes.
- **Definitions**: Houses material definitions, coordinate systems, and variables.

---

## ⚙️ Tools and Customization

From the **Icepak → Tools** menu, we accessed a variety of toolkits and simulation aids:

<img width="500" height="262" alt="Screenshot 2025-07-27 023740" src="https://github.com/user-attachments/assets/68c2a962-4d66-41bf-aa0b-08b36ef45aaa" />

### Toolkit Options:
- **Geometry**: Predefined models for packages and heatsinks.
  - Includes options like **Data Center Components**, **PCB**, **Heatsinks**, and **Flip Chip BGA**. (From where we chose package ) 
- **Modeling**: Tools to simplify or manipulate CAD geometry.
- **Reporting**: Helps automate simulation result exports.
- **Source_From_CSV**: Used to import boundary data or component definitions via CSV files.
- **Write_Average_Metal_Fraction**: Helps analyze metal distribution for thermal conductivity.

> 🔍 Notably, when using **Flip Chip BGA** under the Geometry → Packages tab, we can **export this to Icepak** for direct simulation, reducing manual modeling and improving accuracy.

---

# 🗂️ Lecture 11 : Setting Up A Flip-Chip BGA Package

This lecture documents the complete design workflow of a **Flip Chip Ball Grid Array (BGA)** package using Icepak inside Ansys Electronics Desktop Student Version.

---

## 🧩 Step-by-Step Model Setup

---

### 1️⃣ Package Dimensions

- **Plane:** XY  
- **Length × Width:** 15 mm × 15 mm  
- **Thickness:** 1.6 mm  
- **Symmetry:** Full  
- **Units:** Millimeters  
- **Model as 3D component:** Enabled  

<img width="500" height="275" alt="Screenshot 2025-07-27 030306" src="https://github.com/user-attachments/assets/125a204f-218e-4a35-8c8c-eef12fa1905b" />

---
## 🧊 2. Die Configuration

- **X Length:** 8.56 mm  
- **Y Length:** 8.56 mm  
- **Power:** Defined in watts (set based on simulation needs)  
- **Source Type:** 2D Source  
- **Material:** Si-Typical  
- **Die Underfill:**  
  - **Bump Size:** 0.01 mm  
  - **Material:** Flipchip_underfill  
- **Heatsink:** Not included  
- **3D Component Creation:** Enabled

> The die is placed centrally on the substrate and is the primary heat-generating region in the system. The underfill strengthens bump connections and improves thermal paths.

<img width="500" height="273" alt="Screenshot 2025-07-27 030318 (2)" src="https://github.com/user-attachments/assets/64497c0b-f16d-44b1-a9d8-cd3b21b19627" />

---

### 3️⃣ Substrate Setup

- **Total Thickness:** 0.36 mm (0.2 of total package thickness) 
- **Number of Layers:** 2  
- **Material:** Custom substrate (usually BT epoxy or FR-4)  
- **Top Trace Coverage:** 55%  
- **Bottom Trace Coverage:** 55%  
- **Trace Thickness:** 0.033 mm  
- **Trace Material:** Pure Copper (Cu-pure)  
- **Die attach material:** Die_Attach_SAC305  
- **Thermal vias:** 0  
- **Via diameter:** 0.2 mm  
- **Plating thickness:** 0.05 mm  


<img width="500" height="269" alt="Screenshot 2025-07-27 030341 (1)" src="https://github.com/user-attachments/assets/79f6b243-1c77-4508-b320-718d6e08395d" />

---

### 4️⃣ Solder Ball Configuration

- **Array Size:** 14 × 14  
- **Type:** Full  
- **Pitch (center-to-center spacing):** 1.0 mm  
- **Ball Diameter:** 0.5 mm  
- **Ball Height:** 0.5 mm  
- **Material:** Pb50_Sn50 (50% Lead, 50% Tin alloy)

<img width="500" height="275" alt="Screenshot 2025-07-27 030357" src="https://github.com/user-attachments/assets/fbac824b-7e89-4367-b427-cd591ce0c385" />


---

### 5️⃣ Heat Sink Settings (Optional Block)

- Not applied in this design  
- Instead, **convection and radiation boundaries** were used for thermal simulation
- Turbo mode dissipates more power 

---

### 6️⃣ Boundary Conditions and Mesh

- **Mesh type:** Tetrahedral  
- **Mesh control:** Applied at component boundaries for die and substrate  
- **Thermal boundaries:**  
  - Bottom face set to **natural convection**  
  - Remaining faces as **symmetry planes (if full model not used)**  
- **Power applied to die:** ~1 W (can be configured from Source settings)

---

### 7️⃣ Material Properties Overview

| Component     | Material         | Notes                              |
|---------------|------------------|-------------------------------------|
| Die           | Silicon          | Heat source                         |
| Substrate     | BT/Epoxy or FR-4 | High thermal resistance             |
| Trace         | Cu-Pure          | High electrical/thermal conductivity |
| Die Attach    | SAC305           | Thermally conductive solder paste  |
| Solder Balls  | Pb50_Sn50        | Good thermal & electrical transfer |

---

## 🧩 Final 3D Package Model Structure : 

>After providing  all the required information , we will generate the package model . 

<img width="600" height="219" alt="Screenshot 2025-07-27 030647" src="https://github.com/user-attachments/assets/ed52985c-5629-4177-b7cc-df8a8db040b7" />
<img width="250" height="113" alt="Screenshot 2025-07-27 030707" src="https://github.com/user-attachments/assets/0270d97e-7f8a-44f2-9503-2ccb0acaeaec" />



### 🧱 Model Tree Breakdown

This section describes each group and subcomponent shown in the Ansys Model Tree:

#### 🔹 `Flipchip_BGA1_Group`
- This is the **top-level assembly** representing the entire Flip Chip BGA package.
- It contains all key sub-blocks: die, underfill, substrate, traces, and more.

#### 🔹 `Flipchip_BGA1_ball_Group`
- Represents the **solder ball array**.
- Includes **14 × 14 grid** of solder balls (excluding central regions depending on pad layout).
- Each ball is modeled as a 3D thermal-solid element with **Solder-pb50_sn50** material.

#### 🔹 `Solids`
- This node contains solid bodies of the die, substrate, solder balls, and underfill.
- These solids interact thermally and structurally.

#### 🔹 `Sheets → Conducting Plate → Flipchip_BGA1_trace`
- Contains **trace geometries** on the substrate layer.
- Traces are generated using the `CreateRectangle` command and are covered using `CoverLines`.
- **Material:** Cu-Pure
- **Trace thickness:** 0.033 mm
- **Trace coverage:** 55%

#### 🔹 `Source`
- This defines the **heat generation** in the model.
- The die has a **2D source** applied, corresponding to internal power dissipation (in watts).

#### 🔹 `air`
- The air domain encloses the entire model in a **conduction-convection environment**.
- Used for proper boundary condition setup for thermal simulations.

#### 🔹 `Region`
- Defines the **computational region** for meshing and simulation.

#### 🔹 `Coordinate Systems`
- Default global coordinate system and any additional user-defined systems for positioning components.

---

### 🧊 Visual Representation Summary

The visual model (as seen in the image) clearly shows:
- A **gray rectangular Die** placed at the center.
- A **brown Substrate** underneath with embedded trace layers.
- An invisible underfill (modeled but not shown here).
- The full BGA solder ball array (not displayed in the cut view).
- Red boundary outlines representing the **air region and symmetry boundaries**.


# 📦 Lecture 12: Material Definitions and Thermal Power Sources

In this lecture, we explored how to work within the **Project Management bar** of ANSYS Icepak to define materials, thermal sources, and set up monitors for thermal simulations. This is a key step in analyzing the thermal performance of Flip Chip Ball Grid Array (FCBGA) packaging.
<img width="252" height="285" alt="Screenshot 2025-07-27 041940" src="https://github.com/user-attachments/assets/0dea3ac8-d2d6-4899-86cc-74ab3ff36d24" />

---

## 🧰 Project Management Workflow

### 🔹 1. Model Tab
The **Model** tab in the project management bar helps in setting up the geometry, importing models, and configuring components such as die, underfill, and substrate. All design elements are prepared in this stage before applying thermal properties.

---

### 🔥 2. Thermal Conditions Tab

<img width="250" height="116" alt="Screenshot 2025-07-27 042159" src="https://github.com/user-attachments/assets/78f8423e-2471-421d-957b-f47cd9949afc" />

In this tab, we define all power sources and boundary conditions for heat transfer simulation.

#### 🧪 Power Source (Die)
- The **source** refers to thermal power (in Watts) applied to specific components.
- For this simulation, the **die** is assigned as the power source.
- Power is applied directly on the die component to simulate heat generation during operation.

In "Project Manager" sub-window, expand Thermal section and open the "BGA1_die_source" and configure the thermal condition as shown below:

<img width="500" height="397" alt="Screenshot 2025-07-27 042036" src="https://github.com/user-attachments/assets/a70b7df2-6d3d-4788-86f9-002ccd517b25" />


#### 📦 Boundary Condition (Substrate)
- To add thermal boundary condition for the substrate, right click on "Flipchip_BGA1_substrate" under "Models -> Flipchip_BGA1_Group -> Solids" and assign a Thermal Source.
- The **substrate** is given a **source boundary condition**, which represents heat exchange conditions (like convection or conduction) on its surfaces.
- This helps simulate realistic cooling or heating behavior of the substrate layer.

Set the thermal condition on the substrate to Fixed Temperatue and the temperature as Ambient.

<img width="557" height="507" alt="image" src="https://github.com/user-attachments/assets/2a63b6eb-5ec1-44c2-8e76-d7aa9e9c8bc3" />


### 📍 3. Monitor Tab
<img width="225" height="86" alt="Screenshot 2025-07-27 043625" src="https://github.com/user-attachments/assets/6ac59c71-d7f9-40c1-b9e6-18c94591935e" />

We use the **Monitor** tab to observe how temperature changes at critical locations in the package during simulation.

#### 🔸 Point Monitor on Substrate

- To add a Thermal monitor to the substrate, right click on the "Flipchip_BGA1_substrate" under "Models -> Flipchip_BGA1_Group -> Solids" and choose "Assign Monitor -> Point"
- A **point monitor** is assigned to the substrate to track temperature variation over time or at steady state.
- This helps us evaluate how well the substrate dissipates heat from the die.

#### 🔸 Point Monitor on Die

- Similarly, a **temperature monitor** is placed directly on the **die** to observe peak temperature due to the applied power source.
- This helps in ensuring thermal safety and reliability of the die.

#### 🔸 Point Monitor on Underfill

- An additional monitor is assigned to the **underfill** region to track how heat spreads through this material.
- The underfill plays a critical role in thermal conduction and mechanical stress absorption.

---

## ✅ Key Takeaways

- Proper **thermal source definition** is crucial for accurate thermal simulations.
- **Point monitors** help in tracking temperature across vital packaging materials.
- This step bridges material modeling with thermal analysis, giving insight into how heat is generated and dissipated across the chip-package system.

---



