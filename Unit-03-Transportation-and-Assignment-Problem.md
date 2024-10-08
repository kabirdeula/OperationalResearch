## Unbalanced Transportation Problem

if( Demand > Supply )
Sumbj > sumqi

add a dummy row with cost zero and supply equals to (demand - supply)

else
adda dummy column with cost and demand equals to (supply demand)

|        | P   | Q   | R   | S   | Supply  |
| :----- | :-- | :-- | :-- | :-- | :------ |
| A      | 3   | 5   | 7   | 8   | 100     |
| B      | 4   | 3   | 1   | 2   | 80      |
| C      | 5   | 6   | 2   | 4   | 70      |
| Demand | 50  | 70  | 80  | 10  | 250\210 |

|        | P   | Q   | R   | S   | Dummy | Supply |
| :----- | :-- | :-- | :-- | :-- | ----- | :----- |
| A      | 3   | 5   | 7   | 8   | 0     | 100    |
| B      | 4   | 3   | 1   | 2   | 0     | 80     |
| C      | 5   | 6   | 2   | 4   | 0     | 70     |
| Demand | 50  | 70  | 80  | 10  | 40    | 250    |

Using VAM,

|        | P   | Q   | R   | S   | Dummy       | Supply        | Diff |
| :----- | :-- | :-- | :-- | :-- | ----------- | :------------ | ---- |
| A      | 3   | 5   | 7   | 8   | **0⁴⁰**     | 100 - 40 = 60 | 3    |
| B      | 4   | 3   | 1   | 2   | 0           | 80            | 1    |
| C      | 5   | 6   | 2   | 4   | 0           | 70            | 2    |
| Demand | 50  | 70  | 80  | 10  | 40 - 40 = 0 | 250           |      |
| Diff   | 1   | 2   | 1   | 2   | 0           |               |      |

|        | P   | Q   | R   | S           | Supply       | Diff |
| :----- | :-- | :-- | :-- | :---------- | :----------- | ---- |
| A      | 3   | 5   | 7   | 8           | 60           | 2    |
| B      | 4   | 3   | 1   | **2¹⁰**     | 80 - 10 = 70 | 1    |
| C      | 5   | 6   | 2   | 4           | 70           | 2    |
| Demand | 50  | 70  | 80  | 10 - 10 = 0 | 250          |      |
| Diff   | 1   | 2   | 1   | 2           |              |      |

|        | P   | Q   | R            | Supply     | Diff |
| :----- | :-- | :-- | :----------- | :--------- | ---- |
| A      | 3   | 5   | 7            | 60         | 2    |
| B      | 4   | 3   | 1            | 70         | 2    |
| C      | 5   | 6   | **2⁷⁰**      | 70- 70 = 0 | 3    |
| Demand | 50  | 70  | 80 - 70 = 10 | 250        |      |
| Diff   | 1   | 2   | 1            |            |      |

|        | P   | Q   | R           | Supply       | Diff |
| :----- | :-- | :-- | :---------- | :----------- | ---- |
| A      | 3   | 5   | 7           | 60           | 2    |
| B      | 4   | 3   | **1¹⁰**     | 70 - 10 = 60 | 2    |
| Demand | 50  | 70  | 10 - 10 = 0 | 250          |      |
| Diff   | 1   | 2   | 6           |              |      |

|        | P       | Q   | Supply       | Diff |
| :----- | :------ | :-- | :----------- | ---- |
| A      | **3⁵⁰** | 5   | 60 - 50 = 10 | 2    |
| B      | 4       | 3   | 60           | 1    |
| Demand | 50      | 70  | 250          |      |
| Diff   | 1       | 2   |              |      |

|        | Q                | Supply      | Diff |
| :----- | :--------------- | :---------- | ---- |
| A      | **5¹⁰**          | 10 - 10 = 0 | 2    |
| B      | **3⁶⁰**          | 60 - 60 = 0 | 1    |
| Demand | 70 - 10 - 60 = 0 |             |      |
| Diff   | 2                |             |      |

