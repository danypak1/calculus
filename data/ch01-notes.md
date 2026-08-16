# Module 01 · Limits

## 1.1 Rates of Change and Tangent Lines to Curves

### The idea, in plain words

Imagine you drive from home to a friend's house, 60 miles away, and it takes you 2 hours. Your **average speed** is 30 miles per hour. But you didn't drive at exactly 30 mph the whole time — maybe you were stuck at a red light (0 mph) and later flew down the highway (70 mph). Average speed just tells you the overall "big picture" rate, using only the start and the end.

Now imagine glancing at your speedometer at one exact instant. That's your **instantaneous speed** — your speed *right now*, not averaged over the whole trip.

That's the whole idea of this section:

- **Average rate of change** = comparing two points and asking "how much did y change, divided by how much x changed?" On a graph, this is the slope of the straight line connecting the two points — called a **secant line**.
- **Instantaneous rate of change** = the rate at one single point. On a graph, this is the slope of the line that just barely grazes the curve at that one point — called a **tangent line**.

**Picture it:** Draw a curve. Pick two points on it and connect them with a straight ruler — that's the secant line, and its slope is the average rate of change. Now slide the second point closer and closer to the first point. The ruler keeps tilting until, in the limit, it settles into a line that just kisses the curve at a single point without crossing through it. That final line is the tangent line, and its slope is the instantaneous rate of change.

**How do we actually compute the tangent slope?** We use a trick: pretend the second point is a *tiny* step away from the first, a distance we call $h$. We compute the secant slope using that tiny step, simplify the algebra, and then imagine $h$ shrinking all the way down to $0$. Whatever number the slope settles on is the tangent slope. This is called taking a **limit**, and we'll get more comfortable with limits formally in the next unit — for now, just think of it as "let $h$ shrink to nothing and see what number the slope approaches."

### Toolbox

**Average rate of change** of $f$ from $x=a$ to $x=b$ (slope of the secant line):
$$\text{avg rate of change} = \frac{f(b)-f(a)}{b-a}$$

**Difference quotient** (secant slope using a tiny step $h$ away from $x=a$):
$$\frac{f(a+h)-f(a)}{h}$$

**Slope of the tangent line at $x=a$** (let $h$ shrink to $0$):
$$m = \lim_{h\to 0}\frac{f(a+h)-f(a)}{h}$$

**Equation of the tangent line** at the point $(a, f(a))$, once you know the slope $m$:
$$y - f(a) = m(x-a)$$

**Equation of the normal line** (the line perpendicular to the tangent, at the same point): if the tangent slope is $m$, the normal slope is $-\dfrac{1}{m}$:
$$y - f(a) = -\frac{1}{m}(x-a)$$

### Common mistakes

- **Mixing up average and instantaneous rate.** Average rate uses two separate points; instantaneous rate uses a limit at one single point. Read the problem carefully to see which one is being asked for.
- **Plugging in $h=0$ too early.** If you plug $h=0$ into the *original* difference quotient before simplifying, you get $\frac{0}{0}$, which tells you nothing. You must expand and simplify the algebra *first*, cancel the $h$ in the denominator, and only *then* let $h\to 0$.
- **Algebra slips when expanding $f(a+h)$.** This is the #1 source of errors. Take your time expanding things like $(a+h)^2$ or $(2+h)^2$ — write out every term instead of rushing.
- **Forgetting the normal line uses the negative reciprocal.** If the tangent slope is $m$, the normal slope is $-1/m$, not $-m$ and not $1/m$.
- **Losing track of which point you're evaluating at.** Always write down $f(a)$ and $f(a+h)$ clearly before subtracting — don't try to do it all in your head.

**Practice.** 22 problems on this section — 7 warm-up, 6 standard, 5 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

## 1.2 The Limit of a Function and Limit Laws

### The idea, in plain words

A **limit** answers the question: "As $x$ gets closer and closer to some number, what value does $f(x)$ get closer and closer to?" It's not asking what happens *at* that exact number — it's asking what $f(x)$ is *heading toward* as you approach it.

**Picture it:** Imagine walking toward a friend's house. You never actually need to teleport there — you just need to know that with each step, you're getting closer and closer. The limit is the address you're walking toward, whether or not you ever technically "arrive" (i.e., whether or not $f$ is even defined right at that point).

For most of the functions you'll meet early on — polynomials, square roots, nice fractions — the function behaves the way you'd expect, and the limit is simply what you get by plugging the number in. This is called **direct substitution**.

