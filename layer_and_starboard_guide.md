# Brain2 AI Pendant - Dual Front Controls & 3-Starboard Architecture Guide

## 1. Front Controls & Acoustic Openings

The front side of the pendant now features all requested controls and sound ports:

| Front Element | Component Type | Coordinates / Location | Function & Wiring |
| :--- | :--- | :--- | :--- |
| **1. Indicator LED** | 5mm Blue Through-Hole LED | Upper Center ($Y=72\text{ mm}$) | Connected to ESP32 GPIO 2 via $220\,\Omega$ resistor. Shows Power ON, Recording, Wi-Fi. |
| **2. Push Button** | Round Tactile Push Button | Mid Center ($Y=46\text{ mm}$) | Connected to ESP32 GPIO 0 with internal pullup. Used for Voice Recording trigger / AI interaction. |
| **3. ON/OFF Power Switch** | Miniature Slide Switch | Lower Center ($Y=24\text{ mm}$) | Cuts power between Li-Po battery and MT3608 Boost Converter. Slides between ON and OFF positions. |
| **4. Upper MEMS Mic** | INMP441 I2S Microphone | Top-Left Shoulder ($Y=74\text{ mm}$) | Positioned on the upper side facing user's mouth with a $\varnothing 1.8\text{ mm}$ acoustic front pinhole. |

---

## 2. 3-Starboard Stacked Layer-by-Layer Placement

```
┌────────────────────────────────────────────────────────┐
│  PLATE 1: FRONT CARDBOARD FACEPLATE (2.0 mm)           │
│  - Precision cutouts for:                              │
│    1. Blue LED dome (Ø5.0 mm)                          │
│    2. Round Push Button cap (Ø7.0 mm)                  │
│    3. ON/OFF Slide Switch rectangular slot (8.5×4 mm) │
│    4. Upper Microphone sound pinhole (Ø1.8 mm)         │
└────────────────────────────────────────────────────────┘
                           │
┌────────────────────────────────────────────────────────┐
│  PLATE 2: STARBOARD 1 (FRONT DECK: MIC + SD + CONTROLS)│
│  - INMP441 MEMS Mic on UPPER SIDE facing front hole    │
│  - MicroSD Card Adapter (50 × 25 × 10 mm) on side edge │
│  - 5mm Blue LED + 220Ω resistor                        │
│  - Round Push Button Switch (Tactile momentary)        │
│  - ON/OFF Power Slide Switch (Latching power break)    │
└────────────────────────────────────────────────────────┘
                           │  (8.4 mm Brass Standoffs)
┌────────────────────────────────────────────────────────┐
│  PLATE 3: STARBOARD 2 (MIDDLE DECK: ESP32-S3 CORE)     │
│  - ESP32-S3 DevKit (70 × 39 × 10 mm) centered         │
│  - Dual header pin rows connecting signals to Deck 1   │
│    and regulated 5V power bus to Deck 3                │
└────────────────────────────────────────────────────────┘
                           │  (8.4 mm Brass Standoffs)
┌────────────────────────────────────────────────────────┐
│  PLATE 4: STARBOARD 3 (BOTTOM DECK: POWER SUBSYSTEM)   │
│  - MT3608 5V Step-Up Boost Converter (45 × 23 × 15 mm) │
│  - TP4056 Battery Charger (30 × 18 × 3 mm) with USB-C  │
│  - 800mAh 3.7V Li-Po Battery (37 × 25 × 5 mm)          │
└────────────────────────────────────────────────────────┘
                           │
┌────────────────────────────────────────────────────────┐
│  PLATE 5: OCTAGONAL RIM (34 mm) & BACK COVER (2.0 mm)  │
│  - Dual side cutouts: USB-C charging + MicroSD slot   │
│  - Top strain relief bracket + Neck lanyard cord       │
└────────────────────────────────────────────────────────┘
```

---

## 3. How to Use the 3D Viewer

1. Open your Desktop folder: `C:\Users\Atul Kumar\Desktop\brain2-pendant-cad`
2. Double-click **`ai_pendant_3d_viewer.html`** (or view the already opened browser window).
3. **Interactive Front Controls Testing**:
   - **Flip the ON/OFF Switch**: 
     - Slide to **OFF**: Circuit breaks! The Blue LED turns off, and the push button is disabled.
     - Slide to **ON**: Circuit energizes! The Blue LED illuminates, and the system is ready.
   - **Press the Push Button**:
     - While ON, click **Press Button**: The physical button in 3D depresses, and the Blue LED dome brightens and pulses with sound waves to indicate audio recording to the MicroSD card!
   - **Layer Explosion Slider**:
     - Drag the vertical slider to pull Starboard 1, Starboard 2, Starboard 3, and Cardboard covers apart in mid-air.
