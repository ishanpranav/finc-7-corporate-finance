# Problem Set 5

Ishan Pranav

April 15, 2024

Professor Shan Ge

FINC 7 Corporate Finance

## Definitions

Let $V_n$ represent the present market value of a firm in period $n$,
$V_{{\rm E}_n}$ represent the value of its equity, and $V_{{\rm D}_n}$ represent
the value of its debt (in period $n$).

Denote a firm's net earnings $E$, where a positive value indicates a net income
and a negative value indicates a net loss., Denote its interest
expense $X_{\rm interest}$ and its total tax $X_{\rm tax}$, where negative
values indicate expenses and positive values indicate _contra_ expenses.

Let $v_n$ be the value of some asset in period $n$ and $C$ be its periodic cash
flow. Define $\mathrm{pv}:\mathbb{Q}^4\to\mathbb{Q}$, which yields ${v_0}$ given
$r$, $n$, $C$, and ${v_n}$.

Let $r_{\rm tax}$ denote the corporate tax rate levied on net earnings before
taxes.

### Modigliani–Miller theorem

- **Proposition I:** If there are no taxes and no friction, then changes in the
  capital structure of the firm are independent of its cost of capital.
- **Proposition II:** Suppose there are no taxes and no friction. Denote a
  firm's expected return on equity $r_{\rm E}$, its expected return on debt
  $r_{\rm D}$, and its unlevered cost of capital $r_0$. Then
  $$r_{\rm E}=r_0+\frac{V_{\rm E}}{V_{\rm D}}(r_0-r_{\rm D}).$$

## Question 1

> Acort Industries owns assets that will have a 75% probability of having a
> market value of $52 million in one year. There is a 25% chance that the assets
> will be worth only $22 million. The current risk-free rate is 5%, and Acort's
> assets have a cost of capital of 10%.

### Question 1 Part A

> If Acort is unlevered, what is the current market value of its equity?

Since there is no debt, the current market value of equity is the expectation of
the future assets, discounted at the company's cost of capital.

$$V_{{\rm E}_1}=V_1=(75\%\times\$52\text{ million})+(25\%\times\$22\text{ million}).$$

$$V_{{\rm E}_0}=\mathrm{pv}(r=10\%,n=1,C=0,V_{{\rm E}_1}=\$44.5\text{ million}),$$

$$V_{{\rm E}_0}=\$40.\overline{45}\text{ million}.$$

The market value of equity is about \$40.45 million.

### Question 1 Part B

> Suppose instead that Acort has debt with a face value of $18 million due in
> one year. According to MM (i.e. perfect market), what is the value of Acort's
> equity in this case?

Assume no taxes and no friction. Assume the debt issued is risk-free.

By the
Modigliani–Miller theorem, we have the new discount rate $r'=r=10\%$. Changes in
the capital structure of the firm do not affect its cost of capital.

First we determine the new market value of the debt $V_{{\rm D}_0}$:

$$V_{{\rm D}_0}=\mathrm{pv}(r_{\rm D}=5\%,n=1,C=0,V_{{\rm D}_1}=\$18\text{ million}),$$

$$V_{{\rm D}_0}\approx\$17.1429\dots\text{ million}.$$

The market value of debt is about $17.14 million. Then determine the new market
value of equity $V_{{\rm E}_0}'$:

$$V_0'=V_{{\rm D}_0}+V_{{\rm E}_0}',$$

$$V_{\rm E_0}'\approx\$40.\overline{45}\text{ million}-\$17.1429\dots\text{ million},$$

$$V_{\rm E_0}'\approx\$23.3117\dots\text{ million}.$$

The market value of equity is about $23.31 million.

### Question 1 Part C

> What is the expected return of Acort's equity without leverage? What is the
> expected return of Acort's equity with leverage?

Without leverage, the expected return on equity is the expected return on
assets, which is the same as the cost of capital: 10\%.

Let $r_{\rm E}'$ denote the expected return
on equity with leverage.

$$r_{\rm E}'=r_0+\frac{V_{{\rm D}_0}}{V_{{\rm E}_0}}(r_0-r_{\rm D}),$$

$$r_{\rm E}'\approx 10\%+\left(\frac{\$17.1429\dots\text{ million}}{\$23.3117\dots\text{ million}}\right)(r_0-r_{\rm D}),$$

