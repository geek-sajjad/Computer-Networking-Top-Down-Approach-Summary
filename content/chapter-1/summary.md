
## 1.1 What is the Internet

### 1.1.1 A Nuts-and-Bolts Description

devices that are being hooked up to the Internet. In Internet jargon, all of these devices are called **hosts** or **end systems**.


End systems are connected together by a network of **communication links** and **packet switches**.

that there are many types of communication links, which are made up ofdifferent types of **physical media**,

Different links can transmit data at different rates, with the **transmission rate** of a link measured in bits/second.

When one end system has data to send to another end system, the sending end system segments the data and adds header bytes to each segment. The resulting packages of information, known as **packets**


Packet switches come in many shapes and flavors, but the two most prominent types in today’s Internet are **routers** and **link-layer switches**.


Link-layer switches are typically used in **access networks**, while routers are typically used in the **network core**.


The sequence of communication links and packet switches traversed by a packet from the sending end system to the receiving end system is known as a **route** or **path** through the network.

End systems access the Internet through **Internet Service Providers (ISPs),** including residential ISPs such as local cable or telephone companies; corporate ISPs; university ISPs


The Internet is all about connecting end systems to each other,


End systems, packet switches, and other pieces of the Internet run protocols that control the sending
and receiving of information within the Internet.

The Transmission Control Protocol (TCP) and the
Internet Protocol (IP) are two of the most important protocols in the Internet.


### Ai Summary
**What is the Internet?**

- The Internet is a computer network that interconnects billions of computing devices worldwide
- Devices connected include traditional computers (PCs, servers, workstations) and non-traditional "Internet of Things" devices (smartphones, tablets, TVs, gaming consoles, thermostats, home security systems, appliances, watches, cars, traffic control systems)
- All connected devices are called **hosts** or **end systems**
- Statistics: ~5 billion devices connected in 2015, projected to reach 25 billion by 2020
- Over 3.2 billion Internet users worldwide in 2015 (40% of world population)

**Network Components and Structure**

- **End systems** are connected by communication links and packet switches
- **Communication links** are made of different physical media: coaxial cable, copper wire, optical fiber, radio spectrum
- Links transmit data at different rates (measured in bits/second)
- **Packet switches** forward packets between communication links - two main types:
    - **Routers** (used in network core)
    - **Link-layer switches** (used in access networks)

**How Data Travels**

- Sending end system segments data and adds header bytes to create **packets**
- Packets travel through the network via a **route** or **path** (sequence of links and switches)
- At destination, packets are reassembled into original data
- Transportation analogy: packets = trucks, links = highways/roads, switches = intersections, end systems = buildings

**Internet Service Providers (ISPs)**

- End systems access Internet through ISPs
- Types of ISPs:
    - Residential (cable/telephone companies)
    - Corporate ISPs
    - University ISPs
    - Public WiFi providers (airports, hotels, coffee shops)
    - Cellular data ISPs
- ISPs provide various access types: cable modem, DSL, high-speed LAN, mobile wireless
- ISP hierarchy: lower-tier ISPs interconnected through upper-tier ISPs (Level 3, AT&T, Sprint, NTT)
- Upper-tier ISPs use high-speed routers with fiber-optic links

**Protocols and Standards**

- **Protocols** control sending and receiving of information
- Key protocols: **TCP** (Transmission Control Protocol) and **IP** (Internet Protocol)
- IP specifies packet format between routers and end systems
- Collectively known as **TCP/IP**
- **Internet Engineering Task Force (IETF)** develops Internet standards
- Standards documented in **RFCs** (Requests for Comments) - over 7,000 currently exist
- RFCs define protocols like TCP, IP, HTTP (Web), SMTP (email)
- **IEEE 802 Committee** specifies standards for network components (Ethernet, WiFi)







### 1.1.2 A Services Description
#### **Alternative View of the Internet**

- Internet can be described as **infrastructure that provides services to applications**
- Different perspective from the hardware/software component view
- Focus shifts from physical components to functional services

#### **Internet Applications**

- **Traditional applications**: email, web surfing
- **Modern applications**:
    - Mobile smartphone and tablet apps
    - Internet messaging
    - Real-time mapping with traffic information
    - Music streaming from cloud
    - Movie and television streaming
    - Online social networks
    - Video conferencing
    - Multi-person games
    - Location-based recommendation systems
- All are **distributed applications** - involve multiple end systems exchanging data
- **Key point**: Applications run on end systems, NOT in packet switches in the network core
- Packet switches only facilitate data exchange but don't concern themselves with specific applications

#### **Developing Internet Applications**

- To create a distributed Internet application, you need to:
    - Write programs that run on end systems
    - Use programming languages like Java, C, or Python
    - Enable programs on different end systems to send data to each other
- **Central challenge**: How does one program instruct the Internet to deliver data to another program on a different end system?

#### **Socket Interface**

- **Definition**: Set of rules that specify how a program on one end system asks the Internet to deliver data to a destination program on another end system
- **Postal service analogy**:
    - Alice sending letter to Bob through postal service
    - Alice must follow postal service rules: envelope, full address, zip code, stamp, official mailbox
    - Similarly, Internet has socket interface rules that sending programs must follow
    - Internet delivers data to receiving program when rules are followed

