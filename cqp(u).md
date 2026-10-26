# Python and Quantum Computing Experiments

The original experiment organization and all 82 Python code listings are retained. Each listing is arranged as Aim, Theory, numbered Algorithm, shape-labelled Flowchart, Program, then Conclusion/Result and clear viva/practical tips. Existing correction notes remain at the end.

**Flowchart shape key:** (OVAL) start/end; /PARALLELOGRAM/ input/output; [RECTANGLE] action or process; <DIAMOND> question or decision.

## Experiment 1 — Basic concepts and arithmetic (`sampleex1.pdf`)

### Hello World
#### Practical write-up — Hello World

**Aim:** Display a greeting message.

**Theory:** print sends text to the output; the newline escape moves to a new line.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Print the greeting.
3. **Step 3:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Display greeting/
   ↓
(OVAL — STOP)
```

#### Program

```python
print("Hello World!\n")
```


#### Result and viva tips — Hello World

**Conclusion/Result:** The greeting is displayed.

**Viva and practical tips:**
- No input or calculation is used.
- The explicit newline adds a blank line after the greeting.
- Time and space are O(1).
### Swap variables
#### Practical write-up — Swap variables

**Aim:** Swap A and B and display values before and after.

**Theory:** Simultaneous assignment evaluates the right-hand values before assigning either name.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set A = 5 and B = 10.
3. **Step 3:** Display their original values.
4. **Step 4:** Swap the values with A, B = B, A.
5. **Step 5:** Display the new values.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Set A and B]
   ↓
[RECTANGLE — Swap A and B]
   ↓
/PARALLELOGRAM — Display values before and after/
   ↓
(OVAL — STOP)
```

#### Program

```python
A = 5
B = 10
print("Before Swap:\nA =", A, "\nB =", B)
A, B = B, A
print("\nAfter Swap:\nA =", A, "\nB =", B, "\n")
```


#### Result and viva tips — Swap variables

**Conclusion/Result:** The values are exchanged; A becomes 10 and B becomes 5.

**Viva and practical tips:**
- No temporary variable is needed.
- Try changing the initial values.
- The operation takes O(1) time and extra space.
### Personal information output
#### Practical write-up — Personal information output

**Aim:** Store sample personal details and print each field.

**Theory:** Variables hold sample values; print displays them with labels.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Assign sample name, age, gender, course, and address.
3. **Step 3:** Print each field.
4. **Step 4:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Assign sample details]
   ↓
/PARALLELOGRAM — Display labelled details/
   ↓
(OVAL — STOP)
```

#### Program

```python
Name = "David"
Age = 19
Gender = "Female"
Course = "Computer Science"
Address = "Seattle"
print("Name:", Name)
print("Age:", Age)
print("Gender:", Gender)
print("Course:", Course)
print("Address:", Address, "\n")
```


#### Result and viva tips — Personal information output

**Conclusion/Result:** The fixed sample details are printed.

**Viva and practical tips:**
- These values are hard-coded, not entered by the user.
- Changing an assignment changes the output.
- The example is O(1).
### Personal information using input
#### Practical write-up — Personal information using input

**Aim:** Read a name, age, course, and address, then display them.

**Theory:** input returns text as a string; the age is only echoed and is not converted to a number.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read the four fields.
3. **Step 3:** Display each field with its label.
4. **Step 4:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Name, age, course, and address/
   ↓
/PARALLELOGRAM — Display entered details/
   ↓
(OVAL — STOP)
```

#### Program

```python
Name_Input = input("Enter Name: ")
Age_Input = input("Enter Age: ")
Course_Input = input("Enter Course: ")
Address_Input = input("Enter Address: ")
print("\nName:", Name_Input)
print("Age:", Age_Input)
print("Course:", Course_Input)
print("Address:", Address_Input, "\n")
```


#### Result and viva tips — Personal information using input

**Conclusion/Result:** The entered values are displayed.

**Viva and practical tips:**
- Convert age with int if later calculations are added.
- input accepts text with spaces.
- Processing apart from stored text is O(1).
### Average calculation
#### Practical write-up — Average calculation

**Aim:** Calculate the average of three fixed numbers.

**Theory:** Average is the sum divided by the number of values; Python / returns a floating-point result.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set X = 20, Y = 30, Z = 40.
3. **Step 3:** Calculate (X + Y + Z) / 3.
4. **Step 4:** Display the average.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Set the sample numbers]
   ↓
[RECTANGLE — Calculate their mean]
   ↓
/PARALLELOGRAM — Display the average/
   ↓
(OVAL — STOP)
```

#### Program

```python
X = 20
Y = 30
Z = 40
Average = (X + Y + Z) / 3
print("Average =", Average, "\n")
```


#### Result and viva tips — Average calculation

**Conclusion/Result:** The displayed average is 30.0.

**Viva and practical tips:**
- The values are fixed in the listing.
- For a variable-sized collection, check it is not empty before dividing.
- Time and space are O(1).
### Circle area and circumference
#### Practical write-up — Circle area and circumference

**Aim:** Calculate the area and circumference of a circle.

**Theory:** The formulas are area = pi*r^2 and circumference = 2*pi*r; the code uses r=20 and pi=3.14.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set radius and Pi values.
3. **Step 3:** Calculate area and circumference.
4. **Step 4:** Display both results.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Set radius = 20 and Pi = 3.14]
   ↓
[RECTANGLE — Calculate area and circumference]
   ↓
/PARALLELOGRAM — Display both measurements/
   ↓
(OVAL — STOP)
```

#### Program

```python
Radius = 20
Pi = 3.14
Area = Pi * (Radius ** 2)
Circumference = 2 * Pi * Radius
print("Area =", Area)
print("Circumference =", Circumference, "\n")
```


#### Result and viva tips — Circle area and circumference

**Conclusion/Result:** Area is 1256 and circumference is 125.6 for the sample values.

**Viva and practical tips:**
- A zero radius gives zero for both results.
- A more precise Pi value can be used as a modification.
- The calculations are O(1).
### Simple interest
#### Practical write-up — Simple interest

**Aim:** Calculate simple interest from principal, annual rate, and time.

**Theory:** Simple interest is P*R*T/100; rate is a percentage and time is in years.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read P, R, and T as floating-point values.
3. **Step 3:** Calculate P*R*T/100.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Principal, annual rate, and time/
   ↓
[RECTANGLE — Calculate P*R*T/100]
   ↓
/PARALLELOGRAM — Display simple interest/
   ↓
(OVAL — STOP)
```

#### Program

```python
Principal = float(input("Enter the principal amount (P): "))
Rate = float(input("Enter the annual interest rate (R): "))
Time = float(input("Enter the time period in years (T): "))
Simple_Interest = (Principal * Rate * Time) / 100
print("\nSimple Interest =", Simple_Interest, "\n")
```


#### Result and viva tips — Simple interest

**Conclusion/Result:** The simple-interest amount is displayed.

**Viva and practical tips:**
- Keep rate and time units consistent.
- Try zero principal/rate and fractional values.
- Time and extra space are O(1).
### Compound amount
#### Practical write-up — Compound amount

**Aim:** Calculate compound amount and compound interest.

**Theory:** Amount is P(1+R/100)^T; interest is amount minus principal. The source assumes annual compounding.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read principal, annual rate, and time.
3. **Step 3:** Calculate compound amount.
4. **Step 4:** Subtract principal to find interest.
5. **Step 5:** Display the interest.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Principal, rate, and time/
   ↓
[RECTANGLE — Calculate P*(1+R/100) raised to T]
   ↓
[RECTANGLE — Subtract principal from amount]
   ↓
/PARALLELOGRAM — Display compound interest/
   ↓
(OVAL — STOP)
```

#### Program

```python
Principal = float(input("Enter the principal amount (P): "))
Rate = float(input("Enter the annual interest rate in % (R): "))
Time = float(input("Enter the time period in years (T): "))
Compound_Amount = Principal * (1 + Rate / 100) ** Time
Compound_Interest = Compound_Amount - Principal
print("\nCompound Interest =", Compound_Interest, "\n")
```


#### Result and viva tips — Compound amount

**Conclusion/Result:** The compound-interest amount is displayed.

**Viva and practical tips:**
- Amount includes principal; interest does not.
- The program has no compounding-frequency input.
- The calculation takes O(1) time and space.
## Experiment 2 — Control structures (`sampleex2.pdf`)

### Largest of three numbers
#### Practical write-up — Largest of three numbers

**Aim:** Read three integers and display the largest.

**Theory:** The if/elif chain compares values. Its >= comparisons handle ties by printing the first matching largest value.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read A, B, and C as integers.
3. **Step 3:** If A >= B and A >= C, display A.
4. **Step 4:** Otherwise, if B >= C, display B.
5. **Step 5:** Otherwise, display C.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input A, B, C/
   ↓
<DIAMOND — Is A >= B and A >= C?>
   ├─ Yes → /PARALLELOGRAM — Display A/
   └─ No → <DIAMOND — Is B >= C?>
              ├─ Yes → /PARALLELOGRAM — Display B/
              └─ No → /PARALLELOGRAM — Display C/
   ↓
(OVAL — STOP)
```

#### Program

```python
A = int(input("Enter first number: "))
B = int(input("Enter second number: "))
C = int(input("Enter third number: "))
if A >= B and A >= C:
    print(f"\nThe largest number is: {A}\n")
elif B >= C:
    print(f"\nThe largest number is: {B}\n")
else:
    print(f"\nThe largest number is: {C}\n")
```


#### Result and viva tips — Largest of three numbers

**Conclusion/Result:** The largest input value is displayed.

**Viva and practical tips:**
- Test equal values and a tie for largest.
- Experiment 2 uses integers; Experiment 8 accepts decimals.
- Only fixed comparisons are made: O(1) time and space.
### Even or odd
#### Practical write-up — Even or odd

**Aim:** Check whether an entered integer is even or odd.

**Theory:** An integer is even when its remainder after division by 2 is zero.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** Test Num % 2 == 0.
4. **Step 4:** Display Even if true, otherwise Odd.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Integer Num/
   ↓
<DIAMOND — Is Num % 2 equal to 0?>
   ├─ Yes → /PARALLELOGRAM — Display Even/
   └─ No → /PARALLELOGRAM — Display Odd/
   ↓
(OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
if Num % 2 == 0:
    print("The number is Even.\n")
else:
    print("The number is Odd.\n")
```


#### Result and viva tips — Even or odd

**Conclusion/Result:** The parity of the input is displayed.

**Viva and practical tips:**
- Negative integers are also classified by modulo.
- Test 0, an even number, and an odd number.
- The check is O(1).
### Positive, negative, or zero
#### Practical write-up — Positive, negative, or zero

**Aim:** Classify the input as positive, negative, or zero.

**Theory:** The program checks greater than zero, then less than zero; any remaining value is zero.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** If Num > 0, display Positive.
4. **Step 4:** Else if Num < 0, display Negative.
5. **Step 5:** Otherwise display Zero.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Num/
   ↓
<DIAMOND — Is Num > 0?>
   ├─ Yes → /PARALLELOGRAM — Display Positive/
   └─ No → <DIAMOND — Is Num < 0?>
              ├─ Yes → /PARALLELOGRAM — Display Negative/
              └─ No → /PARALLELOGRAM — Display Zero/
   ↓
(OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
if Num > 0:
    print("The number is Positive.\n")
elif Num < 0:
    print("The number is Negative.\n")
else:
    print("The number is Zero.\n")
```


#### Result and viva tips — Positive, negative, or zero

**Conclusion/Result:** One sign category is displayed.

**Viva and practical tips:**
- Test positive, negative, and zero values.
- Experiment 8 accepts decimal values.
- The decision chain is O(1).
### Leap year
#### Practical write-up — Leap year

**Aim:** Check whether a year is a leap year.

**Theory:** The rule is divisible by 400, or divisible by 4 but not by 100.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Year.
3. **Step 3:** Check the 400 rule or the 4-and-not-100 rule.
4. **Step 4:** Display Leap or Not Leap.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Year/
   ↓
<DIAMOND — Divisible by 400, or by 4 but not 100?>
   ├─ Yes → /PARALLELOGRAM — Display Leap Year/
   └─ No → /PARALLELOGRAM — Display Not a Leap Year/
   ↓
(OVAL — STOP)
```

#### Program

```python
Year = int(input("Enter a year: "))
if Year % 400 == 0 or (Year % 4 == 0 and Year % 100 != 0):
    print("Year is leap.\n")
else:
    print("Year is not leap.\n")
```


#### Result and viva tips — Leap year

**Conclusion/Result:** The program applies the leap-year rule.

**Viva and practical tips:**
- 2000 is leap; 1900 is not; 2024 is leap.
- Keep the parentheses and century-year condition intact.
- The test is O(1).
### Pass or fail
#### Practical write-up — Pass or fail

**Aim:** Report Pass for marks of 35 or more, otherwise Fail.

**Theory:** The inclusive pass threshold in this listing is 35.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read marks.
3. **Step 3:** Check marks >= 35.
4. **Step 4:** Display Pass if true; otherwise display Fail.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Marks/
   ↓
<DIAMOND — Are marks >= 35?>
   ├─ Yes → /PARALLELOGRAM — Display Pass/
   └─ No → /PARALLELOGRAM — Display Fail/
   ↓
(OVAL — STOP)
```

#### Program

```python
Marks = int(input("Enter the marks: "))
if Marks >= 35:
    print("Result: Pass\n")
else:
    print("Result: Fail\n")
```


#### Result and viva tips — Pass or fail

**Conclusion/Result:** The result follows the 35-mark threshold in this code.

**Viva and practical tips:**
- Test the threshold and one mark below it.
- Marks outside the usual range are not rejected.
- The comparison is O(1).
## Experiment 8 — Control structures and loops (`sampleex8.pdf`)

### Largest of three numbers
#### Practical write-up — Largest of three numbers

**Aim:** Read three floating-point numbers and display the largest.

**Theory:** The if/elif chain compares values. Its >= comparisons handle ties by printing the first matching largest value.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read A, B, and C as floating-point numbers.
3. **Step 3:** If A >= B and A >= C, display A.
4. **Step 4:** Otherwise, if B >= C, display B.
5. **Step 5:** Otherwise, display C.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input A, B, C/
   ↓
<DIAMOND — Is A >= B and A >= C?>
   ├─ Yes → /PARALLELOGRAM — Display A/
   └─ No → <DIAMOND — Is B >= C?>
              ├─ Yes → /PARALLELOGRAM — Display B/
              └─ No → /PARALLELOGRAM — Display C/
   ↓
(OVAL — STOP)
```

#### Program

```python
A = float(input("Enter first number: "))
B = float(input("Enter second number: "))
C = float(input("Enter third number: "))
if A >= B and A >= C:
    print("The largest number is:", A, "\n")
elif B >= C:
    print("The largest number is:", B, "\n")
else:
    print("The largest number is:", C, "\n")
```


#### Result and viva tips — Largest of three numbers

**Conclusion/Result:** The largest input value is displayed.

**Viva and practical tips:**
- Test equal values and a tie for largest.
- Experiment 2 uses integers; Experiment 8 accepts decimals.
- Only fixed comparisons are made: O(1) time and space.
### Even or odd
#### Practical write-up — Even or odd

**Aim:** Check whether an entered integer is even or odd.

**Theory:** An integer is even when its remainder after division by 2 is zero.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** Test Num % 2 == 0.
4. **Step 4:** Display Even if true, otherwise Odd.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Integer Num/
   ↓
<DIAMOND — Is Num % 2 equal to 0?>
   ├─ Yes → /PARALLELOGRAM — Display Even/
   └─ No → /PARALLELOGRAM — Display Odd/
   ↓
(OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
if Num % 2 == 0:
    print("The number is Even.\n")
else:
    print("The number is Odd.\n")
```


#### Result and viva tips — Even or odd

**Conclusion/Result:** The parity of the input is displayed.

**Viva and practical tips:**
- Negative integers are also classified by modulo.
- Test 0, an even number, and an odd number.
- The check is O(1).
### Positive, negative, or zero
#### Practical write-up — Positive, negative, or zero

**Aim:** Classify the input as positive, negative, or zero.

**Theory:** The program checks greater than zero, then less than zero; any remaining value is zero.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** If Num > 0, display Positive.
4. **Step 4:** Else if Num < 0, display Negative.
5. **Step 5:** Otherwise display Zero.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Num/
   ↓
<DIAMOND — Is Num > 0?>
   ├─ Yes → /PARALLELOGRAM — Display Positive/
   └─ No → <DIAMOND — Is Num < 0?>
              ├─ Yes → /PARALLELOGRAM — Display Negative/
              └─ No → /PARALLELOGRAM — Display Zero/
   ↓
(OVAL — STOP)
```

#### Program

```python
Num = float(input("Enter a number: "))
if Num > 0:
    print("The number is Positive.\n")
elif Num < 0:
    print("The number is Negative.\n")
else:
    print("The number is Zero.\n")
```


#### Result and viva tips — Positive, negative, or zero

**Conclusion/Result:** One sign category is displayed.

**Viva and practical tips:**
- Test positive, negative, and zero values.
- Experiment 8 accepts decimal values.
- The decision chain is O(1).
### Pass or fail
#### Practical write-up — Pass or fail

**Aim:** Report Pass for marks of 40 or more, otherwise Fail.

**Theory:** The inclusive pass threshold in this listing is 40.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read marks.
3. **Step 3:** Check marks >= 40.
4. **Step 4:** Display Pass if true; otherwise display Fail.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Marks/
   ↓
<DIAMOND — Are marks >= 40?>
   ├─ Yes → /PARALLELOGRAM — Display Pass/
   └─ No → /PARALLELOGRAM — Display Fail/
   ↓
(OVAL — STOP)
```

#### Program

```python
Marks = float(input("Enter the student's marks: "))
if Marks >= 40:
    print("Result: Pass\n")
else:
    print("Result: Fail\n")
```


#### Result and viva tips — Pass or fail

**Conclusion/Result:** The result follows the 40-mark threshold in this code.

**Viva and practical tips:**
- Test the threshold and one mark below it.
- Marks outside the usual range are not rejected.
- The comparison is O(1).
### Grade calculation
#### Practical write-up — Grade calculation

**Aim:** Assign a grade using descending marks thresholds.

**Theory:** The program tests 90, 80, 70, and 60 in order; the first satisfied threshold determines the grade.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read marks.
3. **Step 3:** Check thresholds 90, 80, 70, then 60 in descending order.
4. **Step 4:** Display A, B, C, D, or F for the first matching branch.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input marks/
   ↓
<DIAMOND — Marks >= 90?> → Yes: /PARALLELOGRAM — Display A/
   ↓ No
<DIAMOND — Marks >= 80?> → Yes: /PARALLELOGRAM — Display B/
   ↓ No
<DIAMOND — Marks >= 70?> → Yes: /PARALLELOGRAM — Display C/
   ↓ No
<DIAMOND — Marks >= 60?> → Yes: /PARALLELOGRAM — Display D/; No: /PARALLELOGRAM — Display F/
   ↓
(OVAL — STOP)
```

#### Program

```python
Marks = float(input("Enter the student's marks: "))
if Marks >= 90:
    print("Grade: A\n")
elif Marks >= 80:
    print("Grade: B\n")
elif Marks >= 70:
    print("Grade: C\n")
elif Marks >= 60:
    print("Grade: D\n")
else:
    print("Grade: F\n")
```


#### Result and viva tips — Grade calculation

**Conclusion/Result:** A grade is displayed according to the first matching threshold.

**Viva and practical tips:**
- Boundary values belong to the higher grade because tests use >=.
- Try each exact boundary and a value just below it.
- The source does not validate marks range; the chain is O(1).
### Income tax calculation
#### Practical write-up — Income tax calculation

**Aim:** Calculate tax using the source's progressive income brackets.

**Theory:** Each rate is charged only on income in that bracket; fixed additions carry forward earlier bracket tax.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read annual income.
3. **Step 3:** Choose the bracket: <=250000, <=500000, <=1000000, or above 1000000.
4. **Step 4:** Apply the matching progressive formula.
5. **Step 5:** Display tax and stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input annual income/
   ↓
<DIAMOND — Which bracket applies?>
   ├─ <=250000 → [RECTANGLE — Tax = 0]
   ├─ <=500000 → [RECTANGLE — 5% above 250000]
   ├─ <=1000000 → [RECTANGLE — Add 12500; 20% above 500000]
   └─ >1000000 → [RECTANGLE — Add 112500; 30% above 1000000]
   ↓
/PARALLELOGRAM — Display tax/
   ↓
(OVAL — STOP)
```

#### Program

```python
Income = float(input("Enter your annual income: "))
if Income <= 250000:
    Tax = 0
elif Income <= 500000:
    Tax = (Income - 250000) * 0.05
elif Income <= 1000000:
    Tax = 12500 + (Income - 500000) * 0.20
else:
    Tax = 112500 + (Income - 1000000) * 0.30
print("Income Tax =", Tax, "\n")
```


#### Result and viva tips — Income tax calculation

**Conclusion/Result:** The amount calculated by the sample progressive brackets is displayed.

**Viva and practical tips:**
- Test every bracket boundary and just-above values.
- These are example program rules, not current tax guidance.
- Negative income is not validated and receives zero under the first branch; O(1) time.
### Print 1 to N
#### Practical write-up — Print 1 to N

**Aim:** Print integers from 1 to N.

**Theory:** range(1,N+1) includes 1 but excludes its stop value, so N+1 includes N.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read N.
3. **Step 3:** For i from 1 through N, print i.
4. **Step 4:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input N/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
N = int(input("Enter a number: "))
for i in range(1, N + 1):
    print(i)
print("\n")
```


#### Result and viva tips — Print 1 to N

**Conclusion/Result:** The sequence from 1 through N is printed.

**Viva and practical tips:**
- Test N<=0: the range is empty. The loop is O(N) time and O(1) extra space; range's stop is exclusive.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Reverse while loop (N to 1)
#### Practical write-up — Reverse while loop (N to 1)

**Aim:** Print integers from N down to 1.

**Theory:** The loop repeats while N>=1; decrementing N guarantees progress.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read N.
3. **Step 3:** While N>=1, print N and decrement it.
4. **Step 4:** Stop when N<1.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input N/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
N = int(input("Enter a number: "))
while N >= 1:
    print(N)
    N -= 1
print("\n")
```


#### Result and viva tips — Reverse while loop (N to 1)

**Conclusion/Result:** The positive sequence is printed from N down to 1.

**Viva and practical tips:**
- N<1 prints nothing. Keep the decrement inside the loop. Time is O(N) for positive N.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Multiplication table
#### Practical write-up — Multiplication table

**Aim:** Display the number multiplied by 1 through 10.

**Theory:** A counter-controlled while loop produces ten products.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num and set i=1.
3. **Step 3:** While i<=10, print Num*i and increase i.
4. **Step 4:** Stop when i>10.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Num/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
i = 1
while i <= 10:
    print(Num, "x", i, "=", Num * i)
    i += 1
print("\n")
```


#### Result and viva tips — Multiplication table

**Conclusion/Result:** The ten products are printed.

**Viva and practical tips:**
- Zero and negative inputs still produce a table. This source always runs ten times, so O(1) time.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Sum of first N natural numbers
#### Practical write-up — Sum of first N natural numbers

**Aim:** Calculate the sum from 1 through N.

**Theory:** An accumulator adds each natural number once.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read N; initialize i=1 and Total=0.
3. **Step 3:** While i<=N, add i and increment i.
4. **Step 4:** Display Total.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input N/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
N = int(input("Enter a number: "))
i = 1
Total = 0
while i <= N:
    Total += i
    i += 1
print("Sum of first", N, "natural numbers is:", Total, "\n")
```


#### Result and viva tips — Sum of first N natural numbers

**Conclusion/Result:** The accumulated sum is displayed.

**Viva and practical tips:**
- For N<=0 the loop is skipped and Total remains 0. O(N) time, O(1) space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Factorial using a while loop
#### Practical write-up — Factorial using a while loop

**Aim:** Calculate factorial for a nonnegative integer.

**Theory:** Factorial multiplies 1 through N, with 0! = 1; negative input is rejected.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** If Num<0, show an error.
4. **Step 4:** Otherwise initialize Fact=1 and multiply by i for i=1..Num.
5. **Step 5:** Display Fact.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Num/
   ↓
<DIAMOND — Is Num negative?>
   ├─ Yes → /PARALLELOGRAM — Display error/ → (OVAL — STOP)
   └─ No → [RECTANGLE — Initialize Fact and i]
              ↓
            <DIAMOND — Is i <= Num?>
              ├─ Yes → [RECTANGLE — Multiply Fact by i; increment i] ↖
              └─ No → /PARALLELOGRAM — Display Fact/ → (OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
if Num < 0:
    print("Factorial is not defined for negative numbers.\n")
else:
    i = 1
    Fact = 1
    while i <= Num:
        Fact *= i
        i += 1
    print("Factorial of", Num, "is:", Fact, "\n")
```


#### Result and viva tips — Factorial using a while loop

**Conclusion/Result:** The factorial is displayed for nonnegative input.

**Viva and practical tips:**
- Test 0, 1, positive, and negative input. Fact must start at 1. O(N) time, O(1) space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Count digits
#### Practical write-up — Count digits

**Aim:** Count decimal digits while ignoring the sign.

**Theory:** Repeated integer division by 10 removes one digit each time; zero is handled as one digit.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num and take abs.
3. **Step 3:** Initialize Count to 1 for zero, otherwise 0.
4. **Step 4:** While Num>0, divide by 10 and increment Count.
5. **Step 5:** Display Count.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Integer/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
Num = abs(int(input("Enter an integer: ")))
Count = 1 if Num == 0 else 0
while Num > 0:
    Num //= 10
    Count += 1
print("Number of digits:", Count, "\n")
```


#### Result and viva tips — Count digits

**Conclusion/Result:** The digit count is displayed.

**Viva and practical tips:**
- Zero has one digit; a negative sign is not counted. O(d) time for d digits, O(1) extra space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Reverse a number
#### Practical write-up — Reverse a number

**Aim:** Reverse decimal digits and preserve the sign.

**Theory:** Modulo extracts the last digit; multiplying Rev by 10 appends a digit.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num and save its sign.
3. **Step 3:** Use absolute value and set Rev=0.
4. **Step 4:** While Num>0, append the last digit and remove it from Num.
5. **Step 5:** Restore sign and display Rev.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Integer/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
Sign = -1 if Num < 0 else 1
Num = abs(Num)
Rev = 0
while Num > 0:
    Digit = Num % 10
    Rev = Rev * 10 + Digit
    Num //= 10
Rev *= Sign
print("Reversed number is:", Rev, "\n")
```


#### Result and viva tips — Reverse a number

**Conclusion/Result:** The reversed signed integer is displayed.

**Viva and practical tips:**
- Leading zeroes disappear (120 becomes 21); zero stays zero. O(d) time, O(1) space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Palindrome check
#### Practical write-up — Palindrome check

**Aim:** Check whether a nonnegative integer reads the same forward and backward.

**Theory:** The code reverses digits and compares with the original; negatives are rejected.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num and save Original.
3. **Step 3:** If negative, report not palindrome.
4. **Step 4:** Otherwise reverse digits and compare.
5. **Step 5:** Display the result.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Integer/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
Num = int(input("Enter a number: "))
Original = Num
if Num < 0:
    print("Not a palindrome number\n")
else:
    Rev = 0
    while Num > 0:
        Digit = Num % 10
        Rev = Rev * 10 + Digit
        Num //= 10
    if Original == Rev:
        print("Palindrome number\n")
    else:
        print("Not a palindrome number\n")
```


#### Result and viva tips — Palindrome check

**Conclusion/Result:** The palindrome result is displayed.

**Viva and practical tips:**
- Zero is a palindrome here. A value ending in zero usually fails because its reverse loses the leading zero. O(d).
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Sum of digits
#### Practical write-up — Sum of digits

**Aim:** Find the sum of decimal digits, ignoring a negative sign.

**Theory:** Modulo extracts each digit and integer division removes it.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num and take abs.
3. **Step 3:** Set digit sum to 0.
4. **Step 4:** While Num>0, add Num%10 and divide by 10.
5. **Step 5:** Display sum.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Integer/
   ↓
[RECTANGLE — Initialize counters or accumulators]
   ↓
<DIAMOND — Is another loop iteration required?>
   ├─ Yes → [RECTANGLE — Process current value and update counter] ↖
   └─ No → /PARALLELOGRAM — Display result/ → (OVAL — STOP)
```

#### Program

```python
Num = abs(int(input("Enter a number: ")))
Sum_Digits = 0
while Num > 0:
    Sum_Digits += Num % 10
    Num //= 10
print("Sum of digits:", Sum_Digits, "\n")
```


#### Result and viva tips — Sum of digits

**Conclusion/Result:** The digit sum is displayed.

**Viva and practical tips:**
- For zero the sum is 0. Negative input is processed by magnitude. O(d) time, O(1) space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Prime number check
#### Practical write-up — Prime number check

**Aim:** Check whether an integer is prime.

**Theory:** After small cases and multiples of 2 and 3, test factors 6k-1 and 6k+1 up to the square root.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Num.
3. **Step 3:** Reject Num<=1; accept 2 and 3; reject multiples of 2 or 3.
4. **Step 4:** Test i and i+2 while i*i<=Num, increasing i by 6.
5. **Step 5:** Display prime status.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input Num/
   ↓
<DIAMOND — Is Num <= 1?> → Yes: /PARALLELOGRAM — Display not prime/ → (OVAL — STOP)
   ↓ No
[RECTANGLE — Check small primes and test factors through square root]
   ↓
/PARALLELOGRAM — Display prime status/
   ↓
(OVAL — STOP)
```

#### Program

```python
def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

Num = int(input("Enter a number: "))
if is_prime(Num):
    print(f"{Num} is a prime number.\n")
else:
    print(f"{Num} is not a prime number.\n")
```


#### Result and viva tips — Prime number check

**Conclusion/Result:** Prime status is displayed.

**Viva and practical tips:**
- Test 0, 1, 2, 3, a composite, and a prime. O(sqrt(N)) time, O(1) space.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
### Prime numbers in a range
#### Practical write-up — Prime numbers in a range

**Aim:** Print primes in an inclusive range.

**Theory:** The helper tests divisors through the integer square root.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read Start and End.
3. **Step 3:** For each value in the range, test primality.
4. **Step 4:** Print values that pass.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input range/
   ↓
<DIAMOND — Another candidate in range?>
   ├─ Yes → [RECTANGLE — Test divisors through square root]
   │          ↓
   │        <DIAMOND — Is candidate prime?>
   │          ├─ Yes → /PARALLELOGRAM — Print candidate/
   │          └─ No → [RECTANGLE — Advance candidate]
   │          ↖ Return to range test
   └─ No → (OVAL — STOP)
```

#### Program

```python
def is_prime_range(n):
    if n <= 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

Start = int(input("Enter start of range: "))
End = int(input("Enter end of range: "))
print(f"Prime numbers between {Start} and {End}:")
for num in range(Start, End + 1):
    if is_prime_range(num):
        print(num, end=" ")
print("\n")
```


#### Result and viva tips — Prime numbers in a range

**Conclusion/Result:** All primes in the inclusive range are printed.

**Viva and practical tips:**
- Values <=1 are not prime; Start>End is empty. Approximate O(R*sqrt(M)) time for R candidates up to M.
- Use the correct loop condition and update to avoid off-by-one or non-terminating loops.
## Experiment 4 — Linear algebra operations (`sampleexp04.pdf`)

#### Practical write-up — NumPy vector and matrix operations

**Aim:** Demonstrate NumPy vector/matrix arithmetic, transpose, conjugate transpose, determinant, inverse, and eigenvalues.

**Theory:** NumPy arrays support arithmetic. Transpose swaps axes; conjugate transpose also conjugates complex values. Linear algebra routines calculate determinant, inverse, and eigenvalues.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create vectors and display sum and difference.
3. **Step 3:** Create A and B; display sum, difference, and A transpose.
4. **Step 4:** Create complex C and display conjugate transpose.
5. **Step 5:** Calculate determinant, inverse, and eigenvalues of A.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create vectors and matrices]
   ↓
[RECTANGLE — Calculate sums, differences, transposes, determinant, inverse, and eigenvalues]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
import numpy as np

# Vector operations
v1 = np.array([1, 2, 3])
v2 = np.array([4, 5, 6])
print("Vector 1:", v1)
print("Vector 2:", v2)
print("\nVector Addition:", v1 + v2)
print("Vector Subtraction:", v1 - v2)

# Matrix operations
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])
print("\nMatrix A:\n", A)
print("\nMatrix B:\n", B)
print("\nMatrix Addition:\n", A + B)
print("\nMatrix Subtraction:\n", A - B)
print("\nTranspose of A:\n", A.T)