|     | P       | Q       | R       | S       | Dummy   |
| :-- | :------ | :------ | :------ | :------ | ------- |
| A   | **3⁵⁰** | **5¹⁰** | 7       | 8       | **0⁴⁰** |
| B   | 4       | **3⁶⁰** | **1¹⁰** | **2¹⁰** | 0       |
| C   | 5       | 6       | **2⁷⁰** | 4       | 0       |

No. of Allocation = m + n - 1
7 = 7

### 1

|     | P   | Q   | R   | S          |             |
| --- | --- | --- | --- | ---------- | ----------- |
| A   | 3   | 1   | 7   | 4          | 50          |
| B   | 2   | 6   | 5   | 9          | 40          |
| C   | 8   | 3   | 3   | **2¹⁰**    | 10 - 10 = 0 |
|     | 20  | 15  | 10  | 55-10 = 45 |             |

Using Least Cost Method

second table

|     | P   | Q   | R           | S   |            |
| --- | --- | --- | ----------- | --- | ---------- |
| A   | 3   | 1   | 7           | 4   | 50         |
| B   | 2   | 6   | **5¹⁰**     | 9   | 40-10 = 30 |
|     | 20  | 15  | 10 - 10 = 0 | 45  |            |

third table

|     | P   | Q           | S   |            |
| --- | --- | ----------- | --- | ---------- |
| A   | 3   | **1¹⁵**     | 4   | 50-15 = 35 |
| B   | 2   | 6           | 9   | 30         |
|     | 20  | 15 - 15 = 0 | 45  |            |

fourth table

|     | P           | S   |            |
| --- | ----------- | --- | ---------- |
| A   | 3           | 4   | 35         |
| B   | **2²⁰**     | 9   | 30-20 = 10 |
|     | 20 - 20 = 0 | 45  |            |

fifth table

|     | S                |             |
| --- | ---------------- | ----------- |
| A   | **4³⁵**          | 35 - 35 = 0 |
| B   | **9¹⁰**          | 10 - 10 = 0 |
|     | 45 - 10 - 35 = 0 |             |

|     | P       | Q       | R       | S       |
| --- | ------- | ------- | ------- | ------- |
| A   | 3       | **1¹⁵** | 7       | **4³⁵** |
| B   | **2²⁰** | 6       | **5¹⁰** | **9¹⁰** |
| C   | 8       | 3       | 3       | **2¹⁰** |

```
No. of Allocation = m + n - 1
6 = 6

Total cost = 2 x 10 + 9 x 10 + 4 x 35 + 5 x 10 + 1 x 15 + 2 x 20
Total cost = 355
```

|     | P       | Q       | R       | S       |     |         |
| --- | ------- | ------- | ------- | ------- | --- | ------- |
| A   | 3       | **1¹⁵** | 7       | **4³⁵** | 50  | u₀ = -5 |
| B   | **2²⁰** | 6       | **5¹⁰** | **9¹⁰** | 40  | u₁ = 0  |
| C   | 8       | 3       | 3       | **2¹⁰** | 10  | u₂ = -7 |
|     | 20      | 15      | 10      | 55      |     |         |
|     | v₀ = 2  | v₁ = 6  | v₂ = 5  | v₃ = 9  |

Formula

```
cᵢⱼ = uᵢ + vⱼ

c₂₁ = u₁ + v₀ ⇒ 2 = 0 + v₀ ⇒ v₀ = 2
c₂₃ = u₁ + v₂ ⇒ 5 = 0 + v₂ ⇒ v₂ = 5
c₂₄ = u₁ + v₃ ⇒ 9 = 0 + v₃ ⇒ v₃ = 9
c₁₄ = u₀ + v₃ ⇒ 4 = u₀ + 9 ⇒ u₀ = -5
c₁₂ = u₀ + v₁ ⇒ 1 = -5 + v₁ ⇒ v₁ = 6
c₃₄ = u₂ + v₃ ⇒ 2 = u₂ + 9 ⇒ u₂ = -7
```

for unallocated cell

