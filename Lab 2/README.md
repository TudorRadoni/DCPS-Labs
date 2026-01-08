# Lab 2 - Notes

## Task 3 - Intuition and Formulas

### Failure Rate from MTTF

`λ = 1 / MTTF`

*MTTF = "average life", failure rate = "how fast it dies"*

While MTTF (Mean Time To Failure) gives the average time until a system fails, the failure rate (λ) indicates how often failures occur over time. A higher MTTF results in a lower failure rate, meaning the system is more reliable.

### Reliability from Failure Rate

`R(t) = e ^ (-λ * t)`

*Probability the system is still alive after/at time t.*

Probability that a system will function without failure for a time period t. As time increases, the reliability decreases exponentially, especially with a higher failure rate.

### Parallel (backup) System Reliability

`R_parallel(t) = 1 - (1 - R(t))^n`

*System fails only if **all** components fail.*

In a parallel system with n identical components, the overall system reliability increases because the system continues to function as long as at least one component is operational. The more backups you have, the higher the reliability, **but with diminishing returns**.

### MTTR Note

**For reliability vs time, MTTR is ignored** since it focuses on uptime until failure, not repair time.

### Conclusion

- Adding backups always increases reliability
- Each extra backup helps less than the previous one
- Parallel redundancy is great for long missions
- But it has diminishing returns

## Task 4 - 1oo3 vs 2oo3

By increasing the number of required operational servers from one to two, the system becomes less reliable but guarantees higher operational capacity, trading fault tolerance for performance.
