## RTX 3090: Full Thermal Overhaul

> Demonstrated on a Zotac Trinity

See [Step-by-step Guide](#-step-by-step-guide) if you already have [all supplies](#-bill-of-materials-summary).

## Overview

Complete thermal mod for Zotac RTX 3090 Trinity:

- **GPU die:** PTM7950 phase-change material (24×26mm)
- **Front VRAM:** 2.0mm thermal pads
- **Back VRAM:** 3.0mm thermal pads
- **Deshroud:** two 120mm fans for the main-front heatsink
- **Backplate heatsink:** Four 40×40mm aluminum heatsinks + one 92mm fan
- **Hardware:** 1.0mm Nylon washers for backplate screw tension

## 🛒 Material Shopping List

### 🌡️ 1. Thermal Interface Materials

| Component | Product | Thickness | Quantity | Cut size |
|---|---|---|---|---|
| **GPU die** | Honeywell PTM7950 | 0.25mm | **1 sheet**<br>50mm x 31mm | Cut exact die size<br>26mm x 24mm |
| **Front<br>VRAM** | High-conductivity pad<br>**15 W/mK** | **2.0mm** | **1 sheet**<br>100mm x 100mm | Cut 12 chips<br>12mm x 12mm |
| **Back<br>VRAM**  | High-conductivity pad<br>**15 W/mK** | **3.0mm** | **1 sheet**<br>100mm x 100mm | Cut 12 chips<br>12mm x 12mm |
| **Washers** | Nylon flat washers<br>(M2.5) Ø**2.5mm** | **1.0mm** | **4-6 pieces** |

#### GPU die | Phase-change material

> [**Honeywell PTM7950**](https://www.honeywell.com.cn/content/dam/honcn/documents/advanced-materials/electrical-materials/thermal-interface-materials/ptm7000-series/PTM7950-TDS-EN%202022.12.7.pdf)

![PTM7950](/img/Honeywell_PTM7950_specs.avif) | ![PTM7950](/img/Honeywell_PTM7950.avif)
---|---

**Why 100x100mm sheets instead of 85x45mm?**
- Mistakes allowance (~20% waste)
- Leftover for second GPU 

#### VRAM Thermal pads: Fehonda 15 W/mK soft

> [**Fehonda 15W/mk thermal pad**](https://www.fehonda.com/thermal-pad/15w-mk-fehonda-thermal-pad)

![PTM7950](/img/fehonda.webp)

| Parameters | Unit | Regular | Low permeation Oil | Test standard
|---|---|---|---|---|
| Thermal Conductivity  | **W/m·k**   | 15 | 15 | ASTM D5470 |
| Hardness              | **Shore C** | 40~50 | 40~50 | ASTM D2240 |
| Density               | **g/cc**    | 3.5±0.2 | 3.5±0.2 | ASTM D792 |
| Thickness             | **mm**      | 0.5~3.0 | 0.5~3.0 | ASTM D374 |
| Breakdown Voltage     | **Kv/mm**   | ＞10 | ＞ 10 | ASTM D149 |
| Volume Resistivity    | **Ω.cm**    | ≥1010 | ≥1010 | ASTM D257 |
| Silicone Permeability | **%**       | ≤3 | ≤1 | 125°C/72h（compression50%） |
| Temperature Range     | **℃**      | -40~180 | -40~180 | / |
| Flame Rating          | **/**       | V-0 | V-0 | UL 94 |

Try to buy both 2.0mm and 3.0mm from the same brand to ensure consistent compressibility.

### 🌬️ 2. Deshroud Mod | Dual 120mm Fan

| Component | Product | Specs | Quantity |
|---|---|---|---|
| **Fan bracket** | [Zotac Trinity RTX 3090<br>Bracket Mod Kit + Adapter Cable](https://www.etsy.com/listing/1311068645/zotac-trinity-rtx-3070-3080-3090-video) | Deshroud<br>Dual 120mm fans | 1
| **Fans** | [ARCTIC P12 Max](https://www.amazon.fr/-/en/dp/B0CC8V6PHJ) | 3300 rpm<br>4,35 mmH₂O<br>81 cfm (137 m³/h) | 2

#### Mod

![heatsink-ext](/img/2619.7.0553.png)

![heatsink-ext](/img/2619.7.0553_1.png)

This fan bracket mod kit Allows for the use of two 120mm x 25mm fans, with mounting hardware that includes 8x 30mm M4 screws. Includes a PWM 4-pin fan adapter Y cable that uses a micro 4-pin connector designed to connect to the fan headers on the video card. 

![deshroud](/img/il_1588xN.4188446810_4xs8.webp) | ![deshroud](/img/il_1588xN.7603510144_p1te.webp)
---|---

#### Fans

Recommended:

- [**Arctic P12 PWM PST**](https://www.arctic.de/us/P12-PWM-PST/ACFAN00120A)  
**Best value**: ~\$**10**, best perf, silent enough but louder than Noctua.

- [**Noctua NF-A12x25 G2 PWM**](https://www.noctua.at/en/products/nf-a12x25-g2-pwm) | *Note: the SKU [**Sx2-PP**](https://www.noctua.at/en/products/nf-a12x25-g2-pwm-sx2-pp) is a pack of two starting at ~\$65.*  
**Luxury elite**: ~\$**35** (at least!), great perf, lowest noise.

> [**Tom's Hardware direct 1:1 comparison with the Arctic P12 Pro**](https://www.tomshardware.com/pc-components/case-fans/pc-fan-faceoff-can-arctics-usd7-p12-pro-compete-with-the-usd40-noctua-nf-a12x25-g2)  
> *"the P12 pro gives you almost Noctua-level performance at medium speeds, obscene power at its full duty with over 3000 RPM to play with"*

My personal experience with such a choice is that you want Noctua for the always-on, 24/7 duty. The point is to bring down what will become the permanent noise level of your room. That's for case fans and CPU, generally. For the GPU, it depends on what kind of workload you're going to put on it:

- Half-permanent long-lasting load requiring above 50% fan speed: go Noctua if noise bothers you.
- Spiky, irregular activity, on-demand load: you cut fan budget in half or more by buying Arctic, for half or even a third of the price, and get equal or better performance (depending on whether you choose regular PWM or Pro).

For the highest performance, see the [P12 Pro PST](https://www.arctic.de/us/P12-Pro-PST/ACFAN00306A).  
For daisy-chain capability, take "PST" SKUs.  
For continuous operation, take the CO variants (dual ball bearing: louder but fan lasts longer).  
You may combine all: [P12 Pro PST CO](https://www.arctic.de/us/P12-Pro-PST-CO/ACFAN00312A).

### ♨️ 3. Backplate Cooling Assembly

| Component | Product | Specs | Quantity |
|---|---|---|---|
| **Heatsinks** | Anodized Extruded Aluminum<br>grid-finned (11×10) | **40×40mm** each<br>fin height 20mm | **4 pieces** |
| **Fan** | **Arctic P9 PWM PST**<br>92 × 25mm thick | Airflow: 65,97 m³/h<br>Noise: 39.8 dB | **1 unit** |

Optionally, add fan mounting + dust filter.

| Component | Product | Specs | Quantity |
|---|---|---|---|
| **Fan screws** | M3 x 20-25mm pan-head screws + nuts | Stainless steel | **4 sets** |
| **Fan grille** | 92mm wire fan grille (optional) | Chrome/black | **1 unit** |

#### Backplate Heatsinks

> [**Extruded Aluminum Heatsink Radiator** with 3M Tape (P9JB)](https://fr.aliexpress.com/item/1005007090772998.html)

| ![heatsink-ext](/img/2619.7.0439.png) | ![heatsink-dims](/img/2619.7.0436.png) |
|---|---|

**Mounting method for heatsinks:**
1. Clean backplate with isopropyl alcohol.
1. Place four heatsinks in a 2x2 grid centered over the VRAM backside area.
1. Leave 2-3mm gap between each heatsink for airflow.
1. Press firmly, let cure 24 hours before fan installation.

#### Fan

Recommended:

- [**Arctic P9 PWM PST**](https://www.arctic.de/en/P9-PWM-PST-Black/ACFAN00298A) (best value, ~\$**10**)

- [**Noctua NF-A9 PWM**](https://www.noctua.at/en/products/nf-a9-pwm) (quieter but 2x price at ~\$**20**)

> [**Leo**](https://search.brave.com/search?q=ARCTIC+P9+PWM+PST+noise+dB&source=web&conversation=09112db023901fff98d3f7e53d67b9af8ce0&summary=1)  
> *"Independent testing placed the P9 PWM PST just 1.8 dB(A) above the benchmark Noctua NF-A9 PWM fan (38 dB(A)) while delivering superior cooling performance."*

See [Fans](#fans) section above for a discussion about choosing 120mm fans. The same applies here, as confirmed by Leo (Brave Search AI).

| ![arctic-p9](/img/arctic-p9.jpg) | ![noctua-nf-a9](/img/noctua-nf-a9-pwm.jpg) |
|---|---|

**Mounting method for fans:**
1. Drill or punch four holes through the backplate (if not pre-drilled) in a 92mm fan mounting pattern (standard 82.5mm screw spacing).
1. Use M3 screws through backplate → through heatsink grid → nut on top.
1. Alternatively: use **adhesive fan mount tape** (3M VHB), or **cable zip ties**, to maintain the fan directly against heatsinks — simpler, no drilling.

### 🧴 Supplies

| Component | Product | Specs | Quantity |
|---|---|---|---|
| **Isopropyl alcohol** | 99% purity | 100ml bottle | **1 unit** |
| **Lint-free wipes** | Coffee filters or Kimwipes | – | **10-20 pieces** |
| **Thermal paste** (optional backup) | Arctic MX-6, Thermal Grizzly Kryonaut | 1g syringe | **1 unit** |

### 🪛 Tools

| Tool | Purpose | Recommendation |
|---|---|---|
| **Embroidery scissors** | Cutting pads precisely | **6.4cm (2.5") blade**, sharp point |
| **Steel ruler** | Guiding cuts | 15cm length, metal |
| **Digital calipers** | Measuring die and VRAM | 0.01mm accuracy |
| **Precision screwdriver set** | GPU disassembly | PH0, PH1 bits |
| **Non-magnetic plastic spudger** | Prying connectors | iFixit style |
| **Tweezers** | Placing small pads | Non-magnetic, fine tip |

## 🧾 Bill of Materials Summary

| Qty<br>(max) | Item | Cost (€)<br>+ Ship. | Store<br>Page
|---|---|---|---|
|| **—— 1. Thermal interface materials ——**
| 1 | **Honeywell PTM7950** 50x31mm sheet | 11.05 + 8.49 | [MODDYI](https://www.moddiy.com/products/6061)               | 
| 1 | **Fehonda 15W/mk thermal pad** 100×100×**2.0** mm | 18.99 | [Ali](https://fr.aliexpress.com/item/1005005899514989.html)  | 
| 1 | **Fehonda 15W/mk thermal pad** 100×100×**3.0** mm | 21.59 | [Ali](https://fr.aliexpress.com/item/1005005899514989.html)  | 
|| **—— 2. Deshroud mod ——**
| 1 | Deshroud mod 2×120mm fans [by Osserva] | 31.14 + 14.10 | [Etsy](https://www.etsy.com/listing/1311068645/)             | 
| 2 | Arctic P12 Max | home supply | 🏡
|| **—— 3. Backplate cooling ——**
| 8 | 40×40×20mm aluminum heatsink | 12.38 |  [Ali](https://www.aliexpress.com/item/1005007090772998.html) | 
| 1 | Arctic P9 PWM PST | 10.49 | [Amzn](https://www.amazon.fr/-/en/dp/B09VGR175K)             | 
|| **—— Hardware Mods ——**
| 50 (6) | M2.5 4mm screws | 1.84 | [Ali](https://www.aliexpress.com/item/1005008841266415.html) | 
| 100 (6) | nylon washers | 8.99 | [Amzn](https://www.amazon.fr/-/en/dp/B08XWXMN5Y)             | 
| 1 | Isopropyl alcohol 1L | 7.79 | [Amzn](https://www.amazon.fr/-/en/dp/B07SH9FY7G)             | 
| 100 (?) | Wipes | 9.39 | [Ali](https://www.aliexpress.com/item/1005001689994595.html) | 
|| **—— Tools ——**
| 1 | Polyimide (Kapton) Tape | 9.99 | [Ali](https://www.aliexpress.com/item/1005009367219178.html) | 
| 1 | Embroidery scissors | 6.09 | [Ali](https://www.aliexpress.com/item/1005010744511928.html) | 
||| **TOTAL**
| **1~2** | **RTX 3090 Zotac Complete Thermal Mod** | **172.32** |

We have spare material for another full mod (in 3-5 years) or another GPU.*

\* *Except the deshroud mod, depends on brand/SKU for VRAM pads height and die size.*

---

## 👇 Step-by-Step guide

> [!IMPORTANT]
> Always ensure you will put each screw in the exact place they came from:
> - Take a sheet of paper and draw/print two GPUs shapes with screws positioned.
>     - One on the outside (looking at the backplate) for the cooler screws.
>     - One on the inside (looking at the GPU die) for the backplate screws.
> - Place screws as you disassemble (note in which order they came: 1, 2, 3…), then walk that back to reassemble.

### Check the deshroud manual 📖

Make sure:
- Can you do it last?
- What preparations needs to be done to deshroud?

### Disassemble the GPU 🪛
    
1. **Cooler**: 6 screws

    ![cooler-screws](/img/2619.7.0337.png)

    Unplug 2 fan cables (black, white) + 1 LED cable (black).

    ![cooler-wires](/img/2619.7.0340.png)
    
2. **Backplate** – 6 screws + 1 LED cable (white).

    ![back-screws](/img/2619.7.0341.png)

3. Clean all old thermal material (thermal paste and pads) using isopropyl alcohol wipes.

### Cut VRAM pads ✂️

- 24 pieces total (12x front 2.0mm, 12x back 3.0mm), each 12mm x 12mm 
- Alternatively, simpler: four **strips** on each side, 8 pieces total: 2x ( 4x 4x 3x 1x )

### Apply back VRAM pads 📐

Place on all 12 backside VRAM chips.

![vram-back](/img/2619.7.0343.png)

### Remove pads liner ⚠️

Make sure it's all peeled before the next step.

### Reattach backplate 🔩

Tighten evenly.

### Apply front VRAM pads 📐

Place on all 12 front VRAM chips + small Junction at the top (near white fan header).

![vram-front](/img/2619.7.0344.png)

### Cut PTM7950 ✂️

Aim for an exact 26mm x 24mm rectangle (slightly larger rather than smaller).

![Cut PTM7950 1](/img/2619.7.0410.png) | ![Cut PTM7950 2](2619.7.0411.png)
---|---

### Apply PTM7950 on GPU die 📐

![apply-PTM7950-1](/img/2619.7.0402.png) | ![apply-PTM7950-2](/img/2619.7.0402_2.png) | ![apply-PTM7950-3](/img/2619.7.0402_1.png)
---|---|---
![apply-PTM7950-4](/img/2619.7.0405.png) | ![apply-PTM7950-7](/img/2619.7.0414.png) | ![apply-PTM7950-6](/img/2619.7.0408.png)

### Consider deshrouding now ❔

- If that makes it easier, do it.
- Otherwise, do it after reattaching cooler.  

See instructions in deshroud kit.

### Remove liners ⚠️

On VRAM thermal pads and GPU die.

### Reattach cooler 🔩

- Make sure all plugs are connected.  

    ![plugs](/img/2619.7.0345.png)

- **Place washers**: one nylon washer goes **on the PCB, through the backplate** at each of the 4 screw holes that hold the PCB to the heatsink core.  
This lets screws not bottom out before applying target clamping pressure (30~40 psi).

- **Torque screws evenly in cross-pattern**. Do not overtighten.

    ![cooler-reattach](/img/2619.7.0346.png)

### Install deshroud mod 🔩

0. Deshroud now if not done yet: remove all the plastic covering the heatsink (6 screws, through fans?)

1. Install brackets

    ![deshroud-brackets](/img/il_1588xN.4188462840_k70j.webp)

2. Install fans

    ![deshroud-fans](/img/il_1588xN.4236126167_i9tr.webp)

3. Install cover

    ![deshroud-cover](/img/il_1588xN.4236126215_1c7k.webp)

### Mount backplate heatsinks 📐

- Remove 3M tape liner on the bottom of 40x40mm heatsinks.
- Place them in 2x2 grid on backplate over VRAM area.
- Press firmly.
- Let cure 24 hours.

### Mount backplate fan 🪢

- Adhere fan to top of heatsinks with thermal-resistant tape or zip ties.  
- Wire to outstanding white fan header on GPU (sync with front GPU fans).

### Test 🎛️

- burn it!
- monitor temps
- expect performance to be worse at first, then get better in time for the PTM7950.

## 🧭 Resources

### 📺 RTX 3090 Zotac Trinity

[![Repasting RTX 3090 Zotac Trinity](https://img.youtube.com/vi/VjZfqd2q-iE/maxresdefault.jpg)](https://www.youtube.com/watch?v=VjZfqd2q-iE)   

### 🔗 Honeywell PTM7950

[How to apply **Honeywell PTM7950**?](https://help.moddiy.com/en/article/how-to-apply-honeywell-ptm7950-bm6825/)

### 📄 Fehonda Thermal Pad

[ZOTAC GAMING GeForce RTX 3090 **Trinity OC: VRAM Thermal Pad Guide** (2mm Front, 3mm Back)](https://www.fehonda.com/3090/zotac-gaming-geforce-rtx-3090-trinity-oc)

## ✅ Expected Results

| Metric | Before (stock) | After (modded) |
|---|---|---|
| GPU core temp | 72-78°C | 65-72°C |
| GPU hotspot | 85-95°C | 75-85°C |
| VRAM junction | 104-110°C | **78-92°C** |

---

# Appendix

## VRAM Thermal Pad Height per brand/SKU

> src: https://search.brave.com/search?q=thermal+pads+height+for+rtx+3090+front+and+back&conversation=09100d530fc9b9e982e22c56903df607bbe7&summary=1

Thermal pad thickness for the NVIDIA RTX 3090 varies significantly by manufacturer model, with the **Founders Edition** being the most standardized.

### NVIDIA GeForce RTX 3090 Founders Edition
*   **Front and Back:** **1.5mm** thickness is used uniformly for all VRAM and component pads on both sides.
*   **Configuration:** Requires three pieces of **80x40x1.5mm** (or 85x45x1.5mm) pads to cover the front and back.

### Third-Party Models (Custom Thicknesses Required)
For non-FE cards, you must measure specific components, but general guidelines for popular models include:

*   **GIGABYTE Gaming OC 24G:**
    *   Front VRAM: **2mm**
    *   Back VRAM: **2mm** or **2.5mm** (check gap)
    *   Side Pads (VRMs/MOSFETs): Mix of **1mm** and **1.5mm**
    *   Large Back Pad: **3mm** (50x30mm)

*   **ZOTAC Trinity OC:**
    *   Front VRAM: **2mm**
    *   Back VRAM: **3mm**

*   **ASUS ROG Strix:**
    *   Front/Back VRAM: **2mm** (80x40mm)
    *   Side Pads: Mix of **0.5mm**, **1mm**, and **2.5mm** stripes.

*   **MSI Gaming Trio X:**
    *   Front VRAM: **1.0mm**
    *   Back VRAM: **1.5mm** or **2.5mm** (users often stack 1.5mm + 1.0mm to achieve 2.5mm)

**Important Note:** For all non-FE models, individual VRAM pads must be **custom-cut** to the exact length and width of the memory chips after disassembly. Always verify the gap between the component and the heatsink/backplate to ensure the correct thickness, as using pads that are too thick can cause poor contact, while pads that are too thin will not transfer heat effectively.