```
Δᵢⱼ = cᵢⱼ - (uᵢ + vⱼ)
Δ₁₁ = 3 - (-5 + 2) ⇒ 3 - (-3) ⇒ 6
Δ₁₃ = 7 - (-5 + 5) ⇒ 7
Δ₂₂ = 6 - (0 + 6) ⇒ 0
Δ₃₁ = 8 - (-7 + 2) ⇒ 8 - (-5) ⇒ 13
Δ₃₂ = 3 - (-7 + 6) ⇒ 3 - (-1) ⇒ 4
Δ₃₃ = 3 - (-7 + 5) ⇒ 3 - (-2) ⇒ 5
```

### 2

|        | P   | Q   | R   | S   | Supply |
| ------ | --- | --- | --- | --- | ------ |
| A      | 3   | 1   | 2   | 4   | 250    |
| B      | 12  | 6   | 5   | 9   | 350    |
| C      | 18  | 3   | 3   | 2   | 400    |
| Demand | 200 | 300 | 350 | 150 |        |

using least cost,

|        | P   | Q            | R   | S   | Supply        |
| ------ | --- | ------------ | --- | --- | ------------- |
| A      | 3   | **1²⁵⁰**     | 2   | 4   | 250 - 250 = 0 |
| B      | 12  | 6            | 5   | 9   | 350           |
| C      | 18  | 3            | 3   | 2   | 400           |
| Demand | 200 | 300-250 = 50 | 350 | 150 |               |

|        | P   | Q   | R   | S             | Supply        |
| ------ | --- | --- | --- | ------------- | ------------- |
| B      | 12  | 6   | 5   | 9             | 350           |
| C      | 18  | 3   | 3   | **2¹⁵⁰**      | 400-150 = 250 |
| Demand | 200 | 50  | 350 | 150 - 150 = 0 |               |

|        | P   | Q           | R   | Supply       |
| ------ | --- | ----------- | --- | ------------ |
| B      | 12  | 6           | 5   | 350          |
| C      | 18  | **3⁵⁰**     | 3   | 250-50 = 200 |
| Demand | 200 | 50 - 50 = 0 | 350 |              |

|        | P   | R               | Supply        |
| ------ | --- | --------------- | ------------- |
| B      | 12  | 5               | 350           |
| C      | 18  | **3²⁰⁰**        | 200 - 200 = 0 |
| Demand | 200 | 350 - 200 = 150 |               |

|        | P             | R             | Supply              |
| ------ | ------------- | ------------- | ------------------- |
| B      | **12²⁰⁰**     | **5¹⁵⁰**      | 350 - 200 - 150 = 0 |
| Demand | 200 - 200 = 0 | 150 - 150 = 0 |                     |

|     | P         | Q        | R        | S        |
| --- | --------- | -------- | -------- | -------- |
| A   | 3         | **1²⁵⁰** | 2        | 4        |
| B   | **12²⁰⁰** | 6        | **5¹⁵⁰** | 9        |
| C   | 18        | **3⁵⁰**  | **3²⁰⁰** | **2¹⁵⁰** |

```
No. of Allocation = m + n - 1
6 = 6

Total cost = (1 x 250) + (12 x 200) + (5 x 150) + (3 x 50) + (3 x 200) + (2 x 150)
Total cost = 4450
```

using MODI

|     | P         | Q        | R        | S        |         |
| --- | --------- | -------- | -------- | -------- | ------- |
| A   | 3         | **1²⁵⁰** | 2        | 4        | u₀ = -2 |
| B   | **12²⁰⁰** | 6        | **5¹⁵⁰** | 9        | u₁ = 2  |
| C   | 18        | **3⁵⁰**  | **3²⁰⁰** | **2¹⁵⁰** | u₂ = 0  |
|     | v₀ = 10   | v₁ = 3   | v₂ = 3   | v₃ = 3   |         |