$$r_{\rm E}'\approx 10\%+(0.735376\dots)(r_{\rm E}-f),$$

$$r_{\rm E}'\approx 10\%+(0.735376\dots)(10\%-5\%).$$

$$r_{\rm E}\approx 13.6769\dots\%.$$

With leverage, the expected return on equity is about 13.7%.

### Question 1 Part D

> What is the lowest possible realized return of Acort's equity with and without
> leverage?

Without leverage, the worst-case future value of the equity is $V_{{\rm E}_1}=V_1=\$22\text{ million}$.

$$\left(\frac{V_{{\rm E}_1}}{V_{{\rm E}_0}}-1\right)=\left(\frac{\$22\text{ million}}{\$40.\overline{45}\text{ million}}-1\right)\approx 45.6180\dots\%,$$

The lowest possible realized return without leverage is about -46%.

With leverage, the worst-case future value of the equity is
$V_{{\rm E}_1}'=(V_1-V_{{\rm D}_1})=(\$22\text{ million}-\$18\text{ million})=\$4\text{ million}$.

$$\left(\frac{V_{{\rm E}_1}'}{V_{{\rm E}_0}'}-1\right)=\left(\frac{\$4\text{ million}}{\$23.3117\dots\text{ million}}-1\right)\approx 82.8412\dots\%.$$

The lowest possible realized return with leverage is about -83%.

## Question 2

> Hardmon Enterprises is currently an all-equity firm with an expected return of
> 11.6%. It is considering a leveraged recapitalization in which it would borrow
> and repurchase existing shares. Assume perfect capital markets.

### Question 2 Part A

> Suppose Hardmon borrows to the point that its debt-equity ratio is 0.5. With
> this amount of debt, the debt cost of capital is 6%. What will be the expected
> return of equity after this transaction?

The Modigliani–Miller theorem gives the expected return on equity.

$$r_{\rm E}=11.6\%+0.5\times(11.6\%-6\%),$$

$$r_{\rm E}=14.4\%.$$

The expected return on equity is 14.4%.

### Question 2 Part B

> Suppose instead Hardmon borrows to the point that its debt-equity ratio is
> 1.50. With this amount of debt, Hardmon’s debt will be much riskier. As a
> result, the debt cost of capital will be 8%. What will be the expected return
> of equity in this case?

Let $\frac{V_{\rm D}'}{V_{\rm E}'}=1.50$ denote the new debt-to-equity ratio.
Let $r_{\rm D}'=8\%$ denote the new expected return on debt. Then the
Modigliani–Miller theorem gives the new expected return on equity $r_{\rm E}'$:

$$r_{\rm E}'=11.6\%+1.50\times(11.6\%-8\%),$$

$$r_{\rm E}'=17\%.$$

The new expected return on equity is 17%.

### Question 2 Part C

> A senior manager argues that it is in the best interest of the shareholders to
> choose the capital structure that leads to the highest expected return for the
> stock. How would you respond to this argument?

The argument is fundamentally flawed. If the senior manager is charged with
increasing firm value, then the method is incorect. A high expected return
corresponds to a low price. The manager's goals will result in value destruction
rather than value creation. The manager should instead focus on increasin the
value of the firm.

## Question 3

> Pelamed Pharmaceuticals had EBIT of $189 million in 2018. In addition, Pelamed
> had interest expenses of $73 million and a corporate tax rate of 21%.

### Question 3 Part A

> What is Pelamed’s 2018 net income?

$$E=\$189\text{ million}+X_{\rm interest}+X_{\rm tax},$$

$$X_{\rm tax}=-r_{\rm tax}(\$189\text{ million}+X_{\rm interest}),$$

$$X_{\rm tax}=-21\%\times(\$189\text{ million}-\$73\text{ million}),$$

$$X_{\rm tax}=-\$24.36\text{ million}.$$

$$E=\$189\text{ million}-\$73\text{ million}-\$24.36\text{ million}.$$

$$E=\$91.64\text{ million}.$$

The firm's net income is $91.64 million.

### Question 3 Part B

> If Pelamed had no interest expenses, what would have been its 2018 net income?
> How does it compare to your answer in Part A?

