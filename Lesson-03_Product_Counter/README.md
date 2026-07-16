# Lesson 03 – Product Counter using CTU

## Objective

Design a product counting system using the CTU (Count Up) function block. The conveyor automatically stops when five products have been counted.

---

## Industrial Application

This logic is commonly used in:

- Packaging machines
- Box filling systems
- Production counting
- Conveyor automation
- Batch processing

---

## Components

| Component | Type |
|-----------|------|
| ProductSensor | Normally Open (NO) |
| ResetBtn | Normally Open (NO) |
| CTU Counter | Count Up Function Block |
| BoxFull | Output Coil |
| ConveyorMotor | Output Coil |

---

## Working Principle

1. ProductSensor detects each passing product.
2. Every rising edge increments the CTU counter.
3. When the count reaches 5, CTU.Q becomes TRUE.
4. The BoxFull indicator turns ON.
5. The ConveyorMotor stops automatically.
6. Press ResetBtn to reset the counter and resume operation.

---

## Files

| File | Description |
|------|-------------|
| main.ld | OpenPLC Ladder Logic source code |

---

## Concepts Learned

- Count Up Counter (CTU)
- Rising Edge Detection
- Counter Inputs and Outputs (CU, R, PV, CV, Q)
- Industrial Product Counting
- Conveyor Stop Logic

---

## Software

- OpenPLC Editor (Latest Version)

---

## Status

✅ Completed

---

## Ladder Diagram

Industrial product counting circuit.

![Ladder Diagram](images/ladder.png)

---

## Simulation – Empty Box (CV = 0)

Conveyor running and waiting for products.

![CV = 0](images/count0.png)

---

## Simulation – Counting Products (CV = 4)

The conveyor continues running while the box is not yet full.

![CV = 4](images/count4.png)

---

## Simulation – Box Full (CV = 5)

The fifth product is detected, the BoxFull indicator turns ON, and the conveyor stops automatically.

![CV = 5](images/count5.png)

---

## Simulation – Reset

After replacing the full box, the operator presses ResetBtn. The counter resets to zero and the conveyor resumes operation.

![Reset](images/reset.png)
