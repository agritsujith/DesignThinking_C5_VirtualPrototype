# DesignThinking_C5_VirtualPrototype

Concept - Landowner's Snapshot Rig: Corporate & Absentee Landowner

**Prompt Used:**
Act as a Senior Mechatronics & Creative Front-End Engineer. Create a complete, self-contained interactive 3D virtual prototype of "Concept 5: Absentee Landowner's Snapshot Rig" as a single-file HTML Artifact using Three.js (via CDN) and Tailwind CSS / vanilla CSS.

### 1. CONCEPT SPECIFICATIONS (C5: Corporate & Absentee Landowner Rig)
Model the physical hardware assembly based on these engineering choices:
- Actuation: Gear Motor Drive mounted with an adjustable clamping bracket onto a standard 1.5-inch agricultural pipe and valve lever.
- Power: Off-Grid Solar Unit (tilted photovoltaic panel bracketed to the pole/top of enclosure, micro battery pack, deep sleep power logic).
- Imaging: Integrated ESP32-CAM module with an optical lens port, simulated flash LED, and protective optical window.
- Enclosure: Rugged IP67 weatherproof enclosure (flanged lid, sealing gasket aesthetic, cable glands).
- Telemetry & Connectivity: External high-gain GSM whip antenna mounted to the enclosure top.
- Safety & Protection: Current-sensing stall protection circuit (visualized via a status LED on the PCB/chassis).
- Agronomic Sensing: Probe cabling leading down from the box to a soil sensor assembly.

### 2. 3D SCENE & MODELING REQUIREMENTS (Three.js)
Generate procedural 3D meshes with clean materials (use MeshStandardMaterial with metallic/roughness properties):
- Mounting Pole / Framework: Vertical field pole/post mounting the whole system.
- Enclosure Box: Industrial enclosure (grey/matte finish) with a transparent front bezel revealing internal PCB, ESP32-CAM module, and terminal blocks.
- Camera Sub-Assembly: Lens barrel and LED ring facing outward/downward towards the valve and crop bed.
- Gear Motor Retrofit Assembly: High-torque DC gear motor in a cylindrical/cuboid gearbox housing, connected via a coupler and pivoting clamp arm to a red valve handle.
- Solar Bracket: Monocrystalline-style mini solar panel mounted at a 30–45 degree tilt angle on an adjustable aluminum bracket.
- Antenna: Cylindrical GSM antenna base with a thin black whip antenna extending upward.
- Pipe & Valve: Gray PVC / brass valve body passing under the actuator arm.
- Environment: Minimalist outdoor farm ground plane with subtle ambient lighting, directional sun shadow caster, and orbit grid.

### 3. INTERACTIVE VIRTUAL PROTOTYPE CONTROLS (HUD / UI Overlay)
Provide a modern floating corporate dashboard overlay ("Absentee Landowner 60-Second Snapshot") with interactive controls:
1. "Trigger ESP32-CAM Snapshot":
   - Animates a camera shutter flash on the 3D rig.
   - Captures an instant simulated photo preview in a pop-up viewport with a simulated timestamp, GPS stamp, and optical clarity verification badge.
2. "Actuate Valve (Open / Close)":
   - Animates the gear motor drive turning the mechanical clamp arm 90 degrees smoothly.
   - Includes real-time current readout showing normal torque vs. "Stall Protection Active" status.
3. "Deep Sleep / Wake Cycle":
   - Toggles low-power mode, dims LEDs, displays simulated battery state of charge (SoC) and solar input wattage.
4. "Exploded / Inspect View":
   - Smoothly tweens enclosure cover and components outward so the interior ESP32-CAM and relay/sensing board are inspectable.
5. Camera View Presets:
   - Quick buttons: "Overall Rig", "ESP32-CAM Close-Up", "Gear Motor & Valve Clamp", and "Corporate Landowner Telemetry View".

### 4. IMPLEMENTATION CONSTRAINTS
- Single, self-contained HTML file inside a single code artifact.
- Include Three.js and OrbitControls via reliable cdnjs / unpkg script tags.
- Provide smooth OrbitControls (rotate, pan, zoom) with damping.
- Responsive layout with zero external CSS/JS dependencies beyond standard CDNs.
- Complete working code with no placeholders or truncated sections.