# Conjugate transpose
C = np.array([[1 + 2j, 3 - 1j], [2 + 4j, 5 + 0j]])
print("\nComplex Matrix C:\n", C)
print("\nConjugate Transpose of C:\n", C.conj().T)

# Determinant, inverse, and eigenvalues
det_A = np.linalg.det(A)
print("\nDeterminant of A:", det_A)
inverse_A = np.linalg.inv(A)
print("\nInverse of A:\n", inverse_A)
eigenvalues, eigenvectors = np.linalg.eig(A)
print("\nEigenvalues:", eigenvalues)
```


#### Result and viva tips — NumPy vector and matrix operations

**Conclusion/Result:** The vector and matrix results are displayed.

**Viva and practical tips:**
- Shapes must match for addition/subtraction.
- A is nonsingular in this example; inverse of a singular matrix raises an error.
- Dense n×n determinant/inverse/eigen calculations are generally O(n³); these examples are small.
## Experiment 5 — Vector operations in quantum-state representation (`sampleexp05.pdf`)

#### Practical write-up — Quantum vector operations

**Aim:** Demonstrate complex-vector norms, normalization, products, and orthogonality.

**Theory:** Norm measures vector magnitude; normalization divides by norm. vdot computes a conjugate inner product and outer creates a matrix.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create complex vectors and display norms.
3. **Step 3:** Normalize v2; calculate inner and outer products.
4. **Step 4:** Calculate inner product of v1 and v3 and test orthogonality with isclose.
5. **Step 5:** Create basis vectors |0> and |1>; test their inner product.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create complex vectors]
   ↓
[RECTANGLE — Calculate norms and normalize v2]
   ↓
[RECTANGLE — Calculate inner and outer products]
   ↓
<DIAMOND — Is inner product close to zero?>
   ├─ Yes → /PARALLELOGRAM — Report orthogonal/
   └─ No → /PARALLELOGRAM — Report not orthogonal/
   ↓
(OVAL — STOP)
```