#### **Multiple Internet Services**

- Just as postal service offers multiple services (express delivery, reception confirmation, ordinary mail)
- **Internet provides multiple services** to applications
- Developers must choose appropriate Internet service for their specific application
- Service selection affects how application functions and performs

#### **Two Descriptions Summary**

1. **Hardware/Software Components**: Physical infrastructure view (routers, links, protocols)
2. **Service Infrastructure**: Platform for distributed applications view


## 1.2 The Network Edge
### 1.2.1 Access Networks

### What is an Access Network?

- **Access Network**: The network that physically connects an end system to the first router
- Also connects to the **edge router** on a path from the end system to any other distant end system
- Represents the critical link between end systems and the broader network infrastructure

### Key Terminology

- **End System**: Devices at the "edge of the network" (computers, smartphones, servers, etc.)
- **Edge Router**: The first router encountered on the path from an end system to distant end systems
- **Physical Connection**: The actual infrastructure that provides network connectivity



### Network Hierarchy

- **Edge of Network**: Where applications and end systems reside
- **Access Network**: The connection layer between edge and core network
- **Core Network**: The backbone infrastructure for long-distance communication




### Home Access Networks
#### 1. Digital Subscriber Line (DSL)

##### Basic Operation

- **DSL Modem**: Customer device that connects to existing telephone line
- **DSLAM**: Digital Subscriber Line Access Multiplexer located in telco's Central Office (CO)
- **Infrastructure**: Uses existing twisted-pair copper wire telephone lines
- **Provider Model**: Telephone company (telco) serves as both phone provider and ISP

##### Technical Specifications

- **Physical Medium**: Twisted-pair copper wire
- **Signal Processing**:
    - Home: DSL modem converts digital data to high-frequency tones
    - CO: DSLAM converts analog signals back to digital format

##### Frequency Division Multiplexing

DSL uses **frequency-division multiplexing** to create three separate channels:

- **Downstream Channel**: 50 kHz to 1 MHz band (high-speed)
- **Upstream Channel**: 4 kHz to 50 kHz band (medium-speed)
- **Telephone Channel**: 0 to 4 kHz band (ordinary two-way voice)

##### Equipment and Architecture

- **Customer Side**: Splitter separates data and telephone signals
- **Telco Side**: DSLAM separates signals and routes data to Internet
- **Scale**: Hundreds to thousands of households connect to single DSLAM

##### Performance Standards

- **Standard Rates**:
    - 12 Mbps downstream / 1.8 Mbps upstream [ITU 1999]
    - 55 Mbps downstream / 15 Mbps upstream [ITU 2006]
- **Asymmetric Access**: Downstream and upstream rates differ significantly
- **Actual Performance**: May be limited by provider's tiered service offerings

##### Distance Limitations

- **Maximum Distance**: 5-10 miles from Central Office
- **Performance Factors**:
    - Distance between home and CO
    - Gauge of twisted-pair line
    - Degree of electrical interference
- **Design Constraint**: Expressly designed for short distances

#### 2. Cable Internet Access

##### Basic Operation

- **Provider Model**: Cable television company provides both TV and Internet
- **Infrastructure**: Uses existing cable television infrastructure
- **Cable Modem**: Special modem required (typically external device)
- **Connection**: Cable modem connects to PC via Ethernet port

##### Network Architecture

- **Hybrid Fiber Coax (HFC)**: Combination of fiber optics and coaxial cable
- **Head End to Junction**: Fiber optics connect cable head end to neighborhood junctions
- **Junction to Home**: Traditional coaxial cable reaches individual houses/apartments
- **Neighborhood Scale**: Each junction typically supports 500-5,000 homes

##### Technical Components

- **Cable Modem Termination System (CMTS)**: Located at cable head end
    - Similar function to DSL's DSLAM
    - Converts analog signals from cable modems back to digital format
- **Channel Division**: HFC network divided into downstream and upstream channels

##### Performance Standards

- **DOCSIS 2.0 Standard**:
    - Downstream: Up to 42.8 Mbps
    - Upstream: Up to 30.7 Mbps
- **Asymmetric Access**: Downstream typically faster than upstream
- **Performance Limitations**: May not achieve maximum due to contracted rates or media impairments

##### Shared Medium Characteristics

- **Broadcast Medium**: Cable access is shared among users
- **Downstream Sharing**: Every packet from head end travels to every home
- **Upstream Sharing**: Every packet from home travels to head end
- **Performance Impact**:
    - Multiple simultaneous downloads reduce individual user speeds
    - Light usage (web surfing) may achieve full downstream rate
- **Access Control**: Distributed multiple access protocol needed to coordinate upstream transmissions and avoid collisions

#### 3. Fiber to the Home (FTTH)

##### Overview and Adoption

- **Market Position**: Up-and-coming technology providing higher speeds than DSL/cable
- **Current Dominance**: DSL and cable represent >85% of US residential broadband
- **Global Leaders**: UAE, South Korea, Hong Kong, Japan, Singapore, Taiwan, Lithuania, Sweden (>30% household penetration)

##### Basic Concept