But sometimes, plugging the number straight in gives you $\dfrac{0}{0}$, which tells you *nothing* — it's a mathematical dead end, not an answer. When this happens, it usually means the top and bottom of the fraction share a hidden common piece that's causing trouble at that one point. Our job is to dig that hidden piece out — either by **factoring and canceling**, or by **rationalizing** (multiplying by a clever form of $1$ to get rid of an awkward square root) — and then try substituting again.

### Toolbox

**Limit notation:** $\displaystyle\lim_{x\to a} f(x) = L$ means "as $x$ approaches $a$, $f(x)$ approaches $L$."

**Direct substitution rule:** If $f(x)$ is a polynomial, or any combination of $+,-,\times,\div,\sqrt{\ }$ that doesn't cause a division by zero at $x=a$, then:
$$\lim_{x\to a} f(x) = f(a)$$

**Limit laws** (these let you break a complicated limit into simpler pieces): if $\displaystyle\lim_{x\to a}f(x)$ and $\displaystyle\lim_{x\to a}g(x)$ both exist,

$$\lim_{x\to a}\big[f(x)+g(x)\big] = \lim_{x\to a}f(x) + \lim_{x\to a}g(x)$$
$$\lim_{x\to a}\big[f(x)\cdot g(x)\big] = \lim_{x\to a}f(x) \cdot \lim_{x\to a}g(x)$$
$$\lim_{x\to a}\frac{f(x)}{g(x)} = \frac{\lim_{x\to a}f(x)}{\lim_{x\to a}g(x)}, \quad \text{as long as } \lim_{x\to a}g(x)\ne 0$$
$$\lim_{x\to a}\big[c\cdot f(x)\big] = c \cdot \lim_{x\to a}f(x) \quad \text{(for any constant } c\text{)}$$
$$\lim_{x\to a} x^n = a^n$$

**The $\frac{0}{0}$ fix-it kit:**
- **Factor and cancel:** if plugging in gives $\frac{0}{0}$ on a fraction of polynomials, factor the top and bottom. There will always be a matching factor that cancels out — that factor is exactly what was causing the $0/0$.
- **Rationalize:** if there's a square root involved, multiply the top and bottom by the **conjugate** of the square-root part (same terms, opposite sign in the middle). This uses the pattern $(\sqrt{u}-v)(\sqrt{u}+v) = u - v^2$ to make the square root disappear from one part of the fraction, which usually reveals a common factor you can cancel.

### Common mistakes

- **Giving up when you see $\frac{0}{0}$.** This is *not* the final answer — it's a signal to factor or rationalize and try again.
- **Forgetting to factor completely.** If you cancel one factor but the numerator or denominator still has more work to do, you might miss a further simplification (or a further cancellation).
- **Sign errors while factoring quadratics.** Double-check by mentally re-expanding your factored form before moving on.
- **Canceling terms instead of factors.** You can only cancel something that is *multiplied* on both top and bottom — never cancel a piece that's part of a sum, like trying to cancel the $x$'s in $\dfrac{x+3}{x+5}$ (that's not allowed; $x$ isn't a common factor there).
- **Forgetting to multiply the denominator by the conjugate too.** When rationalizing, whatever you multiply the top by, you must also multiply the bottom by — you're really just multiplying by a clever version of $1$.

**Practice.** 24 problems on this section — 7 warm-up, 7 standard, 6 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

## 1.3 The Precise Definition of a Limit

### The idea, in plain words

Back in §1.2, we said a limit is "the number $f(x)$ gets closer and closer to as $x$ gets closer and closer to $a$." That's a great starting picture, but "closer and closer" is a little fuzzy — closer by how much? This section just makes that fuzzy idea *precise*, using a simple game: the **tolerance game**.

**Picture it like archery, or a factory quality check.** Suppose someone hands you a target number $L$ and says: "I want $f(x)$ to land within a tiny margin of $L$ — say, within $\varepsilon$ (the Greek letter *epsilon*) — no matter how small a margin I ask for." Your job is to find a matching rule for $x$: "As long as $x$ stays within some margin $\delta$ (the Greek letter *delta*) of $a$, I guarantee $f(x)$ will land inside your target band."

- $\varepsilon$ (epsilon) = **how close you want the output**, $f(x)$, to be to $L$. This lives on the **y-axis** (the output side).
- $\delta$ (delta) = **how close the input**, $x$, needs to be to $a$ to guarantee that. This lives on the **x-axis** (the input side).

**The picture:** draw two horizontal dashed lines at $L-\varepsilon$ and $L+\varepsilon$ — that's the "target band" for the output. Then find two vertical dashed lines at $a-\delta$ and $a+\delta$ — the "safe zone" for the input — such that any $x$ inside that safe zone (other than $x=a$ itself) produces an $f(x)$ that lands inside the target band.

