# Brain2 AI Pendant - 3D Interactive Web Viewer & CAD Architecture

An interactive, high-fidelity 3D web viewer and parametric CAD assembly model for the **Brain2 Wearable AI Pendant** prototype built with an octagonal cardboard enclosure and a 3-tier Starboard (perfboard) stacked core.

🌐 **Live 3D Web Viewer**: [https://akcodes-py.github.io/ai_pendant_3d_view/](https://akcodes-py.github.io/ai_pendant_3d_view/)  
📁 **Local File**: Open [`ai_pendant_3d_viewer.html`](ai_pendant_3d_viewer.html) or [`index.html`](index.html) in any browser.

---

## 🌟 Key Features

- **Realistic Electronic Component Rendering**:
  - **ESP32-S3 DevKit**: Rendered with dark PCB traces, gold header pins, silver metal RF shield, micro-USB connector, and silkscreen markings.
  - **INMP441 I2S MEMS Microphone**: Purple PCB with golden circular acoustic MEMS port positioned on the **upper side** facing the front sound pinhole for crystal-clear voice pickup.
  - **MicroSD Card Adapter**: Deep blue PCB, stainless-steel push-push card socket, and partially inserted microSD card facing the side cutout for easy card swapping.
  - **MT3608 5V Step-Up Boost Converter**: Rendered with copper toroidal ferrite inductor coil and precision multi-turn trimmer potentiometer.
  - **TP4056 Battery Charger**: Blue PCB with USB-C connector facing the side wall cutout.
  - **800mAh Li-Po Battery**: Silver metallic vacuum-sealed pouch cell with yellow Kapton insulation tape and silicone power lead wires.
  - **Starboard Perfboards**: Double-sided gold donut solder pads at standard $2.54\text{ mm}$ pitch.
- **Dual Front Controls & Indicator**:
  1. **5mm Blue Indicator LED**: Located at upper-center ($Y=72\text{ mm}$).
  2. **Round Push Button Switch**: Located at mid-center ($Y=46\text{ mm}$) for thumb voice recording trigger.
  3. **ON/OFF Power Slide Switch**: Located at lower-center ($Y=24\text{ mm}$) to disconnect battery power.
  4. **Upper-Side Microphone Sound Pinhole**: Located on the top-left shoulder ($Y=74\text{ mm}$) with golden bezel ring.
- **Interactive Controls Simulator**:
  - **Toggle ON/OFF Switch**: Sliding to OFF cuts circuit power and dims the LED; sliding to ON energizes the system.
  - **Press Push Button**: Depresses the 3D button and activates **`RECORDING AUDIO`** mode with a pulsing Blue LED.
- **Vertical Layer Explosion Slider**:
  - Drag the slider from $0\text{ mm}$ (fully assembled) to $75\text{ mm}$ (exploded view) to pull apart all 3 Starboard decks and cardboard covers in mid-air.
- **Layer Isolation Filtering**:
  - Isolate and inspect any individual plate or starboard deck with zero clutter.

---

## 📐 Measured Component Dimensions (Hand Scale)

| Component Name | Length (cm) | Breadth (cm) | Height (cm) | Converted ($L \times W \times H$) | Stack Deck |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **INMP441 MEMS Mic** | 1.4 | 1.1 | 0.35 | **$14 \times 11 \times 3.5\text{ mm}$** | **Deck 1 (Top / Front)** |
| **MicroSD Card Adapter** | 5.0 | 2.5 | 1.0 | **$50 \times 25 \times 10\text{ mm}$** | **Deck 1 (Top / Front)** |
| **ESP32-S3 DevKit** | 7.0 | 3.9 | 1.0 | **$70 \times 39 \times 10\text{ mm}$** | **Deck 2 (Middle)** |
| **Boost Converter (3V→5V)** | 4.5 | 2.3 | 1.5 | **$45 \times 23 \times 15\text{ mm}$** | **Deck 3 (Bottom / Power)** |
| **TP4056 Battery Charger** | 3.0 | 1.8 | 0.3 | **$30 \times 18 \times 3\text{ mm}$** | **Deck 3 (Bottom / Power)** |
| **800mAh Li-Po Battery** | 3.7 | 2.5 | 0.5 | **$37 \times 25 \times 5\text{ mm}$** | **Deck 3 (Bottom / Power)** |
| **Front Controls** | — | — | — | **$\varnothing 5\text{mm}$ LED, $\varnothing 7\text{mm}$ Button** | **Front Faceplate** |

---

## 🏗️ 3-Starboard Stack Architecture

```
┌────────────────────────────────────────────────────────┐
│  PLATE 1: FRONT CARDBOARD FACEPLATE (2.0 mm)           │
│  - Hole 1: 5mm Blue LED Dome (Ø5.0 mm at Y=72)         │
│  - Hole 2: Round Push Button Cap (Ø7.0 mm at Y=46)     │
│  - Hole 3: ON/OFF Slide Switch Slot (8.5×4 mm at Y=24) │
│  - Hole 4: Upper-Side Mic Sound Pinhole (Ø1.8 mm)      │
└────────────────────────────────────────────────────────┘
                           │
┌────────────────────────────────────────────────────────┐
│  PLATE 2: STARBOARD 1 (FRONT DECK: MIC + SD + CONTROLS)│
│  - INMP441 MEMS Mic on UPPER SIDE facing front hole    │
│  - MicroSD Card Adapter (50 × 25 × 10 mm) on side edge │
│  - 5mm Blue LED + Round Push Button + ON/OFF Switch    │
└────────────────────────────────────────────────────────┘
                           │  (8.4 mm Brass Standoffs)
┌────────────────────────────────────────────────────────┐
│  PLATE 3: STARBOARD 2 (MIDDLE DECK: ESP32-S3 CORE)     │
│  - ESP32-S3 DevKit (70 × 39 × 10 mm) centered         │
│  - Connects logic lines up to Deck 1 & power to Deck 3 │
└────────────────────────────────────────────────────────┘
                           │  (8.4 mm Brass Standoffs)
┌────────────────────────────────────────────────────────┐
│  PLATE 4: STARBOARD 3 (BOTTOM DECK: POWER SUBSYSTEM)   │
│  - MT3608 5V Step-Up Boost Converter (45 × 23 × 15 mm) │
│  - TP4056 Battery Charger (30 × 18 × 3 mm) with USB-C  │
│  - Li-Po 800mAh 3.7V Battery (37 × 25 × 5 mm)          │
└────────────────────────────────────────────────────────┘
                           │
┌────────────────────────────────────────────────────────┐
│  PLATE 5: OCTAGONAL RIM (34 mm) & BACK COVER (2.0 mm)  │
│  - Dual side cutouts: USB-C charging + MicroSD slot   │
│  - Top strain relief bracket + Neck lanyard cord       │
└────────────────────────────────────────────────────────┘
```

---

## ⚡ Electrical Connections & Pinout

```
[ 800mAh Li-Po Battery (3.7V) ]
            │
            ▼
[ TP4056 USB-C Charger (BAT+ / BAT-) ]
            │
    (ON/OFF Slide Switch) ──> Intercepts positive rail
            │
            ▼
[ MT3608 DC-DC Step-Up Converter (IN+ / IN-) ]
    • Input: 3.7V - 4.2V DC
    • Trimmed Output: Exactly 5.0V DC (OUT+ / OUT-)
            │
            ▼
[ Main 5.0V & GND Power Bus on Starboards ]
    ├──> ESP32 DevKit 5V Pin (Internal 3.3V LDO powers ESP32 core)
    ├──> MicroSD Card Adapter VCC (5V)
    ├──> INMP441 MEMS Mic VDD (3.3V pin from ESP32)
    └──> 5mm Blue LED (Anode to GPIO 2 via 220Ω, Cathode to GND)
```

| Component | Pin | ESP32-S3 Pin | Function |
| :--- | :--- | :--- | :--- |
| **INMP441 MEMS Mic** | VDD | 3V3 | 3.3V Clean Power |
| | GND | GND | System Ground |
| | SD | GPIO 32 | I2S Serial Data |
| | WS | GPIO 15 | Word Select (Clock) |
| | SCK | GPIO 14 | Bit Clock |
| **MicroSD Module** | VCC | 5V Bus | 5V Regulated Power |
| | GND | GND | Common Ground |
| | CS | GPIO 5 | SPI Chip Select |
| | SCK | GPIO 18 | SPI Clock |
| | MOSI | GPIO 23 | SPI Master Out |
| | MISO | GPIO 19 | SPI Master In |
| **Controls** | Push Button | GPIO 0 | Voice / Trigger (Internal Pull-Up) |
| | Blue LED | GPIO 2 | Recording indicator (via 220Ω) |
| | ON/OFF Switch | TP4056 OUT+ | Physical battery power cut |

---

## 🚀 How to Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/akcodes-py/ai_pendant_3d_view.git
   cd ai_pendant_3d_view
   ```
2. Open [`index.html`](index.html) or [`ai_pendant_3d_viewer.html`](ai_pendant_3d_viewer.html) in any modern browser (Chrome, Edge, Firefox, Safari). No installation or build steps required.

---

## 📄 License
MIT License. Created for the Brain2 Wearable AI Pendant prototype project.