#### Program

```python
import numpy as np

v1 = np.array([1, 0], dtype=complex)
v2 = np.array([1, 1], dtype=complex)
print("Vector 1:", v1)
print("Vector 2:", v2)
print("\nMagnitude of Vector 1:", np.linalg.norm(v1))
print("Magnitude of Vector 2:", np.linalg.norm(v2))

v2_norm = v2 / np.linalg.norm(v2)
print("\nNormalized Vector 2:", v2_norm)
inner_product = np.vdot(v1, v2_norm)
print("\nInner Product:", inner_product)
outer_product = np.outer(v1, np.conjugate(v2_norm))
print("\nOuter Product:")
print(outer_product)

v3 = np.array([0, 1], dtype=complex)
inner_orthogonal = np.vdot(v1, v3)
print("\nVector 3:", v3)
print("Inner Product of Vector 1 and Vector 3:", inner_orthogonal)
if np.isclose(inner_orthogonal, 0):
    print("Vector 1 and Vector 3 are Orthogonal")
else:
    print("Vector 1 and Vector 3 are Not Orthogonal")

basis0 = np.array([1, 0], dtype=complex)
basis1 = np.array([0, 1], dtype=complex)
print("\nBasis Vectors:")
print("|0> =", basis0)
print("|1> =", basis1)
print("\nBasis Vector Inner Product:", np.vdot(basis0, basis1))
if np.isclose(np.vdot(basis0, basis1), 0):
    print("|0> and |1> are Orthogonal Basis Vectors")
```


#### Result and viva tips — Quantum vector operations

**Conclusion/Result:** Norms, normalized values, products, and orthogonality results are displayed.

**Viva and practical tips:**
- v2=[1,1] has norm √2 and normalizes to [1/√2,1/√2].
- isclose handles floating-point rounding in zero tests.
- A zero vector cannot be normalized; the source vectors are nonzero.
## Experiment 6 — Quantum-state transformations (`sampleexp06.pdf`)

#### Practical write-up — Hadamard and Pauli-X state transformations

**Aim:** Apply Hadamard and then Pauli-X to the initial column state |0>.

**Theory:** A gate matrix multiplies a column state from the left. In XH, H acts first because it is the rightmost matrix.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create state [1,0]ᵀ and Hadamard matrix H.
3. **Step 3:** Apply H to the state.
4. **Step 4:** Create Pauli-X matrix X.
5. **Step 5:** Calculate XH and apply it to the initial state.
6. **Step 6:** Display intermediate and final states; stop.
7. **Step 7:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create state and matrices]
   ↓
[RECTANGLE — Apply H to state]
   ↓
[RECTANGLE — Form X×H and apply the combined matrix]
   ↓
/PARALLELOGRAM — Display states/
   ↓
(OVAL — STOP)
```

#### Program

```python
import numpy as np

state = np.array([[1], [0]])
print("Initial Quantum State:")
print(state)

H = (1 / np.sqrt(2)) * np.array([[1, 1], [1, -1]])
print("Hadamard Matrix:")
print(H)
state_after_H = np.dot(H, state)
print("State after applying Hadamard Gate:")
print(state_after_H)

X = np.array([[0, 1], [1, 0]])
print("Pauli-X Matrix:")
print(X)

combined_matrix = np.dot(X, H)
print("Matrix Multiplication (X x H):")
print(combined_matrix)
final_state = np.dot(combined_matrix, state)
print("Final Quantum State:")
print(final_state)
```


#### Result and viva tips — Hadamard and Pauli-X state transformations

**Conclusion/Result:** The final equal superposition is unchanged by Pauli-X.

**Viva and practical tips:**
- Matrix multiplication is not commutative: XH can differ from HX.
- The rightmost matrix acts first on a column vector.
- Check dimensions: gates are 2×2 and state is 2×1.
## Experiment 7 — Identity matrices and unitary check (`sampleexp7.pdf`)

#### Practical write-up — Identity matrices and unitary check

**Aim:** Build one-, two-, and three-qubit identity matrices, apply them to normalized states, and check Pauli-X unitarity.

**Theory:** Kronecker products expand identities. Identity leaves states unchanged; U is unitary if U†U equals identity.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create I1 and form I2/I3 with Kronecker products.
3. **Step 3:** Normalize sample states and apply matching identities.
4. **Step 4:** Compare each state and result using allclose.
5. **Step 5:** Calculate X†X and compare with I1; form X tensor I1.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create I1, I2, and I3]
   ↓
[RECTANGLE — Apply identities to normalized states and compare]
   ↓
[RECTANGLE — Check X†X against I1 and form X tensor I1]
   ↓
/PARALLELOGRAM — Display matrices and results/
   ↓
(OVAL — STOP)
```

#### Program

```python
import numpy as np

# 1-, 2-, and 3-qubit identity matrices
I1 = np.eye(2, dtype=int)
I2 = np.kron(I1, I1)
I3 = np.kron(I2, I1)
print("1-Qubit Identity Matrix:")
print(I1)
print("\n2-Qubit Identity Matrix:")
print(I2)
print("\n3-Qubit Identity Matrix:")
print(I3)

psi = np.array([1 / np.sqrt(2), 1 / np.sqrt(2)])
result = I1 @ psi
print("Original state:")
print(psi)
print("After applying identity:")
print(result)
print("State unchanged:", np.allclose(psi, result))

psi_2 = np.array([1, 2, 3, 4], dtype=float)
psi_2 = psi_2 / np.linalg.norm(psi_2)
result_2 = I2 @ psi_2
print("Original:", psi_2)
print("After identity:", result_2)
print("Unchanged:", np.allclose(psi_2, result_2))

psi_3 = np.ones(8, dtype=float)
psi_3 = psi_3 / np.linalg.norm(psi_3)
result_3 = I3 @ psi_3
print("Original state:")
print(psi_3)
print("\nAfter applying identity:")
print(result_3)
print("\nUnchanged:", np.allclose(psi_3, result_3))

X = np.array([[0, 1], [1, 0]])
check = X.conj().T @ X
print("X†X =")
print(check)
print("X is unitary:", np.allclose(check, I1))

XI = np.kron(X, I1)
print(XI)
```


#### Result and viva tips — Identity matrices and unitary check

**Conclusion/Result:** Identity operations leave states unchanged and Pauli-X passes the check.

**Viva and practical tips:**
- Identity sizes are 2×2, 4×4, and 8×8.
- A nonzero state is normalized by dividing by its norm.
- allclose is appropriate for floating-point comparisons.
## Experiment 9 — Functions (`sampleexp9.pdf`)

#### Practical write-up — Functions and argument patterns

**Aim:** Demonstrate function arguments, return values, defaults, *args, **kwargs, and multiple returns.

**Theory:** return sends a value to the caller; *args collects positional values in a tuple and **kwargs collects named values in a dictionary.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Define the example functions.
3. **Step 3:** Read values and call square/cube, parity, and factorial functions.
4. **Step 4:** Call simple_interest using default rate and time.
5. **Step 5:** Call *args and **kwargs examples.
6. **Step 6:** Call calculate and unpack sum, average, and maximum.
7. **Step 7:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Values when prompted/
   ↓
[RECTANGLE — Call functions with ordinary and default arguments]
   ↓
[RECTANGLE — Use *args and **kwargs]
   ↓
[RECTANGLE — Return and unpack summary values]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Function with arguments and no return value
def square_cube(num):
    Square = num ** 2
    Cube = num ** 3
    print("Square =", Square)
    print("Cube =", Cube, "\n")

N = int(input("Enter a number: "))
square_cube(N)

# Function with arguments and a return value
def check_even_odd(num):
    if num % 2 == 0:
        return "Even"
    return "Odd"

N = int(input("Enter a number: "))
Result = check_even_odd(N)
print(f"{N} is {Result}.\n")

# Function to calculate factorial
def factorial(num):
    Fact = 1
    for i in range(1, num + 1):
        Fact *= i
    return Fact

N = int(input("Enter a number: "))
if N < 0:
    print("Factorial is not defined for negative numbers.\n")
else:
    print("Factorial =", factorial(N), "\n")

# Function with default arguments
def simple_interest(principal, rate=5, time=1):
    SI = (principal * rate * time) / 100
    print("Simple Interest =", SI, "\n")

P = float(input("Enter Principal Amount: "))
simple_interest(P)

# Function using *args
def calculate_sum(*args):
    Total = sum(args)
    print("Sum =", Total)

calculate_sum(10, 20, 30)
calculate_sum(5, 15, 25, 35, 45)
print("\n")

# Function using **kwargs
def employee_details(**kwargs):
    print("Employee Details:")
    for key, value in kwargs.items():
        print(f"{key}: {value}")
    print("\n")

employee_details(
    Name="David",
    Age=19,
    Gender="Female",
    Department="Computer Science",
    Location="Seattle",
)

# Function returning multiple values
def calculate(values):
    Total = sum(values)
    Average = Total / len(values)
    Maximum = max(values)
    return Total, Average, Maximum

Numbers = [10, 20, 30, 40, 50]
S, Avg, Mx = calculate(Numbers)
print("Sum =", S)
print("Average =", Avg)
print("Maximum =", Mx, "\n")
```


#### Result and viva tips — Functions and argument patterns

**Conclusion/Result:** Each function displays or returns the example result.

**Viva and practical tips:**
- Main checks negative factorial input; calculate assumes a nonempty list because it uses average/max.
- *args is a tuple, **kwargs a dictionary, and multiple returned values are packed in a tuple.
- calculate is O(n) for n values.
## Experiment 10 — Recursive functions (`sampleexp10.pdf`)

#### Practical write-up — Recursive Fibonacci, factorial, and digit sum

**Aim:** Demonstrate recursive Fibonacci, factorial, and sum of digits.

**Theory:** A recursive function calls itself on a smaller input and needs a base case to stop.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Define recursive functions and base cases.
3. **Step 3:** Read number of Fibonacci terms and calculate each term.
4. **Step 4:** Read a nonnegative value and calculate factorial recursively.
5. **Step 5:** Take absolute value and calculate digit sum recursively.
6. **Step 6:** Display results; stop.
7. **Step 7:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Terms and numbers/
   ↓
[RECTANGLE — Call recursive Fibonacci, factorial, and digit-sum functions]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Recursive Fibonacci function
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

Terms = int(input("Enter number of terms: "))
print("Fibonacci Series:")
for i in range(Terms):
    print(fibonacci(i), end=" ")
print("\n\n")

# Recursive factorial function
def factorial_rec(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial_rec(n - 1)

Num = int(input("Enter a number: "))
if Num < 0:
    print("Factorial is not defined for negative numbers.\n")
else:
    print("Factorial of", Num, "is", factorial_rec(Num), "\n")

# Recursive sum of digits
def sum_digits_rec(n):
    if n == 0:
        return 0
    return (n % 10) + sum_digits_rec(n // 10)

Num = abs(int(input("Enter a number: ")))
print("Sum of digits:", sum_digits_rec(Num), "\n")
```