- **FTTH Definition**: Optical fiber path from Central Office directly to the home
- **Technology Advantage**: Provides significantly higher speeds than copper-based alternatives

##### Distribution Architectures

 Direct Fiber

- **Simplest approach**: One fiber leaving CO for each home
- **Less common**: Due to cost and infrastructure requirements

 Shared Fiber Systems

- **Common approach**: Each fiber from CO shared by many homes
- **Splitting point**: Fiber splits into individual customer fibers close to homes

##### Optical Distribution Network Types

###### Active Optical Networks (AONs)

- **Technology Base**: Essentially switched Ethernet
- **Reference**: Detailed discussion in Chapter 6

###### Passive Optical Networks (PONs)

- **Implementation Example**: Used in Verizon's FIOS service
- **Architecture Components**:
    - **Optical Network Terminator (ONT)**: Located in each home
    - **Neighborhood Splitter**: Combines multiple homes (typically <100)
    - **Optical Line Terminator (OLT)**: Located in telco's Central Office
- **Connection Flow**: ONT → Dedicated fiber → Neighborhood splitter → Shared fiber → OLT → Telco router → Internet
- **Home Setup**: Users connect home router (typically wireless) to ONT
- **Signal Distribution**: All packets from OLT replicated at splitter (similar to cable head end)

##### Performance Capabilities

- **Potential Speeds**: Gigabits per second range
- **Service Reality**: Most FTTH ISPs offer tiered rate offerings
- **2011 Average Speeds**:
    - FTTH: ~20 Mbps downstream
    - Cable: ~13 Mbps downstream
    - DSL: <5 Mbps downstream

#### 4. Satellite Internet Access

##### Use Cases and Availability

- **Primary Application**: Locations where DSL, cable, and FTTH unavailable
- **Typical Settings**: Rural areas with limited infrastructure
- **Speed Capability**: More than 1 Mbps
- **Major Providers**: StarBand, HughesNet

##### Technology Characteristics

- **Connection Method**: Satellite link connects residence to Internet
- **Coverage Advantage**: Can reach remote locations
- **Speed Limitation**: Generally slower than terrestrial broadband options

#### 5. Dial-Up Access

##### Technology Basis

- **Infrastructure**: Traditional phone lines (same model as DSL)
- **Equipment**: Home modem connects via phone line to ISP modem
- **Speed**: 56 kbps (described as "excruciatingly slow")
- **Comparison**: Significantly slower than DSL and other broadband technologies
- **Current Relevance**: Legacy technology, largely superseded by broadband



### Enterprise and Home Access Networks
1. Local Area Networks (LANs)
Primary Use Cases

Corporate campuses: Business and organizational networks
University campuses: Academic institution networks
Home settings: Increasingly common in residential environments
Function: Connect end systems to edge router within localized areas

2. Ethernet Access
Market Dominance

Prevalence: Most prevalent access technology in corporate, university, and home networks
Technology Base: Uses twisted-pair copper wire connections

Architecture and Components

Connection Method: Users connect via twisted-pair copper wire to Ethernet switch
Network Expansion: Ethernet switches can be interconnected
Internet Connection: Switch network connects to larger Internet infrastructure

Performance Specifications

Standard User Access:

100 Mbps to Ethernet switch
1 Gbps to Ethernet switch


Server Access:

1 Gbps access
10 Gbps access (high-performance servers)



Technical Details

Reference: Detailed technology discussion in Chapter 6
Physical Medium: Twisted-pair copper wire infrastructure

3. Wireless LAN (WiFi) Access
Technology Evolution

Growing Trend: Increasing wireless access from laptops, smartphones, tablets, IoT devices
Standard: IEEE 802.11 technology (colloquially known as WiFi)
Ubiquity: Available in universities, offices, cafes, airports, homes, airplanes

Network Architecture

Access Point: Wireless users transmit/receive packets to/from access point
Backhaul Connection: Access point connected to enterprise network (typically wired Ethernet)
Internet Connection: Enterprise network connects to wired Internet
Range Limitation: Users must be within few tens of meters of access point

Performance and Coverage

Transmission Rate: Up to more than 100 Mbps (shared among users)
Coverage Density: In many cities, 10-20 base stations accessible from single location
Global Mapping: 802.11 base stations discovered and logged on websites like wigle.net

Home Network Integration

Modern Trend: Ethernet and WiFi increasingly common in home networks
Hybrid Approach: Combination of broadband residential access (cable/DSL) with wireless LAN

Typical Home Network Components (Figure 1.9)

Devices:

Roaming laptop
Wired PC


Infrastructure:

Base Station: Wireless access point for wireless devices
Cable Modem: Provides broadband Internet access
Router: Interconnects base station and wired PC with cable modem


Benefits: Household members get broadband access with mobility throughout home


### Wide-Area Wireless Access
1. Mobile Device Usage Trends

Device Types: iPhones, Android devices, smartphones, tablets
Activities: Messaging, social media photo sharing, movie watching, music streaming
Usage Pattern: "On the run" - mobile, location-independent access

2. Cellular Infrastructure

Technology Base: Same wireless infrastructure used for cellular telephony
Network Architecture: Devices send/receive packets through base stations
Provider: Base stations operated by cellular network providers
Range Advantage: Users need only be within few tens of kilometers of base station (vs. few tens of meters for WiFi)

