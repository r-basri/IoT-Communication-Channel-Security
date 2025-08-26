# IoT-Communication-Channel-Security (Publication Link for Citation: https://www.sciencedirect.com/science/article/pii/S0167739X25000093)
# IoT Lab Development Research Team: Mohammad Mahabub Alam, Rabeya Basri, Prof. Gour Karmakar

## Overview
This repository introduces a new conceptual model named **IPCTCM (Instantaneous Trust Calculation Model)** for detecting **Man-in-the-Middle (MITM) attacks** in IoT communication networks. **IPCTCM** leverages the **end-to-end (E2E) delay** induced by active MITM attacks as a key characteristic for instantaneous trust calculation of IoT communication channels. Since active MITM attacks often incur noticeable delays, monitoring and analyzing E2E delay provides an effective approach for accurate and spontaneous detection.

To estimate the expected E2E delay under normal conditions (without attacks), I utilize two popular time-series estimation techniques:
1. **Kalman Filter**
2. **LSTM (Long Short-Term Memory)**

## Experimentation Environment
The experiments were conducted in a **LoRa-based IoT sensor network** in the **IoT Lab at Federation University Australia**. LoRa (Long Range) is ideally suited for low-power, long-range communication between end devices (e.g., sensors), gateways, and servers. 

### Testbed Configuration
Initially, the testbed consisted of a single LoRa node. To make the setup more versatile and reflective of real-world IoT environments, I expanded the testbed by including **three additional LoRa nodes**. This extension allowed me to simulate various factors, such as:
- **Network congestion**
- **Varying data transmission rates**
- **Hardware limitations**

### Data Transmission Rates and Channel Capacity
The experiments considered various data transmission intervals and LoRa data rates (DRs) with their respective spreading factors (SFs). Some of the intervals and rates exceeded the LoRa channel capacity, highlighting hardware limitations. Here are the key configurations:

### Network Congestion Scenarios
Two network congestion scenarios were simulated:
- **4/1**: Four nodes contending for one active LoRa channel.
- **4/2**: Four nodes contending for two active LoRa channels.

- **Transmission Intervals and Rates**:
- For **1 node-1 channel**:
  - 1ms (272,000 bps)
  - 30ms (9,066.67 bps)
  - 50ms (5,440 bps)
  - 100ms (2,720 bps)
  - 2 minutes (2.27 bps)
- For **4/1 & 4/2**:
  - 2 minutes (9.07 & 4.53 bps)
    
- **LoRa Channel Capacities**:
  - DR5/SF7: 5,470 bps
  - DR3/SF9: 1,760 bps

### Metrics and Analysis
The experiments measured several key metrics:
1. **Estimated Expected E2E Delay**:
   - Represents normal conditions without attacks.
2. **Attack Detection Accuracy**:
   - Indicates how accurately the model detects active MITM attacks.
3. **Trust Sensitivity Score (TSS)**:
   - Reflects the model’s sensitivity to variations in E2E delay caused by attacks.
4. **False Alarms**:
   - Includes both false positives and false negatives.

### Results
The experiments demonstrate the following:
- The **accuracy of E2E delay estimation** directly impacts the detection of MITM attacks. 
- The **trust sensitivity metric (TSS)** indicates how well the model adapts to varying network conditions and detects attacks.
- High transmission rates and network congestion significantly influence the **false alarm rate**, **attack detection accuracy**, and overall system performance.

## Key Contributions
- Developed the **IPCTCM model** to calculate instantaneous trust for IoT communication channels based on E2E delay.
- Used **Kalman Filter** and **LSTM** to estimate normal E2E delay and detect deviations caused by MITM attacks.
- Conducted experiments with a **LoRa-based IoT testbed** under various configurations, including network congestion, varying transmission rates, and hardware limitations.
