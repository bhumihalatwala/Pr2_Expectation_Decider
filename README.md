# 📊 Expectation Decider – Probability Analysis Project

## 📁 Dataset Description

Each row in the dataset represents one student.

| Field                 | Description                                               |
| --------------------- | --------------------------------------------------------- |
| `study_hours`         | Number of hours a student studied per week                |
| `attendance`          | Percentage attendance in lectures                         |
| `group_discussion`    | Participation in group discussions (Yes / No)             |
| `previous_test_score` | Marks obtained in the previous internal test (out of 100) |
| `final_exam_pass`     | Result of competitive exam (Pass / Fail)                  |

The dataset is designed so that **better academic behavior increases the probability of passing**, enabling meaningful probability analysis.

---

## 🧠 Task 1: Understanding the Basics of Probability

### 🔹 What is Probability?

Probability is a numerical measure that describes the **likelihood of an event occurring**. Its value ranges between **0 and 1**, where:

* 0 means the event is impossible
* 1 means the event is certain

In this project, probability helps quantify the chances of students passing an exam based on academic factors.

---

### 🔹 Key Probability Terminology

* **Experiment:** A process that produces outcomes (e.g., selecting a student and checking exam result)
* **Outcome:** A possible result of an experiment (Pass or Fail)
* **Sample Space:** Set of all possible outcomes → `{Pass, Fail}`
* **Event:** A specific outcome or group of outcomes (e.g., student passes the exam)
* **Probability of an Event:**

  P(E) = {Favorable outcomes} / {Total outcomes}

---

### 🔹 Probability Event Examples from Dataset

1. Probability that a student passes the exam
2. Probability that a student has attendance greater than 80%
3. Probability that a student participates in group discussions
4. Probability that a student studies more than 10 hours **and** passes the exam

---

## 🧪 Task 2: Types of Events

### 🔹 Empirical Probability

Empirical probability is calculated using **observed data**.

**Example:** Probability that a randomly selected student passes the exam:

P(Pass) = {Students who passed} / {200}

This value is obtained directly from the dataset.

---

### 🔹 Theoretical Probability

Theoretical probability assumes **all outcomes are equally likely**.

If exam result outcomes are `{Pass, Fail}`:

P(Pass) = 1/2

---

### 🔹 Comparison

| Type        | Nature                           |
| ----------- | -------------------------------- |
| Empirical   | Based on real student data       |
| Theoretical | Based on mathematical assumption |

Empirical probability is more realistic for educational analysis.

---

## 🎯 Task 3: Random Variable & Probability Distribution

### 🔹 Definition of Random Variable

Let:

X = {Number of students passing out of 3 randomly selected students}

Possible values:

[ X ∈ {0,1,2,3} ]

---

### 🔹 Probability Distribution

The random variable follows a **Binomial Distribution** since:

* Fixed number of trials (3 students)
* Two outcomes (Pass / Fail)
* Constant probability of success

P(X = k) = \binom{3}{k} p^k q^{3-k}

---

### 🔹 Mean and Variance

* **Mean:**
 E(X) = np

* **Variance:**
Var(X) = npq

These indicate the expected number of students passing and the consistency of outcomes.

---

## 🔵 Task 4: Venn Diagram in Probability

Two events were analyzed:

* **Event A:** Students studying more than 10 hours/week
* **Event B:** Students with attendance greater than 80%

A Venn diagram visually represents:

* Students satisfying only A
* Students satisfying only B
* Students satisfying **both A and B (A ∩ B)**

The overlap highlights students who are both **hardworking and consistent**.

---

## 📋 Task 5: Contingency Table & Probability Calculations

A contingency table was created between:

* `group_discussion` (Yes / No)
* `final_exam_pass` (Pass / Fail)

### 🔹 Probabilities Calculated

* **Joint Probability:**

  Probability that a student participates in group discussion **and** passes the exam

* **Marginal Probability:**

  Overall probability that a student passes the exam

* **Conditional Probability:**

  Probability that a student passes **given** they participated in group discussion

---

## 🔗 Task 6: Understanding Relationships

### 🔹 Conditional Probability – Intuition

Conditional probability answers:

> "Among students who participated in group discussions, how many passed the exam?"

This helps assess whether participation **influences success**.

---

### 🔹 Independence Analysis

Two events are independent if:

P(B|A) = P(B)

In this project:

* Conditional probability of passing **differs** from overall probability

➡️ Hence, **group discussion participation and exam success are dependent events**.

They are **not mutually exclusive**, as students can both participate and pass.

---

## 🔄 Task 7: Bayes’ Theorem Application

### 🔹 Given Information

* 70% of students who passed had high attendance
* 40% of students who failed had high attendance
* 60% of all students had high attendance

---

### 🔹 Bayes’ Theorem Formula

P(A|B) = {P(B|A) * P(A)} / {P(B)}

Using Bayes’ theorem, the probability that a student **passed the exam given high attendance** was found to be:

P(Pass | High Attendance) ≈ 0.778

---

### 🔹 Interpretation

> A student with high attendance has approximately a **77.8% chance of passing**, confirming that attendance is a strong performance indicator.

---

## ✨ Key Insights

* Academic discipline strongly affects exam outcomes
* Group discussions positively influence success
* Probability theory provides measurable, explainable insights
* Bayes’ theorem helps reverse conditional relationships meaningfully
