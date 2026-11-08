# Baseline: the base-3 set

The 15 integers in 1..50 whose base-3 digits contain no 2:

1, 3, 4, 9, 10, 12, 13, 27, 28, 30, 31, 36, 37, 39, 40

No three of them form an arithmetic progression: if a + c = 2b, add the base-3 digits of a and c column by column. Each digit of a and c is 0 or 1, so no column carries, and every digit of 2b is 0 or 2. That forces each digit of a to equal the matching digit of c, so a = c. All 15 are distinct and lie in 1..50, so the set has size 15.
