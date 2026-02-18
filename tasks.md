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

---

### Task 4 - Explore sensor data for one engine
#### Task 4.1
  - **Pick one engine** (for example, engine_id = 1).
  - **Filter the data** to show only rows for that engine. (Hint: use something like `df[df['engine_id'] == 1]`)
  - **How many cycles** did this engine run for? (Count the rows or use `.shape[0]`)

#### Task 4.2
  - **Make a simple line plot** showing how one sensor changes over time for your chosen engine.
  - Pick any sensor column you like (for example, `sensor_2` or `sensor_3`).
  - Put **cycle** on the x-axis and the **sensor value** on the y-axis.
  - In one sentence: **Does the sensor value go up, down, or stay the same as cycles increase?**
  - .. sensor value goes up ...and i notice the cycles increase, the sensor also increases.

---

### Task 5 - Compare two engines
#### Task 5.1
  - **Pick two engines** (for example, engine_id = 20 and engine_id = 5). 
  - **Find out when each engine failed.** (Hint: look at their `failure_time` or count how many cycles each one ran.)
  engine_20 is failed on 245 and engine_5 is failed on 193
  - **Which engine failed earlier?**
  engine_5 is failed earlier as compare of engine_20

#### Task 5.2
  - **Plot the same sensor for both engines on one graph.**
  - Use the same sensor you picked in Task 4 (fanspeed).
  - Make two lines: one for each engine. (Hint: use different colors or labels so you can tell them apart.)
  - In one or two sentences: **Do the two engines look similar or different? Does the sensor behave the same way in both?**
  data pattern are same but engine_20 slightly forward but in same pattern

### Task 6 - Find which sensors change the most?
#### Task 6.1
  - **Pick one engine** (you can use the same engine from Task 4).
  - **Look at 3 different sensors** for this engine (for example, temperature sensor, pressure sensor, and fan speed).
  - **Make 3 separate line plots** (or one plot with 3 subplots) showing how each sensor changes over the engine's lifetime.

#### Task 6.2
  - **Compare the first cycle and last cycle** for each of the 3 sensors.
  - For each sensor, calculate: **last value - first value**
  - In one or two sentences: **Which sensor changed the most? Which one stayed almost the same? Why do you think some sensors change more than others as the engine gets older?**
  (Physical fan speed) (rpm) sensor is changed most (472.9799), 


### Task 7 - Calculate Remaining Useful Life (RUL)
#### Task 7.1
  - **Pick one engine** and find out when it failed (the max cycle for that engine).
  - **Create a new column** called `RUL` (Remaining Useful Life) for that engine.
  - For each row, calculate: **RUL = max_cycle - current_cycle**
  - Example: If engine failed at cycle 100, then at cycle 95 the RUL = 5 (5 cycles left before failure)

#### Task 7.2
  - **Make a plot** showing RUL over time for your chosen engine.
  - Put **cycle** on x-axis and **RUL** on y-axis.
  - In one sentence: **What pattern do you see? Does RUL go up or down as cycles increase?**
  Fron RUL to cycle is going downwards with straight line from 250 to 250
  

#### Task 7.3
  - In one or two sentences: **Why is RUL important? If you could predict RUL, how would that help in real life?** (Think: when would you want to replace an engine part?)
