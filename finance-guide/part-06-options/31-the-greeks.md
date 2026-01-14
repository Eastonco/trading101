# Chapter 31: The Greeks Explained

## Overview

The Greeks are risk metrics that measure how option prices change in response to various factors. Understanding delta, gamma, theta, and vega allows you to predict how your positions will behave and manage risk effectively. While the math behind them is complex, the concepts are essential for any options trader.

---

## Why the Greeks Matter

### Options Are Multi-Dimensional

**Stocks are simple:** Price goes up, you make money. Price goes down, you lose.

**Options depend on multiple factors:**
- Underlying price
- Time remaining
- Volatility
- And how those factors interact

### The Greeks Help You

- **Predict** how your position will move
- **Measure** risk exposure
- **Compare** different options/strategies
- **Manage** portfolio risk
- **Understand** why your P&L changed

---

## Delta (Δ)

### What Delta Measures

**Delta = How much the option price changes when the stock moves $1**

### Delta Values

**Calls:** Delta ranges from 0 to +1.00
**Puts:** Delta ranges from 0 to -1.00

| Option Type | Strike Location | Typical Delta |
|-------------|-----------------|---------------|
| Deep ITM Call | Way below stock | +0.90 to +1.00 |
| ATM Call | Near stock price | +0.50 |
| OTM Call | Above stock | +0.05 to +0.30 |
| ATM Put | Near stock price | -0.50 |
| OTM Put | Below stock | -0.05 to -0.30 |
| Deep ITM Put | Way above stock | -0.90 to -1.00 |

### Delta Example

**Stock at $50, you own a $50 call with 0.55 delta:**

- Stock rises $1 to $51
- Option increases ~$0.55
- Stock falls $1 to $49
- Option decreases ~$0.55

### Delta as Probability

**Rough approximation:** Delta ≈ probability of expiring in-the-money.

- 0.30 delta call ≈ 30% chance of expiring ITM
- 0.70 delta call ≈ 70% chance of expiring ITM
- 0.50 delta (ATM) ≈ 50/50 chance

**Not exact,** but useful for quick mental math.

### Delta as Share Equivalence

**Delta tells you equivalent stock exposure:**

- 1 contract (100 shares) with 0.50 delta = 50 share equivalent exposure
- 10 contracts with 0.30 delta = 300 share equivalent exposure

**Portfolio delta:** Sum of all position deltas tells you net directional exposure.

### Position Delta

| Position | Delta Effect |
|----------|--------------|
| Long call | Positive (bullish) |
| Short call | Negative (bearish) |
| Long put | Negative (bearish) |
| Short put | Positive (bullish) |
| Long stock | +1.00 per share |

---

## Gamma (Γ)

### What Gamma Measures

**Gamma = How much delta changes when the stock moves $1**

Gamma is the rate of change of delta—the acceleration.

### Gamma Characteristics

**ATM options have highest gamma:**
- Their delta changes most rapidly
- Small stock move = big delta change

**ITM and OTM options have lower gamma:**
- Delta changes more slowly
- More stable directional exposure

### Gamma Example

**You own a $50 call with:**
- Delta: 0.50
- Gamma: 0.08

**Stock moves from $50 to $51:**
- New delta: 0.50 + 0.08 = 0.58
- The call now moves $0.58 for each additional $1 stock move

### Gamma Risk

**Long gamma (long options):**
- Position accelerates in your direction
- Delta increases as you win
- Delta decreases as you lose
- Generally beneficial

**Short gamma (short options):**
- Position accelerates against you
- As stock moves against you, exposure worsens
- Delta increases as you lose
- Dangerous with big moves

### Gamma and Expiration

**Gamma increases as expiration approaches** for ATM options.

Near expiration, ATM options flip rapidly between worthless and valuable—high gamma environment.

**This is why:**
- Short-dated ATM options are volatile
- Week of expiration can see wild option swings
- Managing gamma risk matters most near expiration

---

## Theta (Θ)

### What Theta Measures

**Theta = How much the option price decreases each day due to time decay**

Theta is typically expressed as a negative number for long options.

### Theta Characteristics

**ATM options have highest theta:**
- Most time value to lose
- Decay fastest

**ITM and OTM have lower theta:**
- Less extrinsic value
- Less to decay

### Theta Example

**You own a $50 call with:**
- Price: $2.50
- Theta: -0.05

**Tomorrow (all else equal):**
- Option price: $2.50 - $0.05 = $2.45
- You lost $5 per contract just from time passing

### Theta Acceleration

**Theta increases (becomes more negative) as expiration approaches.**

| Days to Expiration | Daily Theta |
|-------------------|-------------|
| 60 days | -$0.02 |
| 30 days | -$0.04 |
| 14 days | -$0.07 |
| 7 days | -$0.12 |
| 1 day | -$0.25 |

### Theta Position

| Position | Theta Effect |
|----------|--------------|
| Long call | Negative (loses to time) |
| Short call | Positive (gains from time) |
| Long put | Negative (loses to time) |
| Short put | Positive (gains from time) |

**Option buyers:** Time is your enemy
**Option sellers:** Time is your friend

### Weekend Theta

Options decay over weekends too. Some models include weekend decay in Friday's theta, others spread it out. Be aware of this when holding over weekends.

---

## Vega (ν)

### What Vega Measures

**Vega = How much the option price changes when IV moves 1 percentage point**

Note: Vega isn't actually a Greek letter—it's named for consistency.

### Vega Characteristics

**All options have positive vega** (for long positions):
- Higher IV = Higher option prices
- Lower IV = Lower option prices

