
### **1. What is CRC?**
CRC (Cyclic Redundancy Check) is an error-detecting code used in digital networks and storage devices to detect accidental changes to raw data. It works by performing binary division of the data bits by a predetermined generator polynomial and appending the remainder (CRC bits) to the data. 

#### Example:
Information: `1100`  
Generator Polynomial: `1011`  

**Step 1:** Append zeros equal to the degree of the generator polynomial to the data:  
New data: `1100000` (three zeros appended since \( \text{degree} = 3 \))  

**Step 2:** Perform binary division of the new data (`1100000`) by the generator polynomial (`1011`):  
- Perform XOR for each division step (division in binary uses XOR).  
  ```
      1011 | 1100000
             1011
            ------
             0110 (remainder after first XOR)
             0110
            ------
             0000 (remainder = 0)
  ```
- The remainder after division is `000`.  

**Step 3:** Append the remainder to the original data:  
Transmitted data = `1100` + `000` = `1100000`.

---

### **2. Transmitted bit stream with CRC**
#### Given:
Data: `10011101`  
Generator Polynomial: \( x^3 + 1 \) → Binary = `1001`

**Step 1:** Append three zeros to the data:  
New data = `10011101000`

**Step 2:** Perform binary division:  
Divide `10011101000` by `1001`.  
- Resulting remainder (CRC bits) = `111`.  

**Step 3:** Transmitted bit string:  
`10011101` + `111` = `10011101111`.

#### Error detection:
If the third bit is inverted during transmission, the received bit string becomes `10111101111`.  
- Perform binary division of the received string by `1001`.  
- If the remainder is non-zero, the error is detected.

---

### **3. Forward Error Correction (FEC) vs. Retransmission**
| **Aspect**             | **Forward Error Correction (FEC)**     | **Error Correction by Retransmission**       |
|------------------------|---------------------------------------|---------------------------------------------|
| **Definition**         | Corrects errors during transmission without retransmission. | Detects errors and requests retransmission of corrupted data. |
| **Use Case**           | Used in real-time applications (e.g., video streaming). | Used in applications where retransmission is feasible. |
| **Overhead**           | Higher computational complexity.       | Additional transmission time for error recovery. |
| **Reliability**        | Good for correcting small errors.      | Ensures perfect error correction. |

---

### **4. Internet checksum**
#### Given:
String: `"network"`  
ASCII values:  
- `n = 0x6E`, `e = 0x65`, `t = 0x74`, `w = 0x77`, `o = 0x6F`, `r = 0x72`, `k = 0x6B`.

**Step 1:** Pair bytes for checksum calculation:  
```
0x6E65 + 0x7477 + 0x6F72 + 0x6B00
```

**Step 2:** Add values and handle carry:  
Sum = \( 0x6E65 + 0x7477 + 0x6F72 + 0x6B00 = 0x22FA4 \).  
Handle overflow: \( 0x22FA4 → 0x2FA4 + 0x02 = 0x2FA6 \).  

**Step 3:** Complement the result:  
Checksum = \( \sim 0x2FA6 = 0xD059 \).  

---

### **5. Two-dimensional parity**
#### Given:
Bit pattern: `1010101010101011`  
4-bit data chunks:  
```
1010  
1010  
1010  
1011  
```

**Step 1:** Compute row and column parity:  
- Row parity: Add parity bits for each row (odd parity).  
- Column parity: Add parity bits for each column (odd parity).  

**Step 2:** Correctable bits:  
In a 2D parity scheme, **single-bit errors** can be detected and corrected.

---

### **6. Hamming Code**
#### Given:
Message: `111011`  
**Step 1:** Calculate parity bits:  
Hamming code uses positions \( 2^n \) for parity bits. Place parity bits and calculate them based on XOR of relevant bits.  

---

### **7. CRC with generator polynomial**
#### Given:
Data: `1010011110`  
Generator: \( x^4 + x^2 + x + 1 \) → Binary = `11011`.  

**Step 1:** Append zeros and divide:  
Binary division provides the codeword.

---

### **8. Hamming Code for `1011101`**
Use positions \( 2^n \) for parity bits. Calculate parity and check for errors. Correct flipped bit based on parity check.

---

### **9. 2D Parity for "TEST"**
#### Given:
String: `"TEST"` → ASCII values:  
- `T = 84`, `E = 69`, `S = 83`, `T = 84`.  
Represent as binary and compute row/column parities.

#### Error correction:
Locate the flipped bit using row and column parity bits.

---

### **10. FEC vs Retransmission**
Refer to Question 3 for details.  

