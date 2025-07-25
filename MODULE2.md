# 📦 Module 2 : From wafers to package - assembly and manufacturing essentials 

## 🔍 1. Overview of Semiconductor Supply Chain
The semiconductor supply chain involves multiple critical stages, each contributing to the creation of the final electronic product. The entire process transforms a circuit idea into a packaged and tested IC ready to be deployed in commercial products.

<img width="500" height="248" alt="30664ebf-f4aa-405d-8e6d-53aa1eb52a7f (1)" src="https://github.com/user-attachments/assets/2a1a7006-9c39-4628-a331-e42b7fd95d5b" />


Design House → Wafer Fabrication → Package Assembly & Test → Board Assembly & Test → Product Assembly & Test


| Stage                    | Description                               | Inputs                        | Outputs                   |
|--------------------------|-------------------------------------------|-------------------------------|---------------------------|
| **Design House**         | Responsible for IC design using EDA tools | EDA tools, Foundry PDKs       | GDSII file, Test program  |
| **Wafer Fabrication**    | Manufacturing of ICs on silicon wafers    | Silicon wafers, equipment     | Wafer with fabricated ICs |
| **Package Assembly & Test** | Assembling individual ICs into packages | Substrates, chemicals, lids   | Packaged ICs (e.g., A15)  |
| **Board Assembly & Test**| Assembling packages onto PCBs             | PCBs, tools, materials         | Tested system boards      |
| **Product Assembly & Test** | Final product integration              | Components, tools              | Finished products (e.g., smartphones) |

---

## 🛠️ 2. Focus on Package Management (ATMP)

The **ATMP** stage is where *Assembly, Testing, Marking, and Packaging* of ICs takes place. It ensures that the silicon dies are converted into usable electronic components.

- **ATMP**: Assembly, Testing, Marking & Packaging
- **OSAT**: Outsourced Semiconductor Assembly and Test  
  - Companies: ASE, Amkor, TATA, etc.
- Can also be done **in-house** by companies like:
  - Intel
  - TSMC
  - Micron
  - Samsung
  - SK Hynix

> 🧠 *ATMP is the bridge between wafer fabrication and system-level integration. It ensures functional, reliable, and high-yield IC packaging.*

---

## 🏭 3. Example: Micron ATMP Facility – Sanand, Gujarat

