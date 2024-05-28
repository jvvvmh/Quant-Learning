# Active Equity Management

超级量化小小兔 2024

## 1 Introduction

### **Efficient Market Hypothesis**

1. weak: price reflects past market price
2. semi-strong: publicly available information
3. strong: all information

Below are the points against the foundation of ``EMH``.

**Investors are not always rational**

1. overconfidence: overestimate their skills and underestimate the risks
2. anchoring effect: tilt estimates towards analysts' target prices for stocks
3. confirmation bias: seek out information that confirms their personal beliefs
4. loss aversion: a loss has more than **twice** the impact on a person as a gain of equal magnitude. avoid high risk-adjusted returns because of the potential risks + herding among portfolio managers
5. disposition effect: sell winning stocks too soon and sell losing stocks too late (they believe that only when they sell the losing stocks, paper losses will turn into actual losses)

**Market structure** (analysts' relationship to seniors of a firm, index funds replicate value weighted benchmarks, short sale restrictions, individual investors do not routinely short) -> a stock can stay overvalued for a long time before correction

**Costs of arbitrage**

1. information
2. transaction (commissions, bid-ask, market impact costs)
3. noise trader: willing to bet against the noise traders and manage losses caused by sustained mis-pricing?
4. idiosyncratic risk and event risk: to bet on a single anomaly, you need to hedge other risks. but vol is hard to be explained by common risk factors + event (acquisition, bankruptcy) is uncorrelated across assets

**Beat average investors**

1. information edge: information about a company's suppliers, customers, and competitors
2. insight edge
3. implementation edge: effective cost reduction and risk management, low-cost financing
4. conviction edge: short-term or long-term performance?



### **Technical VS Fundamental Analysis**

short-term: fundamentals do not change, price is driven by supply and demand -> technical and sentiment signals play larger roles.

long-term: a stock's price is determined by its merit.

### Quantitative Analysis

Not all information all quantifiable: management team changes, new product, competitors' strategic shift

Slow to respond to events: earthquake, fundamental traders assesses the direct damage to companies impacted by earthquake + indirect impact to suppliers or customers, while quantitative strategies wait until the impact shows up in statistics

### Active Mutual Funds and Hedge Funds

mutual funds: long only, no leverage, no derivatives, evaluated by active returns against indices rather than absolute returns

### Fundamental Law of Active Management

Information Ratio $\text {IR} = \text {IC }\times \sqrt N$

- $\text {IC}$: rank correlation coefficient between stock selection signals and realized future returns (>3-4%)

- $N$: number of independent bets each year

$\text {IR} = \text {IC }\times \sqrt N \times \text{TC} $ transfer coefficient

- by relaxing the long only constraint, a 130/30 strategy can increase the information ratio by 30%

$\text {IR} = \text {IC }\times \sqrt N \times \text{TC} - (\text{TCost} \times \text{TR} \times 2 / \text{TE})$ 

- $\text {TCost}$: trading cost / trade value
- $\text{TR}$: annual portfolio turnover
- $\text{TE}$: portfolio tracking error (expected volatility of alpha)

 

## 2 Data





