#### Result and viva tips — Recursive Fibonacci, factorial, and digit sum

**Conclusion/Result:** The sequence, factorial, and digit sum are displayed.

**Viva and practical tips:**
- Naive Fibonacci repeats work and is exponential-time; memoization reduces it to O(n).
- Factorial and digit-sum recursion use O(n) and O(d) stack depth.
- Main guards negative factorial; fibonacci assumes nonnegative input.
## Experiment 11 — Operations on lists (`sampleexp-11.pdf`)

#### Practical write-up — Core list operations

**Aim:** Demonstrate list mutation, access, slicing, searching, sorting, copying, and summaries.

**Theory:** Lists are mutable ordered sequences. Some operations mutate the list; slicing and concatenation create new lists.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create sample lists.
3. **Step 3:** Apply append, insert, pop, remove, slicing, and extend.
4. **Step 4:** Access, concatenate, repeat, update, search, and compare.
5. **Step 5:** Sort/reverse and use count, copy, len, sum, max, clear, and del.
6. **Step 6:** Display results; stop.
7. **Step 7:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample lists]
   ↓
[RECTANGLE — Apply mutation, query, slicing, and ordering operations]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Append
A = [2, 3, 4, 5, 6, 9, 8]
A.append(10)
print("A =", A, "\n")

# Insert
A = [45, 67, 44, 14, 22, 13]
A.insert(3, 50)
print("A =", A, "\n")

# Delete by index (pop)
A = [22, 45, 14, 5, 67, 88]
A.pop(4)
print("A =", A, "\n")

# Remove by value
A = [45, 67, 33, 69, 39, 40]
A.remove(40)
print("A =", A, "\n")

# Slicing
A = [12, 46, 67, 33, 45, 22, 90, 55]
Slice_Start = A[0:7]
print("Slice:", Slice_Start, "\n")

# Extend
A = [22, 45, 5, 78, 14, 60]
B = [1, 2, 4, 10]
A.extend(B)
print("Extended A:", A, "\n")

# Indexing
A = [12, 23, 34, 56, 67, 78]
print("Element at index 4:", A[4], "\n")

# Concatenation
A = [44, 56, 67, 12, 34]
B = [50, 34, 22, 1]
print("Concatenation:", A + B, "\n")

# Repetition
A = [20, 30, 40]
print("Repetition:", A * 4, "\n")

# Updating
A = [34, 2, 12, 66, 7, 98]
print("Before update element at index 2:", A[2])
A[2] = 80
print("Updated A:", A, "\n")

# Membership
A = [23, 44, 36, 88, 79]
print("Is 5 in A?", 5 in A, "\n")

# Comparison
A = [33, 4, 5, 13, 88]
B = [45, 56, 7, 78]
print("Is A != B?", A != B, "\n")

# Sorting
A = [3, 5, 9, 4, 2, 7, 6]
A.sort()
print("Sorted A:", A, "\n")

# Reversing
B = [78, 68, 33, 90, 34, 14, 44]
B.reverse()
print("Reversed B:", B, "\n")

# Count, copy, length, sum, maximum, clear, and delete
A = [4, 6, 9, 7, 2, 8, 9]
print("Count of 9 in A:", A.count(9), "\n")
A = [2, 3, 4, 5, 5, 6, 7, 7, 8]
B = A.copy()
print("Copied B:", B, "\n")
A = [4, 5, 6, 778, 89, 23]
print("Length of A:", len(A), "\n")
A = [22, 45, 6, 3, 21, 2]
print("Sum of A:", sum(A), "\n")
A = [23, 88, 98, 786, 14, 2]
print("Maximum in A:", max(A), "\n")
A = [23, 4, 5, 67, 78, 90]
A.clear()
print("Cleared A:", A, "\n")
A = [3, 54, 56, 67, 78, 98]
del A[3]
print("After deleting element at index 3:", A, "\n")
```


#### Result and viva tips — Core list operations

**Conclusion/Result:** The sample operations display their results.

**Viva and practical tips:**
- append is amortized O(1); middle insert/delete and membership are O(n); sorting is O(n log n).
- pop uses an index; remove uses a value and raises ValueError if missing.
- sort/reverse mutate; slicing and concatenation create new lists; copy is shallow.
## Experiments 11 & 12 — Advanced list and set operations (`sampleexp11&12.pdf`)

#### Practical write-up — Advanced list and set operations

**Aim:** Demonstrate reverse iteration, min/max scan, list operations, and set operations.

**Theory:** Lists preserve order and duplicates; sets retain unique items and support membership, union, intersection, and difference.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create sample lists.
3. **Step 3:** Reverse-iterate and scan for minimum and maximum.
4. **Step 4:** Extend a list and find common elements.
5. **Step 5:** Convert a list to a set; demonstrate search, difference, union, and intersection.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create lists and sets]
   ↓
[RECTANGLE — Reverse-iterate and scan for min/max]
   ↓
[RECTANGLE — Extend and find common values]
   ↓
[RECTANGLE — Apply set operations]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Reverse list iteration
print("--- Reverse List Iteration ---")
A = [1, 2, 3, 4, 5]
for i in range(len(A) - 1, -1, -1):
    print(A[i], end=" ")
print("\n\n")

# Maximum and minimum in a list
print("--- Max and Min in List ---")
A = [10, 25, 8, 50, 3]
Maximum = A[0]
Minimum = A[0]
for i in A:
    if i > Maximum:
        Maximum = i
    if i < Minimum:
        Minimum = i
print("Maximum =", Maximum)
print("Minimum =", Minimum, "\n")

# Extend list
print("--- Extend List ---")
List1 = [1, 2, 3]
List2 = [4, 5, 6]
List1.extend(List2)
print("Extended List:", List1, "\n")

# Common elements in two lists
print("--- Common Elements ---")
List1 = [1, 2, 3, 4]
List2 = [3, 4, 5, 6]
Common = []
for i in List1:
    if i in List2:
        Common.append(i)
print("Common Elements:", Common, "\n")

# Create set from list
print("--- Set Creation ---")
List1 = [1, 2, 2, 3, 4, 4, 5]
Set1 = set(List1)
print("Set from list:", Set1, "\n")

# Element search in set
print("--- Set Element Search ---")
Set1 = {"apple", "banana", "cherry"}
if "banana" in Set1:
    print("Element Found\n")
else:
    print("Element Not Found\n")

# Set difference
print("--- Set Difference ---")
Set1 = {1, 2, 3, 4}
Set2 = {3, 4, 5, 6}
print("Difference (Set1 - Set2):", Set1.difference(Set2), "\n")

# Set union
print("--- Set Union ---")
Set1 = {1, 2, 3}
Set2 = {3, 4, 5}
print("Union:", Set1.union(Set2), "\n")

# Set intersection
print("--- Set Intersection ---")
Set1 = {1, 2, 3}
Set2 = {2, 3, 4}
print("Intersection:", Set1.intersection(Set2), "\n")
```


#### Result and viva tips — Advanced list and set operations

**Conclusion/Result:** The examples display requested list and set results.

**Viva and practical tips:**
- The min/max scan starts at A[0], so assumes a nonempty list.
- The common-element loop is O(nm) worst-case; duplicate source values can repeat in output.
- Set conversion removes duplicates and display order is not guaranteed.
## Experiment 13 — Tuple operations (`sampleexp13.pdf`)

#### Practical write-up — Tuple operations

**Aim:** Demonstrate tuple access, slicing, summaries, search, filtering, duplicate removal, ordering, reversal, and name deletion.

**Theory:** Tuples are ordered and immutable. Slicing/concatenation create new tuples; dict.fromkeys preserves first-seen order while removing duplicates.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create tuples and access, combine, or slice values.
3. **Step 3:** Calculate sum, average, and length; search and filter even/odd values.
4. **Step 4:** Remove duplicates and sort distinct values for second extremes.
5. **Step 5:** Reverse a tuple and delete a tuple variable name.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Search value when prompted/
   ↓
[RECTANGLE — Access, slice, and combine tuples]
   ↓
[RECTANGLE — Calculate summaries and filter values]
   ↓
[RECTANGLE — Remove duplicates, sort, reverse, and delete a name]
   ↓
/PARALLELOGRAM — Display results/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Accessing
print("--- Tuple Accessing ---")
A = (10, 20, 30, 40)
print("Element at index 3:", A[3], "\n")

# Concatenation
print("--- Tuple Concatenation ---")
A = (20, 30, 40, 59, 90)
B = (34, 56, 60, 79, 90)
C = A + B
print("The new tuple is:", C, "\n")

# Slicing
print("--- Tuple Slicing ---")
A = (20, 30, 40, 59, 90)
print("Sliced Tuple:", A[:4], "\n")

# Sum and average
print("--- Sum and Average ---")
T = (10, 20, 30, 40, 50)
Total = sum(T)
Average = Total / len(T)
print("Sum =", Total)
print("Average =", Average, "\n")

# Length of tuple
print("--- Length Calculation ---")
T = (10, 20, 30, 40, 50)
Count = 0
for i in T:
    Count += 1
print("Length of tuple =", Count, "\n")

# Search element
print("--- Search Element ---")
T = (10, 20, 30, 40, 50)
Element = int(input("Enter element to search: "))
if Element in T:
    print("Element exists in the tuple.\n")
else:
    print("Element does not exist.\n")

# Extract even and odd numbers
print("--- Even and Odd Extraction ---")
T = (18, 15, 22, 37, 48, 51, 64)
print("Even numbers:")
for i in T:
    if i % 2 == 0:
        print(i, end=" ")
print("\nOdd numbers:")
for i in T:
    if i % 2 != 0:
        print(i, end=" ")
print("\n\n")

# Remove duplicates while preserving order
print("--- Remove Duplicates ---")
T = (10, 20, 10, 30, 40, 20, 50)
New_Tuple = tuple(dict.fromkeys(T))
print("Original tuple:", T)
print("Tuple after removing duplicates:", New_Tuple, "\n")

# Second-smallest and second-largest distinct values
print("--- Second Smallest and Largest ---")
T = (10, 50, 30, 20, 40)
Values = sorted(set(T))
if len(Values) < 2:
    raise ValueError("At least two distinct values are required")
print("Second smallest =", Values[1])
print("Second largest =", Values[-2], "\n")

# Reverse tuple
print("--- Reverse Tuple ---")
T = (10, 20, 30, 40, 50)
Rev = ()
for i in T:
    Rev = (i,) + Rev
print("Original tuple:", T)
print("Reversed tuple:", Rev, "\n")

# Delete tuple name
print("--- Tuple Deletion ---")
A = (1, 2, 3, 4, 5, 6, 7, 8, 9, 0)
print("Before Deletion:", A)
del A
print("Tuple variable deleted")
```


#### Result and viva tips — Tuple operations

**Conclusion/Result:** Results for the tuple operations are displayed.

**Viva and practical tips:**
- Tuples cannot be changed in place; del A removes the name, not an object referenced elsewhere.
- Second-extreme code checks for two distinct values; average assumes nonempty tuple.
- Search is O(n); sorting distinct values is O(n log n).
## Experiment 14 — Dictionary operations (`sampleexp14.pdf`)

The following snippets are separate exercises; each creates its own sample dictionary.

#### Practical write-up — Create a dictionary and display all keys and values

**Aim:** Display dictionary keys.

**Theory:** A view or items iterator can be traversed with a loop.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Visit each keys.
4. **Step 4:** Print each item.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create dictionary]
   ↓
<DIAMOND — Is another entry available?>
   ├─ Yes → /PARALLELOGRAM — Display item/ → [RECTANGLE — Advance] ↖
   └─ No → (OVAL — STOP)
```

