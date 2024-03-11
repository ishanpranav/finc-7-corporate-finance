# Problem Set 4

Ishan Pranav

March 8, 2024

Professor Shan Ge

FINC 7 Corporate Finance

## Definitions

Let $V$ represent the total market value of a firm's capital structure. Define
$V=V_{\rm D}+V_{\rm E}+V_{\rm P}$, where $V_{\rm D}$ represents the total market
value of debt, $V_{\rm E}$ represents the market value of common stock, and
$V_{\rm P}$ represents the market value of preferred stock.

Given an asset $X$, let $\beta_X$ represent its systematic risk with respect to
the market.

Given a random variable $R$, denote its expectation $\mathbb{E}(R)$.

Let $\mu^*$ represent the expected return of the market and $f$ represent the
risk-free rate. Then the market risk premium is given by $(\mu^*-f)$.

Let $D_t$ represent the dividend of a firm in year $t$, $P_t$ represent the
price of an asset in year $t$, $C_t$ represent the cash flow of an project in
year $t$, and $g$ represent a firm's dividend growth rate.

## Question 1

> MV Corporation has debt with market value of \$95 million, common equity with
> a book value of \$95 million, and preferred stock worth \$20 million
> outstanding. Its common equity trades at \$49 per share, and the firm has 6.4
> million shares outstanding. What weights should MV Corporation use in its
> WACC?

$$V=V_{\rm D}+V_{\rm E}+V_{\rm P},$$
$$V_{\rm D}=\$95\text{ million},$$
$$V_{\rm P}=\$20\text{ million},$$
$$V_{\rm E}=(\$49\text{ per share})\times6.4\text{ million shares}=\$313.6\text{ million},$$
$$V=\$428.6\text{ million}.$$

The proportion of debt is $\frac{\$95\text{ million}}{\$428.6\text{ million}}\approx 0.2217\dots$

The proportion of common stock is $\frac{\$20\text{ million}}{\$428.6\text{ million}}\approx 0.0467\dots$

The proportion of preferred stock is $\frac{\$313.6\text{ million}}{\$428.6\text{ million}}\approx 0.7317\dots$

## Question 2

> Steady Company’s stock has $\beta_{\rm Steady}=0.16$. If the risk-free rate is 6.1% and the
> market risk premium is 6.8%, what is an estimate of Steady Company’s cost of
> equity?

The capital asset pricing model gives an estimate of Steady Company's total cost
of equity $R_{\rm Steady}$:

$$\mathbb{E}(R_{\rm Steady})-f=\beta_{\rm Steady}(\mu^*-f),$$
$$\mathbb{E}(R_{\rm Steady})=\beta_{\rm Steady}(\mu^*-f)+f,$$
$$\mathbb{E}(R_{\rm Steady})=(0.16\times 6.8\%)+6.1\%,$$
$$\mathbb{E}(R_{\rm Steady})=7.188\%.$$

A proxy for the total cost of equity is 7.188\%.

## Question 3

> Mackenzie Company has a price of $38 and will issue a dividend of \$2.00 next
> year. It has a beta of 1.3, the risk-free rate is 5.2\%, and the market risk
> premium is estimated to be 4.9\%.

### Question 3 Part A

> Estimate the equity cost of capital for Mackenzie.

The capital asset pricing model gives an estimate of Mackenzie's total cost of equity $R_{\rm Mackenize}$:

$$\mathbb{E}(R_{\rm Mackenzie})-f=\beta_{\rm Mackenzie}(\mu^*-f),$$
$$\mathbb{E}(R_{\rm Mackenzie})=\beta_{\rm Mackenzie}(\mu^*-f)+f,$$
$$\mathbb{E}(R_{\rm Mackenzie})=(1.3\times 4.9\%)+5.2\%.$$
$$\mathbb{E}(R_{\rm Mackenzie})=11.57\%.$$

A proxy for the total cost of equity is 11.57\%.

### Question 3 Part B

> Under the constant dividend growth model, at what rate do you need to expect
> Mackenzie's dividends to grow to get the same equity cost of capital as in
> Part A?

The constant dividend growth model also gives an estimate for Mackenzie's
total cost of equity $r$:

$$r=\frac{D_1}{P_0}+g,$$

$$g=r-\frac{D_1}{P_0}.$$

$$r\equiv R_{\rm Mackenzie}.$$

$$g=11.57\%-\frac{\$2.00}{\$38},$$

$$g=6.307\%.$$

Since both models provide a proxy for the same rate, we would expect about
6.307\% dividend growth for the models to converge at the same estimate for the
equity cost of captal.

## Question 4

> AllCity, Inc., is financed 40% with debt, 8% with preferred stock, and 52%
> with common stock. Its cost of debt is 5.7%, its preferred stock pays an
> annual dividend of $2.49 and is priced at $30. It has an equity beta of 1.15.
> Assume the risk-free rate is 1.7%, the market risk premium is 7.3%
> and AllCity's tax rate is 35%. What is its after-tax WACC?

Let $R_{\rm E}$ represent the cost of equity, $R_{\rm D}$ represent the cost of
debt, and $R_{\rm T}$ represent the effective corporate tax rate.

The weighted average cost of capital $R_{\rm AllCity}$ is given by:

$$R_{\rm AllCity}=R_{\rm D}(1-R_{T})\frac{V_{\rm D}}{V}+R_{\rm E}\frac{V_{\rm E}}{V}+R_{\rm P}\frac{V_{\rm P}}{V},$$

The capital asset pricing model provides a proxy for the common stock equity of
capital:

$$\mathbb{E}(R_{\rm E})-f=\beta_{\rm E}(\mu^*-f),$$
$$\mathbb{E}(R_{\rm E})=(1.15\times 7.3\%)+1.7\%,$$
$$\mathbb{E}(R_{\rm E})=10.095\%.$$

The preferred stock dividend is a proxy for the preferred equity cost of
capital:

$$R_{\rm P}=\frac{2.49}{30}\times 8\%=6.64\%.$$

Based on these proxies, we can estimate the weighted average cost of capital:

$$R_{\rm AllCity}=(5.7\%\times(1-35\%)\times 40\%)+\\(10.095\%\times 52\%)+\\(6.64\%\times 8\%).$$

$$R_{\rm AllCity}=7.2626\%.$$

The firm's cost of capital is about 7.2626%.

## Question 5

> A retail coffee company is planning to open 105 new coffee outlets that are
> expected to generate \$16.2 million in free cash flows per year, with a growth
> rate of 3.2\% in perpetuity. If the coffee company’s WACC is 9.2\%, what is
> the net present value of this expansion?

Assume the project has no upfront cost.  Let $r$ represent the firm's cost of
capital. The net present value is about \$270 million:

$$\frac{C}{r-g}=\frac{\$16.2\text{ million}}{9.2\%-3.2\%}=\$270\text{ million}.$$
