# Brain2 AI Pendant - Cardboard Cutting Template (3-Starboard Stack)

> All dimensions in **millimeters (mm)**.  
> **Shape: OCTAGONAL** (Rectangle with 45° chamfered corners).  
> Material: Heavy Craft / Corrugated Cardboard (**2.0 mm thickness**).

---

## 1. Outer Dimensions & Blueprint Summary

| Parameter | Exact Size | Notes |
| :--- | :--- | :--- |
| **Enclosure Width ($X$)** | **62.0 mm** | Outer width |
| **Enclosure Height ($Y$)** | **90.0 mm** | Outer height |
| **Enclosure Depth ($Z$)** | **38.0 mm** | Total depth (Back cover to Front cover) |
| **Corner Chamfers** | **8.0 mm** | Cut 8 mm × 8 mm at 45° off each of the 4 corners |
| **Cardboard Thickness** | **2.0 mm** | Standard rigid cardboard |
| **Internal Starboard Size**| **54.0 × 82.0 mm** | Green FR4 perfboard plates (3 identical pieces) |

```
              8 mm chamfer
             |<--->|
         +-----------+---------------------+-----------+
         |  /                                     \  |
         | /                                       \ |  8 mm chamfer
         |/         [ UPPER-SIDE MIC HOLE ]         \|
         |          Ø1.8 mm (X=14, Y=74)             |
         |                                           |
         |             [ 5mm BLUE LED ]              |
         |             Ø5.0 mm (X=31, Y=72)          |
         |                                           |
 90 mm   |                                           |
 Height  |         [ ROUND PUSH BUTTON ]             |
         |         Ø7.0 mm (X=31, Y=46)              |
         |                                           |
         |                                           |
         |        [ ON/OFF SLIDE SWITCH ]            |
         |        8.5 × 4.0 mm (X=31, Y=24)          |
         |                                           |
         |\                                         /|
         | \                                       / |
         |  \                                     /  |
         +-----------+---------------------+-----------+
                     |<------ 62.0 mm ------>|
```

---

## 2. Piece-by-Piece Cutting Instructions

### Piece 1: Front Cardboard Faceplate (Quantity: 1)
- **Outer Size**: $62.0\text{ mm (Width)} \times 90.0\text{ mm (Height)} \times 2.0\text{ mm (Thick)}$.
- **Chamfers**: Mark $8\text{ mm}$ from each corner and cut off the 4 corner triangles at $45^\circ$.
- **Precision Front Cutouts (Measured from bottom-left corner at $X=0, Y=0$)**:
  1. **Upper-Side Microphone Acoustic Pinhole**:
     - Hole diameter: $\varnothing 1.8\text{ mm}$
     - Position: $X = 14.0\text{ mm}$, $Y = 74.0\text{ mm}$ (Upper-left shoulder)
  2. **5mm Blue Indicator LED Hole**:
     - Hole diameter: $\varnothing 5.0\text{ mm}$
     - Position: $X = 31.0\text{ mm}$ (center), $Y = 72.0\text{ mm}$
  3. **Round Push Button Switch Hole**:
     - Hole diameter: $\varnothing 7.0\text{ mm}$
     - Position: $X = 31.0\text{ mm}$ (center), $Y = 46.0\text{ mm}$
  4. **ON/OFF Power Slide Switch Slot**:
     - Slot dimensions: $8.5\text{ mm (Length)} \times 4.0\text{ mm (Width)}$
     - Position: Centered at $X = 31.0\text{ mm}$, $Y = 24.0\text{ mm}$
     - Mark "ON" on the right and "OFF" on the left with a fine-tip pen.

---

### Piece 2: Perimeter Side Wall Strip (Quantity: 1)
- **Dimensions**: Length $= 284\text{ mm}$, Width $= 34.0\text{ mm}$, Thickness $= 2.0\text{ mm}$.
- **Fold Segments (Creased every face of the octagon)**:
  - Bottom edge: $46.0\text{ mm}$
  - Bottom-right chamfer: $11.3\text{ mm}$
  - Right edge: $74.0\text{ mm}$ (Houses dual cutouts!)
  - Top-right chamfer: $11.3\text{ mm}$
  - Top edge: $46.0\text{ mm}$
  - Top-left chamfer: $11.3\text{ mm}$
  - Left edge: $74.0\text{ mm}$
  - Bottom-left chamfer: $11.3\text{ mm}$
- **Right Edge Side Cutouts**:
  1. **TP4056 USB-C Charging Port**:
     - Cutout size: $11.0\text{ mm} \times 6.5\text{ mm}$
     - Location: Centered $18.0\text{ mm}$ from bottom edge, aligned with Starboard 3 ($Z \approx 4\text{ mm}$).
  2. **MicroSD Card Insertion Slot**:
     - Cutout size: $14.0\text{ mm} \times 6.5\text{ mm}$
     - Location: Centered $48.0\text{ mm}$ from bottom edge, aligned with Starboard 1 ($Z \approx 28\text{ mm}$).

---

### Piece 3: Back Cardboard Cover (Quantity: 1)
- **Outer Size**: $62.0\text{ mm (Width)} \times 90.0\text{ mm (Height)} \times 2.0\text{ mm (Thick)}$.
- **Chamfers**: Cut $8\text{ mm}$ off each of the 4 corners at $45^\circ$.
- **Lanyard Cord Holes**:
  - Drill two $\varnothing 3.5\text{ mm}$ holes at the top edge, spaced $16.0\text{ mm}$ apart ($X = 23\text{ mm}$ and $X = 39\text{ mm}$, $Y = 84\text{ mm}$).
  - Thread the neckband lanyard cord through and secure with a small cardboard backing clamp.

---

## 3. Starboard (FR4 Perfboard) Cutting Dimensions (Quantity: 3)
Cut 3 identical perfboard plates:
- **Size**: **$54.0\text{ mm (Width)} \times 82.0\text{ mm (Height)} \times 1.6\text{ mm (Thickness)}$**
- **Corner Trim**: Nip $6\text{ mm}$ off each corner so the board fits snugly inside the octagonal perimeter.
- **Corner Mounting Holes**: Drill four $\varnothing 2.5\text{ mm}$ holes in the corners ($4\text{ mm}$ inset from edges) to accept M2/M2.5 brass standoffs.