3. Third-Generation (3G) Technology
Investment and Deployment

Industry Investment: Telecommunications companies made enormous investments
Technology Type: Packet-switched wide-area wireless Internet access
Performance: Speeds in excess of 1 Mbps

Market Position

Current Status: Widely deployed and established technology
Evolution: Foundation for next-generation technologies

4. Fourth-Generation (4G) and LTE Technology
Technology Evolution

4G Definition: Fourth-generation wide-area wireless networks
Deployment Status: Already being deployed (higher speeds than 3G)

LTE (Long-Term Evolution)

Acronym Humor: Noted as "candidate for Bad Acronym of the Year Award"
Technology Foundation: Has roots in 3G technology
Performance Capabilities:

Basic rates: In excess of 10 Mbps
Commercial deployments: Many tens of Mbps downstream rates reported



Performance Comparison

3G: >1 Mbps speeds
LTE: >10 Mbps basic, up to tens of Mbps in commercial deployments
Trend: Continuous improvement in wide-area wireless speeds

5. Technology Coverage Reference

Comprehensive Discussion: Chapter 7 covers:

Basic principles of wireless networks and mobility
WiFi technology details
3G technology specifics
LTE technology implementation
Additional wireless technologies
## 1.3 The Network Core

Having examined the Internet’s edge, let us now delve more deeply inside the network core—the **mesh of packet switches and links** that interconnects the Internet’s end systems.

### 1.3.1 Packet Switching

#### Core Concept

- **Packet switching** is the fundamental method used in networks for transmitting data between end systems
- **Messages** can contain control functions (like "Hi" in handshaking) or data (email, JPEG images, MP3 files)
- Long messages are broken into smaller chunks called **packets** for transmission

#### Basic Packet Transmission Process

- **Source end system** breaks messages into packets
- **Packets** travel through communication links and packet switches
- **Two main types of packet switches:**
    - Routers
    - Link-layer switches
- **Transmission rate**: Packets transmitted at full transmission rate (R bits/sec) of the link
- **Transmission time formula**: L/R seconds (where L = packet size in bits, R = transmission rate)

---

### Store-and-Forward Transmission

#### Definition and Mechanism

- **Store-and-forward transmission**: Packet switch must receive the entire packet before beginning to transmit the first bit onto outbound link
- Process involves **buffering** (storing) complete packets before forwarding
- Routers must receive, store, and process entire packets before forwarding

#### Timing Calculations

##### Single Packet Transmission

- **Simple network setup**: Two end systems connected by single router
- **Timeline for one packet (L bits)**:
    - Time 0: Source begins transmission
    - Time L/R: Source completes transmission, router receives entire packet
    - Time L/R: Router begins forwarding packet
    - Time 2L/R: Destination receives entire packet
- **Total delay**: 2L/R seconds

##### Multiple Packet Transmission

- **Three packet example**:
    - Time L/R: Router forwards packet 1, source sends packet 2
    - Time 2L/R: Destination receives packet 1, router receives packet 2
    - Time 3L/R: Destination receives packets 1-2, router receives packet 3
    - Time 4L/R: Destination receives all three packets

##### General Formula

- **End-to-end delay for N links**: d_end-to-end = NL/R
- **N links** means N-1 routers between source and destination
- Each link has transmission rate R

---

### Queuing Delays and Packet Loss

#### Buffer Management

- **Output buffer (output queue)**: Each packet switch maintains buffers for each attached link
- **Purpose**: Store packets waiting to be transmitted when link is busy
- **Queue operation**: Arriving packets wait if outbound link is occupied

#### Types of Delays

- **Store-and-forward delays**: Fixed delays from packet processing
- **Queuing delays**: Variable delays depending on network congestion level
- **Congestion**: Occurs when packet arrival rate exceeds link transmission capacity

#### Packet Loss Mechanism

- **Finite buffer space**: Limited storage capacity in output buffers
- **Buffer overflow**: When buffer is completely full with waiting packets
- **Packet dropping**: Either arriving packet or queued packet is discarded
- **Loss occurs**: When arrival rate consistently exceeds transmission capacity

#### Practical Example

- **Network setup**: Hosts A and B sending to Host E
- **Link capacities**: 100 Mbps Ethernet links to router, 15 Mbps outbound link
- **Congestion scenario**: If combined arrival rate > 15 Mbps, queuing occurs
- **Burst traffic**: Five packets from each host simultaneously causes significant queuing
- **Real-world analogy**: Similar to waiting in bank teller or tollbooth lines

---

### Forwarding Tables and Routing Protocols

#### IP Addressing System

- **IP address**: Unique identifier for every end system on Internet
- **Hierarchical structure**: Similar to postal addresses
- **Header inclusion**: Source includes destination IP address in packet header

#### Forwarding Process

- **Router examination**: Router checks portion of destination address
- **Forwarding table**: Maps destination addresses to outbound links
- **Address lookup**: Router searches table using destination address
- **Packet direction**: Router forwards packet to appropriate outbound link

#### Routing Analogy: The Road Trip Example

**Scenario**: Joe driving from Philadelphia to 156 Lakeside Drive, Orlando, Florida