Suppose Pelamed had no interest expenses. Denote the new net earnings $E'$ and
the new total tax $X_{\rm tax}'$.

$$X_{\rm tax}'=-21\%\times\$189\text{ million}=-\$39.69\text{ million}.$$

$$E'=\$189\text{ million}+X_{\rm tax}',$$

$$E'=\$189\text{ million}-\$39.69\text{ million}=\$149.31\text{ million}.$$

The firm's new net income is $149.31 million.

### Question 3 Part C

> What is the amount of Pelamed’s interest tax shield in 2018?

$$r_{\rm tax}X_{\rm interest}=(21\%\times 73\text{ million})=\$15.33\text{ million}.$$

The amount of the interest tax shield is $15.33 million.

## Question 4

> Suppose the corporate tax rate is 30%. Consider a firm that earns $3,500 in
> earnings before interest and taxes each year with no risk. The firm's capital
> expenditures equal its depreciation expenses each year, and it will have no
> changes to its net working capital. The risk-free interest rate is 5%.

### Question 4 Part A

> Suppose the firm has no debt and pays out its net income as a dividend each
> year. What is the value of the firm's equity?

$$V_{\rm E}=V=\frac{E}{r_{\rm E}}.$$
$$E=\$3500\times(1-r_{\rm tax}),$$
$$E=\$3500\times(1-30\%)=\$2450.$$

Since the firm's earnings are risk-free, the expected return on equity is the
risk free rate $f=5\%$.

$$V_{\rm E}=\frac{E}{f}=\frac{\$2450}{5\%}=\$49000.$$

The value of the firm's equity is $49,000.

### Question 4 Part B

> Suppose instead the firm makes interest payments of $2,000 per year. What is
> the value of equity? What is the value of debt?

The value of debt is the present value of the interest payments.

$$V_{\rm D}=\frac{X_{\rm interest}}{f}=\frac{\$2000}{5\%}=\$40000.$$

The value of the firm's debt is $40,000.

Let $E'$ denote the new net earnings, based upon the interest expense and the
new total tax $X_{\rm tax}'$.

$$E'=\$3500+X_{\rm interest}+X_{\rm tax}',$$

$$X_{\rm tax}'=-30\%\times(\$3500+X_{\rm interest}),$$

$$X_{\rm tax}'=-30\%\times(\$3500-\$2000),$$

$$X_{\rm tax}'=-\$450,$$

$$E'=\$3500-\$2000-\$450.$$

$$E'=\$1050.$$

The value of equity is the present value of the dividend payments.

$$V_{\rm E}=\frac{E'}{f}=\frac{\$1050}{5\%}=\$21000.$$

The value of the firm's equity is $21,000.

### Question 4 Part C

> What is the difference between the total value of the firm with leverage and
> without leverage?

The total value of the firm without leverage is $49,000. With leverage, the
total value of the firm is $61,000. Leverage increases the firm value by
$12,000.

## Question 5

Now that your firm has matured, you are considering adding debt to your capital
structure for the first time. Your all-equity firm has a market value of $21
million and you are considering issuing $2 million in debt with an interest rate
of 5% and using it to repurchase shares. You pay a corporate tax rate of 40%.
Assume taxes are the only imperfection and the debt is expected to be permanent.

### Question 5 Part A

> What will be the total value of the firm after the change in capital
> structure?

The change in capital structure is equal to the tax savings from the interest
expense deduction. Let $V'$ denote the new value of the firm.

There is a causal relationship between the interest payments and the tax
savings.

$$V'=V+\frac{r_{\rm tax}X_{\rm interest}}{r_{\rm D}},$$

$$V'=\$21\text{ million}+\frac{40\%\times5\%\times\$2\text{ million}}{5\%},$$

$$V'=\$21.8\text{ million}.$$

The new value of the firm is $21.8 million.

### Question 5 Part B

> What will be the value of the remaining equity after the change in capital
> structure?

The new value of the equity $V_{\rm E}'$ is the residual value of the firm:

$$V_{\rm E}'=V'-V_{\rm D},$$
$$V_{\rm E}'=\$21.8\text{ million}-\$2\text{ million}=\$19.8\text{ million}.$$

The new value of the equity is $19.8 million.
