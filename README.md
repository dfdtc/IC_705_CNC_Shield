## Other languages
- zh_CN [简体中文](README.zh_CN.md)

## Project Overview

This project provides a set of optional features, is highly extensible, and offers a cost‑effective model for an ICOM IC‑705 device shield kit.

---

## Repository & File Structure

This project contains many derived model files, along with some reference models. Therefore: **Please do not simply send the whole folder to a fabrication shop; otherwise you will receive several sets of shields with different configurations and the manufacturing cost will be extremely high.**

### Path Structure

#### Accessories

```
Accessories
```

This folder contains some custom machining accessories as well as modeled standard parts for commercial use (e.g., 4020 aluminum angle code). Purchase or place orders for CNC machining as needed.

#### Machined Parts

```
BasePlate
TopPlate
Handle
```

These files all require CNC machining; order according to the BOM quantities.

#### Aluminum Profile Supports

```
SupportColumn-支撑柱
```

This folder contains model files for aluminum profile supports. They are provided only as references and should not be sent to a CNC or 3D printer.

#### Assembly Explosions & Reference Finished Models

```
AssembleReference
```

This folder contains assembly exploded views and finished product models. They are for reference only and should not be sent to a CNC or 3D printer.

### Naming Convention

Additional features of the derived models are distinguished by suffixes separated with an underscore “_”, e.g.:

- `"底板_开快装板螺纹底孔"` = ordinary base plate + flat-head screw holes + standard tripod quick‑mount threaded bottom holes
- `"底板_开快装板螺纹底孔_沉头_自立"` = self‑standing base plate + countersunk screw holes + standard tripod quick‑mount threaded bottom holes

## Part Machining Recommendations

### 1. Fabrication Notes

#### 1.1  
Because some outsourcing factories provide free edge chamfering / deburring (e.g., CNC-AiCNC-Ai), the top and bottom plate models have no edge chamfers. Pay attention to whether your chosen factory offers this service.

#### 1.2  
The handle model is provided in both un‑chamfered & non‑countersunk versions, as well as chamfered & countersunk variants.

#### 1.3  
Two screw designs are included: tapered countersink and no‑countersink (suitable for cup heads or flat-head screws). Countersunk designs look cleaner but cost a bit more; the no‑countersink version is cheaper but leaves a protruding screw head cap.

#### 1.4  
CNC shops usually offer anodizing and painting, but off‑the‑shelf aluminum profiles may not be available in all colors (see section 2.3). Configure surface treatment options yourself.

#### 1.5  
The handle model is thick and contains a large “c”‑shaped chamfer; CNC machining time can be long. If cost is an issue, consider 3D printing—strength requirements are fully met.

#### 1.6  
The top plate has M4 holes for fixing the finished Picatinny rails (3/7/11 slots). It’s recommended to thread these yourself during fabrication.

#### 1.7  
Because the base plate is thick, tripod screws cannot directly lock into pre‑machined threaded holes on the machine. Therefore, the base plate offers two configurations: `"开快装板螺纹底孔"` and `"脚架位避让"`.  
- The former already has a 1/4‑20 bottom hole; if your factory supports imperial threading, you can let them thread it, or take the semi‑finished part back to finish it yourself.  
- The latter opens a circular cutout (3.2 cm diameter) at the original tripod screw position, allowing some round mounting brackets to fit into this cutout.

### 2. Aluminum Profile Supports

#### 2.1  
The “EU‑standard 1020 rail” and “EU‑standard 1040 rail” models in the package are only references; do not send them for CNC machining. Find a Taobao shop that cuts 85–88 mm long profiles (the original design is 84.7 mm, so 86/87 mm is recommended to account for machining tolerance and part clearance). Drill holes: M5 on the 1020 rail, M4 on the 1040 rail.

#### 2.2  
Four 1020 rails are required; one 1040 rail is optional and provides extra mounting points and structural support.

#### 2.3  
Commercially available aluminum rails are usually anodized in natural color (some sellers offer black EU‑standard 1020 rails, but not yet for 1040). If you want uniform color, paint as needed, or ask the shop that supplies the profile to provide anodizing/coloring services.

### 3. Installation Notes

#### 3.1  
Because the IC‑705 body bottom is not level, the base plate must have at least a 1.5–2 mm rubber pad around each of the four mounting holes, or use similar thickness rubber washers to achieve sufficient clearance. Otherwise, tightening the mounting screws will impose stress on the machine and the base plate.

### 4. Custom Reference Assembly

#### Derived Model Combination

```
"底板_脚架位避让_沉头_自立" + "顶板_沉头_自立" + "手握_倒角_沉头"
```

#### Factory Choices

- Base/Top Plate: CNC-Ai
- Handle: JLC-CNC (Note: You can also choose CNC-Ai)  
- Antenna Bracket: JLC Sheet Metal  
- Vertical Column: Any Taobao/AliExpress vendor

**Manufacturing Cost (In China, Unit:CNY)**

| Item | Unit Price | Qty | Total |
|---|---|---|---|
| Top Plate | 43 ¥ | 1 | 43 ¥ |
| Bottom Plate | 43 ¥ | 1 | 43 ¥ |
| Handle | 11 ¥ | 2 | 22 ¥ |
| 1020 aluminum post (incl. machining) | 5.3 ¥ | 4 | 21.2 ¥ |
| 1040 aluminum post (incl. machining) | 5.3 ¥ | 1 | 5.3 ¥ |
| Rubber pad | 8 ¥ | 1 | 8 ¥ |
| Fasteners | – | – | ≈30 ¥ |
| Support foot | 12 ¥ | 1 | 12 ¥ |
| **Total** |   |   | **≈180 ¥** |

#### Tips

I have also 3D‑printed an engineering prototype myself, but I do **not** recommend using 3D printing for this project. The design is optimized for metal CNC; if you wish to use 3D printing, consider other open‑source 3D‑printable shield projects.

---