**Saying "the limit is $L$" really just means:** no matter how thin someone makes that target band ($\varepsilon$), you can *always* find a safe zone ($\delta$) around $a$ that keeps you inside it. That's all the "precise definition" is doing — turning "gets closer and closer" into an actual tolerance-matching game you can play with real numbers.

**Good news for this section:** we'll only play this game with straight-line functions ($f(x) = mx+b$), because for a line, there's a clean, simple shortcut for finding a matching $\delta$ — no formal proof-writing needed, just some algebra.

### Toolbox

**What each symbol means:**
- $a$ = the input value we're approaching
- $L$ = the limit (the target output value), often $L = f(a)$ for our examples
- $\varepsilon$ = the allowed margin of error on the *output* (how close $f(x)$ must be to $L$)
- $\delta$ = the allowed margin of error on the *input* (how close $x$ must be to $a$)

**The tolerance-matching statement:** we want to guarantee

$$|f(x) - L| < \varepsilon \quad \text{whenever} \quad 0 < |x-a| < \delta$$

**The straight-line shortcut:** if $f(x) = mx+b$ and $L = f(a)$, then

$$|f(x)-L| = |m(x-a)| = |m|\cdot|x-a|$$

So $|f(x)-L| < \varepsilon$ exactly when $|x-a| < \dfrac{\varepsilon}{|m|}$. That means:

$$\delta = \frac{\varepsilon}{|m|}$$

