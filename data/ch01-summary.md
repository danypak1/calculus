# Intuitive Calculus · Module 01 — Limits

Everything examinable from sections 1.1–1.6, distilled into tables. If you read one page the night before, read this one.

## 1.1 Rates of change and tangent lines

| Idea | Formula |
| --- | --- |
| Average rate ($a$ to $b$) | $\dfrac{f(b)-f(a)}{b-a}$ |
| Difference quotient | $\dfrac{f(a+h)-f(a)}{h}$ |
| Tangent slope at $a$ | $m=\lim\limits_{h\to 0}\dfrac{f(a+h)-f(a)}{h}$ |
| Tangent line | $y-f(a)=m(x-a)$ |
| Normal line | $y-f(a)=-\dfrac{1}{m}(x-a)$ |

Secant slope = average rate (two points). Tangent slope = instantaneous rate (one point, via a limit).

## 1.2 Limit laws

Assume $\lim\limits_{x\to a}f$ and $\lim\limits_{x\to a}g$ both exist. Write $F=\lim\limits_{x\to a}f(x)$, $G=\lim\limits_{x\to a}g(x)$.

| Law | Statement |
| --- | --- |
| Sum / difference | $\lim (f\pm g)=F\pm G$ |
| Product | $\lim (f\cdot g)=F\cdot G$ |
| Quotient | $\lim \dfrac{f}{g}=\dfrac{F}{G}$, needs $G\ne 0$ |
| Constant multiple | $\lim (c\,f)=c\,F$ |
| Power | $\lim\limits_{x\to a}x^{n}=a^{n}$ |
| Direct substitution | $\lim\limits_{x\to a}f(x)=f(a)$ if no division by $0$ |

## The $0/0$ toolkit

$\frac{0}{0}$ is a signal, never an answer. Pick the move that matches the shape.

| Shape you see | Move | Then |
| --- | --- | --- |
| Polynomial over polynomial | Factor top and bottom | Cancel the shared factor, substitute |
| A square root present | Multiply by the conjugate | Use $(\sqrt{u}-v)(\sqrt{u}+v)=u-v^{2}$, cancel |
| Fraction inside a fraction | Combine over a common denominator | Flip and multiply, cancel |
| Sign looks wrong | Use $1-x=-(x-1)$ | Cancel, then substitute |

Worked shapes: $\dfrac{x^{2}-9}{x-3}\to x+3\to 6$; $\dfrac{\sqrt{x+9}-3}{x}\to\dfrac{1}{\sqrt{x+9}+3}\to\frac16$.

## 1.3 The precise definition

| Symbol | Axis | Meaning |
| --- | --- | --- |
| $\varepsilon$ | $y$ (output) | how close $f(x)$ must be to $L$ |
| $\delta$ | $x$ (input) | how close $x$ must be to $a$ |

Goal: $\lvert f(x)-L\rvert<\varepsilon$ whenever $0<\lvert x-a\rvert<\delta$.

| Task | Line shortcut ($f=mx+b$) |
| --- | --- |
| Given $\varepsilon$, find $\delta$ | $\delta=\dfrac{\varepsilon}{\lvert m\rvert}$ |
| Given $\delta$, find $\varepsilon$ | $\varepsilon=\lvert m\rvert\cdot\delta$ |
| Two constraints | take the **smaller** $\delta$ |
| Smaller $\delta$ offered | still valid |

Steeper line (bigger $\lvert m\rvert$) needs a **smaller** $\delta$ for the same $\varepsilon$.

## 1.4 One-sided vs two-sided

| Notation | Approach from | Use |
| --- | --- | --- |
| $\lim\limits_{x\to a^{-}}f(x)$ | left, $x<a$ | the piece valid **below** $a$ |
| $\lim\limits_{x\to a^{+}}f(x)$ | right, $x>a$ | the piece valid **above** $a$ |
| $\lim\limits_{x\to a}f(x)=L$ | both | exists only if both sides $=L$ |

If the two sides give different numbers, the limit **does not exist** (DNE).

Absolute value: $\lvert x-a\rvert=x-a$ for $x\ge a$, and $-(x-a)$ for $x<a$.

## 1.5 Continuity — the three conditions

$f$ is continuous at $x=a$ exactly when all three hold.

| # | Condition | Fails when |
| --- | --- | --- |
| 1 | $f(a)$ is defined | no point on the graph |
| 2 | $\lim\limits_{x\to a}f(x)$ exists | sides disagree |
| 3 | $\lim\limits_{x\to a}f(x)=f(a)$ | dot in the wrong place |

