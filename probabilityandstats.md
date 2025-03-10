### Probability and Statistics

## **1. Overview of Statistics**
Statistics is divided into **Descriptive** and **Inferential** statistics:

- **Descriptive Statistics**: 
  - Focuses on summarizing and organizing data from a sample.
  - Charts like bar charts and line graphs are used to represent the data visually.

- **Inferential Statistics**:
  - Uses data from a sample to make **predictions** or **generalizations** about a larger population.
  - Involves **uncertainty** and **probability**, as the conclusions are not always 100% certain.

**Example**: 
A study analyzed **3,000 data scientist job postings** to identify trends in hiring, top companies, and preferred skills. If researchers want to generalize these findings to **all** data scientist job postings in the US, they must use **inferential statistics**, which introduces uncertainty.

---

## **2. Understanding Probability**
Probability measures the **likelihood of an event occurring**. It is expressed as a number between **0 and 1**.

- It is used in various fields such as **weather forecasting**, **stock market predictions**, and **coin flipping experiments**.
- **Probability Theory** helps model **uncertain systems** by predicting the behavior of events in the long run (**Law of Large Numbers**).

**Example**:
- If a **fair coin** is flipped multiple times, over time, the ratio of heads to tails will approach **1:1**.

---

## **3. Difference Between Probability and Inferential Statistics**
- **Probability Theory** is used **before** data is collected, predicting outcomes based on known rules.
- **Inferential Statistics** is used **after** data is collected, trying to determine what model best explains the data.

**Example**:
- A probability-based model might **assume** a fair coin has a 50% chance of landing on heads.
- Inferential statistics might analyze **actual** coin flips to determine whether a coin is biased.

---

## **4. Relationship Between Probability and Statistics**
- **Probability Theory** is the **mathematical foundation** for statistics.
- **Statistics applies** probability concepts to real-world data.
- Many statistical techniques (**confidence intervals, hypothesis testing**) rely on probability.

---

## **5. Two Schools of Inferential Statistics**
- **Bayesian Inference**:
  - Probability is interpreted as a **degree of belief**.
  - Uses **prior knowledge** to update probabilities using **Bayes’ Theorem**.
  
- **Frequentist Inference**:
  - Probability is based on **repeated trials**.
  - Focuses on long-run frequencies of events.
  - Uses **hypothesis testing, confidence intervals, and p-values**.

**Example**:
- A Bayesian might estimate the probability of rain tomorrow based on **past weather patterns**.
- A Frequentist might say that "it rained on 30 out of 100 similar days in the past, so the probability of rain is 30%."

### **Bayes’ Theorem Formula**
Bayes' Theorem is used to compute the probability of an event based on prior knowledge of related conditions. The formula is:

$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$

Where:
- $P(A|B)$ = Posterior probability (Probability of event \( A \) given that event \( B \) has occurred)
- $P(B|A)$ = Likelihood (Probability of event \( B \) occurring given that event \( A \) is true)
- $P(A)$ = Prior probability (Initial probability of event \( A \))
- $P(B)$ = Marginal probability (Total probability of event \( B \))

---

### **Python Implementation of Bayes’ Theorem**
Let's apply **Bayes' Theorem** in a real-world example.

#### **Problem Statement**
A medical test for a certain disease has:
- **10% probability** that a person has the disease (**Prior probability, \( P(A) \)**).
- **90% accuracy rate** in detecting the disease when the person actually has it (**Likelihood, \( P(B|A) \)**).
- **5% false positive rate**, meaning 5% of people **without** the disease still test positive (**False alarm probability, \( P(B|\neg A) \)**).

Given that a person **tests positive**, what is the probability that they **actually have the disease**?

---

### **Python Code for Bayes’ Theorem**
```python
# Defining known probabilities
P_A = 0.10  # Prior: Probability of having the disease
P_B_given_A = 0.90  # Likelihood: Probability of testing positive given disease
P_B_given_not_A = 0.05  # False positive rate: Probability of testing positive without disease
P_not_A = 1 - P_A  # Complementary probability: Not having the disease

# Computing marginal probability P(B) using the Law of Total Probability
P_B = (P_B_given_A * P_A) + (P_B_given_not_A * P_not_A)

# Applying Bayes' Theorem
P_A_given_B = (P_B_given_A * P_A) / P_B

# Displaying results
print(f"Probability of having the disease given a positive test result: {P_A_given_B:.4f}")
```

