# Lab 4 - Notes

## Task 1

I saved the results and Excel file in the folder.

## Task 2 - Availability (One Repair Facility)

- The logic stays the same as in Task 1, but the repair capacity is limited.
- Transition Change: `S2​ -> S1​` rate becomes μ instead of 2μ, because only one server can be repaired at a time.

## Task 3

- The logic changes: reliability treats total failure as an absorbing state (S2​) where the system cannot return to an "Up" state
- Moreover, repair transitions are removed because repair is inhibited while the backup is operational
- This becomes a no repair model, similar to RBD

## Task 4 - Availability (Two Repair Facilities)

- Now, the system can be repaired while the backup is running, but S2​ remains an absorbing state for reliability
- This system will be more reliable than Task 3 because it can "recover" to S0​ before the second server fails