```
cᵢⱼ = uᵢ + vⱼ

c₃₂ = u₂ + v₁ ⇒ 3 = 0 + v₁ ⇒ v₁ = 3
c₃₃ = u₂ + v₂ ⇒ 3 = 0 + v₂ ⇒ v₂ = 3
c₃₄ = u₂ + v₃ ⇒ 2 = 0 + v₃ ⇒ v₃ = 2
c₁₂ = u₀ + v₁ ⇒ 1 = u₀ + 3 ⇒ u₀ = -2
c₂₃ = u₁ + v₂ ⇒ 5 = u₁ + 3 ⇒ u₁ = 2
c₂₁ = u₁ + v₀ ⇒ 12 = 2 + v₀ ⇒ v₀ = 10
```

for unallocated cell

```
Δᵢⱼ = cᵢⱼ - (uᵢ + vⱼ)

Δ₁₁ = 3  - (-2 + 10) ⇒ 3 - 8 ⇒ -5
Δ₁₃ = 2 - (-2 + 3) ⇒ 2 - 1 ⇒ 1
Δ₁₄ = 4 - (-2 + 3) ⇒ 4 - 1 ⇒ 3
Δ₂₂ = 6 - (2 + 3) ⇒ 6 - 5 ⇒ 1
Δ₂₄ = 9 - (2 + 3) ⇒ 9 - 5 ⇒ 4
Δ₃₁ = 18 - (0 + 10) ⇒ 18 - 10 ⇒ 8
```

### 3

|        | P   | Q   | R   | S   | T   | Supply |
| ------ | --- | --- | --- | --- | --- | ------ |
| A      | 10  | 2   | 3   | 15  | 9   | 35     |
| B      | 5   | 10  | 15  | 2   | 4   | 40     |
| C      | 15  | 5   | 14  | 7   | 15  | 20     |
| D      | 20  | 15  | 13  | 25  | 8   | 30     |
| Demand | 20  | 20  | 40  | 10  | 35  |        |

using least cost,

|        | P   | Q   | R   | S       | T   | Supply |
| ------ | --- | --- | --- | ------- | --- | ------ |
| A      | 10  | 2   | 3   | 15      | 9   | 35     |
| B      | 5   | 10  | 15  | **2¹⁰** | 4   | 40-10  |
| C      | 15  | 5   | 14  | 7       | 15  | 20     |
| D      | 20  | 15  | 13  | 25      | 8   | 30     |
| Demand | 20  | 20  | 40  | 10      | 35  |        |

|        | P   | Q       | R   | T   | Supply |
| ------ | --- | ------- | --- | --- | ------ |
| A      | 10  | **2²⁰** | 3   | 9   | 35-20  |
| B      | 5   | 10      | 15  | 4   | 30     |
| C      | 15  | 5       | 14  | 15  | 20     |
| D      | 20  | 15      | 13  | 8   | 30     |
| Demand | 20  | 20      | 40  | 35  |        |

|        | P   | R       | T   | Supply |
| ------ | --- | ------- | --- | ------ |
| A      | 10  | **3¹⁵** | 9   | 15     |
| B      | 5   | 15      | 4   | 30     |
| C      | 15  | 14      | 15  | 20     |
| D      | 20  | 13      | 8   | 30     |
| Demand | 20  | 40-15   | 35  |        |

|        | P   | R   | T       | Supply |
| ------ | --- | --- | ------- | ------ |
| B      | 5   | 15  | **4³⁰** | 30     |
| C      | 15  | 14  | 15      | 20     |
| D      | 20  | 13  | 8       | 30     |
| Demand | 20  | 25  | 35-30   |        |

|        | P   | R   | T      | Supply |
| ------ | --- | --- | ------ | ------ |
| C      | 15  | 14  | 15     | 20     |
| D      | 20  | 13  | **8⁵** | 30-5   |
| Demand | 20  | 25  | 5      |        |

|        | P   | R        | Supply |
| ------ | --- | -------- | ------ |
| C      | 15  | 14       | 20     |
| D      | 20  | **13²⁵** | 25     |
| Demand | 20  | 25-25    |        |

|        | P        | Supply |
| ------ | -------- | ------ |
| C      | **15²⁰** | 20     |
| Demand | 20       |        |

