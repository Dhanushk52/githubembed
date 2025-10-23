---

# 🧮 Chapter: Number System

---

## 🔹 1. What is a Number System?

A **Number System** is a **way of representing numbers** using symbols or digits.
It defines how we **count, represent, and perform operations** like addition, subtraction, etc.

In simple terms, it’s the **language of numbers** that computers and humans use to communicate.

---

### ⚙️ Everyday Example:

* Humans usually use **Decimal (Base 10)** — digits from 0 to 9.
* Computers use **Binary (Base 2)** — digits 0 and 1.
* Engineers often use **Hexadecimal (Base 16)** — digits 0–9 and A–F (A=10, B=11, …, F=15).

---

### 📘 Definition:

> A **Number System** is defined by its **base (or radix)** — the total number of unique digits it uses.

---

### 🔢 Formula for Base Representation:

If you have a number `(N)` in base `b`:
[
N = (d_{n-1}d_{n-2}...d_1d_0)_b
]
where each digit ( d_i ) satisfies ( 0 \le d_i < b )

---

### 🧠 Quick Question 1:

> Q: In base 8, what are the valid digits?
> A: 0 to 7 ✅

---

## 🔹 2. Why Do We Need Different Number Systems?

Different number systems exist because **different devices and contexts** need different ways to represent and process numbers.

| Context     | Common System         | Reason                                           |
| ----------- | --------------------- | ------------------------------------------------ |
| Humans      | Decimal (Base 10)     | Easy for human counting                          |
| Computers   | Binary (Base 2)       | Digital circuits have 2 states: ON (1) / OFF (0) |
| Engineers   | Hexadecimal (Base 16) | Compact form for binary data                     |
| Programmers | Octal (Base 8)        | Used in older systems, file permissions, etc.    |

---

### 💡 Example:

Binary `1010` → Decimal `10` → Hexadecimal `A`

They all represent the same value but in **different forms**.

---

### 🧠 Quick Question 2:

> Q: Why can’t computers use the decimal system directly?
> A: Because hardware (transistors) can only detect two states — ON (1) and OFF (0).

---

## 🔹 3. Where Are Number Systems Used?

| Area                    | Application                                |
| ----------------------- | ------------------------------------------ |
| 🖥️ Computer Memory     | Addresses and data in binary or hex        |
| ⚙️ Embedded Systems     | Sensor values, register addresses (in hex) |
| 💾 Networking           | IP addresses (in decimal and binary)       |
| 💡 Digital Logic Design | Binary, Octal, and Hex are heavily used    |

---

### Example:

In Embedded Systems,
register `GPIOA_ODR` might hold value `0x0F` (hexadecimal) meaning lower 4 pins are HIGH.

---

### 🧠 Quick Question 3:

> Q: If `0x0F` is written in binary, what will it be?
> A: `00001111` ✅

---

## 🔹 4. Types of Number Systems

| Type        | Base | Digits   | Example |
| ----------- | ---- | -------- | ------- |
| Binary      | 2    | 0, 1     | (1011)₂ |
| Octal       | 8    | 0–7      | (57)₈   |
| Decimal     | 10   | 0–9      | (93)₁₀  |
| Hexadecimal | 16   | 0–9, A–F | (2A)₁₆  |

---

### 🔹 Binary System (Base 2)

Used by computers.
Each bit represents a power of 2.

**Example:**
[
(1011)*2 = 1×2^3 + 0×2^2 + 1×2^1 + 1×2^0 = 8 + 0 + 2 + 1 = 11*{10}
]

---

### 🔹 Decimal System (Base 10)

Used by humans.
Each digit represents a power of 10.

**Example:**
[
(345)_{10} = 3×10^2 + 4×10^1 + 5×10^0 = 300 + 40 + 5 = 345
]

---

### 🔹 Octal System (Base 8)

Each digit represents powers of 8.
Commonly used in UNIX permissions.

**Example:**
[
(57)*8 = 5×8^1 + 7×8^0 = 40 + 7 = 47*{10}
]

---

### 🔹 Hexadecimal System (Base 16)

Used for compact binary representation.
Each digit represents 4 bits.

**Example:**
[
(2A)*{16} = 2×16^1 + 10×16^0 = 32 + 10 = 42*{10}
]

---

### 🧠 Quick Question 4:

> Q: What is the binary equivalent of `(2A)₁₆`?
> A: `0010 1010` ✅

---

## 🔹 5. How to Convert Between Number Systems

Let’s go step-by-step 👇

---

### ➤ Decimal → Binary

**Method:** Divide by 2 repeatedly, record remainders (bottom to top).

Example:
Convert (13)₁₀ to Binary

| Step | Division | Quotient | Remainder |
| ---- | -------- | -------- | --------- |
| 1    | 13 ÷ 2   | 6        | 1         |
| 2    | 6 ÷ 2    | 3        | 0         |
| 3    | 3 ÷ 2    | 1        | 1         |
| 4    | 1 ÷ 2    | 0        | 1         |

Binary: **(1101)₂**

---

### ➤ Binary → Decimal

Multiply each bit by its positional power of 2.

Example:
[
(1101)*2 = 1×2^3 + 1×2^2 + 0×2^1 + 1×2^0 = 8 + 4 + 0 + 1 = (13)*{10}
]

---

### ➤ Binary ↔ Hexadecimal

Group 4 bits = 1 Hex digit.

Example:
Binary `11001110` → `1100 1110` = `CE`
Hex `(CE)₁₆`

---

### 🧠 Quick Question 5:

> Q: Convert `(101011)₂` to decimal.
> A: 43 ✅

---

## 🔹 6. Common Real-World Usage in Embedded Systems

| Format  | Example        | Use Case                         |
| ------- | -------------- | -------------------------------- |
| Binary  | 0b10101010     | Writing to registers             |
| Hex     | 0xFF or 0x1A3B | Memory addresses                 |
| Decimal | 255            | Displaying human-readable output |

---

### Example:

```c
GPIOA->ODR = 0x0F; // Turn ON lower 4 pins
```

Here, `0x0F` is **hexadecimal** → `00001111` binary → `15` decimal.

---

### 🧠 Quick Question 6:

> Q: What is the advantage of Hexadecimal in embedded coding?
> A: It’s short, readable, and directly maps to binary bits. ✅

---

## 🔹 7. Summary

| System      | Base | Symbol Count | Example | Used In                     |
| ----------- | ---- | ------------ | ------- | --------------------------- |
| Binary      | 2    | 2            | (1010)₂ | Computers                   |
| Octal       | 8    | 8            | (57)₈   | File systems                |
| Decimal     | 10   | 10           | (93)₁₀  | Everyday use                |
| Hexadecimal | 16   | 16           | (2A)₁₆  | Embedded, Memory, Debugging |

---

### ✅ Quick Recap:

* **What:** System of representing numbers
* **Why:** Different contexts (human vs. machine)
* **Where:** Everywhere from software to hardware
* **How:** Depends on base and conversion methods

---

### 🧩 Practice Questions

1. Convert `(25)₁₀` to binary.
2. Convert `(11001)₂` to decimal.
3. What is `(1F)₁₆` in binary?
4. What base uses digits 0–7?
5. Convert `(57)₈` to decimal.
6. Why do embedded engineers prefer hexadecimal?
7. Represent `(255)₁₀` in hex.
8. What is `(1001 0110)₂` in hex?
9. How many bits are in one hexadecimal digit?
10. Convert `(A5)₁₆` to binary and decimal.

---
