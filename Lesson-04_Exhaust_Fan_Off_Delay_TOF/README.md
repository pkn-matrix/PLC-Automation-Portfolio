# Lesson 04 - Exhaust Fan Off-Delay System (TOF)

## Objective

Design an industrial cooling system where the machine stops immediately when the operator presses the STOP button, while the exhaust fan continues running for 10 seconds before turning OFF.

---

## Industrial Application

This logic is commonly used in:

- CNC Machines
- Welding Stations
- Industrial Ovens
- Compressor Rooms
- Electrical Control Panels

The cooling fan removes residual heat after the machine has stopped.

---

## Components Used

Inputs
- Start Push Button
- Stop Push Button

Outputs
- Machine
- Exhaust Fan

PLC Instruction
- TOF (Off Delay Timer)

Preset Time
- 10 Seconds

---

## Working Principle

1. Press START.
2. Machine starts immediately.
3. Exhaust fan starts immediately.
4. Press STOP.
5. Machine stops immediately.
6. Exhaust fan continues running for 10 seconds.
7. Fan turns OFF automatically after the delay.

---

## Files

- main.ld
- Ladder Diagram
- Simulation Screenshots

---

## Concepts Learned

- TOF (Off Delay Timer)
- Seal-In (Latching)
- Output Delay Logic
- Industrial Cooling Sequence
- Timer-Based Automation

---

## Software

- OpenPLC Editor
- Ladder Logic (IEC 61131-3)

---

## Status

✅ Completed

---

---

## Ladder Diagram

### Ladder Logic

This ladder program implements an industrial exhaust fan control system using an Off-Delay Timer (TOF). The machine starts and stops immediately, while the exhaust fan continues operating for 10 seconds after the machine stops.

![Ladder Diagram](images/ladder.png)

---

## Simulation

### 1. Machine Running

The operator presses the START push button. The machine starts immediately, and the exhaust fan also starts running.

![Machine Running](images/machine_running.png)

---

### 2. STOP Button Pressed

The STOP button is pressed. The machine stops immediately, while the TOF begins its off-delay timing.

![STOP Pressed](images/stop_pressed.png)

---

### 3. Fan Running During Delay

Although the machine has already stopped, the exhaust fan continues operating while the TOF counts the preset delay time.

![Fan Delay](images/fan_delay.png)

---

### 4. Fan Stops After 10 Seconds

After the 10-second off-delay expires, the TOF output becomes FALSE and the exhaust fan turns OFF automatically.

![Fan Stopped](images/fan_stopped.png)