|     | P        | Q       | R        | S       | T       |
| --- | -------- | ------- | -------- | ------- | ------- |
| A   | 10       | **2²⁰** | **3¹⁵**  | 15      | 9       |
| B   | 5        | 10      | 15       | **2¹⁰** | **4³⁰** |
| C   | **15²⁰** | 5       | 14       | 7       | 15      |
| D   | 20       | 15      | **13²⁵** | 25      | **8⁵**  |

no of allocations = m + n - 1
7 != 8

the problem is degenerate

Total cost = 2 x 20 + 3 x 15 + 2 x 10 + 4 x 30 + 15 x 20 + 13 x 25 + 8 x 5

Total cost = 890

```

to make the solution non degenerate we add temporary variable to the least cost.

```

|     | P        | Q       | R        | S       | T       |
| --- | -------- | ------- | -------- | ------- | ------- |
| A   | 10       | **2²⁰** | **3¹⁵**  | 15      | 9       |
| B   | 5        | 10      | 15       | **2¹⁰** | **4³⁰** |
| C   | **15²⁰** | **5⁺ᵉ** | 14       | 7       | 15      |
| D   | 20       | 15      | **13²⁵** | 25      | **8⁵**  |

using MODI,

|     | P          | Q       | R        | S       | T       |          |
| --- | ---------- | ------- | -------- | ------- | ------- | -------- |
| A   | 10         | **2²⁰** | **3¹⁵**  | 15      | 9       | u₀ = -10 |
| B   | 5₊ₓ        | 10      | 15       | **2¹⁰** | **4³⁰** | u₁ = -4  |
| C   | **15²⁰₊ₓ** | **5⁺ᵉ** | 14       | 7       | 15      | u₂ = -7  |
| D   | 20         | 15      | **13²⁵** | 25      | **8⁵**  | u₃= 0    |
|     | v₀ = 22    | v₁ = 12 | v₂ = 13  | v₃ = 6  | v₄ = 8  |          |

```

C₄₅ = u₃ + v₄ ⇒ 8 = 0 + v₄ ⇒ v₄ = 8
C₂₅ = u₁ + v₄ ⇒ 4 = u₁ + 8 ⇒ u₁ = -4
C₂₄ = u₁ + v₃ ⇒ 2 = -4 + v₃ ⇒ v₃ = 6
C₄₃ = u₃ + v₂ ⇒ 13 = 0 + v₂ ⇒ v₂ = 13
C₁₃ = u₀ + v₂ ⇒ 3 = u₀ + 13 ⇒ u₀ = -10
C₁₂ = u₀ + v₁ ⇒ 2 = -10 + v₁ ⇒ v₁ = 12
C₃₂ = u₂ + v₁ ⇒ 5 = u₂ + 12 ⇒ u₂ = -7
C₃₁ = u₂ + v₀ ⇒ 15 = -7 + v₀ ⇒ v₀ = 22
```

for unallocated cell

```
Δᵢⱼ = cᵢⱼ - (uᵢ + vⱼ)

Δ₁₁ = 10 - (-10 + 22) ⇒ 10 - (+12) ⇒ -02
Δ₁₃ = 15 - (-10 + 06) ⇒ 15 - (-04) ⇒ +19
Δ₁₄ = 09 - (-10 + 08) ⇒ 09 - (-02) ⇒ +11
Δ₂₁ = 05 - (-04 + 22) ⇒ 05 - (+18) ⇒ -13
Δ₂₂ = 10 - (-04 + 12) ⇒ 10 - (+08) ⇒ +02
Δ₂₃ = 15 - (-04 + 08) ⇒ 15 - (+04) ⇒ +11
Δ₃₃ = 14 - (-07 + 13) ⇒ 14 - (+06) ⇒ +08
Δ₃₄ = 07 - (-07 + 06) ⇒ 07 - (-01) ⇒ +08
Δ₃₅ = 15 - (-07 + 12) ⇒ 15 - (+05) ⇒ +10
Δ₄₁ = 20 - (+00 + 22) ⇒ 20 - (+22) ⇒ +02
Δ₄₂ = 15 - (+00 + 12) ⇒ 15 - (+12) ⇒ +03
Δ₄₄ = 25 - (+00 + 06) ⇒ 25 - (+06) ⇒ +19
```

