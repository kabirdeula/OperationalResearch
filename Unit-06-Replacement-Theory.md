# Unit 06 - Replacement Theory

## Replacement of Items that fail completely

1. Individual replacement policy
2. Group replacement policy

P = M(t - 1) - M(t)/M(t - 1)

| t   | M(t) | Pi   |
| --- | ---- | ---- |
| 0   | 100  | -    |
| 1   | 94   | 0.06 |
| 2   | 82   | 0.12 |
| 3   | 58   | 0.24 |
| 4   | 40   | 0.18 |
| 5   | 28   | 0.12 |
| 6   | 19   | 0.09 |
| 7   | 13   | 0.06 |
| 8   | 7    | 0.06 |
| 9   | 3    | 0.04 |
| 10  | 0    | 0.03 |

# Following mortality rates have been observed for certain types of light bulbs.

| Time         | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| ------------ | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| No. of Bulbs | 100 | 94  | 82  | 58  | 40  | 28  | 19  | 13  | 7   | 3   | 0   |

calculate the probability of failure.

Pp = M(t - 1) - M(t) / N
Pi = 100 - 94 / 100 = 0.06

```
we can observe that average cost is minimum (Ps 1575) during the sixth year and then rises. Hence, the machine should be replaced after six years of its use.
```

2. Group Replacement Policy

Following mortality rates have been observed for a certain type of electronic component.

| Year                               | 0   | 1   | 2   | 3   | 4   | 5   | 6   |
| ---------------------------------- | --- | --- | --- | --- | --- | --- | --- |
| % surviving at the end of the year | 100 | 97  | 90  | 70  | 30  | 15  | 0   |

There are 10000 items in operation and it costs Re 1 to replace an individual item and 35 paise per item, if all items are replaced simultaneously, It is decided to replace all items at fixed intervals and to continue replacing individual items as and when they fail. At what interval shoulda ll items be replaced.

Soln,

| Year(Xi) | %Survived at the end of year | Prob. of failure(Pi) |
| -------- | ---------------------------- | -------------------- |
| 0        | 100                          | -                    |
| 1        | 97                           | 0.03                 |
| 2        | 90                           | 0.07                 |
| 3        | 70                           | 0.20                 |
| 4        | 30                           | 0.4                  |
| 5        | 15                           | 0.15                 |
| 6        | 0                            | 0.15                 |

Case 1 (Individual Replacement)

Expected Life = Summation Xi Pi

= 1 x 0.03 + 2 x 0.07 + 3 x 0.20 + 4 x 0.4 + 5 x 0.15 + 6 x 0.15
= 4.02 years

Therefore, Average no of replacement in each year = N\Av exp life

= 10000/4.02
= 2487.5
= 2488 items

Here average cost of yearly individual replacement policy
= 2488 x 1 = Rs. 2488

Ni denote the number of items replaced at the end of ith year

N0 = No. of items in the beginning = 10000

N1 = No of items during 1st year x prob of an item fails
= 10000 x 0.03 = 300

N2 = N0P2 + N1P1 = 10000 x 0.07 + 300 x 0.03 = 709

N3 = N0P3 + N1P2 + N2P1 = 10000 x 0.2 + 300 x 0.07 + 709 x 0.03 = 2042

N4 = N0P4 + N1P3 + N2P2 + N3P1 = 10000 x 0.4 + 340 x 0.2 + 709 x 0.07 + 2042 x 0.03 = 4171

N5 = N0P5 + N1P4 + N2P3 + N3P2 + N4P1 = 2030

N6 = N0P6 + N1P5 + N2P4 + N3P3 + N4P2 + N5P1 = 2590

| End of year | No. of year | Cum no of failure | Cost of rep after failure | Cost of all rep | TC   | Tave    |
| ----------- | ----------- | ----------------- | ------------------------- | --------------- | ---- | ------- |
| 1           | 300         | 300               | 300                       | 3500            | 3800 | 3800    |
| 2           | 709         | 1009              | 1009                      | 3540            | 4509 | 2254.5  |
| 3           | 2042        | 3051              | 3051                      | 3500            | 6551 | 2183.66 |

### 1.

The original cost of machine is Rs. 6200 and its scrap value is Rs. 200. The maintenance costs found from experience are as follows:

| Year             | 2014 | 2015 | 2016 | 2017 | 2018 | 2019 | 2020 | 2021 |
| ---------------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| Maintenance Cost | 100  | 250  | 400  | 600  | 900  | 1200 | 1600 | 2000 |

when should the machine be repaired

C = original cost, S = Scrap Value, M.C = Maintenance Cost

Tave = (Total Cost / No of years)

| Years of Service | Original Price - Scrap(C-S) | AMC  | Sum of AMC | Total Cost | Average AC |
| ---------------- | --------------------------- | ---- | ---------- | ---------- | ---------- |
| 1                | 6000                        | 100  | 100        | 6100       | 6100       |
| 2                | 6000                        | 250  | 350        | 6350       | 3175       |
| 3                | 6000                        | 400  | 750        | 6750       | 2250       |
| 4                | 6000                        | 600  | 1350       | 7350       | 18375      |
| 5                | 6000                        | 900  | 2250       | 8250       | 1650       |
| 6                | 6000                        | 1200 | 3450       | 9450       | 1575       |
| 7                | 6000                        | 1600 | 5050       | 11050      | 1578       |
| 8                | 6000                        | 2000 | 7000       | 13050      | 1631       |
