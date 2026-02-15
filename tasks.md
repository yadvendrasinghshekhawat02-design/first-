### Task 1 - describe the training data
#### Task 1.1
Using `failure_time` (max cycle per engine):
  - Compute **mean**, **median**, **min**, and **max** failure cycle.



# Question1. in average, engines fail around cycle 206. The shortest-lived engine failed at cycle 128, the longest at 362.

---

### Task 2 - Visualize how failure cycles are spread
#### Task 2.1
Using the same `failure_time` (max cycle per engine) from Task 1:
  - Make a **histogram** of failure cycles (pick a sensible number of bins, e.g. 15–25).
  - Add a **vertical line** at the mean failure cycle so you can see how the average compares to the distribution.

#### Task 2.2
  - In one or two sentences: **What does the shape of the histogram tell you?** (e.g. Are most engines failing in a similar range? Is it symmetric or skewed? Any surprises?)
  - mostly engine fail between 150 to 250 ,and i am suprisely see after 150 its was get break then continue that's why its skewed and its mean approx 205 to 210 

---

### Task 3 - Get to know the dataset
#### Task 3.1
  - **How many engines** are in the training data? (Hint: each engine has one `failure_time` — so the number of rows in your failure-time table, or `len(failure_time)`, is the number of engines.)
  - **How many columns** does the full training dataframe have? (Use `.shape` or `.columns`.)
  - **Print the first 5 rows** of the training data so you can see what a few rows look like.
