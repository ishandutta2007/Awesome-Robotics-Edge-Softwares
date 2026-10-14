# Awesome-Robotics-Edge-Softwares

# Top Robotics Edge Software Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Edge AI Inference, Real-Time Control & Hardware-Agnostic Deployment*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Robotics Edge Software**. These tools enable robots to process sensor data, run AI models, and execute control loops directly on edge hardware — reducing latency, preserving bandwidth, and maintaining operation when cloud connectivity is unavailable.

**Examples** include NVIDIA Isaac OS, Micro-ROS, eProsima Fast DDS, Canonical Ubuntu Core, NEPI by Numurus, Edge Impulse, AWS IoT Greengrass, Balena, ADLINK Edge, and Hivecell (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom inference pipelines, and transparent edge orchestration — ideal for robotics engineers prioritizing control, researchers building edge AI stacks, and teams avoiding cloud dependency.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[NVIDIA Isaac OS](https://developer.nvidia.com/isaac)**  
  Edge AI operating system layer for robotics with GPU-accelerated perception, model deployment, and real-time control. Provides Isaac ROS packages for hardware-accelerated perception and navigation.

- **[Micro-ROS](https://micro-ros.github.io/)**  
  Brings ROS 2 to microcontrollers and embedded devices with a lightweight client library. Enables resource-constrained robots to participate in ROS 2 networks without full middleware overhead. Open-source core with commercial support options.

- **[eProsima Fast DDS](https://www.eprosima.com/)**  
  High-performance DDS middleware for real-time edge communication. Default ROS 2 middleware with ~30% lower inter-process latency than Cyclone DDS. Commercial support available.

- **[Canonical Ubuntu Core](https://ubuntu.com/core)**  
  Transactional, snap-based OS for edge devices and robots with OTA updates, secure boot, and app confinement. Enterprise support and device management available.

- **[NEPI by Numurus](https://numurus.com/)**  
  Source-available edge AI platform built on ROS/ROS2 providing ~90% of foundational software for smart systems. Hardware-agnostic with drivers, AI model management, and browser-based UI. Runs fully at the edge with no cloud dependency. Commercial licensing for production deployments. 

- **[Edge Impulse](https://www.edgeimpulse.com/)**  
  Edge AI development platform for deploying ML models to microcontrollers and edge devices. Supports model training, optimization, and deployment to robotics hardware.

- **[AWS IoT Greengrass](https://aws.amazon.com/greengrass/)**  
  Edge runtime for AWS cloud services with local compute, messaging, and ML inference. Bridges ROS 2 systems to AWS for fleet management and data ingestion.

- **[Balena](https://www.balena.io/)**  
  IoT device fleet management platform with container-based updates, device monitoring, and edge orchestration for robotics deployments.

- **[ADLINK Edge](https://www.adlinktech.com/)**  
  Edge computing platform with hardware and software for industrial robotics, including ROS 2 integration and edge AI capabilities.

- **[Hivecell](https://hivecell.com/)**  
  Edge-as-a-Service platform providing managed compute at the edge for robotics and industrial applications.

## Open-Source GitHub Projects

- **[NexusOS](https://pypi.org/project/nexusos-robotics/)**  
  Universal OS and fleet middleware for heterogeneous robots, solving the "Tower of Babel" through zero-dependency hardware abstraction. Unifies multi-vendor fleets (mobile rovers, arms, quadrupeds, drones) under standardized messaging, control, and safety. Features asynchronous Python HAL plugin architecture (Serial, CAN, Modbus, ROS 2, MicroPython), Protobuf/WebSocket/gRPC transport, FastAPI cloud backend, and glassmorphic web dashboard with 2D pose trajectory and teleoperation. Docker Compose orchestration. 

- **[HORUS](https://pypi.org/project/horus-robotics/)**  
  Ultra-low latency robotics framework in Rust with Python bindings. Claims **87ns IPC latency and 12M+ messages/second throughput** — 100x faster than ROS 2. Zero-copy shared memory transport, type-safe message validation, cross-language interoperability (Rust/C++/Python), and real-time priority-based scheduling with deadline guarantees. Apache 2.0 licensed. 

- **[TinyEdge Runtime](https://pypi.org/project/tinyedge-runtime/)**  
  Open-source execution kernel and strategy SDK for running model-driven workloads on edge devices and robots. Provides strict versioned contracts, side-effect-free compatibility resolution, and deterministic fail-closed lifecycle. Implements synchronous `local_sync_v1` strategy, standard-library-only and device-free. Defines neutral physical-system manifest, sequential protocol, and terminal run-record contracts. 

- **[robot-lidar-fusion](https://pypi.org/project/robot-lidar-fusion/)**  
  Deterministic control loop running at configurable frequency (default 100 Hz) with strict cycle-time enforcement. Features sub-100ms LiDAR/camera sensor fusion, hardware-agnostic control stack with mock backend, multi-signal hazard manager (proximity, voltage, gas, pedestrian), fault detection, mission planning with A*-ready navigation, power management with thermal profiles, and predictive state estimation. Supports both ROS2 topic subscription and direct vendor SDK ingestion. 

- **[Dora (dora-rs)](https://github.com/dora-rs/dora)**  
  Robotics dataflow framework and distributed orchestrator for edge AI pipelines. Supports multi-language nodes (Rust, Python, C, C++) with zero-copy shared-memory transport and columnar formats for minimal latency on large payloads. Includes bidirectional bridges to external ecosystems. Rust-based.

- **[Links and Nodes (LN)](https://gitlab.com/links_and_nodes/ln)**  
  Open-source middleware for distributed real-time robotic systems from DLR. Combines process management with fast publish/subscribe messaging and request/response services. Complex multi-process systems reproduced from one text file. Developed since 2010, released 2015. Supports deterministic behavior and low-latency communication across hosts and languages. 

- **[Open-RAIL](https://github.com/CMCC-TAO/open-rail)**  
  Middleware from China Mobile linking Vision-Language-Action (VLA) and World-Action Models (WAM) to real robot hardware. Three-thread asynchronous pipeline (observation, inference, control) with two-level online smoothing. Hardware abstraction layer standardizes control, state reading, and action execution. Adapting new VLA/WAM models requires ~50-100 lines of code. Apache 2.0 licensed.

- **[SONNY OS](https://github.com/JackTrainer/Sonny)**  
  Ultra-lightweight microkernel for any robot (arms, AMRs, drones, humanoids). Built in Rust and Zenoh, positioned as ROS 2 replacement eliminating memory leaks and latency. JSON-based hardware abstraction layer, WASM sandbox for skill execution, real-time hard-watchdog monitoring sub-millisecond jitter. Supports KUKA, Comau, Universal Robots, Franka Emika, Luwu Dynamics XGO, and standard AMRs. AGPLv3 licensed.

- **[LeRobot](https://github.com/huggingface/lerobot)**  
  Hugging Face's ML library for real-world robotics in PyTorch. Provides datasets, pretrained models, and training utilities for imitation learning and robot policies. Supports edge deployment of vision-language-action models.

- **[Edge Impulse CLI](https://github.com/edgeimpulse/edgeimpulse-cli)**  
  Command-line tools for deploying Edge Impulse models to edge devices, including microcontrollers and single-board computers.

- **[Balenalib](https://github.com/balena-io/balena-cli)**  
  CLI and SDK for Balena device fleet management, enabling container-based edge deployments and OTA updates.

- **[GreenGrass CLI](https://github.com/aws/aws-iot-greengrass-cli)**  
  AWS Greengrass command-line interface for managing edge deployments, components, and local Lambda functions.

### Additional Strong Open-Source Options

- **[Open-RMF](https://github.com/open-rmf/rmf)** — Open Robot Management Framework for multi-fleet robot coordination at the edge. 
- **[openTCS](https://github.com/openTCS/opentcs)** — Transport control system for coordinating fleets of autonomous vehicles. 
- **[Micro-ROS for Arduino](https://github.com/micro-ROS/micro_ros_arduino)** — Micro-ROS fork available in Arduino Library Manager for microcontroller robotics. 
- **rclcpp / rclpy** — Official C++ and Python client libraries for building ROS 2 edge nodes. 
- **SROS2** — Security framework providing authentication, encryption, and access control for ROS 2 edge communications. 
- **ros2_medkit** — Structured fault management for ROS 2 with persistent fault lifecycle, REST/SSE API, and root cause correlation. 

**Frameworks for building custom systems**: Combine **HORUS** or **NexusOS** for ultra-low-latency edge communication, **TinyEdge Runtime** for deterministic model-driven workloads, **robot-lidar-fusion** for sensor fusion and control loops, **Dora** for dataflow orchestration, and **Open-RAIL** or **LeRobot** for deploying VLA models to robot hardware to build a complete self-hosted robotics edge stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Robotics edge software must comply with safety regulations, real-time constraints, and applicable industry standards. Edge deployments require validation against target hardware before operational use.
- Self-hosted open-source solutions require proper hardware selection, thermal management, and real-time performance validation.

---

**Made for robotics engineers, edge AI developers, embedded systems teams, and developers building autonomous systems infrastructure.**  
Let's make robotics edge software more open, performant, and hardware-agnostic.
