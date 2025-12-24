# AutomotiveSWLearn
Embedded C++ Development in Automotive 

____Home Project 1 – C++ Sensor Abstraction Layer (SAL)__________________________________
Project Objective

Design and implement a modular, extensible C++17 Sensor Abstraction Layer that simulates automotive sensors (Camera, Radar, Lidar) and exposes their data in a thread-safe, real-time-aware manner.

This mimics the lower application / middleware boundary of an ADAS platform.
🎯 Completion Criteria

You are done when:
-->Code builds cleanly with -Wall -Wextra
-->No memory leaks (valgrind clean)
-->Threads start/stop reliably
-->README explains architectural decisions

*Here the required steps to master the project if you gonna re-code:*

**1. Functional Requirements (What it MUST do)**
FR-1: Generic Sensor Interface
FR-2: Sensor Types

    Implement at least three concrete sensors:

CameraSensor	Image frame (2D matrix)	30 Hz
RadarSensor	Object list (range, velocity)	20 Hz
LidarSensor	Point cloud	10 Hz

FR-3: Thread-Safe Data Delivery
Each sensor pushes data into a thread-safe queue.

FR-4: Data Ownership & Memory Safety
FR-5: Sensor Manager

**2. Non-Functional Requirements (Equally Important)**
NFR-1: Modern C++
C++17 minimum

NFR-2: Deterministic Timing
Each sensor must:
Use std::chrono::steady_clock
Sleep to maintain target frequency
Log if it misses a deadline

NFR-3: Clean Build System
Use CMake
No IDE-specific files

**3. Directory Structure**

**4. Main Program Behavior**

**5. Simulated Data Definitions**

**6. Documentation (README.md must include)**
