# Lesson 02 – TON (On-Delay Timer)

## Objective

Design a motor control circuit that starts the motor only after a 5-second delay using the TON (On-Delay Timer) function block.

---

## Industrial Application

This logic is commonly used in:

- Conveyor systems
- Pump startup delay
- Industrial fans
- Compressors
- Machine safety startup sequence

---

## Components

| Component | Type |
|-----------|------|
| Start Push Button | Normally Open (NO) |
| Stop Push Button | Normally Closed (NC) |
| RunCmd | Internal Memory Bit |
| TON Timer | On-Delay Timer |
| Motor | Output Coil |

---

## Working Principle

1. Press **Start**.
2. `RunCmd` latches and remains TRUE.
3. The TON timer starts counting.
4. After 5 seconds, the timer output (`Q`) becomes TRUE.
5. The Motor turns ON.
6. Press **Stop** to reset `RunCmd`, stop the timer, and turn the Motor OFF.

---

## Files

| File | Description |
|------|-------------|
| `main.ld` | OpenPLC Ladder Logic source code |

---

## Concepts Learned

- Internal Memory Bit (`RunCmd`)
- TON (On-Delay Timer)
- Timer Inputs and Outputs (`IN`, `PT`, `ET`, `Q`)
- Structured Multi-Rung PLC Programming

---

## Software

- OpenPLC Editor (Latest Version)

---

## Status

✅ Completed

---

## Ladder Diagram

Implementation of a motor start circuit using a latched Run Command and TON timer.

![Ladder Diagram](Images/ladder_diagram.png)

---

## Simulation - Timer Running

Timer counting before the motor starts.

![Timer Running](Images/simulation_timer_running.png)

---

## Simulation - Motor Running

Motor turns ON after the timer reaches 5 seconds.

![Motor Running](Images/simulation_motor_running.png)
