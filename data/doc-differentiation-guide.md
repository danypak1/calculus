# Which differentiation rule?

## How to use this sheet

Work through these questions in order, top to bottom, and stop at the first "yes". Many problems need **more than one rule stacked together**, so don't stop at the first "yes" if there's still more structure left to handle inside that piece.

---

## Step 1: Is it a sum or difference of separate terms?

$$\text{Example: } y = x^3 + \sin x - e^x$$

$\rightarrow$ **Differentiate each term completely separately**, then add/subtract the results. Handle each individual term using the rest of this guide.

---

## Step 2: Look at one term at a time. Is it two *different* functions multiplied together?

(Not a constant times a function — an actual product of two functions that both involve $x$.)

$$\text{Examples: } y=x^2\sin x \qquad y=xe^x \qquad y=\ln x\cdot x^3$$

$\rightarrow$ **Product Rule:** $\dfrac{d}{dx}[fg] = f'g+fg'$

**Before reaching for this:** check if the product would be *easier* to just expand out first (like $x(x^2-3)$) — if so, expand and skip the product rule entirely.

---

## Step 3: Is it one function divided by another?

$$\text{Example: } y = \frac{\sin x}{x} \qquad y=\frac{x^2}{x+1}$$

$\rightarrow$ **Quotient Rule:** $\dfrac{d}{dx}\left[\dfrac fg\right] = \dfrac{f'g-fg'}{g^2}$

**Before reaching for this:** check if the fraction simplifies by dividing term-by-term (like $\dfrac{x^2+4x}{x}=x+4$) — if so, simplify first and use the power rule instead. It's almost always faster.

---

## Step 4: Is there a "function wrapped inside another function"?

(The output of one function is being fed directly into another — a composition.)

$$\text{Examples: } y=\sin(x^2) \qquad y=e^{3x} \qquad y=(x^2+1)^5 \qquad y=\ln(\cos x) \qquad y=\sqrt{x^3+2}$$

$\rightarrow$ **Chain Rule:** identify the "outer" function and the "inner" function. Differentiate the outer function (leaving the inside alone), then multiply by the derivative of the inside.

$$\frac{d}{dx}\big[f(g(x))\big] = f'(g(x))\cdot g'(x)$$

---

## Step 5: Does the problem combine several of the above?

This is extremely common — don't be surprised when a single term needs two or three rules layered together.

**Product + Chain, example:** $y = x^2\sin(3x)$

$\rightarrow$ Use the **Product Rule** first (treating $x^2$ and $\sin(3x)$ as the two factors). While differentiating the $\sin(3x)$ piece, you'll need the **Chain Rule** (since the inside is $3x$, not plain $x$).

**Quotient + Chain, example:** $y = \dfrac{e^{2x}}{x+1}$

$\rightarrow$ Use the **Quotient Rule** first. While finding the derivative of $e^{2x}$ (the numerator), you'll need the **Chain Rule**.

---

## Step 6: Is $y$ defined *implicitly* — mixed up with $x$ in an equation, not solved for $y$ by itself?

$$\text{Example: } x^2y+xy^2=8$$

$\rightarrow$ **Implicit Differentiation.** Differentiate both sides with respect to $x$, and remember: every single time you differentiate a term containing $y$, you must tack on a $y'$ (chain rule, since $y$ is secretly a function of $x$). Then collect all the $y'$ terms on one side and solve for $y'$.

---

## The special-function derivative reference

| Function | Derivative |
|---|---|
| $x^n$ | $nx^{n-1}$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2 x$ |
| $e^x$ | $e^x$ |
| $\ln x$ | $\dfrac1x$ |
| $\arcsin x$ | $\dfrac{1}{\sqrt{1-x^2}}$ |
| $\arctan x$ | $\dfrac{1}{1+x^2}$ |

For any of these with something other than plain $x$ inside (like $\sin(3x)$ or $\ln(x^2+1)$), multiply by the chain rule factor $u'$.

---

*Intuitive Calculus — an independent, original study guide. Not affiliated with any university, publisher or instructor.*
