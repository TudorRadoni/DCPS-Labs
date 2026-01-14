# Lab 3 – Notes

## Task 1 – Single Component

- **No redundancy:** The system fails when the single component fails.
- **Lowest reliability and availability.**
- Serves as the **baseline case**.

## Task 2 – One Operational Component + One Backup (1oo2)

- **Parallel redundancy** improves reliability and availability.
- System tolerates **one component failure**.
- Failure occurs **only if both components fail**.

## Task 3 – One Operational Component + Two Backups (1oo3)

- **Increased redundancy** further improves reliability.
- **Diminishing returns** compared to Task 2 (as seen in the previous lab as well).

## Task 4 – k-out-of-n System (2oo3)

- **Stricter operational requirement:** At least two components must be operational.
- Reliability is **lower than in Task 3**, but higher than in simpler systems.
- Trades **fault tolerance for guaranteed performance capacity**.

## Task 5 – Series–Parallel System

- One component is a **single point of failure**, combined with a parallel subsystem.
- **Reliability dominated by the series component.**
- Demonstrates how **mixed architectures balance simplicity and redundancy**.
