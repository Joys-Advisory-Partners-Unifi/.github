# Joys Advisory Partners - UniFi Integration Suite

**A comprehensive solution for simplified access to the Ubiquiti UniFi API ecosystem**

---

## About

**Joys Advisory Partners** has developed a suite of open-source libraries and tools designed to simplify integration with Ubiquiti's UniFi network infrastructure. Our goal is to provide developers and home automation enthusiasts with clean, well-documented APIs that abstract away the complexity of the UniFi Controller's REST interface.

**Roger Joys**
*Managing Partner*

---

## Vision

The UniFi ecosystem offers powerful network management capabilities, but accessing these features programmatically can be challenging. Our solution provides:

- **Layered Architecture** - From low-level API access to high-level, device-centric abstractions
- **Smart Home Integration** - First-class support for HomeKit and other smart home platforms
- **Type Safety** - Strongly-typed interfaces that reduce errors and improve developer experience
- **Comprehensive Documentation** - Clear examples and API references for all components

---

## Project Suite

### Core Libraries

| Project | Description | Language |
|---------|-------------|----------|
| [JSONUtils](https://github.com/Joys-Advisory-Partners-Unifi/JSONUtils) | JSON parsing and navigation utilities | Java |
| [UnifiUtils](https://github.com/Joys-Advisory-Partners-Unifi/UnifiUtils) | Low-level UniFi Controller API wrapper (129 endpoints) | Java |
| [UniFiHomeKit](https://github.com/Joys-Advisory-Partners-Unifi/UnifiHomeKit) | High-level, device-centric API for smart home integration | Java |

### Applications

| Project | Description | Language |
|---------|-------------|----------|
| [homebridge-unifi-network](https://github.com/Joys-Advisory-Partners-Unifi/homebridge-unifi-network) | Homebridge plugin for Apple HomeKit integration | TypeScript |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Smart Home Platforms                      │
│              (Apple HomeKit, Home Assistant)                 │
├─────────────────────────────────────────────────────────────┤
│                 homebridge-unifi-network                     │
│            (Homebridge Plugin - TypeScript)                  │
├─────────────────────────────────────────────────────────────┤
│                     UniFiHomeKit                             │
│     (Device-centric API: Device, Client, SiteHealth)        │
├─────────────────────────────────────────────────────────────┤
│                      UnifiUtils                              │
│         (Low-level API wrapper - 129 endpoints)             │
├─────────────────────────────────────────────────────────────┤
│                      JSONUtils                               │
│              (JSON parsing and navigation)                   │
├─────────────────────────────────────────────────────────────┤
│               UniFi Controller REST API                      │
│                  (Ubiquiti Infrastructure)                   │
└─────────────────────────────────────────────────────────────┘
```

---

## Key Features

### Presence Detection
Track device connectivity for home automation triggers. Know when family members arrive or leave based on their phone's network connection.

### Device Monitoring
Monitor the health and status of your network infrastructure - access points, switches, and gateways - with real-time updates exposed to HomeKit.

### Network Control
Enable or disable wireless networks, restart devices, and manage client access directly from your smart home interface.

### Internet Health
Monitor WAN status, latency, and speed test results as HomeKit-accessible sensors.

---

## Getting Started

### Prerequisites

- Java 21 or later
- Node.js 18+ (for Homebridge plugin)
- UniFi Controller with API access enabled
- Maven (for building Java libraries)

### Quick Start

```bash
# Clone and build the core libraries
cd JSONUtils && mvn clean install
cd ../UnifiUtils && mvn clean install
cd ../UniFiHomeKit && mvn clean install

# Install the Homebridge plugin
cd ../homebridge-unifi-network
npm install
npm run build
```

---

## License

All projects in this suite are licensed under the **Apache License 2.0**.

See individual project LICENSE files for details.

---

## Contributing

We welcome contributions from the community. Please see individual project README files for specific contribution guidelines.

---

## Contact

**Joys Advisory Partners**

For inquiries regarding this project suite or consulting services, please reach out to Roger.Joys@JoysAdvisoryPartners.com or through the GitHub repository.

---

*Copyright 2026 Roger Joys / Joys Advisory Partners. All rights reserved.*