**Step-by-step process**:

1. **Philadelphia gas station**: Extracts "Florida" → directs to I-95 South
2. **Jacksonville, Florida**: Extracts "Orlando" → continue I-95 to Daytona Beach
3. **Daytona Beach**: Extracts "Orlando" → take I-4 to Orlando
4. **Orlando**: Extracts "Lakeside Drive" → provides local directions
5. **Lakeside Drive**: Kid extracts "156" → points to specific house

**Key analogy elements**:

- **Gas station attendants = Routers**
- **Address portions = IP address hierarchy**
- **Route directions = Forwarding table entries**
- **Progressive refinement = Hierarchical routing**

#### Forwarding Table Configuration

- **Manual configuration**: Possible but impractical for large networks
- **Automated procedure**: Internet uses special routing protocols
- **Routing protocols**: Automatically configure forwarding tables
- **Shortest path algorithms**: Determine optimal routes from each router to destinations
- **Dynamic updates**: Tables updated automatically based on network conditions

---

### Key Formulas and Relationships

#### Transmission Calculations

- **Single packet transmission time**: L/R seconds
- **Store-and-forward delay (2 nodes)**: 2L/R seconds
- **End-to-end delay (N links)**: NL/R seconds
- **Where**: L = packet size (bits), R = transmission rate (bits/sec), N = number of links

#### Performance Factors

- **Fixed delays**: Store-and-forward processing
- **Variable delays**: Queuing delays (depend on congestion)
- **Capacity constraints**: Output link transmission rates
- **Buffer limitations**: Finite storage causing packet loss

---

### Important Concepts for Review

#### Core Principles

- Packet switching breaks messages into smaller, manageable units
- Store-and-forward ensures reliable packet processing
- Queuing manages traffic when demand exceeds capacity
- Hierarchical addressing enables scalable routing

#### Critical Understanding Points

- Why routers can't forward bits immediately (need complete packets)
- How queuing delays vary with network congestion
- Role of forwarding tables in routing decisions
- Relationship between transmission rates and delays

#### Practical Applications

- Network congestion management
- Router configuration and operation
- Internet addressing and routing
- Performance optimization in packet networks




---
### 1.3.2 Circuit Switching

### **Definition and Characteristics**

- **Circuit**: A dedicated connection maintained by switches between sender and receiver
- Network establishes connection **before** data transfer begins
- Switches maintain **connection state** for the duration of the session
- **Guaranteed constant transmission rate** reserved for the connection

### **Traditional Example: Telephone Networks**

- Must establish connection before sending voice or fax data
- Dedicated end-to-end path with reserved bandwidth
- Connection persists for entire communication session

### Circuit-Switched Network Structure

### **Network Components**

- **Circuit Switches**: Interconnected switching devices
- **Links**: Connections between switches, each supporting multiple circuits
- **Hosts**: End devices (PCs, workstations) directly connected to switches

### **Example Network Configuration**

- 4 circuit switches interconnected by 4 links
- Each link supports **4 circuits** (4 simultaneous connections)
- Each connection gets **1/4 of link's total transmission capacity**
- Example: 1 Mbps link → each circuit gets **250 kbps** dedicated rate

### **Connection Establishment Process**

- Network reserves one circuit on each required link
- Dedicated end-to-end connection created between hosts
- Resources remain allocated for entire session duration

### Multiplexing in Circuit-Switched Networks

### **Two Implementation Methods**

#### **Frequency-Division Multiplexing (FDM)**

- **Frequency spectrum** of link divided among connections
- Each connection gets dedicated **frequency band** for entire duration
- **Telephone networks**: typically **4 kHz bandwidth** per connection
- **FM radio example**: 88-108 MHz spectrum divided among stations

#### **Time-Division Multiplexing (TDM)**

- **Time divided into frames** of fixed duration
- Each frame contains **fixed number of time slots**
- Each connection gets **one dedicated time slot per frame**
- **Transmission rate** = frame rate × bits per slot
- **Example calculation**: 8,000 frames/sec × 8 bits/slot = **64 kbps per circuit**

### **Visual Example (4-Circuit Link)**

- **FDM**: Frequency domain segmented into 4 bands of 4 kHz each
- **TDM**: Time domain segmented into frames with 4 time slots each

### Circuit Switching vs. Packet Switching Comparison

### **Packet Switching Process**

- Packets sent **without reserving link resources**
- No guaranteed delivery time (best effort service)
- Packets may experience **delays due to congestion**
- Must queue at transmission links when congested

### **Arguments Against Circuit Switching**

#### **Resource Waste Issues**

- **Silent periods**: Dedicated circuits idle when not actively transmitting
- **Telephone example**: Unused frequency bands/time slots during conversation pauses
- **Radiologist example**:
    - Sets up connection to view X-rays
    - Network resources wasted during image contemplation periods
    - Resources allocated but not used between image requests

#### **Complexity Issues**

- Establishing end-to-end circuits is **complicated**
- Requires **complex signaling software**
- Must coordinate operation of all switches along the path

### Numerical Example: File Transfer Analysis

### **Scenario Setup**