## Assignment Problem

How should the jobs

1. balanced ⇒ (n x n)
2. unbalanced ⇒ (m x n) m != n

## Hungarian Method

1. Row approach subtract the minimum element from all the elements in respective row we get row reduction matrix.

2. Column reduction: subtract the minimum element from all the elements in respective column.

3. Draw minimum no of horizontal and vertical line (N) to cover all zero
   a. if N = n, n = orderof matrix then an optimal solution can be made.
   b. if N < n, the go to next step.

4. Determine the smallest uncovered element (n)
   a. Write uncovered value = uncovered value - n
   b. Intersection value = intersection value + n
   c. Line Value (other value) in same.

### 1

Solve the AP by using Hungarian method. Assign the jobs for different machines so as to minimize the total cost.

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 13  | 8   | 16  | 18  | 19  |
| 2   | 9   | 15  | 24  | 9   | 12  |
| 3   | 12  | 9   | 4   | 4   | 4   |
| 4   | 6   | 12  | 10  | 8   | 13  |
| 5   | 15  | 17  | 18  | 12  | 20  |

Row Reduction,

| Job | A           | B           | C           | D           | E           |
| --- | ----------- | ----------- | ----------- | ----------- | ----------- |
| 1   | 13 - 8 = 5  | 8 - 8 = 0   | 16 - 8 = 8  | 18 - 8 = 10 | 19 - 8 = 11 |
| 2   | 9 - 9 = 0   | 15 - 9 = 6  | 24 - 9 = 15 | 9 - 9 = 0   | 12 - 9 = 3  |
| 3   | 12 - 4 = 8  | 9 - 4 = 5   | 4 - 4 = 0   | 4 - 4 = 0   | 4 - 4 = 0   |
| 4   | 6 - 6 = 0   | 12 - 6 = 6  | 10 - 6 = 4  | 8 - 6 = 2   | 13 - 6 = 7  |
| 5   | 15 - 12 = 3 | 17 - 12 = 5 | 18 - 12 = 6 | 12 - 12 = 0 | 20 - 12 = 8 |

Output,

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 5   | 0   | 8   | 10  | 11  |
| 2   | 0   | 6   | 15  | 0   | 3   |
| 3   | 8   | 5   | 0   | 0   | 0   |
| 4   | 0   | 6   | 4   | 2   | 7   |
| 5   | 3   | 5   | 6   | 0   | 8   |

Column Reduction,

| Job | A         | B         | C         | D         | E     |
| --- | --------- | --------- | --------- | --------- | ----- |
| 1   | ~~5~~     | ~~**0**~~ | 8         | ~~10~~    | 11    |
| 2   | ~~0~~     | ~~6~~     | 15        | ~~0~~     | 3     |
| 3   | ~~8~~     | ~~5~~     | ~~**0**~~ | ~~0~~     | ~~0~~ |
| 4   | ~~**0**~~ | ~~6~~     | 4         | ~~2~~     | 7     |
| 5   | ~~3~~     | ~~5~~     | 6         | ~~**0**~~ | 8     |

N = 4, n = 5
Since the N < n is true,it means this is not an optimal solution.

| Job | A         | B         | C           | D         | E          |
| --- | --------- | --------- | ----------- | --------- | ---------- |
| 1   | ~~5~~     | ~~**0**~~ | 8 - 3 = 5   | ~~10~~    | 11 - 3 = 8 |
| 2   | ~~0~~     | ~~6~~     | 15 - 3 = 12 | ~~0~~     | 3 - 3 = 0  |
| 3   | ~~8~~     | ~~5~~     | ~~**0**~~   | ~~0~~     | ~~0~~      |
| 4   | ~~**0**~~ | ~~6~~     | 4 - 3 = 1   | ~~2~~     | 7 - 3 = 4  |
| 5   | ~~3~~     | ~~5~~     | 6 - 3 = 3   | ~~**0**~~ | 8 - 3 = 5  |