| Feature                 | Detail                                   |
|------------------------|------------------------------------------|
| **Total Area**         | 1.4 million sq. ft.                       |
| **Clean Room Area**    | 500,000 sq. ft.                          |
| **Clean Room Class**   | Class 1000 / Class 10000                 |
| **Reference**          | [Forbes India Article](https://www.forbesindia.com/article/news/micron-commences-construction-of-assembly-test-facility-in-gujarat/88253/1) |

---

## 🏗️ 4. ATMP Unit Layout

A typical ATMP unit includes various zones for different operations, all within a controlled cleanroom environment:

<img width="700" height="256" alt="sbazd124 (1)" src="https://github.com/user-attachments/assets/f05300ca-2cd3-4d2f-b63c-c45f573bd5b3" />


### 📌 Key Zones

#### ➤ Processing Zone
- ISO Class 6 & 7 cleanroom
- Die bonding and flip-chip bonding
- Encapsulation and RDL formation

#### ➤ Testing Area
- Electrical testing
- Burn-in reliability testing
- Thermal & reliability chambers

#### ➤ Material Preparation and Storage
- Incoming materials: substrates, lids, chemicals
- Strict inventory and cleanliness control

---

## ✅ Summary

| Key Takeaways |
|---------------|
| ATMP is a crucial stage connecting wafer fabrication to system integration. |
| OSAT players and in-house units handle high-volume packaging and testing. |
| Cleanrooms and automated testing ensure reliability and high yield. |
| India is growing in ATMP space with Micron’s investment in Gujarat. |



---




# 🏭 Activities Inside the Cleanroom Area (ATMP Flow)

---

## 🏭 Wafer Preparation Area – ISO Class 7 Cleanroom

The **Wafer Preparation Area** is a critical cleanroom zone where wafers undergo multiple preprocessing steps before packaging. These operations are carried out under strict contamination control to ensure product reliability and yield.

### 📷 Visual Reference

<img width="600" height="337" alt="7f96d445-a7ca-43aa-b4c0-633809e7d09f (1) (4)" src="https://github.com/user-attachments/assets/d3beb29e-498a-4f6d-87ff-23307d6a2cea" />


## 🧾 Step-by-Step Breakdown of Cleanroom Activities

---

### 1️⃣ Incoming Wafer Carrier
- Wafers are delivered from the fab in specialized carriers known as **FOUPs (Front Opening Unified Pods)**.
- These carriers protect wafers from particles, humidity, and ESD (Electrostatic Discharge).
- Operators carefully open the FOUPs in laminar flow hoods inside ISO 7 environments to avoid contamination.

---

### 2️⃣ Wafer Inspection
- Optical and automated inspection tools scan wafers for defects.
- Checks are made for:
  - Surface irregularities
  - Contaminants or particles
  - Wafer ID and lot tracking
- Critical for filtering out damaged wafers before further processing.

---

### 3️⃣ Wafer Front Tape Lamination
- A **protective UV-sensitive tape** is laminated on the front side of the wafer.
- Purpose:
  - Shields delicate circuitry from physical damage during grinding.
  - Ensures structural integrity during handling.
- This tape can later be removed using UV exposure.

---

### 4️⃣ Wafer Backside Grinding
- Reduces wafer thickness (from ~700 µm to ~100 µm or less) to support thin-package applications.
- Grinding process:
  - Wafer is mounted face-down on a **grinding chuck**.
  - A rotating **grinding wheel** removes material from the backside.
  - Coolant and spindle force are precisely controlled to avoid cracks.

---

### 5️⃣ Tape Frame Mounting to Wafer Backside
- Post-grinding, the thin wafer is mounted onto a **dicing tape** held by a ring frame.
- Functions of the tape frame:
  - Secures wafer during dicing.
  - Maintains die alignment.
  - Prevents wafer breakage due to low mechanical strength.

---

### 6️⃣ Two-Step Wafer Dicing  
**(a) Laser Grooving**  
- Laser scribing creates shallow pre-cut grooves along scribe lines.
- Benefits:
  - Reduces mechanical stress during blade dicing.
  - Enhances die edge quality.

**(b) Blade Dicing**  
- A high-precision rotating diamond blade fully separates the individual dies.
- Conducted under water to reduce heat and wash away debris.

---

### 7️⃣ Final Wafer Inspection & SPC (Statistical Process Control)
- Post-dicing, each die and frame undergo:
  - Visual inspection (manual + automated vision systems).
  - Die count verification and placement accuracy.
  - Crack and chipping detection.
- **SPC Tools** monitor process metrics like blade wear, die yield, thickness, and more.
- Data is analyzed for:
  - Process drift detection
  - Outlier identification
  - Yield improvement

---

## ✅ Summary Table

| Step | Process Stage                          | Objective                                        |
|------|----------------------------------------|--------------------------------------------------|
| 1    | Incoming Wafer Carrier                 | Safe wafer transport and controlled loading      |
| 2    | Wafer Inspection                       | Identify defects and ensure quality              |
| 3    | Wafer Front Tape Lamination           | Protect frontside circuitry during grinding      |
| 4    | Wafer Backside Grinding               | Reduce wafer thickness for packaging             |
| 5    | Tape Frame Mounting                   | Secure wafer for stable dicing                   |
| 6    | Two-Step Wafer Dicing (Laser + Blade) | Isolate individual dies with minimal stress      |
| 7    | Final Inspection & SPC                | Ensure die quality, process control, and yield   |

---

## 🧠 Key Takeaways

- Cleanroom operations are essential to maintain **yield**, **reliability**, and **quality**.
- Every step involves specialized tools, monitoring, and **strict contamination control**.
- The combination of **laser + blade dicing** offers better die edge quality and minimizes cracks.
- **SPC is the backbone** of quality assurance in semiconductor packaging.

---

# 🧪  Wire Bond Packaging – Activities Inside the Cleanroom Area

In semiconductor packaging, **Wire Bonding** is a key interconnect technology used to establish electrical connections between the die and the package substrate. This lecture walks us through the **step-by-step process** inside the cleanroom where wire bond packaging takes place.

---

<img width="550" height="272" alt="0fa22407-ae10-4e7c-9d64-888c4fadc5e1 (1)" src="https://github.com/user-attachments/assets/bddf2f56-0f3e-4726-a34e-b2db3b67feb8" />

## 📌 Overview of the Wire Bond Packaging Flow:

The overall process includes:

1. **Die Attach**
2. **Curing**
3. **Wire Bonding**
4. **Molding (Transfer Molding)**
5. **Marking (Laser Marking)**
6. **Singulation (Dicing)**

---

## 🧩 1. Die Attach

> Die attach is the process of fixing the semiconductor die onto the package substrate using an adhesive.

**Steps involved:**
- **Epoxy Dispensing:** A precise amount of epoxy is dispensed on the package substrate.
- **Chip Pick-up:** A robotic pick-up head selects the individual die from the wafer.
- **Placement:** The die is placed carefully on the **Die Attach Film (DAF)** located on the substrate.

This step is critical for ensuring physical stability and thermal/electrical conductivity between the chip and substrate.

---

## 🔥 2. Curing

> After the die is attached, the epoxy must be **cured** (hardened) to provide a secure mechanical bond.

- The assembly is passed through a **curing oven** or subjected to **infrared (IR) heating**.
- Proper curing ensures the die doesn’t shift during further processing and maintains adhesion strength.

---

## ⚡ 3. Wire Bonding

> Wire bonding forms the electrical connections between the **bond pads on the die** and the **bond fingers on the substrate** using fine gold or copper wires.

### Types of Bonds:
- **Ball Bonding (using gold wires)**
- **Wedge Bonding (using aluminum wires)**

### Key Steps:
1. **Wire Tail Formation:** A fine wire is fed through a capillary tool.
2. **EFO Spark (Electronic Flame-Off):** Creates a free air ball at the end of the wire.
3. **Ball Bond Formation:** The ball is pressed onto the die pad using **ultrasound and heat** to form a **strong metallurgical bond**.
4. **Wire Looping:** The capillary forms a wire loop as it moves to the substrate bond pad.
5. **Crescent Bond:** Another bond is formed on the package substrate.
6. **Wire Clipping:** The wire is cut to complete one connection.

Wire bonding is repeated for all required pads with **high speed and precision**.

---

## 🧫 4. Molding (Transfer Molding)

> After bonding, the entire die and wires are encapsulated in a **mold compound** to protect them from mechanical damage, moisture, and contaminants.

- **Resin Flow:** A thermosetting resin is injected into a mold cavity using high pressure.
- It flows around the die and wires, then solidifies on curing to form a **rigid protective shell**.

This ensures long-term reliability and robustness of the packaged device.

---

## 🔍 5. Marking (Laser)

> Each packaged chip is marked using **laser etching**.

- **Laser Marking** is used to print product information, traceability codes, or logos.
- Non-contact method, fast, and suitable for high-volume manufacturing.

---

## ✂️ 6. Singulation (Dicing)

> This is the process of **separating individual units** from a molded array.

- A **thin dicing blade** is used to cut along the pre-defined saw streets between units.
- Ensures minimal chipping and clean edges for high-yield and reliable packaging.

---

## ✅ Final Output

At the end of these steps, each individual die is:
- Electrically connected to its substrate,
- Protected by a mold compound,
- Clearly marked for identification,
- And separated into individual units ready for testing and shipment.

---

📌 **Note:** All these operations occur in a **controlled cleanroom environment** to avoid contamination and ensure the highest quality and reliability of the semiconductor package.

---

# 🔁 Flip Chip Packaging – Mass Reflow and Thermo-Compression Flow

**Flip Chip Packaging** is an advanced packaging technique where the die is flipped upside down, and **solder bumps** are used to connect the chip directly to the substrate. This enables high-density, high-performance, and compact interconnects, ideal for modern electronics.

This lecture explores the **step-by-step cleanroom process** for flip chip packaging, including **bump formation, chip mounting, reflow, underfill, and molding**.

---
<img width="550" height="272" alt="a0799f23-209f-47c5-b700-e7ad4106c352 (1)" src="https://github.com/user-attachments/assets/0a88b855-ed0a-4869-9b73-945512cded8a" />



## 📌 1. Bump Formation on Silicon (Si)

> Bumps are tiny solder balls that form the electrical and mechanical connection between the silicon die and the substrate.

### 🔹 Step-by-step bump formation:
- **Solder Deposition:** Solder is deposited on the die bond pads.
- **Before Reflow:** The solder appears as cylindrical deposits sitting on top of UBM (Under Bump Metallization).
- **Reflow:** The entire wafer is heated. The solder melts and forms spherical bumps due to surface tension.
- **After Reflow:** Rounded solder balls are formed and solidified in place.

✅ **Result:** Bumps are ready for flip-chip mounting.

---

## 🔄 2. Flipping the Chip

> The chip is flipped so that the bumps face downward and align with the bond pads on the package substrate.

This "flip" gives the packaging its name — **Flip Chip** — and enables direct connection without wire bonding.

---

## 💧 3. Flux Dispensing

> **Flux** is dispensed onto the substrate to clean and prepare the surface for solder bonding.

- Flux removes oxides from the metal surfaces and improves solder wetting.
- Ensures good mechanical and electrical connections during reflow.

🧪 **Flux is applied precisely** over the bond pads on the substrate using dispensing tools.

---

## 📍 4. Chip Placement

> The bumped chip is placed onto the substrate such that each bump aligns with its respective pad.

- Done using **high-precision pick-and-place** tools.
- Alignment is critical to ensure proper solder bonding.

---

## 🔥 5. Solder Reflow

> The assembly is passed through a **reflow oven** to melt the solder bumps and form permanent bonds.

- The solder melts and wets both the die pads and the substrate pads.
- As it cools, a **solid metallurgical bond** forms at each bump location.

This step is similar to the reflow process used in PCB manufacturing.

---

## 💨 6. Flux Cleansing

> After reflow, **residual flux** must be removed using solvent spray.

- Cleansing prevents corrosion or contamination of the solder joints.
- Performed in a controlled environment using **chemically safe solvents**.

---

## 🧴 7. Underfill Dispensing

> Underfill is an **epoxy resin** material that is dispensed to fill the gap between the chip and the substrate.

### Why Underfill?
- Improves **mechanical stability**.
- Reduces **stress** on solder joints due to thermal expansion mismatch.
- Enhances **moisture resistance** and **long-term reliability**.

The underfill flows under the chip by **capillary action**.

---

## ♨️ 8. Underfill Cure

> The underfill material is **cured using heat** to solidify it into a strong, supportive layer.

- Curing ovens or hot plates are used.
- Ensures the chip is rigidly held in place, minimizing mechanical stress.

---

## 🧱 9. Molding

> The chip and underfill assembly are **encapsulated using a protective mold compound**.

- Mold material is injected around the chip for mechanical and environmental protection.
- Prevents damage from moisture, dust, or mechanical shock.

---

## ✍️ 10. Marking

> Final packages are marked using **laser marking systems**.

- Adds product identification, batch numbers, or branding.
- Enables traceability during manufacturing and logistics.

---

## ⚙️ 11. Ball Mounting on the Substrate (BGA Balls)

> **Ball Grid Array (BGA) balls** are added on the bottom side of the package for final PCB assembly.

- The BGA balls provide interconnection between the package and the PCB.
- The pattern and pitch depend on the device application.

---

## 🔥 12. Final Reflow After Ball Mounting

> The BGA balls are reflowed onto the substrate to form the final interconnects.

- This is similar to earlier solder reflow but now connects the **package to the PCB side**.
- Ensures robust connection ready for system-level integration.

---

## ✅ Final Outcome

After these steps, the **Flip Chip Package** is:
- Electrically connected using **solder bumps**,
- Mechanically stabilized with **underfill**,
- Protected with **molding**, and
- Ready for integration into PCBs using **BGA balls**.

---

### 📌 Advantages of Flip Chip Packaging:
- Shorter electrical paths → **Better performance**
- High I/O density
- Excellent heat dissipation
- Compact form factor

---

### 🧪 Flip Chip Summary Flow:

```plaintext
Bump Formation → Chip Flip → Flux Dispensing → Chip Placement → Solder Reflow →
Flux Cleansing → Underfill → Underfill Cure → Molding → Marking →
BGA Mounting → Final Reflow





