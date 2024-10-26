

# Key Formulas and Notations in Computer Networks

---

### 1. **Sequence Number Calculation**

The formula for finding the sequence number for the \(n\)-th packet in a limited sequence number space (e.g., 5-bit sequence numbers):

$$
\text{Sequence Number} = n \bmod 2^b
$$

Where:
- \( n \) = Packet number
- \( b \) = Number of bits in the sequence number field

**Example**: For the 100th packet with 5-bit sequence numbers:
$$
100 \bmod 32 = 4
$$

---

### 2. **Fragmentation Offsets and Sizes**

1. **Fragment Size**:  
   $$ 
   \text{Fragment Size} = \text{MTU} - \text{IP Header Size} 
   $$

2. **Offset Calculation** (in units of 8 bytes):  
   $$
   \text{Offset} = \frac{\text{Bytes Sent So Far}}{8}
   $$

---

### 3. **Total Length of a UDP Packet**

The total length of a UDP packet is calculated as:

$$
\text{Total Length} = \text{UDP Header Length} + \text{Data Length}
$$

Where:
- **UDP Header Length** is 8 bytes.

---

### 4. **TCP Window Size Calculation**

The effective window size in TCP:

$$
\text{Effective Window Size} = \text{Receiver Window Size} - \text{Unacknowledged Data}
$$

---

### 5. **Checksum Calculation (TCP/UDP)**

To ensure data integrity, the checksum is calculated over both the header and data:

$$
\text{Checksum} = \text{1's Complement of the Sum of All 16-bit Words}
$$

---

### 6. **Round-Trip Time (RTT) Calculation**

The Estimated RTT in TCP is updated using:

$$
\text{Estimated RTT} = (1 - \alpha) \times \text{Estimated RTT} + \alpha \times \text{Sample RTT}
$$

Where:
- \(\alpha\) is typically set to 0.125.

---

### 7. **Bandwidth-Delay Product**

The Bandwidth-Delay Product (BDP) represents the amount of data that can fill the network link:

$$
\text{BDP} = \text{Bandwidth} \times \text{Round-Trip Time (RTT)}
$$

---

### 8. **Throughput Calculation**

Throughput is defined as the rate of successful message delivery:

$$
\text{Throughput} = \frac{\text{Total Data Transferred}}{\text{Total Time}}
$$

---

### 9. **Utilization in Stop-and-Wait Protocol**

For the Stop-and-Wait protocol:

$$
\text{Utilization} = \frac{\text{Transmission Time}}{\text{Transmission Time} + \text{Propagation Delay}}
$$

--- 

These formulas in Markdown will display well on GitHub and provide a neat and clear view of each network formula.
