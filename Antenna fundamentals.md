# Fresnel Zone Fundamentals

##  Overview
When a radio wave travels between two antennas, it doesn’t only move in a straight line. Instead, it spreads into an **elliptical region** called the **Fresnel zone**. This zone determines how much clearance is needed for reliable wireless communication.

![Fresnel Zone](Network/Screenshot%202025-08-11%20at%208.49.04%20AM.png "Fresnel Zone")


The **1st Fresnel zone** is the most critical — obstructions inside it can cause diffraction and signal loss, even if there’s visual line-of-sight (LOS).

---

##  Why It Matters
- **Signal Quality**: Obstacles in the Fresnel zone cause reflections and diffraction.
- **Loss Prevention**: More than ~40% blockage of the 1st zone radius can cause noticeable attenuation.
- **Design Goal**: Keep **at least 60% of the 1st Fresnel zone radius** clear.

---

##  Shape & Geometry
- **Cross-section**: Circle  
- **Overall shape**: Ellipsoid between antennas  
- **Size**: Narrowest near antennas, widest at the midpoint

---

##  Fresnel Zone Radius Formula

General form for the n-th Fresnel zone:
Fₙ = √[ (n × λ × d₁ × d₂) / (d₁ + d₂) ]


Where:
- `Fₙ` = radius of the n-th Fresnel zone (meters)
- `n` = zone number (1 for the 1st zone)
- `λ` = wavelength (meters)
- `d₁` = distance from the point to one antenna (meters)
- `d₂` = distance from the point to the other antenna (meters)

---

**Engineering form for the 1st Fresnel zone (n = 1)**:

F₁ = 17.32 × √[ (d₁ × d₂) / (f × (d₁ + d₂)) ]


Where:
- `f` in GHz
- `d₁`, `d₂` in kilometers
- Result `F₁` in meters

---

##  Example Calculation
**Link:**
- Frequency: `5 GHz` (λ = 0.06 m)
- Distance: `10 km` (5 km each side from midpoint)

Midpoint 1st Fresnel radius:

F₁ = 17.32 × √[ (5 × 5) / (5 × (5 + 5)) ]
F₁ ≈ 7.7 m


**Clearance needed:** ~4.6 m (60% of radius) at midpoint.

---

##  Visualization

Antenna ----(narrow)====(bulge)====(narrow)---- Antenna
| |
Near end Midpoint (max radius)


Think of it as a **fat invisible bubble** around the line-of-sight.

---

##  Key Points
- The **1st Fresnel zone** is the most important for link quality.
- Lower frequency → larger Fresnel zone radius.
- Obstructions inside the Fresnel zone can cause major signal loss.
- Always aim for **≥ 60% clearance** of the 1st zone.

---