always works. (Any *smaller* delta than this also works — it's not the one "correct" answer, just a safe one.)

**Working backward:** if you're told a $\delta$ was used, the guaranteed output tolerance is

$$\varepsilon = |m|\cdot \delta$$

### Common mistakes

- **Mixing up which axis epsilon and delta belong to.** Epsilon is always about the output ($y$), delta is always about the input ($x$).
- **Thinking there's only one "correct" delta.** Any delta smaller than or equal to $\varepsilon/|m|$ works. If a smaller window on $x$ works, a slightly larger one that's still $\le \varepsilon/|m|$ works too — there isn't a single magic number.
- **Forgetting to use the absolute value / size of the slope.** A steep negative slope (like $m=-5$) still needs $|m|=5$ in the formula — the sign of the slope doesn't matter here, only its size.
- **Assuming a bigger epsilon needs a bigger delta — that part's true — but forgetting that a *steeper* line needs a *smaller* delta for the same epsilon.** A steep line amplifies small changes in $x$ into big changes in $y$, so you need to control $x$ more tightly.
- **Forgetting to double-check by plugging the boundary values back in.** Plugging in $x=a+\delta$ and $x=a-\delta$ is a great way to confirm your delta actually lands $f(x)$ right at (or inside) the tolerance band.

**Practice.** 20 problems on this section — 6 warm-up, 6 standard, 4 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

## 1.4 One-Sided Limits

### The idea, in plain words

So far we've asked "what does $f(x)$ approach as $x$ gets close to $a$?" — sneaking up on $a$ from *both* directions at once. But sometimes a function behaves differently depending on which side you sneak up from. **One-sided limits** let us check each direction separately.

**Picture it:** imagine walking along a graph toward a certain $x$-value, $a$.

- If you're walking in from the **left** (from smaller $x$-values, heading up toward $a$), the height you're approaching is called the **left-hand limit**, written $\displaystyle\lim_{x\to a^-} f(x)$.
- If you're walking in from the **right** (from larger $x$-values, heading down toward $a$), the height you're approaching is called the **right-hand limit**, written $\displaystyle\lim_{x\to a^+} f(x)$.

Most of the time — for nice smooth curves — it doesn't matter which side you approach from; you land at the same height either way. But **piecewise functions** (functions built out of different formulas glued together at a breakpoint) can behave very differently on the two sides. Imagine a staircase: walking up to a step from the left, you're at one height; stepping in from the right, you might be at a completely different height. In that case, there's no single "the limit" — the two sides disagree.

**The big rule:** the ordinary (two-sided) limit only exists if *both* one-sided limits exist *and* agree with each other. If they don't match, we say the limit "does not exist" (DNE) at that point.

**Important reminder:** a limit only cares about what $f(x)$ is doing *near* $a$ — it does not care what $f(a)$ itself equals, or even whether $f$ is defined at $a$ at all. Don't let the actual value at the point distract you from what the function is approaching.

### Toolbox

**Left-hand limit:** consider only $x$-values slightly *less than* $a$.
$$\lim_{x\to a^-} f(x)$$

**Right-hand limit:** consider only $x$-values slightly *greater than* $a$.
$$\lim_{x\to a^+} f(x)$$

**Existence rule:**
$$\lim_{x\to a} f(x) = L \quad \Longleftrightarrow \quad \lim_{x\to a^-}f(x) = L \ \text{ and }\ \lim_{x\to a^+}f(x) = L$$

If the two one-sided limits are different numbers, the two-sided limit **does not exist**.

**For piecewise functions:** use whichever formula applies just *below* $a$ to compute the left-hand limit, and whichever formula applies just *above* $a$ to compute the right-hand limit. Then plug $a$ into each formula (direct substitution, or factor-and-cancel first if needed, same as §1.2).

**For absolute value expressions**, remember:
$$|x-a| = \begin{cases} x-a, & x \ge a \\ -(x-a), & x < a \end{cases}$$
This is exactly why absolute value functions are a classic source of one-sided limit problems — the formula genuinely changes depending on which side you're on.

### Common mistakes

- **Grabbing the wrong piece.** Always double check: which formula is valid for $x$-values *just below* $a$? Which one for *just above*? It's easy to grab the wrong one under time pressure.
- **Stopping after checking only one side.** To claim the two-sided limit exists, you must check *both* sides and confirm they match — don't skip the second side.
- **Confusing the limit with the function's actual value at $a$.** A piecewise function often defines a specific (sometimes weird) value right at the breakpoint — that value is irrelevant to the limit computation.
- **Forgetting the sign flip inside an absolute value.** For $x<a$, $|x-a|$ becomes $-(x-a)$, not $(x-a)$. Missing this sign flip is the most common error on these problems.
- **Arithmetic slips when plugging the breakpoint into each formula.** Take an extra moment — these are usually simple substitutions, so a careless error is the main risk, not the concept itself.

**Practice.** 21 problems on this section — 6 warm-up, 6 standard, 5 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

## 1.5 Continuity

### The idea, in plain words

A function is **continuous** at a point if you could trace its graph through that point without lifting your pencil off the paper. No holes, no sudden jumps, no shooting off to infinity — just a smooth, unbroken path.

In the last unit, we learned to check whether the left-hand and right-hand limits agree. That was step one. Continuity asks one more question on top of that: **does the function's actual value at that point match what it's approaching?**

Here's the full checklist — think of it like a 3-question inspection you run at a single point $x=a$:

1. **Is $f(a)$ actually defined?** (Is there even a dot on the graph there?)
2. **Does the limit exist as $x\to a$?** (Do the left and right limits agree — no jump?)
3. **Does that limit actually equal $f(a)$?** (Does the dot sit exactly where the two sides are heading — no hole, no mismatch?)

If all three answers are "yes," the function is continuous at $a$. If even one fails, it's discontinuous there.

**The three ways continuity can break, pictured:**
- **Removable discontinuity (a hole):** the limit exists just fine, but either $f(a)$ is undefined, or it's defined to some *other* value that doesn't match the limit. Picture an open circle on the curve with a lonely dot sitting somewhere else (or no dot at all). You could "fix" this by simply redefining that one point.
- **Jump discontinuity:** the left and right limits exist but disagree with each other — like a staircase step. No single point-fix can repair this; the two sides are just heading toward different places.
- **Infinite discontinuity:** the function shoots off toward $+\infty$ or $-\infty$ near that point (usually because of a denominator hitting zero without anything canceling it). Picture a vertical asymptote.

### Toolbox

**The continuity checklist at $x=a$:** $f$ is continuous at $a$ if and only if all three hold:

$$\text{1. } f(a) \text{ is defined} \qquad \text{2. } \lim_{x\to a} f(x) \text{ exists} \qquad \text{3. } \lim_{x\to a}f(x) = f(a)$$

**Where continuity usually "just works" automatically:** polynomials are continuous everywhere; rational functions (fractions of polynomials) are continuous everywhere except where the denominator is zero; square roots are continuous everywhere they're defined (inside the domain).

**Solving for an unknown to force continuity at a breakpoint:** set the left-hand piece's value/limit equal to the right-hand piece's value/limit at that breakpoint, then solve the resulting equation for the unknown.

**Classifying a discontinuity:**
- Limit exists, but doesn't match $f(a)$ (or $f(a)$ is undefined) → **removable**
- Left limit $\ne$ right limit → **jump**
- Function blows up toward $\pm\infty$ → **infinite**

### Common mistakes

- **Checking only that the left and right limits agree, and stopping there.** That only confirms the limit *exists* — you still have to check it matches $f(a)$.
- **Forgetting to check that $f(a)$ is even defined in the first place.** A function can't be continuous at a point where there's no dot at all.
- **Assuming a piecewise function is automatically continuous everywhere just because each individual piece is a nice, continuous formula.** You must still separately check every breakpoint where the pieces are glued together.
- **Mixing up removable and jump discontinuities.** A hole (removable) can be patched by redefining one point; a jump cannot, because the two sides are approaching genuinely different values.
- **Sign or algebra slips while solving for the unknown parameter.** These problems usually reduce to a simple one-variable equation — take it slow.

**Practice.** 21 problems on this section — 6 warm-up, 6 standard, 5 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

## 1.6 Limits Involving Infinity and Asymptotes

### The idea, in plain words

This section asks two closely related questions:

1. **"What happens to $f(x)$ as $x$ grows forever, in either direction?"** — this is a **limit at infinity**, and it tells us about **horizontal asymptotes**: flat lines the graph flattens out toward (but doesn't necessarily touch) way out on the left or right.
2. **"What happens to $f(x)$ as $x$ approaches some specific number where the function blows up?"** — this connects straight back to the infinite discontinuities from §1.5, and tells us about **vertical asymptotes**: vertical lines the graph shoots up or down alongside, without ever crossing.

**Picture it:** imagine a graph that, way off to the right, gets flatter and flatter, hugging a horizontal line more and more closely — that flat line is the horizontal asymptote. Now imagine a totally different spot on the same graph where, as you approach one particular $x$-value, the curve rockets straight up (or down) like a rocket ship — that's a vertical asymptote.

**The key trick for limits at infinity with fractions of polynomials:** you can't just "plug in infinity" — infinity isn't a number. Instead, we divide every single term (top and bottom) by the *highest power of $x$ found in the denominator*. Every term that ends up with an $x$ in the bottom (like $\frac{1}{x}$ or $\frac{5}{x^2}$) shrinks to $0$ as $x\to\infty$, since dividing by a bigger and bigger number gives you less and less. What's left tells you the answer instantly.

### Toolbox

**Limits of simple power terms:**
$$\lim_{x\to\infty}\frac{c}{x^n} = 0 \quad \text{for any constant } c \text{ and any } n>0$$

**The three-case rule for rational functions** (fraction of polynomial over polynomial) as $x\to\infty$ or $x\to-\infty$ — compare the **degree** (highest power of $x$) on top versus bottom:

- **Top degree $<$ bottom degree:** the limit is $0$. Horizontal asymptote: $y=0$.
- **Top degree $=$ bottom degree:** the limit is the ratio of the **leading coefficients** (the numbers in front of the highest powers). Horizontal asymptote: $y = \dfrac{\text{leading coeff. of top}}{\text{leading coeff. of bottom}}$.
- **Top degree $>$ bottom degree:** the limit is $+\infty$ or $-\infty$ (the fraction grows without bound). There is no horizontal asymptote in this case.

**How to actually compute it:** divide every term in the numerator and denominator by $x^n$, where $n$ is the highest power appearing in the *denominator*. Then apply $\lim_{x\to\infty}\frac{c}{x^k}=0$ to every leftover fraction term.

**Vertical asymptotes:** for a rational function $\dfrac{P(x)}{Q(x)}$, a vertical asymptote occurs at any $x=a$ where $Q(a)=0$ **and** $P(a)\ne 0$ (the factor causing the zero does *not* cancel out). This is exactly the infinite-discontinuity idea from §1.5.

**The cancellation trap (important!):** always factor the top and bottom fully *before* deciding on vertical asymptotes. If a factor cancels between the numerator and denominator, that $x$-value is only a **removable hole**, not a vertical asymptote — the graph doesn't blow up there at all.

### Common mistakes

- **Trying to "plug in infinity."** Infinity is not a number you can substitute — always divide by the highest power in the denominator instead.
- **Forgetting to factor before finding vertical asymptotes.** If you skip factoring, you might mistakenly call a removable hole a vertical asymptote (or vice versa).
- **Mixing up which direction the graph shoots — $+\infty$ or $-\infty$.** Check the sign of the expression just barely to the left and just barely to the right of the asymptote separately; they can be different.
- **Assuming top degree $=$ bottom degree always gives a "nice" horizontal asymptote of $1$.** It's the *ratio of leading coefficients*, not automatically $1$ — don't forget to actually read off the coefficients.
- **Forgetting that a graph *can* cross its horizontal asymptote** (just not near $\pm\infty$) — unlike a vertical asymptote, which the graph never touches at all.

**Practice.** 21 problems on this section — 6 warm-up, 6 standard, 5 challenge, 4 applied — are in the [Problems tab](#/ch01/problems), each with its worked solution.

---

*Intuitive Calculus — an independent, original study guide. Not affiliated with any university, publisher or instructor.*