- **File size**: 640,000 bits
- **Network configuration**: All links use TDM with 24 slots
- **Link bit rate**: 1.536 Mbps
- **Circuit establishment time**: 500 msec

### **Calculations**

1. **Circuit transmission rate**: 1.536 Mbps ÷ 24 slots = **64 kbps per circuit**
2. **File transmission time**: 640,000 bits ÷ 64 kbps = **10 seconds**
3. **Total time**: 10 seconds + 0.5 seconds (setup) = **10.5 seconds**

### **Key Insight**

- **Transmission time independent of number of links**
- Same 10 seconds whether circuit passes through 1 link or 100 links
- (Note: Actual delay also includes propagation delay - covered in Section 1.4)

### Key Advantages and Disadvantages

### **Circuit Switching Advantages**

- **Guaranteed bandwidth** and transmission rate
- **Predictable performance** once connection established
- **No queuing delays** during data transmission
- **Suitable for real-time applications** (voice, video)

### **Circuit Switching Disadvantages**

- **Resource waste** during idle periods
- **Setup overhead** (time and complexity)
- **Inflexible resource allocation**
- **Complex signaling requirements**
- **Connection setup delay** before transmission begins

### 1.3.3 A Network of Networks

#### General Overview

- The Internet is a **network of networks**, not just isolated end-systems and access ISPs.

- **Access ISPs** connect end-systems (like smartphones, PCs, servers) using wired or wireless technologies (DSL, FTTH, Wi-Fi, cellular).

- Merely connecting users to access ISPs isn't enough—the access ISPs themselves need to be interconnected.


---

#### 🧱 Network Structures (1–5)

#### **Network Structure 1: One Global Transit ISP**

- All access ISPs connect to a **single global transit ISP**.

- The global ISP spans the globe and connects to every access ISP.

- This is costly for the global ISP; access ISPs pay for connectivity (customer-provider model).


#### **Network Structure 2: Multiple Competing Global ISPs**

- Several global transit ISPs exist and **compete** with one another.

- Access ISPs **choose providers** based on cost and services.

- Global ISPs **must interconnect** so that users of different ISPs can communicate.

- This creates a **two-tier hierarchy**: global transit ISPs (top) and access ISPs (bottom).


#### **Network Structure 3: Regional ISPs and Tier-1 ISPs**

- Global ISPs don’t reach everywhere; **regional ISPs** act as intermediaries.

- Access ISPs → Regional ISPs → Tier-1 ISPs.

- **Tier-1 ISPs** are top-level networks that don’t pay others and peer with each other.

- Example hierarchy: Access ISPs (city) → Provincial ISPs → National ISPs → Tier-1 ISPs (e.g., AT&T, Sprint, NTT).

- This forms a **multi-tier hierarchy** with customer-provider relationships at every level.


#### **Network Structure 4: Peering, PoPs, IXPs, and Multi-Homing**

- **Points of Presence (PoPs):** Physical locations with routers where ISPs connect.

- **Multi-homing:** An ISP connects to multiple providers for reliability and resilience.

- **Peering:** ISPs at the same level interconnect **directly** (often settlement-free) to avoid transit costs.

- **IXPs (Internet Exchange Points):** Facilities where multiple ISPs peer, enabling efficient data exchange.

- More than **400 IXPs** exist worldwide.


#### **Network Structure 5: Content Provider Networks**

- Large content providers (e.g., **Google**) build their own **private global networks**.

- Google has 50–100 data centers worldwide, interconnected via its **own TCP/IP network**.

- These networks **peer directly** with lower-tier ISPs (settlement-free), bypassing higher-tier ISPs where possible.

- They still **pay tier-1 ISPs** when transit through them is necessary.

- Content providers gain **cost savings** and **better control** over service delivery.

## 1.4 Delay, Loss, and Throughput in Packet-Switched Networks

### 1.4.1 Overview of Delay in Packet-Switched Networks

The total delay a packet experiences as it travels from source to destination in a packet-switched network is the sum of four types of delays—**processing, queuing, transmission, and propagation**. Understanding these delays is essential for analyzing network performance.


Types of Delays in a Router (Nodal Delays):
- **1. Processing Delay (`d_proc`)**

    - Time to examine packet header and check for errors.

    - Typically very short (microseconds or less).

    - Depends on router’s speed and processing capacity.

- **2. Queuing Delay (`d_queue`)**

    - Time spent waiting in queue before transmission.

    - Depends on traffic load: low traffic = low delay, high traffic = high delay.

    - Varies from microseconds to milliseconds.

- **3. Transmission Delay (`d_trans`)**

    - Time to push all bits of a packet onto the link.

    - Formula: `L / R` where `L = packet size`, `R = transmission rate`.

    - Independent of distance.

    - Can be negligible in high-speed networks.

- **4. Propagation Delay (`d_prop`)**

    - Time for bits to travel across the link to next router.

    - Formula: `d / s` where `d = distance`, `s = propagation speed`.

    - Independent of packet size and transmission rate.

    - Depends on medium (e.g., fiber, copper).

Key Formula:
```
Total Nodal Delay = d_proc + d_queue + d_trans + d_prop

```

**Transmission vs Propagation Delay**:

- **Transmission** = time to "send" bits into the wire.

- **Propagation** = time for bits to "travel" across the wire.

