

### **1. Explain the need for the data plane and control plane in the network layer.**  
- **Data Plane**: This plane handles the actual packet forwarding. It is responsible for deciding how a packet arriving at a router's input port is forwarded to the appropriate output port. It operates at high speeds and focuses on data processing and transmission.  
  - **Need**: Ensures fast packet forwarding, routing, and handling of data at scale.  

- **Control Plane**: This plane manages the routing process by determining the best path for packets. It uses routing algorithms and protocols to maintain a routing table.  
  - **Need**: Manages and updates routing decisions dynamically, enabling adaptability and efficient network utilization.  

---

### **2. IPv4 protocol is an unreliable protocol. Is it possible to make it reliable for the application layer? Justify your answer.**  
- **Answer**: Yes, IPv4 can be made reliable by using protocols like **TCP** in the transport layer.  
  - **Justification**: TCP provides features like:  
    - Error detection and correction.  
    - Acknowledgments for received packets.  
    - Sequence numbers to reorder packets.  
    - Retransmission of lost packets.  
    - Flow control and congestion control.  
  - **Conclusion**: While IPv4 itself is unreliable, reliability is achieved at higher layers (e.g., TCP in the transport layer).

---

### **3. IP Datagram Analysis**  
The header (hexadecimal): **45 00 00 54 00 03 00 00 20 06 00 00 7C 4E 03 02 B4 0E 0F 02**  

#### **a. Are there any options?**  
- The first nibble (4) indicates IPv4. The second nibble (5) specifies the header length as 5 words (20 bytes).  
- **No options** are present because the header length is the minimum 20 bytes.  

#### **b. Is the packet fragmented?**  
- Fragmentation flag (6th byte, bits 14–16): **00**  
- **Not fragmented**, as the flag value is 0 and the fragment offset is 0.  

#### **c. What is the size of the data?**  
- Total length: **0x0054 = 84 bytes**  
- Data size = Total length - Header length = 84 - 20 = **64 bytes**.  

#### **d. Is a checksum used?**  
- Yes, checksum is in the header for error detection (**00 00**).  

#### **e. How many more routers can the packet travel to?**  
- Time-to-Live (TTL): **0x20 = 32**  
- The packet can travel through **32 more routers**.  

#### **f. What is the identification number of the packet?**  
- Identification field: **0x0003 = 3**.  

#### **g. What is the type of service?**  
- ToS field: **0x00**  
- Default service (no specific priority or flags).  

---

### **4. Subnet Addressing**  
Given: Subnet prefix **223.1.17/24**  

#### Subnetting:  
- **Subnet 1**: Requires 4 interfaces → Subnet **223.1.17.0/30**  
- **Subnet 2**: Requires 6 interfaces → Subnet **223.1.17.4/29**  
- **Subnet 3**: Requires 12 interfaces → Subnet **223.1.17.16/28**  

Addresses are assigned optimally, leaving room for further subnets.  

---

### **5. Datagram Fragmentation**  
Given:  
- Datagram size = 2400 bytes  
- MTU = 700 bytes  
- Header size = 20 bytes  
- Data per fragment = MTU - Header = 700 - 20 = 680 bytes  
- Number of fragments = \( \lceil \frac{2400}{680} \rceil = 4 \)  

#### Fragment Fields:  
1. **Fragment 1**:  
   - Offset = 0  
   - Data size = 680 bytes  
   - Flags = More Fragments (MF) = 1  

2. **Fragment 2**:  
   - Offset = \( \frac{680}{8} = 85 \)  
   - Data size = 680 bytes  
   - Flags = MF = 1  

3. **Fragment 3**:  
   - Offset = \( \frac{1360}{8} = 170 \)  
   - Data size = 680 bytes  
   - Flags = MF = 1  

4. **Fragment 4**:  
   - Offset = \( \frac{2040}{8} = 255 \)  
   - Data size = 360 bytes (remaining data)  
   - Flags = MF = 0  

---

### **6. Maximum Hosts Per Subnet**  
Given subnet mask: **255.255.248.0**  
- Total bits: 32  
- Subnet bits: \( \log_2(256 - 248) = 3 \)  
- Host bits = 32 - (16 + 3) = 13  
- Max hosts = \( 2^{13} - 2 = 8190 \).  

---

### **7. Network and Broadcast Addresses**  
Given: **182.44.82.16/26**  
- Block size = \( 2^{32-26} = 64 \).  
- Network address: **182.44.82.0**  
- Broadcast address: **182.44.82.63**.  

---

### **8. ISP Subnets**  
Given: **245.248.128.0/20**  
- Total addresses: \( 2^{32-20} = 4096 \).  
- **Organization A**: \( 245.248.128.0/21 \) → 2048 addresses.  
- **Organization B**: \( 245.248.136.0/22 \) → 1024 addresses.  
- Remaining: \( 4096 - 3072 = 1024 \) addresses.  

---

### **9. Fragmentation and Reassembly**  
Given:  
- MTUs: 1024 bytes and 576 bytes  
- TCP message size = 1024 bytes + 20-byte header  

#### Fragments:  
1. **First Fragment**: 1024 bytes  
   - Offset = 0  

2. **Second Fragment**: 552 bytes (576 - 20)  
   - Offset = \( \frac{1024}{8} = 128 \).  

---

### **10. ISP Subnetting**  
Given: 1024 addresses for 1024 customers.  

#### **i. Does it need subnetting?**  
- Yes, subnetting is required for individual allocation.  

#### **ii. Does it need a mask?**  
- Yes, subnet mask is needed.  

#### **iii. Subnet mask**:  
- \( 2^0 = 1 \) host per subnet → Mask = **/32**.