| Discontinuity | Test | Patchable? |
| --- | --- | --- |
| Removable (hole) | limit exists, $\ne f(a)$ | yes, redefine one point |
| Jump | left $\ne$ right | no |
| Infinite | $f\to\pm\infty$ | no |

Continuous automatically: polynomials everywhere; rationals except where the bottom is $0$; roots on their domain. Piecewise functions must still be checked **at every breakpoint**.

To force continuity: set left value $=$ right value at the breakpoint and solve for the unknown.

## 1.6 Asymptotes

**Horizontal** — compare degrees of $\dfrac{P(x)}{Q(x)}$ as $x\to\pm\infty$.

| Degrees | Limit | HA |
| --- | --- | --- |
| top $<$ bottom | $0$ | $y=0$ |
| top $=$ bottom | ratio of leading coeffs | $y=\dfrac{a_{n}}{b_{n}}$ |
| top $>$ bottom | $\pm\infty$ | none |

Method: divide every term by the highest power in the **denominator**, then use $\lim\limits_{x\to\infty}\dfrac{c}{x^{n}}=0$.

**Vertical** — factor completely first.

| At $x=a$ | Result |
| --- | --- |
| $Q(a)=0$, $P(a)\ne 0$ | vertical asymptote $x=a$ |
| factor cancels | removable hole, no VA |

A graph may cross a horizontal asymptote; it never crosses a vertical one.

## Traps, and what to do instead

| Trap | Do this instead |
| --- | --- |
| Confusing average and instantaneous rate | Two points $\Rightarrow$ average; one point $\Rightarrow$ limit |
| Setting $h=0$ before simplifying | Expand, cancel the $h$, **then** let $h\to 0$ |
| Rushing $(a+h)^{2}$ | Write every term out |
| Normal slope $=-m$ | Negative **reciprocal**, $-1/m$ |
| Answering "$0/0$" | Factor or rationalise, then substitute |
| Cancelling terms in a sum | Cancel **factors** only |
| Conjugate on the top only | Multiply top **and** bottom |
| Swapping $\varepsilon$ and $\delta$ | $\varepsilon$ is output ($y$), $\delta$ is input ($x$) |
| Hunting the one "true" $\delta$ | Any $\delta\le\varepsilon/\lvert m\rvert$ works |
| Dropping the absolute value on $m$ | Use $\lvert m\rvert$; the sign is irrelevant |
| Checking only one side | Check both, then compare |
| Grabbing the wrong piece | Match the piece to the side |
| Forgetting the sign flip in $\lvert x-a\rvert$ | For $x<a$, it is $-(x-a)$ |
| Reading $f(a)$ as the limit | The limit ignores the value at $a$ |
| Stopping once both sides match | Also check condition 3 |
| Assuming a piecewise $f$ is continuous | Test each breakpoint |
| Mixing removable and jump | Hole is patchable; jump is not |
| "Plugging in infinity" | Divide by the top power of the bottom |
| Skipping the factoring before VAs | Cancelled factor $=$ hole, not VA |
| Assuming equal degrees give $1$ | Read the leading coefficients |
| Claiming a HA is never crossed | It can be crossed, just not far out |

## The sentences most likely to appear on the exam

1. The tangent slope at $x=a$ is $m=\lim\limits_{h\to 0}\dfrac{f(a+h)-f(a)}{h}$; cancel the $h$ **before** letting $h\to 0$.
2. If the tangent slope is $m$, the normal slope is $-\dfrac{1}{m}$.
3. Direct substitution gives the limit whenever the function is a polynomial, root or quotient with a non-zero denominator at $a$.
4. $\dfrac{0}{0}$ means factor or rationalise and try again — it is never the final answer.
5. Only common **factors** cancel; you may never cancel a term out of a sum.
6. $\lim\limits_{x\to a}f(x)=L$ if and only if the left-hand and right-hand limits both exist and both equal $L$; otherwise the limit does not exist.
7. The limit at $a$ does not depend on $f(a)$ — the function need not even be defined there.
8. $f$ is continuous at $a$ if and only if $f(a)$ is defined, $\lim\limits_{x\to a}f(x)$ exists, and the two are equal.
9. For a line, $\delta=\dfrac{\varepsilon}{\lvert m\rvert}$ always works, and so does any smaller $\delta$.
10. For a rational function, the horizontal asymptote is $y=0$ if the top degree is smaller, the ratio of leading coefficients if the degrees are equal, and there is none if the top degree is larger; a vertical asymptote sits where the denominator is zero **after** all common factors have cancelled.

---

*Intuitive Calculus — an independent, original study guide. Not affiliated with any university, publisher or instructor.*