### 1.4.2 Queuing Delay and Packet Loss

Queuing delay in packet-switched networks is a variable and complex type of nodal delay that heavily depends on traffic patterns and system capacity. It's influenced by traffic intensity (arrival rate vs. transmission rate) and becomes problematic when the system approaches or exceeds full utilization, often leading to packet loss and performance degradation.


#### **What is Queuing Delay?**

- It's one of four types of nodal delays (others: processing, transmission, propagation).

- Unlike the others, queuing delay is highly **variable** and **unpredictable**.

- It occurs **when packets wait in a buffer** before being transmitted.


#### **Statistical Nature**

- Described using **average**, **variance**, and **probability** of exceeding a threshold.
- Depends on how **many packets** are already in the queue when a new one arrives.

#### **Traffic Intensity Concept**

- Defined as **La/R**, where:

    - **L** = packet length (bits)
    - **a** = average arrival rate (packets/sec)
    - **R** = transmission rate (bits/sec)

- If **La/R > 1**: bits arrive faster than they can be sent → queue grows infinitely → **delay approaches infinity**.

- If **La/R ≤ 1**: delays depend on **traffic patterns**.


#### **Traffic Patterns**

- **Periodic arrivals** (one packet every L/R seconds): no queuing delay.
- **Burst arrivals** (e.g., N packets every (L/R)N seconds): delay increases linearly for each successive packet.
- **Random arrivals**: most realistic, and queuing delay depends more on statistical variations.

#### **Behavior Near Capacity**

- As **La/R → 1**, even small increases cause **huge spikes in delay**.
- **Queue length and delay grow rapidly** near full utilization.
- Real-world analogy: **traffic congestion on highways**.
#### **Packet Loss**

- Real queues have **finite capacity** → not all packets can be stored.
- When full, **incoming packets are dropped**.
- Loss probability increases as **traffic intensity increases**.
- Loss impacts performance and often triggers **retransmission protocols**.



**Keep traffic intensity below 1** to maintain reasonable delay and avoid packet loss.
### 1.4.3 End-to-End Delay

**end-to-end delay** in packet-switched networks

#### **End-to-End Delay Components**

- **Nodal delay** refers to delay at a single router.

- **End-to-end delay** is the total delay from source to destination.

- Assuming an uncongested network:

    dend-to-end=N(dproc+dtrans+dprop)d_{\text{end-to-end}} = N (d_{\text{proc}} + d_{\text{trans}} + d_{\text{prop}})dend-to-end​=N(dproc​+dtrans​+dprop​)
    - dprocd_{\text{proc}}dproc​: processing delay

    - dtrans=LRd_{\text{trans}} = \frac{L}{R}dtrans​=RL​: transmission delay (packet size / rate)

    - dpropd_{{prop}}dprop​: propagation delay

- The equation generalizes earlier formulas by including all key delay components.
#### **Other End-to-End Delays**

- **Shared medium access delay** (e.g., in WiFi or cable).

- **Media packetization delay** (especially in **VoIP**): time to fill a packet with audio before sending.

### 1.4.4 Throughput in Computer Networks

Throughput in computer networks is a key performance metric that measures the rate at which data is successfully transferred from sender to receiver. It is often constrained by the **slowest (bottleneck) link** along the path or by **shared usage of links**, especially in access networks or when multiple transfers occur simultaneously.


- **Definition of Throughput**:

    - Instantaneous throughput: Rate (in bits/sec) at which the receiver gets data at any given moment.

    - Average throughput: Total file size (F bits) divided by total transfer time (T seconds), i.e., `F/T` bits/sec.

- **Application Requirements**:

    - **Low-latency & steady throughput** are important for real-time applications like VoIP or video calls.

    - **High throughput** is preferred for non-real-time applications like file downloads.

- **Two-link Example**:

    - Server ↔ Router (Rs), Router ↔ Client (Rc).

    - Throughput = `min{Rs, Rc}`; bottleneck link determines the throughput.

    - If Rs = 2 Mbps and Rc = 1 Mbps, throughput = 1 Mbps, so a 32 Mb file takes 32 seconds.

- **Multi-link Path**:

    - For N links: Throughput = `min{R1, R2, ..., RN}`.

    - The slowest link (bottleneck) along the path limits throughput.

- **Real-World Internet Example**:

    - Server and client have access links Rs and Rc.

    - Internet core has very high-capacity links.

    - Throughput is constrained by `min{Rs, Rc}`, not the core.

- **Shared Core Link Example**:

    - 10 server-client pairs using a shared core link with capacity R.

    - If R is high (>> Rs, Rc), throughput per transfer = `min{Rs, Rc}`.

    - If R is small (≈ Rs, Rc), throughput per transfer = `R/10`.

- **Important Insight**:

    - Throughput is not just about the path’s link capacities but also about **contention from other traffic**.

    - A link with high capacity can still be a bottleneck if shared by many flows.

## 1.5 Protocol Layers and Their Service Models
1.5.1 Layered Architecture:

### Protocol Layering
- **Protocol Layering Concept**:

    - Network protocols are organized into **layers** for structure and modularity.

    - Each layer provides services to the **layer above it**, forming a _service model_.

    - A layer performs functions within itself and uses the services of the **layer below**.