| Job | A          | B         | C         | D         | E          |
| --- | ---------- | --------- | --------- | --------- | ---------- |
| 1   | ~~5~~      | ~~**0**~~ | 5 + 3 = 8 | ~~10~~    | 8 + 3 = 11 |
| 2   | ~~0~~      | ~~6~~     | 12        | ~~0~~     | 0          |
| 3   | 8 + 3 = 11 | 5 + 3 = 8 | ~~**0**~~ | 0 + 3 = 3 | ~~0~~      |
| 4   | ~~**0**~~  | ~~6~~     | 1         | ~~2~~     | 4          |
| 5   | ~~3~~      | ~~5~~     | 3 + 3 = 6 | ~~**0**~~ | 5 + 3 = 8  |

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 5   | 0   | 8   | 10  | 11  |
| 2   | 0   | 6   | 12  | 0   | 0   |
| 3   | 11  | 8   | 0   | 3   | 0   |
| 4   | 0   | 6   | 1   | 2   | 4   |
| 5   | 3   | 5   | 6   | 0   | 8   |

| Job | A         | B         | C         | D         | E         |
| --- | --------- | --------- | --------- | --------- | --------- |
| 1   | ~~5~~     | ~~**0**~~ | 8         | ~~10~~    | 11        |
| 2   | ~~0~~     | ~~6~~     | ~~12~~    | ~~0~~     | ~~**0**~~ |
| 3   | ~~11~~    | ~~8~~     | ~~**0**~~ | ~~3~~     | ~~0~~     |
| 4   | ~~**0**~~ | ~~6~~     | 1         | ~~2~~     | 4         |
| 5   | ~~3~~     | ~~5~~     | 6         | ~~**0**~~ | 8         |

N = 5

n = 5

| Jobs | Machine | Time/ Cost |
| ---- | ------- | ---------- |
| 1    | B       | 8          |
| 2    | E       | 12         |
| 3    | C       | 4          |
| 4    | A       | 6          |
| 5    | D       | 12         |

### 2

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 4   | 3   | 6   | 2   | 7   |
| 2   | 10  | 12  | 11  | 14  | 16  |
| 3   | 4   | 3   | 2   | 1   | 5   |
| 4   | 8   | 7   | 6   | 9   | 6   |

Row reduction,

| Job | A           | B           | C           | D           | E           |
| --- | ----------- | ----------- | ----------- | ----------- | ----------- |
| 1   | 4 -2 = 2    | 3 - 2 = 1   | 6 - 2 = 4   | 2 - 2 = 0   | 7 - 2 = 5   |
| 2   | 10 - 10 = 0 | 12 - 10 = 2 | 11 - 10 = 1 | 14 - 10 = 4 | 16 - 10 = 6 |
| 3   | 4 - 1 = 3   | 3 - 1 = 2   | 2 - 1 = 1   | 1 - 1 = 0   | 5 - 1 = 4   |
| 4   | 8 - 6 = 2   | 7 - 6 = 1   | 6 - 6 = 0   | 9 - 6 = 3   | 6 - 6 = 0   |
| 5   | 0           | 0           | 0           | 0           | 0           |

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 2   | 1   | 4   | 0   | 5   |
| 2   | 0   | 2   | 1   | 4   | 6   |
| 3   | 3   | 2   | 1   | 0   | 4   |
| 4   | 2   | 5   | 4   | 7   | 4   |
| 5   | 0   | 0   | 0   | 0   | 0   |

Answer,

| Job | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| 1   | 2   | 1   | 4   | 0   | 5   |
| 2   | 0   | 2   | 1   | 4   | 6   |
| 3   | 3   | 2   | 1   | 0   | 4   |
| 4   | 2   | 1   | 0   | 3   | 0   |
| 5   | 0   | 0   | 0   | 0   | 0   |