---

### **Output**
```
Probability of having the disease given a positive test result: 0.6667
```

---

### **Interpretation**
Even though the test is **90% accurate**, the probability that a person **actually has the disease given a positive test result is only 66.67%**. This is because of the **false positive rate** affecting the final probability.



---

## **6. Key Takeaways**
- **Descriptive statistics** organizes and summarizes data.
- **Inferential statistics** generalizes from a sample to a population.
- **Probability Theory** models uncertainty and is used in both statistics and real-world predictions.
- Probability reasons from **population to sample** (deductive reasoning).
- Statistics reasons from **sample to population** (inductive reasoning).

---
### **Probability and Statistics for Data Science**

---

## **1. Introduction**
- The session introduces **probability and statistics** as essential concepts for **data science**.
- The instructor shares a **real-life example** of how surveys collect **family planning data** to estimate state-wide averages (e.g., average number of children per family).
- The **key objective** is to understand:
  1. **Statistics for data science**
  2. **Probability for data science**
  3. **Hands-on exercises using Python**

---

## **2. Understanding Statistics**
### **What is Statistics?**
- **Statistics** is the study of data, used to **analyze, interpret, and derive insights**.
- It helps in **understanding trends** and making **informed decisions**.
- **Example**: Government surveys estimate state population trends by sampling a **subset** of households instead of surveying every home.

### **Types of Statistics**
1. **Descriptive Statistics**:
   - Focuses on summarizing and organizing data.
   - Uses **tables, graphs, averages, and central tendency measures** to describe data.
   - Example: Finding the **average age** of students in a class.

2. **Inferential Statistics**:
   - Uses **sample data** to make **predictions or generalizations** about a **population**.
   - Involves **uncertainty** and **probability**.
   - Example: **Predicting state-wide employment rates** based on a survey sample.

---

## **3. Understanding Probability**
### **What is Probability?**
- Probability is the **likelihood** that a specific event will occur.
- It is a **number between 0 and 1**, where:
  - **0** means an event will **never** happen.
  - **1** means an event will **certainly** happen.

### **Examples of Probability:**
- **Coin Toss:** Probability of getting heads is **50% (0.5)**.
- **Weather Forecast:** If past data shows similar weather patterns, we can estimate the probability of **rain tomorrow**.

### **Types of Probability:**
1. **Marginal Probability** – The probability of a **single event** happening.
2. **Joint Probability** – The probability of **two events occurring together**.
3. **Conditional Probability** – The probability of one event **given** another event has occurred.

**Example of Conditional Probability:**
- What is the probability that a person has a **liver disease** given that they are a **heavy drinker**?
- Uses **Bayes’ Theorem** to calculate such probabilities.

---

## **4. Probability in Machine Learning**
- **Why is probability important in data science?**
  - All machine learning models provide **approximations** rather than **exact predictions**.
  - **Model accuracy** is usually expressed as a probability (e.g., "90% accuracy").
  - Probability distributions, such as the **normal distribution**, help in understanding **data behavior**.

### **Probability Distributions**
1. **Normal Distribution (Bell Curve)**
   - The most commonly used distribution in **statistics and machine learning**.
   - Example: **Height of people in a population follows a normal distribution**.

2. **Central Limit Theorem (CLT)**
   - If we take multiple samples and compute their means, the **means will follow a normal distribution** even if the original data is not normally distributed.

---

## **5. Statistical Measures**
### **Measures of Central Tendency**
1. **Mean (Average)**:
   - Sum of all values divided by the number of values.
   - **Example**: Average student score in a class.
   
2. **Median**:
   - The **middle value** of a sorted dataset.
   - Less affected by **outliers** than the mean.
   
3. **Mode**:
   - The **most frequently occurring value** in a dataset.
   - Used in **recommendation systems** (e.g., Amazon’s "frequently bought items").

### **Measures of Variability (Spread)**
1. **Range** – Difference between **maximum and minimum values**.
2. **Interquartile Range (IQR)** – Measures the **spread of the middle 50% of data**.
3. **Variance & Standard Deviation** – Measure **how spread out** the data is from the mean.
4. **Outliers**:
   - **Extreme values** that don’t follow the general pattern of data.
   - Example: If most students score between **50-70**, but one student scores **100**, their score is an **outlier**.

