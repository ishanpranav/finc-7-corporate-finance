# Problem Set 2

Ishan Pranav

February 25, 2024

Professor Shan Ge

FINC 7 Corporate Finance

## Definitions

Let $r$ be the discount rate and $n$ be the number of periods.

Given an asset $X$, let ${V_X}_j$ be its value in period $j$ where $0\leq j\leq
n$ and , ${C_X}_j$ be its cash flow in period $j$.

Given a random variable $R$, denote its expectation $\mathbb{E}(R)$.

Define $\mathrm{pv}:\mathbb{Q}^4\to\mathbb{Q}$, which yields ${V_X}_0$ given
$r$, $n$, $C_X$, and ${V_X}_n$. Define $\mathrm{fv}:\mathbb{Q}^4\to\mathbb{Q}$,
which yields ${V_X}_n$ given $r$, $n$, $C_X$, and ${V_X}_0$.

## Question 1

> You are preparing to produce some goods for sale. You will sell them in one
> year and you will incur costs of \$90,000 immediately. If your cost of capital
> is 6.8\%, what is the minimum dollar amount you need to sell the goods for in
> order for this to be a non-negative NPV project?

The minimum sale price is the future value of \$90,000 at 6.8\%:

$$V_1=\mathrm{fv}(r=6.8\%,n=1,C=0,V_0=\$90000.00),$$

$$V_1=\$90000.00(1+6.8\%),$$

$$V_1=\$96120.00.$$

The minimum sale price is \$96,120.00.

## Question 2

> You are CEO of AMD, maker of high-performance graphic cards for gaming
> computers. You are considering whether to launch a new product. See the cash
> flows every year below:
>
> -\$895,000 in year 0, \$261,450 in year 1, \$607,500 in year 2, \$360,225 in
> year 3, \$199,496 in year 4, and \$95,022 in year 5.

### Question 2 Part A

> What is the project's net present value (NPV) if the project's cost of capital
> is 9.4\%?

The result is given by the sum of the present values of the cash flows:

$$V_0=\mathrm{npv}\left(r=9.4\%,\begin{bmatrix}\$895000\\\$261450\\\$607500\\\$360225\\\$199496\\\$95022\end{bmatrix}\right),$$

$$V_0=\sum_{j=0}^{n}{\mathrm{pv}(r=9.4\%,j,0,C_j)},$$

$$V_0=\sum_{j=0}^{n}{\frac{C_j}{(1+r)^j}},$$

$$V_0=\$326602.87.$$

The NPV is \$326,602.87.

### Question 2 Part B

> Use your intuition to guess whether IRR should be higher than 9.4% or not,
> without calculating the IRR. Explain your intuition.

Intuitively, the internal rate of return IRR should be greater than 9.4\%
because this is a positive-NPV project where cash flows are provided at the end
of successive future periods.

## Question 3

> You are thinking about placing a sign advertising your services at a local bus
> stop near West 4th Street station where there’s an ongoing basketball
> tournament. The sign will cost \$4,700 and it will be posted for one week. You
> expect that it will generate additional revenue of \$846 per day. What is the
> payback period (in nearest day)?

The payback period $n$ is given by the ratio of cost $V_0$ to average periodic
cash flow $C$.

$$n=\frac{V_0}{C},$$

$$n=\frac{\$4700}{\$846}=5.\overline{5}\approx 6.$$

Thus the payback period is 6 days.

## Question 4

> You have \$1M. There are two projects. Each requires an upfront investment of
> \$1M, then generates positive cash flows every year after that. Project A has
> an NPV of \$5M, an IRR of 10\%. Project B has an NPV of \$3M, an IRR of 15\%.
> Which project should get funding? Explain why. If your answer depends on
> specific assumptions, state your assumptions.

Assume we can raise additional capital. We will invest in both Project A and
Project B because both projects have positive NPV. This means that, even
considering our cost of capital, these projects are expected to make us
wealthier.

**Option 1:** We can invest our \$1M in one project and raise an additional \$1M
to invest in the other.

**Option 2:** Or, we return our \$1M to shareholders and raise \$2M to finance
the projects.

## Question 5

> You are considering setting up a firm to produce electric cars. The cost of
> the project is \$30M today. The demand for widgets is uncertain. It can be
> either high or low with equal probability. When the demand is high, cash flows
> in year 1 are \$66M and when the demand is low, cash flows in year 1 are
> \$34M. The discount rate is 10\%.

### Question 5 Part A

> What is the NPV of the project?

The result in millions of dollars is given by the present value of the expected
cash flow $\mu_{V_1}$, minus the initial investment:

$${V_A}_0=\mathrm{pv}(r=10\%,n=1,0,\mu_{V_1})-30.$$

$$\mu_{{V_A}_1}=\mathbb{E}({V_A}_1)=\frac{66+34}{2}=50.$$

$${V_A}_0=\frac{\mu_{{V_A}_1}}{1+r}-30,$$

$${V_A}_0=\frac{50}{1+10\%}-30,$$

$${V_A}_0=45.\overline{45}-30=15.\overline{45}.$$

The NPV of the project is about $15.45 million.

### Question 5 Part B

> Suppose you can commission a study that tells you whether the demand for
> widgets will be high or low. The study takes one year to complete. That is, if
> you commission the study you must decide in year 1 whether to invest. If you
> invest, the cash flows will arrive in year 2. What is the maximum amount you
> are willing to pay for the study today?

The NPV of the project without conducting the study is
${V_A}_0=15.\overline{45}$ (millions of dollars).

Assume an efficient market. Our willingness to pay $D$ for a study with NPV
${V_B}_0$ is the price such that the NPV is the same (all figures in millions of
dollars). This follows from the law of one price:

$${V_B}_0-D={V_A}_0.$$

$$D={V_B}_0-15.\overline{45}.$$

To determine ${V_B}_0$, the NPV of the project if the study is conducted, there
are two cases:

1. Suppose the study determines that the demand for widgets is low.

   1. Suppose we undertake the project. Then
   $${V_B}_0=\mathrm{npv}\left(r=10\%,\begin{bmatrix}0\\-30\\34\end{bmatrix}\right),$$
   $${V_B}_0=\frac{(-30)}{1+10\%}+\frac{34}{(1+10\%)^2},$$
   $${V_B}_0\approx 0.8264\dots$$
   2. Suppose we do not undertake the project. Then ${V_B}_0=0.$

   So if demand is low we undertake the project.

2. Suppose instead the study determines that the demand for widgets is high.

    1. Suppose we undertake the project. Then
    $${V_B}_0=\mathrm{npv}\left(r=10\%,\begin{bmatrix}0\\-30\\66\end{bmatrix}\right),$$
    $${V_B}_0=\frac{(-30)}{1+10\%}+\frac{66}{(1+10\%)^2},$$
    $${V_B}_0=27.\overline{27}.$$
    2. Suppose we do not undertake the project. Then ${V_B}_0=0.$

    So if demand is high we undertake the project.

Since in both cases we undertake the project, we have $D<0$ and we are
completely unwilling to pay for the study.