### 3

Unbalanced Assignment Problem

|     | A   | B   | C   | D   |
| --- | --- | --- | --- | --- |
| P   | 10  | 9   | 8   | 12  |
| Q   | 3   | 4   | 5   | 2   |
| R   | 25  | 20  | 14  | 16  |
| S   | 7   | 9   | 10  | 9   |
| T   | 18  | 14  | 16  | 25  |

Adding Dummy Column,

|     | A   | B   | C   | D   | E   |
| --- | --- | --- | --- | --- | --- |
| P   | 10  | 9   | 8   | 12  | 0   |
| Q   | 3   | 4   | 5   | 2   | 0   |
| R   | 25  | 20  | 14  | 16  | 0   |
| S   | 7   | 9   | 10  | 9   | 0   |
| T   | 18  | 14  | 16  | 25  | 0   |

Using Column Reduction,

|     | A           | B           | C           | D           | E     |
| --- | ----------- | ----------- | ----------- | ----------- | ----- |
| P   | 10 - 3 = 7  | 9 - 4 = 5   | 8 - 5 = 3   | 12 - 2 = 0  | ~~0~~ |
| Q   | 3 - 3 = 0   | 4 - 4 = 0   | 5 - 5 = 0   | 2 - 2 = 0   | ~~0~~ |
| R   | 25 - 3 = 22 | 20 - 4 = 16 | 14 - 5 = 9  | 16 - 2 = 14 | ~~0~~ |
| S   | 7 - 3 = 4   | 9 - 4 = 5   | 10 - 5 = 5  | 9 - 2 = 7   | ~~0~~ |
| T   | 18 - 3 = 5  | 14 - 4 = 10 | 16 - 5 = 11 | 25 - 2 = 23 | ~~0~~ |

|     | A     | B     | C     | D     | E     |
| --- | ----- | ----- | ----- | ----- | ----- |
| P   | 7     | 5     | 3     | 0     | ~~0~~ |
| Q   | ~~0~~ | ~~0~~ | ~~0~~ | ~~0~~ | ~~0~~ |
| R   | 22    | 16    | 9     | 14    | ~~0~~ |
| S   | 4     | 5     | 5     | 7     | ~~0~~ |
| T   | 5     | 10    | 11    | 23    | ~~0~~ |

|     | A   | B   | C   | D     |
| --- | --- | --- | --- | ----- |
| P   | 7   | 5   | 3   | ~~0~~ |
| R   | 22  | 16  | 9   | 14    |
| S   | 4   | 5   | 5   | 7     |
| T   | 5   | 10  | 11  | 23    |

## Crew Assignment Problem

<u>ABC Airline</u>

| Flight No. | Pokhara | KTM    |            | KTM    | Pokhara |
| ---------- | ------- | ------ | ---------- | ------ | ------- |
|            | Depart  | Arrive | Flight No. | Depart | Arrive  |
| A1         | 6 AM    | 8 AM   | B1         | 8 AM   | 10 AM   |
| A2         | 8 AM    | 10 AM  | B2         | 9 AM   | 11 AM   |
| A3         | 2 PM    | 4 PM   | B3         | 2 PM   | 4 PM    |
| A4         | 8 PM    | 10 PM  | B4         | 7 PM   | 9 PM    |

(Crew must have a minimum lay over of 5 hours between flights)

(Crew based on pokhara)

|     | B1  | B2  | B3  | B4  |
| --- | --- | --- | --- | --- |
| A1  | 24  | 25  | 6   | 11  |
| A2  | 22  | 23  | 28  | 9   |
| A3  | 16  | 17  | 22  | 27  |
| A4  | 10  | 11  | 28  | 16  |

(Crew based on kathmandu)

|     | B1  | B2  | B3  | B4  |
| --- | --- | --- | --- | --- |
| A1  | 20  | 19  | 14  | 9   |
| A2  | 22  | 21  | 16  | 11  |
| A3  | 28  | 27  | 22  |     |
| A4  |     |     |     |     |
