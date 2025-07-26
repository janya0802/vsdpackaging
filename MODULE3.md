# 📘 Module 3  – Labs : Thermal simulation of semiconductor analysis with ANYSYS 

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