#### Program

```python
# Create a dictionary and display all keys and values
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
print("Student Details:")
for Key, Value in Student.items():
    print(Key, ":", Value)
```


#### Result and viva tips — Create a dictionary and display all keys and values

**Conclusion/Result:** The sample dictionary's keys are displayed.

**Viva and practical tips:**
- Displaying n pairs is O(n).
- Keys are unique; assigning an existing key replaces its value.
#### Practical write-up — Access values using keys

**Aim:** Use a sample dictionary to look up sample fields by key.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Look up sample fields by key
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Look up sample fields by key]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Access values using keys
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
print("Roll No:", Student["Roll No"])
print("Name:", Student["Name"])
print("Age:", Student["Age"])
print("Location:", Student["Location"], "\n")
```


#### Result and viva tips — Access values using keys

**Conclusion/Result:** The result of look up sample fields by key is shown.

**Viva and practical tips:**
- Average lookup is O(1).
- A missing key raises KeyError; get can provide a default.
#### Practical write-up — Count key-value pairs

**Aim:** Use a sample dictionary to count entries with len().

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Count entries with len()
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Count entries with len()]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count key-value pairs
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
print("Total key-value pairs:", len(Student), "\n")
```


#### Result and viva tips — Count key-value pairs

**Conclusion/Result:** The result of count entries with len() is shown.

**Viva and practical tips:**
- len is O(1).
- Adding a new key changes the count; changing a value does not.
#### Practical write-up — Check whether a key exists

**Aim:** Check whether the entered key is present.

**Theory:** in tests dictionary keys.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Read a key.
4. **Step 4:** Test membership.
5. **Step 5:** Display whether it exists.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Search key/
   ↓
<DIAMOND — Is key present?>
   ├─ Yes → /PARALLELOGRAM — Display exists/
   └─ No → /PARALLELOGRAM — Display not found/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Check whether a key exists
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
Key_Search = input("Enter key to search: ")
if Key_Search in Student:
    print("Key exists in dictionary\n")
else:
    print("Key does not exist in dictionary\n")
```


#### Result and viva tips — Check whether a key exists

**Conclusion/Result:** The membership result is displayed.

**Viva and practical tips:**
- in tests keys, not values; average lookup is O(1).
- Entered text must match exactly.
#### Practical write-up — Update an existing value

**Aim:** Use a sample dictionary to assign a new value to age.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Assign a new value to Age
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Assign a new value to Age]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Update an existing value
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
Student["Age"] = 20
print("Updated dictionary:", Student, "\n")
```


#### Result and viva tips — Update an existing value

**Conclusion/Result:** The result of assign a new value to age is shown.

**Viva and practical tips:**
- Average lookup/update is O(1).
- Assigning a missing key creates an entry.
#### Practical write-up — Add a key-value pair

**Aim:** Use a sample dictionary to add gender and its value.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Add Gender and its value
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Add Gender and its value]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Add a key-value pair
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
Student["Gender"] = "Female"
print("Updated dictionary:", Student, "\n")
```


#### Result and viva tips — Add a key-value pair

**Conclusion/Result:** The result of add gender and its value is shown.

**Viva and practical tips:**
- Average insertion is O(1).
- An existing key's value is replaced.
#### Practical write-up — Delete a specific key

**Aim:** Use a sample dictionary to remove a key with del.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Remove a key with del
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Remove a key with del]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Delete a specific key
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
del Student["Location"]
print("Dictionary after deletion:", Student, "\n")
```


#### Result and viva tips — Delete a specific key

**Conclusion/Result:** The result of remove a key with del is shown.

**Viva and practical tips:**
- Average deletion is O(1).
- Deleting a missing key raises KeyError.
#### Practical write-up — Remove the last inserted key-value pair

**Aim:** Use a sample dictionary to remove the last inserted pair with popitem().

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Remove the last inserted pair with popitem()
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Remove the last inserted pair with popitem()]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Remove the last inserted key-value pair
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
Removed = Student.popitem()
print("Removed item:", Removed)
print("Dictionary:", Student, "\n")
```


#### Result and viva tips — Remove the last inserted key-value pair

**Conclusion/Result:** The result of remove the last inserted pair with popitem() is shown.

**Viva and practical tips:**
- Average removal is O(1).
- An empty dictionary raises KeyError.
#### Practical write-up — Clear all dictionary entries

**Aim:** Use a sample dictionary to remove all entries with clear().

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Remove all entries with clear()
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Remove all entries with clear()]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Clear all dictionary entries
Student = {"Roll No": 42, "Name": "David", "Age": 21, "Location": "Seattle"}
Student.clear()
print("Dictionary after clearing:", Student, "\n")
```


#### Result and viva tips — Clear all dictionary entries

**Conclusion/Result:** The result of remove all entries with clear() is shown.

**Viva and practical tips:**
- Clearing n entries is O(n).
- The dictionary object remains available.
#### Practical write-up — Display all key-value pairs with items()

**Aim:** Display dictionary pairs.

**Theory:** A view or items iterator can be traversed with a loop.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Visit each pairs.
4. **Step 4:** Print each item.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create dictionary]
   ↓
<DIAMOND — Is another entry available?>
   ├─ Yes → /PARALLELOGRAM — Display item/ → [RECTANGLE — Advance] ↖
   └─ No → (OVAL — STOP)
```

#### Program

```python
# Display all key-value pairs with items()
Student = {"Roll No": 42, "Name": "David", "Course": "Computer Science", "CGPA": 8.5}
for Key, Value in Student.items():
    print(Key, ":", Value)
```


#### Result and viva tips — Display all key-value pairs with items()

**Conclusion/Result:** The sample dictionary's pairs are displayed.

**Viva and practical tips:**
- Displaying all pairs is O(n).
- items() is a dynamic view.
#### Practical write-up — Display all keys

**Aim:** Use a sample dictionary to display the keys() view.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Display the keys() view
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Display the keys() view]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Display all keys
Student = {"Roll No": 42, "Name": "David", "Course": "Computer Science", "CGPA": 8.5}
print("Keys:", Student.keys(), "\n")
```


#### Result and viva tips — Display all keys

**Conclusion/Result:** The result of display the keys() view is shown.

**Viva and practical tips:**
- Printing all keys takes O(n).
- keys() is a view, not a list copy.
#### Practical write-up — Display keys using a loop

**Aim:** Display dictionary keys.

**Theory:** A view or items iterator can be traversed with a loop.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Visit each keys.
4. **Step 4:** Print each item.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create dictionary]
   ↓
<DIAMOND — Is another entry available?>
   ├─ Yes → /PARALLELOGRAM — Display item/ → [RECTANGLE — Advance] ↖
   └─ No → (OVAL — STOP)
```

#### Program

```python
# Display keys using a loop
Student = {"Roll No": 42, "Name": "David", "Course": "Computer Science", "CGPA": 8.5}
for Key in Student.keys():
    print(Key)
```


#### Result and viva tips — Display keys using a loop

**Conclusion/Result:** The sample dictionary's keys are displayed.

**Viva and practical tips:**
- The loop is O(n).
- Modern Python dictionaries preserve insertion order.
#### Practical write-up — Display all values

**Aim:** Display dictionary values.

**Theory:** A view or items iterator can be traversed with a loop.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Visit each values.
4. **Step 4:** Print each item.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create dictionary]
   ↓
<DIAMOND — Is another entry available?>
   ├─ Yes → /PARALLELOGRAM — Display item/ → [RECTANGLE — Advance] ↖
   └─ No → (OVAL — STOP)
```

#### Program

```python
# Display all values
Student = {"Roll No": 42, "Name": "David", "Course": "Computer Science", "CGPA": 8.5}
for Value in Student.values():
    print(Value)
```


#### Result and viva tips — Display all values

**Conclusion/Result:** The sample dictionary's values are displayed.

**Viva and practical tips:**
- Displaying values is O(n).
- Values may repeat.
#### Practical write-up — Sum numeric values

**Aim:** Use a sample dictionary to sum the marks values.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Sum the marks values
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Sum the marks values]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Sum numeric values
Marks = {"Maths": 80, "Physics": 75, "Chemistry": 85, "Python": 90}
Total = sum(Marks.values())
print("Sum of values:", Total, "\n")
```


#### Result and viva tips — Sum numeric values

**Conclusion/Result:** The result of sum the marks values is shown.

**Viva and practical tips:**
- sum takes O(n).
- Values must be numeric; keys are not added.
#### Practical write-up — Find maximum and minimum values

**Aim:** Use a sample dictionary to find max and min of values.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Find max and min of values
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Find max and min of values]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Find maximum and minimum values
Marks = {"Maths": 80, "Physics": 75, "Chemistry": 85, "Python": 90}
Maximum = max(Marks.values())
Minimum = min(Marks.values())
print("Maximum value:", Maximum)
print("Minimum value:", Minimum, "\n")
```


#### Result and viva tips — Find maximum and minimum values

**Conclusion/Result:** The result of find max and min of values is shown.

**Viva and practical tips:**
- Two scans take O(n).
- An empty dictionary raises ValueError.
#### Practical write-up — Reverse dictionary item order

**Aim:** Use a sample dictionary to reverse items and build a new dictionary.

**Theory:** A dictionary maps unique keys to values; this snippet applies one operation to a fixed example.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Create the sample dictionary.
3. **Step 3:** Perform Reverse items and build a new dictionary
4. **Step 4:** Display the selected value or changed dictionary.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Create sample dictionary]
   ↓
[RECTANGLE — Reverse items and build a new dictionary]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Reverse dictionary item order
Student = {"Roll No": 42, "Name": "David", "Course": "Computer Science", "CGPA": 8.5}
Reverse = dict(reversed(list(Student.items())))
print("Original dictionary:", Student)
print("Reversed dictionary:", Reverse, "\n")
```


#### Result and viva tips — Reverse dictionary item order

**Conclusion/Result:** The result of reverse items and build a new dictionary is shown.

**Viva and practical tips:**
- Uses O(n) time and O(n) extra space.
- The original dictionary is unchanged.
## Experiment 15 — String operations (`sampleexp15.pdf`)

#### Practical write-up — List slicing (as shown in source)

**Aim:** Perform the string task: slice positions 1 through 3 of a list.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Slice positions 1 through 3 of a list.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Slice positions 1 through 3 of a list]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# List slicing (as shown in source)
Numbers = [10, 20, 30, 40, 50, 60]
print("Sliced list:", Numbers[1:4], "\n")
```


#### Result and viva tips — List slicing (as shown in source)

**Conclusion/Result:** The result of slice positions 1 through 3 of a list is displayed.

**Viva and practical tips:**
- This source block slices a list, not a string.
- The stop index is excluded; slicing k items is O(k).
#### Practical write-up — String concatenation

