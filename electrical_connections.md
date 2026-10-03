# Brain2 AI Pendant - Complete Electrical Connections & Pinout Guide

## 1. Power Distribution Flow

```
[ 800mAh LiPo Battery (3.7V) ]
            │
            ▼
[ TP4056 USB-C Charger (BAT+ / BAT-) ]
            │
    (ON/OFF Slide Switch) ──> Intercepts positive rail between battery/charger and booster
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

---

## 2. Deck-by-Deck Wiring Pinout

### Deck 1: Starboard 1 (Front Deck — Mic + SD Card + Controls)

#### 1. INMP441 I2S MEMS Microphone (Upper-Side Placement)
| INMP441 Pin | ESP32-S3 Pin | Function / Description |
| :--- | :--- | :--- |
| **VDD** | **3V3** | 3.3V Clean logic power from ESP32 |
| **GND** | **GND** | System Ground |
| **SD** | **GPIO 32** | I2S Serial Data input |
| **WS (LRCLK)**| **GPIO 15** | Word Select (Left/Right clock) |
| **SCK (BCLK)**| **GPIO 14** | Bit Clock |
| **L/R** | **GND** | Left channel select |

#### 2. MicroSD Card Adapter (SPI Bus)
| MicroSD Pin | ESP32-S3 Pin | Function / Description |
| :--- | :--- | :--- |
| **VCC** | **5V Bus** | Powered from regulated 5.0V bus |
| **GND** | **GND** | Common Ground |
| **CS** | **GPIO 5** | Chip Select |
| **SCK** | **GPIO 18** | SPI Clock |
| **MOSI** | **GPIO 23** | SPI Master Out Slave In |
| **MISO** | **GPIO 19** | SPI Master In Slave Out |

#### 3. Front Controls (Two Buttons + Blue LED)
| Control | Connection 1 | Connection 2 | Notes |
| :--- | :--- | :--- | :--- |
| **Indicator Blue LED** | **GPIO 2** via **220Ω** resistor | **GND** | Illuminates when recording; idle heartbeat when standby |
| **Push Button** | **GPIO 0** (or GPIO 34) | **GND** | Momentary tactile switch with ESP32 internal pullup |
| **ON/OFF Slide Switch** | **TP4056 OUT+** | **MT3608 IN+** | Physical latching slide switch breaks the 3.7V battery circuit to turn the entire pendant ON and OFF |

---

### Deck 2: Starboard 2 (Middle Deck — ESP32-S3 DevKit)
- Centrally mounted with dual socket headers.
- **Top side**: Connects SPI bus, I2S bus, Button signal, and LED signal upward to Starboard 1.
- **Bottom side**: Receives +5V regulated power and GND upward from Starboard 3.

---

### Deck 3: Starboard 3 (Bottom Deck — Power Subsystem)
- **Battery**: Red wire (+) to TP4056 `B+`, Black wire (-) to TP4056 `B-`.
- **TP4056**:
  - `OUT+` routes to the **ON/OFF Slide Switch** on Deck 1.
  - `OUT-` connects directly to MT3608 `IN-` and common system ground.
- **MT3608 Boost Converter**:
  - `IN+`: Returns from the ON/OFF slide switch.
  - `OUT+`: Regulated **+5.00V DC** (preset with precision multi-turn trimmer screw before assembly).
  - `OUT-`: System ground bus.
