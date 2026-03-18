# Probability exercises
Due end of day March 18th. Submit using Canvas.
---
### **Problem 1 — Valid Probability Measure**
Define a sample space  
$$\Omega = \{a, b, c, d\}$$
and assign  
$$\mathbb{P}(a)=0.2,\quad \mathbb{P}(b)=0.3,\quad \mathbb{P}(c)=x,\quad \mathbb{P}(d)=0.1.$$

1. Find all values of $x$ for which this defines a valid probability measure.  
2. With the valid $x$, compute  
   - $\mathbb{P}(\\{a, c\\})$  
   - $\mathbb{P}(\\{b, d\\}^c)$

---

### **Problem 2 — Event Construction and Counting**
A geophysicist classifies observations into  
- $H$ = high‑frequency tremor  
- $L$ = low‑frequency tremor  
- $N$ = noise  

Let the sample space be all ordered triples of three consecutive observations (repeated event is allowed).

1. How many elements does $\Omega$ have?  
2. Define the event "at least one $H$ occurs before any $L$ occurs."  
3. Compute its probability if each of $\{H,L,N\}$ occurs independently with probabilities $\{0.3, 0.2, 0.5\}$.

---
### **Problem 3 — Mixed CDF**
Consider the function  
```math
F(x)=\begin{cases}0, & x<0\\0.4, & 0\le x<1\\0.4 + 0.3(x-1), & 1 \le x < 2\\1, & x\ge 2.\end{cases}
```

1. Verify that this is a valid CDF.  
2. Identify the discrete and continuous components.  
3. What is the probability that $X=0$? How about $X=1.5$?

<!-- ### **Problem 4 — Variance of the Sample Mean**
Let $X_1,\dots,X_n$ be independently and identically distributed (i.i.d). with  
$$
\mathbb{E}[X_i] = \mu,\quad \mathrm{Var}(X_i) = \sigma^2.
$$
Define  
$$
S_n = \frac{1}{n}\sum_{i=1}^n X_i.
$$

1. Compute $\mathbb{E}[S_n]$ and $\mathrm{Var}(S_n)$.  
2. Show that $\mathrm{Var}(S_n) = \sigma^2/n$. -->

---

### **Problem 4 — Constructing Counter Examples**

#### Part A: Zero Covariance but Dependence
Construct a random variable example where $\mathrm{Cov}(X, Y) = 0$ but $X$ and $Y$ are **not independent**.

1. Clearly specify your choice of $(X, Y)$ (with their joint distribution or explicit formula).  
2. Compute $\mathbb{E}[X]$, $\mathbb{E}[Y]$, and $\mathbb{E}[XY]$.  
3. Verify that $\mathrm{Cov}(X, Y) = 0$.  
4. Prove that $X$ and $Y$ are dependent by showing $f_{X,Y}(x,y) \neq f_X(x) \cdot f_Y(y)$ or $\mathbb{P}(X \in A, Y \in B) \neq \mathbb{P}(X \in A) \cdot \mathbb{P}(Y \in B)$ for some sets $A, B$.

#### Part B: Dependence and Variance of Sums
Construct random variables $X$ and $Y$ that are **not independent** and show that $\mathrm{Var}(X + Y) \neq \mathrm{Var}(X) + \mathrm{Var}(Y)$.

5. Clearly specify your choice of $(X, Y)$.  
6. Compute $\mathrm{Var}(X)$, $\mathrm{Var}(Y)$, and $\mathrm{Var}(X + Y)$ directly.  
7. Compute $\mathrm{Cov}(X, Y)$.  
8. Verify the identity: $\mathrm{Var}(X + Y) = \mathrm{Var}(X) + \mathrm{Var}(Y) + 2\mathrm{Cov}(X, Y)$.

---
### **Problem 5 — Discrete Conditional Probability**
A seismic network detects either a **true event** ($E$) or **noise** ($N$). The joint probability distribution is:

$$\begin{array}{c|cc}
 & E & N \\
\hline
\text{Detected} & 0.06 & 0.14 \\
\text{Not Detected} & 0.04 & 0.76
\end{array}$$

1. Compute the marginal probabilities: $\mathbb{P}(E)$, $\mathbb{P}(N)$, $\mathbb{P}(\text{Detected})$, and $\mathbb{P}(\text{Not Detected})$.  
2. What is $\mathbb{P}(E | \text{Detected})$? (i.e., given that something was detected, what is the probability it was a true event?)  
3. What is $\mathbb{P}(\text{Detected} | E)$? (i.e., given a true event, what is the probability it was detected?)  
4. Verify the Bayes' formula relating $\mathbb{P}(E | \text{Detected})$ and $\mathbb{P}(\text{Detected} | E)$?  
5. Are the events $E$ and $\text{Detected}$ independent? Justify your answer numerically.

---
### **Problem 6 — Deriving the Poisson Distribution from Exponential Waiting Times**
Earthquakes arrive at a seismic station according to the following model (called the Poisson point process):

- The waiting times between successive events are independently and identically distributed (i.i.d) exponential random variables with rate $\lambda > 0$.
- If $W_i$ denotes the waiting time between event $i-1$ and event $i$, then  
  $$f_{W_i}(w) = \lambda e^{-\lambda w}, \qquad w > 0.$$

Let $N(t)$ be the total number of events observed in the time interval $[0,t]$.

This exercise guides you through the derivation that $N(t)$ is Poisson distributed with parameter $\lambda t.$

1. Probability of zero events: The event $\{N(t) = 0\}$ occurs if and only if the first arrival time $W_1 > t$. 
   Compute $\mathbb{P}(N(t) = 0) = \mathbb{P}(W_1 > t)$ using the tail probability of the exponential distribution.

2. Probability of exactly one event: The event $\{N(t) = 1\}$ occurs if the first arrival happens before time $t$, but the second one happens after time $t$.  We can write the probability as:
   $$\mathbb{P}(N(t) = 1) = \int_0^t \mathbb{P}(W_2 > t - w_1 \mid W_1 = w_1) \cdot f_{W_1}(w_1) \, dw_1$$
    Note that $W_1$ and $W_2$ are independent. Use this fact to simplify the integral. Show that $\mathbb{P}(N(t) = 1) = \lambda t e^{-\lambda t}$.

You do not need to derive this unless you are interested. But following the same logic, and using mathematical induction, the probability of exactly $k$ events in $[0, t]$ is:
   $$\mathbb{P}(N(t) = k) = \frac{(\lambda t)^k e^{-\lambda t}}{k!}$$
   
   This is the **Poisson distribution** with parameter $m = \lambda t$.

3. With $\lambda = 2$ events per hour and $t = 1$ hour, compute:
   - $\mathbb{P}(N(1) = 0)$  
   - $\mathbb{P}(N(1) = 1)$  
   - $\mathbb{P}(N(1) = 2)$

4. Verify that $\mathbb{E}[N(t)] = \lambda t$. Hint: remind yourself the Taylor series for the exponential function.