**ATM options have highest vega:**
- Most sensitive to volatility changes

**Longer-dated options have higher vega:**
- More time for volatility to matter

### Vega Example

**You own a $50 call with:**
- Price: $3.00
- Vega: 0.15
- Current IV: 30%

**If IV increases to 32%:**
- Change: +2 percentage points
- Price impact: 2 × $0.15 = +$0.30
- New option price: $3.30

**If IV decreases to 25%:**
- Change: -5 percentage points
- Price impact: 5 × $0.15 = -$0.75
- New option price: $2.25

### Vega Position

| Position | Vega Effect |
|----------|-------------|
| Long call | Positive (benefits from IV rise) |
| Short call | Negative (hurt by IV rise) |
| Long put | Positive (benefits from IV rise) |
| Short put | Negative (hurt by IV rise) |

### Vega and Events

**Before earnings:**
- IV elevated
- High vega exposure matters

**After earnings:**
- IV crushes
- Long vega positions suffer even if direction is correct

---

## Minor Greeks

### Rho (ρ)

**Rho = Sensitivity to interest rate changes**

- Calls have positive rho (benefit from rate increases)
- Puts have negative rho

**Practical impact:** Usually negligible except for LEAPS or in high-rate environments.

### Charm

**Charm = Rate of change of delta over time**

How delta changes as time passes, even without stock movement. Relevant near expiration.

### Vanna

**Vanna = Rate of change of delta with respect to IV**

Or equivalently, rate of change of vega with respect to stock price. Used in advanced trading.

### Volga (Vomma)

**Volga = Rate of change of vega with respect to IV**

How vega itself changes when IV moves. Advanced risk management.

---

## Greeks in Action: A Complete Example

### The Position

**Long 5 contracts of XYZ $100 call**
- Stock price: $100
- Option price: $4.00
- Delta: 0.52
- Gamma: 0.05
- Theta: -0.08
- Vega: 0.20
- IV: 25%

### Total Position Greeks

- Position delta: 5 × 100 × 0.52 = +260 (equivalent to 260 shares)
- Position gamma: 5 × 100 × 0.05 = +25
- Position theta: 5 × 100 × (-0.08) = -$40/day
- Position vega: 5 × 100 × 0.20 = +100

### Scenario Analysis

**Scenario 1: Stock rises $2, IV unchanged**
- Delta gain: 260 × $2 = $520
- Theta loss (1 day): -$40
- New delta: ~260 + (25 × 2) = 310
- **Net gain: ~$480**

**Scenario 2: Stock flat, IV drops 3%**
- Delta gain: $0
- Vega loss: 100 × (-3) = -$300
- Theta loss (1 day): -$40
- **Net loss: ~$340**

**Scenario 3: Stock drops $1, IV rises 2%**
- Delta loss: 260 × (-$1) = -$260
- Vega gain: 100 × 2 = +$200
- Theta loss: -$40
- **Net loss: ~$100**

---

## Using Greeks for Strategy Selection

### Want to Profit from Direction?

**Focus on delta:**
- High delta for stock replacement
- Lower delta for leveraged bets
- Consider gamma for acceleration

### Want to Profit from Time?

**Focus on theta:**
- Sell options (positive theta)
- ATM options for highest decay
- Manage gamma risk

### Want to Profit from Volatility?

**Focus on vega:**
- Long options when IV is low
- Short options when IV is high
- Trade around events (carefully)

### Neutral Strategies

**Balance the Greeks:**
- Delta-neutral (no directional bias)
- Theta-positive (collect time decay)
- Manage vega exposure

---

## Greek Risk Management

### Position Limits by Greek

**Example risk limits:**
- Maximum position delta: ±1,000 (equivalent shares)
- Maximum position theta: -$200/day
- Maximum vega exposure: ±500

### Hedging with Greeks

**To reduce delta:** Buy/sell stock or opposite options
**To reduce gamma:** Close ATM options or widen strikes
**To reduce theta:** Close short-dated positions
**To reduce vega:** Close positions before IV spikes

### The Trade-Offs

**You can't optimize all Greeks simultaneously:**
- High theta (selling) = negative gamma (risk)
- Positive gamma (long) = negative theta (bleeding)
- Long vega = positive if IV rises, negative if it falls

---

## Greeks Summary Table

| Greek | Measures | Range | ATM Value | Time Effect |
|-------|----------|-------|-----------|-------------|
| Delta | Price sensitivity | 0 to ±1 | ±0.50 | Stable |
| Gamma | Delta sensitivity | 0+ | Highest | Increases near expiry |
| Theta | Time decay | Negative (long) | Most negative | Increases near expiry |
| Vega | IV sensitivity | 0+ | Highest | Decreases near expiry |

---

## Key Takeaways

- **Delta tells you directional exposure** - How much you make/lose per $1 stock move
- **Gamma is the accelerator** - How quickly your exposure changes
- **Theta is the daily toll** - What you pay (or collect) for holding
- **Vega is volatility sensitivity** - Critical around events
- **ATM options have the most gamma, theta, and vega** - Most sensitive overall
- **Long options: negative theta, positive gamma and vega**
- **Short options: positive theta, negative gamma and vega**
- **Use Greeks to compare strategies and manage risk** - Not just to pick trades

---

## What's Next

In [Chapter 32: Basic Options Strategies](32-basic-options-strategies.md), we'll apply these concepts to fundamental strategies like covered calls, cash-secured puts, and protective puts.

---

*Remember: The Greeks transform options from mysterious black boxes into understandable risk exposures. Master them and you'll understand why your positions move the way they do.*
