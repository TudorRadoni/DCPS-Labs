# Introductory Dependability Lab

## 1. Fault, Error, and Failure

**Dependability** relates to a system’s ability to perform its intended functions correctly and reliably. The 3 important concepts are:

- **Fault**: A physical or logical defect in the system.  
*Example:* A corrupted disk sector or a hardware short circuit.

- **Error**: An invalid internal system state caused by a fault.  
*Example:* An incorrect value read into memory from a damaged disk sector.

- **Failure**: A visible deviation from the system’s specified behavior.  
*Example:* An application crash or incorrect output.

**Example chain:** A corrupted disk sector (**Fault**) leads to an incorrect file read (**Error**), resulting in an application crash during a save operation (**Failure**).

## 2. Fault Types

- **Permanent fault**: A persistent defect that remains until the component is repaired or replaced.  
*Example:* A burned-out processor core.

- **Transient fault**: A temporary fault that disappears after a short time.  
*Example:* A bit flip caused by electromagnetic interference (or cosmic ray!).

- **Intermittent fault**: A recurring fault that appears and disappears unpredictably.  
*Example:* A loose cable causing sporadic connection failures.

## 3. Dependability Calculations

The cumulative distribution function (CDF) of the time to failure is given by:

`F_T(t) = 1 - 1 / (0.00003 * t^2 + 1)`

### a) Probability of failure by `t = 720 h`

```plaintext
0.00003 * 720^2 = 15.552
=> F_T(720) = 1 - 1 / (15.552 + 1)
= 1 - 1 / 16.552
= 0.93959 ~= 0.94
```

There is approximately a **94% probability** that the system will fail within the first 720 hours.

### b) Reliability at `t = 720 h`

```plaintext
R(t) = 1 - F_T(t)
R(720) = 1 - 0.94
~= 0.06
```

There is only a **6% probability** that the system remains operational after 720 hours.

### c) Failure rate lambda(t) at `t = 720 h`

The reliability function is:

`R(t) = 1 / (0.00003 * t^2 + 1)`

The failure rate is:

```plaintext
lambda(t) = (2 * 0.00003 * t) / (0.00003 * t^2 + 1)
lambda(720) = 0.0432 / 16.552 ~= 0.0026 failures/hour
```

This value represents the instantaneous failure rate at 720 hours.

### d) Mean Time To Failure (MTTF)

```plaintext
MTTF = integral from 0 to infinity of R(t) dt
MTTF = ∫₀^∞ [1 / (0.00003 * t^2 + 1)] dt
MTTF ~= 286.8 hours
```

The system is expected to operate for approximately **286.8 hours** before failure.

## 4. Steady-State Availability

Given:

- MTTF ~= 286.8 h
- MTTR = 24 h  

The steady-state availability `A` is calculated as:

```plaintext
A = MTTF / (MTTF + MTTR)
A = 286.8 / (286.8 + 24)
A ~= 0.92
```

The system is available and operational approximately **92% of the time** in steady state.
