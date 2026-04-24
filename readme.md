
---

# Transfer Function Derivation of Filters

## 1. Low-Pass Filter (RC Low Pass)

### Circuit Description

* Resistor ( R ) in series
* Capacitor ( C ) connected to ground
* Output taken across the capacitor

---

### Step 1: Impedance Representation

* Resistor:
  $$
  Z_R = R
  $$

* Capacitor:
  $$
  Z_C = \frac{1}{sC}
  $$

---

### Step 2: Apply Voltage Divider Rule

$$
V_{out} = V_{in} \cdot \frac{Z_C}{Z_R + Z_C}
$$

Substituting values:

$$
V_{out} = V_{in} \cdot \frac{\frac{1}{sC}}{R + \frac{1}{sC}}
$$

---

### Step 3: Simplification

Multiply numerator and denominator by ( sC ):

$$
V_{out} = V_{in} \cdot \frac{1}{sRC + 1}
$$

---

### Transfer Function

$$
H(s) = \frac{V_{out}}{V_{in}} = \frac{1}{1 + sRC}
$$

---

### Cutoff Frequency

$$
\omega_c = \frac{1}{RC}
$$

---

## 2. Band-Pass Filter (RC Band Pass)

### Circuit Description

* Combination of:

  * High-Pass Filter
  * Low-Pass Filter
* Connected in cascade

---

### Step 1: High-Pass Filter Transfer Function

$$
H_{HP}(s) = \frac{sRC_1}{1 + sRC_1}
$$

---

### Step 2: Low-Pass Filter Transfer Function

$$
H_{LP}(s) = \frac{1}{1 + sRC_2}
$$

---

### Step 3: Overall Transfer Function

Since the filters are cascaded:

$$
H(s) = H_{HP}(s) \cdot H_{LP}(s)
$$

$$
H(s) = \frac{sRC_1}{1 + sRC_1} \cdot \frac{1}{1 + sRC_2}
$$

---

### Final Transfer Function

$$
H(s) = \frac{sRC_1}{(1 + sRC_1)(1 + sRC_2)}
$$

---

### Cutoff Frequencies

* Lower cutoff frequency:
  $$
  \omega_L = \frac{1}{RC_1}
  $$

* Upper cutoff frequency:
  $$
  \omega_H = \frac{1}{RC_2}
  $$

---