---

## **6. Sampling Techniques**
- **Why Sampling?**
  - It is **impractical** to collect data from an entire population.
  - Instead, we collect data from a **representative subset**.

### **Types of Sampling**
1. **Random Sampling** – Selecting individuals **randomly**.
2. **Systematic Sampling** – Selecting every **nth** individual (e.g., every 10th person).
3. **Stratified Sampling** – Dividing the population into **groups** (e.g., gender, age) and sampling proportionally.

---

## **7. Hands-On Python Implementation**
The instructor demonstrates how to perform **statistical analysis** using Python with **Pandas and NumPy**.

### **Python Examples:**
1. **Calculating Mean, Median, and Mode**
   ```python
   import pandas as pd
   import numpy as np

   data = {'Age': [23, 25, 25, 30, 35, 40, 45, 23, 25, 28, 29, 32]}
   df = pd.DataFrame(data)

   print("Mean:", df['Age'].mean())      # Average
   print("Median:", df['Age'].median())  # Middle value
   print("Mode:", df['Age'].mode()[0])   # Most common value
   ```
   
2. **Handling Outliers**
   ```python
   df['Age'].mean()  # Calculates mean
   
   df.loc[df['Age'] > 90, 'Age'] = df['Age'].median()  # Replacing outliers with median
   ```

3. **Visualizing Data**
   ```python
   import matplotlib.pyplot as plt
   df['Age'].hist(bins=5)
   plt.show()
   ```

---

## **8. Key Takeaways**
- **Descriptive Statistics** helps summarize and visualize data.
- **Inferential Statistics** helps make predictions from a sample.
- **Probability** is essential for uncertainty modeling in machine learning.
- **Central Limit Theorem (CLT)** ensures that sample means form a normal distribution.
- **Sampling Techniques** ensure efficient data collection.
- **Python Libraries (Pandas, NumPy, Matplotlib)** enable statistical analysis.

---

## **9. Conclusion**
The session concludes with:
- The importance of **probability and statistics in data science**.
- Practical applications in **machine learning models and business analytics**.
- Encouragement to **practice Python-based statistical analysis**.

[check this link - online statistics calculator](https://datatab.net/statistics-calculator/descriptive-statistics)

### **Top 10 Must-Know Probability Concepts**

## **1. Experimental Probability**
**Definition:**  
Experimental probability is calculated **based on actual experiments or observations**.

**Formula:**
\[
P(A) = \frac{\text{Number of times event A occurs}}{\text{Total number of trials}}
\]

**Example:**  
- Flip a coin **10 times** and count how many times it lands on tails.
- If tails appears **3 out of 10 times**, then:
  \[
  P(Tails) = \frac{3}{10} = 0.3 \text{ (or 30%)}
  \]
- **Law of Large Numbers** states that the **more trials conducted, the closer the experimental probability will be to the theoretical probability**.

---

## **2. Theoretical Probability**
**Definition:**  
Theoretical probability is based on **mathematical reasoning** rather than experiments.

**Formula:**
\[
P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of possible outcomes}}
\]

**Examples:**
1. **Rolling a Die:**  
   - Probability of rolling a **4**:
     \[
     P(4) = \frac{1}{6}
     \]
2. **Drawing a Card:**  
   - Probability of drawing **a King** from a deck of 52 cards:
     \[
     P(King) = \frac{4}{52} = \frac{1}{13}
     \]
3. **Drawing a Red Marble:**  
   - A bag contains **3 red, 2 blue, and 5 green** marbles.  
   - Probability of drawing **a red marble**:
     \[
     P(Red) = \frac{3}{10}
     \]

---

## **3. Probability Using Sets**
Probability can be represented using **Venn Diagrams**. Two important concepts:

1. **Intersection (AND) - \( A \cap B \)**:  
   - Represents outcomes **common** to both sets.  
   - Example: Probability of liking **both hockey and basketball**.

2. **Union (OR) - \( A \cup B \)**:  
   - Represents outcomes in **either** or **both** sets.  
   - Formula:
     \[
     P(A \cup B) = P(A) + P(B) - P(A \cap B)
     \]
   - Example: Probability of liking **either basketball or soccer**.