**Aim:** Perform the string task: join two strings with a space.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Join two strings with a space.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Join two strings with a space]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# String concatenation
First = "Hello"
Second = "Python"
Result = First + " " + Second
print("Concatenation:", Result, "\n")
```


#### Result and viva tips — String concatenation

**Conclusion/Result:** The result of join two strings with a space is displayed.

**Viva and practical tips:**
- Strings are immutable; + creates a new string.
- The separator space is inserted explicitly.
#### Practical write-up — String length

**Aim:** Perform the string task: find the sample string length.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Find the sample string length.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Find the sample string length]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# String length
A = "college"  # Corrected spelling from source's "collage".
print("Length of string:", len(A))
print("String:", A, "\n")
```


#### Result and viva tips — String length

**Conclusion/Result:** The result of find the sample string length is displayed.

**Viva and practical tips:**
- college has length 7.
- len is O(1) for Python strings.
#### Practical write-up — Uppercase and lowercase conversions

**Aim:** Perform the string task: convert combined text to upper and lower case.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Convert combined text to upper and lower case.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Convert combined text to upper and lower case]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Uppercase and lowercase conversions
First = "Hello"
Second = "Alex"
Result = First + " " + Second
print("Uppercase:", Result.upper())
print("Lowercase:", Result.lower(), "\n")
```


#### Result and viva tips — Uppercase and lowercase conversions

**Conclusion/Result:** The result of convert combined text to upper and lower case is displayed.

**Viva and practical tips:**
- upper/lower return new strings.
- Each conversion is O(n).
#### Practical write-up — Replace substring

**Aim:** Perform the string task: replace world with python.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Replace World with Python.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Replace World with Python]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Replace substring
Text = "Hello World"
Text = Text.replace("World", "Python")
print("Replaced string:", Text, "\n")
```


#### Result and viva tips — Replace substring

**Conclusion/Result:** The result of replace world with python is displayed.

**Viva and practical tips:**
- replace returns a new string and replaces all exact matches.
- Absent old text leaves the string unchanged.
#### Practical write-up — Count vowels, consonants, digits, and other characters

**Aim:** Perform the task: Count input characters by category.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count vowels, consonants, digits, and other characters
Text = input("Enter a string: ")
Vowels = Consonants = Digits = Special = 0
for Ch in Text:
    if Ch.isalpha():
        if Ch.lower() in "aeiou":
            Vowels += 1
        else:
            Consonants += 1
    elif Ch.isdigit():
        Digits += 1
    else:
        Special += 1
print("Vowels:", Vowels)
print("Consonants:", Consonants)
print("Digits:", Digits)
print("Special Characters:", Special, "\n")
```


#### Result and viva tips — Count vowels, consonants, digits, and other characters

**Conclusion/Result:** The result for count input characters by category is displayed.

**Viva and practical tips:**
- One pass is O(n), with O(1) counters.
- Spaces and punctuation count as special characters here.
#### Practical write-up — Frequency of a specific character

**Aim:** Perform the task: Count exact occurrences of the entered character.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Frequency of a specific character
Text = input("Enter a string: ")
Ch = input("Enter character to find: ")
Count = 0
for C in Text:
    if C == Ch:
        Count += 1
print("Frequency of", Ch, "is:", Count, "\n")
```


#### Result and viva tips — Frequency of a specific character

**Conclusion/Result:** The result for count exact occurrences of the entered character is displayed.

**Viva and practical tips:**
- Comparison is case-sensitive; scan is O(n).
- A multi-character search value will not match a single character.
#### Practical write-up — Count words starting with a vowel

**Aim:** Perform the task: Count words whose first character is a vowel.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count words starting with a vowel
Sentence = input("Enter a sentence: ")
Words = Sentence.split()
Count = sum(1 for Word in Words if Word[0].lower() in "aeiou")
print("Words starting with a vowel:", Count, "\n")
```


#### Result and viva tips — Count words starting with a vowel

**Conclusion/Result:** The result for count words whose first character is a vowel is displayed.

**Viva and practical tips:**
- split separates on whitespace; scan is O(n).
- Empty input yields zero words safely.
#### Practical write-up — Find longest and shortest word

**Aim:** Find the longest and shortest word.

**Theory:** split creates words; max/min select by length.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read and split the sentence.
3. **Step 3:** If empty, display the no-words message.
4. **Step 4:** Otherwise select longest and shortest.
5. **Step 5:** Display them and stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input sentence/
   ↓
[RECTANGLE — Split into words]
   ↓
<DIAMOND — Is list empty?>
   ├─ Yes → /PARALLELOGRAM — Display no-words message/ → (OVAL — STOP)
   └─ No → [RECTANGLE — Select longest and shortest]
              ↓
            /PARALLELOGRAM — Display words/
              ↓
            (OVAL — STOP)
```

#### Program

```python
# Find longest and shortest word
Sentence = input("Enter a sentence: ")
Words = Sentence.split()
if not Words:
    print("No words were entered.")
else:
    Longest = max(Words, key=len)
    Shortest = min(Words, key=len)
    print("Longest word:", Longest)
    print("Shortest word:", Shortest, "\n")
```


#### Result and viva tips — Find longest and shortest word

**Conclusion/Result:** The selected words or empty-input message are displayed.

**Viva and practical tips:**
- Empty input is handled.
- The scan is O(w) for w words; ties return first matching word.
#### Practical write-up — Find most frequent character

**Aim:** Find a most frequent character and its count.

**Theory:** The code tests distinct characters using str.count.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text.
3. **Step 3:** If empty, display the empty-input message.
4. **Step 4:** Otherwise find a character with greatest count.
5. **Step 5:** Display character and frequency; stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text/
   ↓
<DIAMOND — Is text empty?>
   ├─ Yes → /PARALLELOGRAM — Display empty message/ → (OVAL — STOP)
   └─ No → [RECTANGLE — Count each distinct character]
              ↓
            /PARALLELOGRAM — Display selected character and count/
              ↓
            (OVAL — STOP)
```

#### Program

```python
# Find most frequent character
Text = input("Enter a string: ")
if not Text:
    print("No characters were entered.")
else:
    Most_Frequent = max(set(Text), key=Text.count)
    print("Most frequent character:", Most_Frequent)
    print("Frequency:", Text.count(Most_Frequent), "\n")
```


#### Result and viva tips — Find most frequent character

**Conclusion/Result:** The most frequent character and its count are displayed.

**Viva and practical tips:**
- Empty input is handled.
- str.count for each distinct character can make this O(n²); tie choice is not fixed.
#### Practical write-up — Count words in a sentence

**Aim:** Perform the task: Count whitespace-separated words.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count words in a sentence
Sentence = input("Enter a sentence: ")
Words = Sentence.split()
print("Number of words:", len(Words), "\n")
```


#### Result and viva tips — Count words in a sentence

**Conclusion/Result:** The result for count whitespace-separated words is displayed.

**Viva and practical tips:**
- split collapses repeated whitespace.
- Empty input has zero words; scan is O(n).
#### Practical write-up — Find duplicate words

**Aim:** Perform the task: Find repeated words without listing them more than once.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Find duplicate words
Sentence = input("Enter a sentence: ")
Words = Sentence.lower().split()
Duplicates = []
for Word in Words:
    if Words.count(Word) > 1 and Word not in Duplicates:
        Duplicates.append(Word)
print("Duplicate words:", Duplicates, "\n")
```


#### Result and viva tips — Find duplicate words

**Conclusion/Result:** The result for find repeated words without listing them more than once is displayed.

**Viva and practical tips:**
- Input is lowercased, so matching ignores case.
- Words.count in a loop can be O(w²).
#### Practical write-up — Remove duplicate words while preserving order

**Aim:** Perform the task: Keep each word's first occurrence in order.

**Theory:** The program scans or splits text and applies a character or word condition.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read text or sentence.
3. **Step 3:** Scan characters/words and apply the condition.
4. **Step 4:** Display count or selected words.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Text or sentence/
   ↓
[RECTANGLE — Scan and apply the condition]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Remove duplicate words while preserving order
Sentence = input("Enter a sentence: ")
Words = Sentence.split()
Result = list(dict.fromkeys(Words))
New_Sentence = " ".join(Result)
print("After removing duplicates:")
print(New_Sentence, "\n")
```


#### Result and viva tips — Remove duplicate words while preserving order

**Conclusion/Result:** The result for keep each word's first occurrence in order is displayed.

**Viva and practical tips:**
- dict.fromkeys preserves first-seen order; average work O(w).
- This version is case-sensitive.
#### Practical write-up — Reverse each word in a sentence

**Aim:** Perform the string task: reverse each word while keeping word order.

**Theory:** Strings are immutable sequences; slicing and methods return values rather than changing a string in place.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set or read the source text.
3. **Step 3:** Perform Reverse each word while keeping word order.
4. **Step 4:** Display the result.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Input text if requested/
   ↓
[RECTANGLE — Reverse each word while keeping word order]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Reverse each word in a sentence
Sentence = input("Enter a sentence: ")
Words = Sentence.split()
Result = [Word[::-1] for Word in Words]
New_Sentence = " ".join(Result)
print("Reversed words:")
print(New_Sentence, "\n")
```


#### Result and viva tips — Reverse each word in a sentence

**Conclusion/Result:** The result of reverse each word while keeping word order is displayed.

**Viva and practical tips:**
- Words are reversed with slicing.
- split/join normalize whitespace; work is O(n).
#### Practical write-up — Basic email validation

**Aim:** Apply the source's basic email-like checks.

**Theory:** The conditions check one @, a dot, and simple placement rules only.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read email text.
3. **Step 3:** Check all simple format conditions.
4. **Step 4:** Display Valid if all pass, otherwise Invalid.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
/PARALLELOGRAM — Email text/
   ↓
<DIAMOND — Do all simple checks pass?>
   ├─ Yes → /PARALLELOGRAM — Display Valid/
   └─ No → /PARALLELOGRAM — Display Invalid/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Basic email validation
Email = input("Enter email address: ")
if (
    "@" in Email
    and "." in Email
    and Email.count("@") == 1
    and not Email.startswith("@")
    and not Email.endswith("@")
    and not Email.startswith(".")
    and not Email.endswith(".")
):
    print("Valid email address\n")
else:
    print("Invalid email address\n")
```


#### Result and viva tips — Basic email validation

**Conclusion/Result:** The program reports whether its conditions pass.

**Viva and practical tips:**
- Checks @ count, a dot, and simple placement only.
- This is not full email-standard validation.
## Experiment 16 — File operations (`sampleexp16.pdf`)

The PDF labels this experiment as “String Operations and Manipulations,” but its programs demonstrate file handling, so this heading reflects the code content.

#### Practical write-up — Read a file if it exists

**Aim:** Display student.txt if its path exists; otherwise show a message.

**Theory:** exists checks path existence before opening.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Set filename.
3. **Step 3:** Check whether the path exists.
4. **Step 4:** If yes, read and display; otherwise show missing-file message.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Set filename]
   ↓
<DIAMOND — Does path exist?>
   ├─ Yes → [RECTANGLE — Open and read file] → /PARALLELOGRAM — Display contents/
   └─ No → /PARALLELOGRAM — Display missing-file message/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Read a file if it exists
import os

filename = "student.txt"
if os.path.exists(filename):
    with open(filename, "r") as file:
        print(file.read())
else:
    print("File does not exist.")
```


#### Result and viva tips — Read a file if it exists

**Conclusion/Result:** File contents or a missing-file message are displayed.

**Viva and practical tips:**
- exists does not guarantee a file can be opened.
- Relative paths use the current working folder; with closes the file.
#### Practical write-up — Read the first three lines

**Aim:** Display up to the first three lines.

**Theory:** readline returns an empty string at end-of-file.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Open the file.
3. **Step 3:** Read and display up to three lines.
4. **Step 4:** Stop early at EOF; close automatically.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Open file]
   ↓
<DIAMOND — Three lines read or EOF?>
   ├─ No → [RECTANGLE — Read next line] → /PARALLELOGRAM — Display line/ ↖
   └─ Yes → (OVAL — STOP)
```

