# Lesson 01 – Start/Stop Motor using Ladder Logic

## Objective

Design a basic motor Start/Stop control circuit using Ladder Logic with seal-in (latching) functionality.

---

## Industrial Application

This logic is commonly used in:

- Conveyor belt motors
- Water pumps
- Industrial fans
- Compressors
- Production machines

---

## Components

| Component | Type |
|-----------|------|
| Start Push Button | Normally Open (NO) |
| Stop Push Button | Normally Closed (NC) |
| Motor Coil | Output |
| Seal-in Contact | Normally Open |

---

## Working Principle

1. Press **Start**.
2. The motor energizes.
3. The seal-in contact keeps the motor ON after releasing the Start button.
4. Press **Stop**.
5. The motor de-energizes immediately.

---

## Files

| File | Description |
|------|-------------|
| `main.ld` | OpenPLC Ladder Logic source code |

---

## Concepts Learned

- Normally Open (NO) Contact
- Normally Closed (NC) Contact
- Output Coil
- Seal-in (Latching) Logic
- PLC Scan Cycle

---

## Software

- OpenPLC Editor 

---

## Status

✅ Completed

## Ladder Diagram

Implementation of a basic motor start/stop control circuit using seal-in (latching) logic.

![Ladder Diagram](Images/ladder_diagram.png)

---

## Simulation - Motor Running

Motor energized after pressing the Start push button.

![Motor Running](Images/simulation_motor_on.png)

---

## Simulation - Motor Stopped

Motor de-energized after pressing the Stop push button.

![Motor Stopped](Images/simulation_motor_off.png)