---

## **4. Conditional Probability**
**Definition:**  
The probability of an event occurring **given that another event has already occurred**.

**Formula:**
\[
P(B|A) = \frac{P(A \cap B)}{P(A)}
\]
where:
- \( P(B|A) \) = Probability of event B given A has occurred
- \( P(A \cap B) \) = Probability of both events happening
- \( P(A) \) = Probability of A happening

**Example:**
- Given that a student is **female**, what is the probability she **likes school**?
  - Find how many **females like school** and divide by the total number of **females**.

---

## **5. Multiplication Rule (Independent & Dependent Events)**
- **Independent Events:** One event **does not** affect another.
  \[
  P(A \cap B) = P(A) \times P(B)
  \]
  - Example: Rolling a **3 on a die** and flipping **tails on a coin**.
    \[
    P(3 \cap Tails) = \frac{1}{6} \times \frac{1}{2} = \frac{1}{12}
    \]

- **Dependent Events:** One event **affects** another.
  \[
  P(A \cap B) = P(A) \times P(B|A)
  \]
  - Example: **Drawing two Kings in a row (without replacement)**:
    \[
    P(King \cap King) = \frac{4}{52} \times \frac{3}{51} = \frac{1}{221}
    \]

---

## **6. Permutations**
**Definition:**  
A **permutation** is an ordered arrangement of objects.

**Formula:**
\[
P(n, r) = \frac{n!}{(n - r)!}
\]

**Example:**  
- How many different ways can **first, second, and third place** be awarded in a 10-person race?
  \[
  P(10, 3) = \frac{10!}{(10-3)!} = 10 \times 9 \times 8 = 720
  \]

---

## **7. Combinations**
**Definition:**  
A **combination** is a selection **without considering order**.

**Formula:**
\[
C(n, r) = \frac{n!}{r!(n - r)!}
\]

**Example:**
- How many ways can you **form a team of 3 from 5 people**?
  \[
  C(5, 3) = \frac{5!}{3!(5-3)!} = \frac{5 \times 4}{2 \times 1} = 10
  \]

---

## **8. Continuous Probability Distributions (Normal Distribution)**
**Definition:**  
A **continuous** probability distribution models an **infinite** range of outcomes.

- The **Normal Distribution** (bell curve) is the most important.
  - **68%** of values lie within **1 standard deviation**.
  - **95%** within **2 standard deviations**.
  - **99.7%** within **3 standard deviations**.

**Example:**
- If smokers have a **mean lifespan of 68 years** with a **standard deviation of 10**, what percentage lives **beyond 76**?
  - Convert **76 to a z-score**:
    \[
    Z = \frac{76 - 68}{10} = 0.8
    \]
  - Using a **Z-table**, find the probability to the right of **Z = 0.8**.
  - The result: **21.9% of smokers live beyond 76 years**.

---

## **9. Binomial Probability Distribution**
**Definition:**  
Models the probability of **k successes** in **n trials**.

**Formula:**
\[
P(X = k) = C(n, k) \times p^k \times (1 - p)^{n-k}
\]

**Example:**
- Probability of rolling a **three** exactly **twice** in **four rolls** of a die.
  \[
  P(2) = C(4,2) \times \left(\frac{1}{6}\right)^2 \times \left(\frac{5}{6}\right)^2
  \]
  - Computed probability: **0.157 (or 15.7%)**.

---

## **10. Geometric Probability Distribution**
**Definition:**  
Models the number of trials **until the first success**.

**Formula:**
\[
P(X = k) = (1 - p)^{k-1} \times p
\]

**Example:**
- Probability of **getting doubles** when rolling two dice, **on the 4th try**.
  \[
  P(4) = (5/6)^3 \times (1/6)
  \]
  - Computed probability: **0.0965 (or 9.65%)**.
- Expected number of rolls until **first doubles**:
  \[
  E(X) = \frac{1}{p} = \frac{1}{1/6} = 6
  \]

---

### **Final Takeaways**
- Probability is a **core principle** in statistics and machine learning.
- **Different distributions (binomial, normal, geometric)** help model real-world uncertainty.
- **Knowing when to apply permutations, combinations, and conditional probability** is crucial.

[Probability Top 10 Must Knows](https://www.youtube.com/watch?v=LgLgexX7iTs)