- **Layer Example**:

    - For instance, **layer n** may provide reliable delivery by using the **unreliable delivery** of **layer n−1** and adding error detection and retransmission.

- **Implementation**:

    - **Application-layer** and **transport-layer protocols** (e.g., HTTP, SMTP) are typically implemented in **software** on end systems.

    - **Physical** and **data link layers** are often implemented in **hardware** (e.g., NICs like Ethernet or WiFi).

    - The **network layer** is usually a **hybrid of hardware and software**.

    - A protocol layer is **distributed** across various network components (end systems, switches, etc.).

- **Advantages of Layering**:

    - Offers a **structured way** to discuss and design systems.

    - Promotes **modularity**, which simplifies updates and maintenance.

- **Drawbacks of Layering**:

    - **Duplication of functionality** (e.g., error recovery at multiple layers).

    - **Cross-layer dependencies**, where one layer needs information from another, violating separation.

- **Protocol Stack**:

    - A complete set of layered protocols is called a **protocol stack**.

    - The **Internet protocol stack** has **five layers**:

        - Physical

        - Link

        - Network

        - Transport

        - Application

    - The book uses a **top-down approach**, starting with the application layer.


### Application Layer
- The **application layer** contains **network applications** and their **protocols**.

- Common **Internet application-layer protocols** include:

    - **HTTP** – for web document requests and transfers.

    - **SMTP** – for sending email messages.

    - **FTP** – for file transfers between systems.

    - **DNS** – for translating domain names (e.g., `www.ietf.org`) into IP addresses.

- Application-layer protocols are **distributed across multiple end systems**.

    - One application's instance communicates with another using **messages** (application-layer data).

### Transport Layer

- The **transport layer** is responsible for **transferring application-layer messages** between endpoints.

- The Internet uses two main **transport protocols**:

    - **TCP (Transmission Control Protocol)**:

        - Provides a **connection-oriented** service.

        - Ensures **reliable delivery** of messages.

        - Includes **flow control** (matches sender/receiver speeds).

        - Breaks large messages into smaller **segments**.

        - Implements **congestion control** to manage network traffic.

    - **UDP (User Datagram Protocol)**:

        - Provides a **connectionless** service.

        - Offers **no reliability**, **no flow control**, and **no congestion control**.

        - Lightweight and minimal overhead.

- In this context, a **transport-layer packet** is called a **segment**.

### Network Layer
- The **network layer** is responsible for moving **datagrams** (network-layer packets) from source to destination.

- It receives **transport-layer segments** along with **destination addresses** and delivers them to the correct destination host.

- Key component: **IP (Internet Protocol)**:

    - Defines the **structure of datagrams**.

    - Dictates how **end systems and routers** handle these datagrams.

    - There is **only one IP protocol**, and it must run on all Internet-connected devices with a network layer.

- The network layer also includes various **routing protocols**:

    - Determine the **paths** datagrams take through the network.

    - Network administrators can choose routing protocols within their own networks.

- Commonly referred to as the **IP layer**, as IP is the central protocol unifying the Internet.


### Link Layer
- The **link layer** helps the **network layer** move datagrams **between adjacent nodes** (hosts or routers) along a route.

- At each hop:

    - The **network layer passes** the datagram to the link layer.

    - The **link layer delivers** it to the next node.

    - The next node’s link layer **passes it back up** to its network layer.

- The **services of the link layer** depend on the **specific link-layer protocol** used:

    - Some provide **reliable delivery** over a single link (different from TCP’s end-to-end reliability).

- Examples of **link-layer protocols**:

    - **Ethernet**

    - **WiFi**

    - **DOCSIS** (used in cable networks)

- **Multiple link-layer protocols** may be used along a single datagram’s path.

    - For example: Ethernet on one link, PPP on another.

- In this book, a **link-layer packet** is called a **frame**.

### Physical Layer
- The **physical layer** is responsible for moving **individual bits** within a frame from one node to the next.

- It works in conjunction with the **link layer**, which moves entire **frames** between adjacent nodes.

- Physical-layer protocols are:

    - **Link-dependent**.

    - Dependent on the **transmission medium** (e.g., copper wire, fiber optics).

- **Ethernet**, for example, has multiple physical-layer protocols:

    - One for **twisted-pair copper wire**.

    - Another for **coaxial cable**.

    - Another for **fiber optics**.

- Each protocol defines **how bits are transmitted** over the medium.



1.5.2 Encapsulation:
- **Encapsulation**: Wrapping data with headers at each protocol layer.

- **Layers**:

    - App → creates message

    - Transport → adds header (port info) → **segment**

    - Network → adds IP header → **datagram**

    - Link → adds MAC header → **frame**

- **At Receiver**: Each layer removes its header (decapsulation).

- **Devices**:

    - **Host**: all 5 layers

    - **Router**: layers 1–3 (reads IP)

    - **Switch**: layers 1–2 (reads MAC)

- **Analogy**: Memo → interoffice envelope → postal envelope → delivery

- **Payload = data from upper layer**

- Large messages may be split and reassembled.






## 1.6 Networks Under Attack
No Content for this section, check it book itself.
