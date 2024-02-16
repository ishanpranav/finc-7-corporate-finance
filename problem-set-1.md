# Problem Set 1

Ishan Pranav

February 16, 2024

Professor Shan Ge

FINC 7 Corporate Finance

## Definitions

Let $r$ be the discount rate and $n$ be the number of periods.

Given an asset $X$, let ${V_X}_j$ be its value in period $j$ where $0\leq j\leq
n$, ${C_X}_j$ be its cash flow in period $j$, and $g_X$ be the growth rate of
its cash flows. Let $\beta_X$ represent its systematic risk with respect to the
market.

Define $\mathrm{pv}:\mathbb{Q}^4\to\mathbb{Q}$, which yields ${V_X}_0$ given
$r$, $n$, $C_X$, and ${V_X}_n$.

## Question 1

> You expect to have \$8,000 in one year. A bank is offering loans at 4.5\%
> interest per year. How much can you borrow today?

We can safely borrow the present value of \$8,000 discounted at 4.5\% compounded
annually for 1 year:

$$V_0=\mathrm{pv}(r=4.5\%,\,n=1,\,C=0,\,V_1=\$8000.00),$$

$$V_0=\frac{\$8000.00}{1+4.5\%},$$

$$V_0\approx\$7655.50.$$

We can borrow up to \$7,655.50.

## Question 2

> Qualcomm has developed a groundbreaking new CPU chip. You expect the chip's
> profits to be \$4 million in its first year and that this amount will grow at
> a rate of 5\% per year for the next 17 years. Once the patent expires, Intel
> will be able to produce the same chip and competition will likely drive
> profits to zero. What is the present value of the new chip if the interest
> rate is 8\% per year?

We can model the chip as a growing annuity:

$$V_0=\sum_{j=1}^n{\frac{C(1+g)^{j-1}}{(1+r)^j}},$$

$$V_0=\frac{C}{r-g}\left(1-\frac{(1+g)^n}{(1+r)^n}\right),$$

$$V_0=\frac{\$4000000.00}{8\%-5\%}\left(1-\frac{(1+5\%)^{17}}{(1+8\%)^{17}}\right),$$

$$V_0=\$50738481.67$$

The present value is about $50,738,481.67.

## Question 3

> Assume that Social Security promises you $50,000 per year starting when you
> retire 45 years from today (the first $50,000 will get paid 45 years from
> now). If the discount rate is 4%, compounded annually, and you plan to live
> for 17 years after retiring (so that you will receive a total of 18 payments
> including the first one), what is the value today of Social Security's
> promise?

We can model Social Security as an annuity:

$$V_{44}=\mathrm{pv}(r=4\%,\,n=18,\,C=\$50000.00,\,V_{62}=0).$$

The present value is given by discounting:

$$V_0=\mathrm{pv}(r=4\%,\,n=44,\,C=0,\,V_{44}),$$

$$V_0\approx\$112697.08.$$

The present value is about \$112,697.08.

## Question 4

> Consider the following 3 stocks:
>
> Stock $A$ is expected to provide a dividend of \$10 per share forever.
>
> Stock $B$ is expected to pay a dividend of \$5 next year. The dividend growth
> is expected to be 4\% per year forever.
>
> Stock $C$ is expected to pay a dividend of \$5 next year. The dividend is
> expected to grow by 20\% annually for 5 years (i.e., until year 6) and then
> become zero forever.
>
> If the discount rate for each stock is 10\%, what stock is the most valuable?

We can model $A$ as a perpetuity:

$${V_A}_0=\sum_{j=1}^\infty{\frac{C_A}{(1+r)^j}}=\frac{C_{A}}{r},$$

$${V_A}_0=\frac{\$10.00\text{ per share}}{10\%}=\$100.00\text{ per share}.$$

We model $B$ as a growing perpetuity:

$${V_B}_0=\sum_{j=1}^\infty{\frac{{C_B}(1+g_B)^{j-1}}{(1+r)^j}}=\frac{C_{B}}{r-g_B},$$

$${V_B}_0=\frac{\$5\text{ per share}}{10\%-4\%}\approx\$83.33\text{ per share}.$$

We model $C$ as a growing annuity:

$${V_C}_0=\frac{C_C}{r-g_C}\left(1-\frac{(1+g_C)^n}{(1+r)^n}\right),$$

$${V_C}_0=\frac{\$5\text{ per share}}{10\%-20\%}\left(1-\frac{(1+20\%)^6}{(1+10\%)^6}\right),$$

$${V_C}_0\approx\$34.28\text{ per share}.$$

Ergo Stock A is the most valuable.

## Question 5

> To get a company’s discount rate to value potential projects, the quick way of
> using the past two-year average realized returns are usually approximately
> correct. Is this correct?

No, this is not appropriate. Expected returns or the cost of capital should be
used as proxies for the discount rate. _Realized_ returns over a short period do
not provide sufficient data to reliably estimate the true expected return. The
method proposed will introduce significant statistical bias.

## Question 6

> Your cousin is currently 13 years old. She will be going to college in 5
> years. Your aunt and uncle would like to have $95,000 in a savings account to
> fund her education at that time. If the account promises to pay a fixed
> interest rate of 3.7% per year, how much money do they need to put into the
> account today to ensure that they will have $95,000 in 5 years.

We must invest the present value of $95,000 discounted at 3.7% compounded
annually for 5 years:

$$V_0=\mathrm{pv}(r=3.7\%,\,n=5,\,C=0,\,V_5=\$95000.00),$$

$$V_0\approx\$79219.09.$$

We must invest at least \$79,219.09.

## Question 7

> Is it good news for managers when a company’s expected return on its stocks
> increases?

No, it not good news for a manager when a company's expected return on its
shares increases. For an equity-financed company, the expected return on its
shares directly corresponds to its cost of capital. An increase in the expected
return indicates that the financing cost of projects—and thus their viability
and performance as measured by net present value—decreases. Of course, this does
not hold if all the company's projects are self-financed. Still, due to the
price-yield relation, an increase in the expected return is a decrease in the
share price, and thus bad news for managers.

## Question 8

> Coeing used to sell planes to commercial passenger airlines. At a strategy
> meeting today, the top management decided to sell planes to the military going
> forward. The discount rate the firm uses to value its future project should
> not change because the way we calculate $\beta$ for capital asset pricing
> model (CAPM) will yield the same number as before. Is this statement correct?

This statement is not strictly correct. Historically, military spending
increases even during periods of economic downturn. Perhaps after contracting
with the military, the company would perform better during recessions than it
used to. In this case, the company's systematic risk measured by $\beta$
decreases, and the CAPM provides a lower discount rate.

## Question 9

> Ling has two job offers. Offer $A$ is a receptionist at an investment bank.
> Offer $B$ is a teacher at a public school. The expected first year pay and pay
> growth rates are the same between the two offers. Which has a higher net
> present value (NPV)?

Historically, spending on public education persists even during periods of
economic downturn. Whereas public school salaries are resistant to market
movements, compensation at investment banks is extremely dependent on market
performance.  Thus, with respect to the market, the systematic risk of $B$ is
less than that of $A$. So $\beta_B<\beta_A$. Applying CAPM _caeteris paribus_
gives an expected return of $B$ less than that of $A$. Ergo the NPV of $B$ is
greater than that of $A$.