#### Program

```python
# Read the first three lines
filename = "student.txt"
with open(filename, "r") as file:
    for i in range(3):
        line = file.readline()
        if line == "":
            break
        print(line, end="")
```


#### Result and viva tips — Read the first three lines

**Conclusion/Result:** Up to three lines are displayed.

**Viva and practical tips:**
- readline returns empty text at EOF.
- Short files display available lines only.
#### Practical write-up — Read the last three lines

**Aim:** Display the last three lines.

**Theory:** readlines stores lines in a list; negative slicing selects up to three at the end.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read all lines.
3. **Step 3:** Select the last three.
4. **Step 4:** Display them and stop.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read lines]
   ↓
[RECTANGLE — Select last three]
   ↓
/PARALLELOGRAM — Display selected lines/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Read the last three lines
filename = "student.txt"
with open(filename, "r") as file:
    lines = file.readlines()
for line in lines[-3:]:
    print(line, end="")
```


#### Result and viva tips — Read the last three lines

**Conclusion/Result:** The last available lines are displayed.

**Viva and practical tips:**
- readlines stores the whole file, O(n) memory.
- A short file returns fewer than three lines.
#### Practical write-up — Read the last three lines (repeated example in source)

**Aim:** Display the last three lines.

**Theory:** readlines stores lines in a list; negative slicing selects up to three at the end.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read all lines.
3. **Step 3:** Select the last three.
4. **Step 4:** Display them and stop.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read lines]
   ↓
[RECTANGLE — Select last three]
   ↓
/PARALLELOGRAM — Display selected lines/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Read the last three lines (repeated example in source)
filename = "student.txt"
with open(filename, "r") as file:
    lines = file.readlines()
for line in lines[-3:]:
    print(line, end="")
```


#### Result and viva tips — Read the last three lines (repeated example in source)

**Conclusion/Result:** The last available lines are displayed.

**Viva and practical tips:**
- This repeated source example loads all lines, O(n) memory.
- Short files yield fewer lines.
#### Practical write-up — Count lines, words, and characters

**Aim:** Count lines, words, and characters.

**Theory:** A context manager reads text from the file before a summary or transformation is applied.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Open the file with a context manager.
3. **Step 3:** Read its content or lines.
4. **Step 4:** Apply Count lines, words, and characters.
5. **Step 5:** Display result and stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Open and read file]
   ↓
[RECTANGLE — Count lines, words, and characters]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count lines, words, and characters
with open("student.txt") as f:
    data = f.read()
print("No. of Lines:", len(data.splitlines()))
print("No. of Words:", len(data.split()))
print("No. of Characters:", len(data))
```


#### Result and viva tips — Count lines, words, and characters

**Conclusion/Result:** The result of count lines, words, and characters is displayed.

**Viva and practical tips:**
- Reading/scanning is O(n) time and O(n) memory.
- Check how the selected split expression counts empty files and newlines.
#### Practical write-up — Count digits and special characters

**Aim:** Count digits and special characters.

**Theory:** A context manager reads text from the file before a summary or transformation is applied.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Open the file with a context manager.
3. **Step 3:** Read its content or lines.
4. **Step 4:** Apply Count digits and special characters.
5. **Step 5:** Display result and stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Open and read file]
   ↓
[RECTANGLE — Count digits and special characters]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Count digits and special characters
with open("student.txt") as f:
    data = f.read()
print("Digits:", sum(c.isdigit() for c in data))
print("Special characters:", sum(not c.isalnum() and not c.isspace() for c in data))
```


#### Result and viva tips — Count digits and special characters

**Conclusion/Result:** The result of count digits and special characters is displayed.

**Viva and practical tips:**
- The scan is O(n) after reading all text.
- Check whether spaces count as special characters.
#### Practical write-up — Replace a word in a file

**Aim:** Update the file: Replace matching text and save the file.

**Theory:** The program reads the complete file, applies replace, and rewrites it.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read the full file.
3. **Step 3:** Read old/new text if requested.
4. **Step 4:** Replace matches in memory.
5. **Step 5:** Open in write mode and save revised text.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read file]
   ↓
[RECTANGLE — Replace matching text]
   ↓
[RECTANGLE — Rewrite in write mode]
   ↓
/PARALLELOGRAM — Save revised contents/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Replace a word in a file
with open("student.txt") as f:
    data = f.read()
data = data.replace(input("Old word: "), input("New word: "))
with open("student.txt", "w") as f:
    f.write(data)
```


#### Result and viva tips — Replace a word in a file

**Conclusion/Result:** The file is rewritten with replacements applied.

**Viva and practical tips:**
- The full file is read into memory.
- Write mode truncates old content; replace changes every exact match.
#### Practical write-up — Replace a sentence or phrase in a file

**Aim:** Update the file: Replace a phrase and rewrite the file.

**Theory:** The program reads the complete file, applies replace, and rewrites it.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read the full file.
3. **Step 3:** Read old/new text if requested.
4. **Step 4:** Replace matches in memory.
5. **Step 5:** Open in write mode and save revised text.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read file]
   ↓
[RECTANGLE — Replace matching text]
   ↓
[RECTANGLE — Rewrite in write mode]
   ↓
/PARALLELOGRAM — Save revised contents/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Replace a sentence or phrase in a file
with open("student.txt") as f:
    data = f.read()
data = data.replace(input("Old sentence: "), input("New sentence: "))
with open("student.txt", "w") as f:
    f.write(data)
```


#### Result and viva tips — Replace a sentence or phrase in a file

**Conclusion/Result:** The file is rewritten with replacements applied.

**Viva and practical tips:**
- The whole file is loaded, O(n) memory.
- Write mode replaces prior content; empty old text can be surprising.
#### Practical write-up — Find longest and shortest lines

**Aim:** Find the longest and shortest lines.

**Theory:** The program selects lines by length and checks for an empty file.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read all lines.
3. **Step 3:** If empty, show the empty-file message.
4. **Step 4:** Otherwise select and display longest and shortest.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read lines]
   ↓
<DIAMOND — Is file empty?>
   ├─ Yes → /PARALLELOGRAM — Display empty-file message/ → (OVAL — STOP)
   └─ No → [RECTANGLE — Select longest and shortest]
              ↓
            /PARALLELOGRAM — Display both lines/
              ↓
            (OVAL — STOP)
```

#### Program

```python
# Find longest and shortest lines
with open("student.txt") as f:
    lines = f.readlines()
if lines:
    print("Longest:", max(lines, key=len))
    print("Shortest:", min(lines, key=len))
else:
    print("The file is empty.")
```


#### Result and viva tips — Find longest and shortest lines

**Conclusion/Result:** The selected lines or empty-file message are displayed.

**Viva and practical tips:**
- The empty-file case is handled.
- Reading and selection are O(n) in file size.
#### Practical write-up — Most common word

**Aim:** Find a most common word.

**Theory:** A context manager reads text from the file before a summary or transformation is applied.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Open the file with a context manager.
3. **Step 3:** Read its content or lines.
4. **Step 4:** Apply Find a most common word.
5. **Step 5:** Display result and stop.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Open and read file]
   ↓
[RECTANGLE — Find a most common word]
   ↓
/PARALLELOGRAM — Display result/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Most common word
from collections import Counter

with open("student.txt") as f:
    words = f.read().lower().split()
print(Counter(words).most_common(1))
```


#### Result and viva tips — Most common word

**Conclusion/Result:** The result of find a most common word is displayed.

**Viva and practical tips:**
- Counter builds frequencies in average O(n) time.
- Empty file returns an empty result; punctuation stays attached.
#### Practical write-up — Compare two files

**Aim:** Compare the full text of two files.

**Theory:** Both files are read as strings and compared for exact equality.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Read the first file.
3. **Step 3:** Read the second file.
4. **Step 4:** Compare the strings.
5. **Step 5:** Display same/different result.
6. **Step 6:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Read first file]
   ↓
[RECTANGLE — Read second file]
   ↓
<DIAMOND — Are contents equal?>
   ├─ Yes → /PARALLELOGRAM — Display same/
   └─ No → /PARALLELOGRAM — Display different/
   ↓
(OVAL — STOP)
```

#### Program

```python
# Compare two files
file1 = "student.txt"
file2 = "data.txt"
with open(file1, "r") as f1:
    content1 = f1.read()
with open(file2, "r") as f2:
    content2 = f2.read()
if content1 == content2:
    print("Both files have the same content.")
else:
    print("The files have different content.")
```


#### Result and viva tips — Compare two files

**Conclusion/Result:** The program reports whether the complete text matches.

**Viva and practical tips:**
- Whitespace, newlines, and capitalization count as differences.
- Both full contents are loaded, O(n+m) memory.
#### Practical write-up — Combine two files into combined.txt

**Aim:** Combine both input files into combined.txt.

**Theory:** Input files are read and contents plus a newline are written to an output in write mode.

**Algorithm:**

1. **Step 1:** Start.
2. **Step 2:** Open output file in write mode.
3. **Step 3:** For each input, read content and write it plus a newline.
4. **Step 4:** Display success and stop.
5. **Step 5:** Stop.

**Flowchart (shape-labelled):**

```text
(OVAL — START)
   ↓
[RECTANGLE — Open output file]
   ↓
<DIAMOND — Another input file?>
   ├─ Yes → [RECTANGLE — Copy content and add newline] ↖
   └─ No → /PARALLELOGRAM — Display success/ → (OVAL — STOP)
```

#### Program

```python
# Combine two files into combined.txt
files = ["student.txt", "data.txt"]
with open("combined.txt", "w") as output:
    for filename in files:
        with open(filename, "r") as file:
            output.write(file.read())
            output.write("\n")
print("Files combined successfully into combined.txt")
```


#### Result and viva tips — Combine two files into combined.txt

**Conclusion/Result:** Both input contents are written in sequence.

**Viva and practical tips:**
- Write mode replaces an old output file.
- A newline is written after each file; missing inputs raise an error.
## Corrections and uncertainties

- The 15 named PDFs were visually reviewed page by page (46 pages total). Printed outputs were not copied as code. No code characters or lines were unreadable in the supplied PDFs.
- `sampleexp2.pdf`: corrected leap-year logic to account for century years, and made the largest-number example handle ties.
- `sampleex8.pdf`: the largest-number logic was adjusted for ties; factorial and digit-sum examples now handle negative input safely.
- `sampleexp-11.pdf`: removed an unrelated `square_cube(N)` call that depended on a variable and function from another notebook/session, where it would otherwise fail when run independently.
- `sampleexp13.pdf`: corrected the tuple access label/index wording and removed the final attempt to print a tuple variable after deleting it, which raised `NameError`. Duplicate removal now preserves order; second-extreme values validate there are at least two distinct items.
- `sampleexp15.pdf`: corrected `collage` to `college`; added empty-input handling to word/character operations.
- `sampleexp16.pdf`: fixed a missing closing parenthesis in the special-character counter; used context managers for file reading; added empty-file handling where needed.
- The source PDFs include overlapping material: one file is titled Experiments 11 & 12, and another separately contains Experiment 11 list operations. Both are retained as separate sections.
- `F:\pqc` also contained an unlisted Qiskit installation guide PDF; it was not included in this extraction because it was not among the files you listed.


