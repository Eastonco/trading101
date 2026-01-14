# Chapter 30: How Options Are Priced

## Overview

Understanding what drives option prices is essential for making informed trading decisions. Option premiums consist of intrinsic and extrinsic value, with extrinsic value determined primarily by time and implied volatility. This chapter explains the factors that determine what you pay (or receive) for options.

---

## The Components of Option Price

### Option Premium = Intrinsic Value + Extrinsic Value

**Intrinsic value:** Real, tangible value (could be captured through exercise)
**Extrinsic value:** Time value plus volatility premium (evaporates by expiration)

### Example Breakdown

**Stock trading at $55:**
- $50 call trading at $7.50
- Intrinsic value: $55 - $50 = $5.00
- Extrinsic value: $7.50 - $5.00 = $2.50

**Stock trading at $55:**
- $60 call trading at $1.50
- Intrinsic value: $0 (out-of-the-money)
- Extrinsic value: $1.50 (100% time value)

---

## Intrinsic Value Deep Dive

### Calculation

**For calls:** Max(Stock Price - Strike Price, 0)
**For puts:** Max(Strike Price - Stock Price, 0)

Intrinsic value cannot be negative.

### Intrinsic Value Table (Stock at $100)

| Strike | Call Intrinsic | Put Intrinsic |
|--------|----------------|---------------|
| $90 | $10 | $0 |
| $95 | $5 | $0 |
| $100 | $0 | $0 |
| $105 | $0 | $5 |
| $110 | $0 | $10 |

### At Expiration

At expiration, options are worth **only** their intrinsic value:
- ITM options: Worth intrinsic value
- ATM/OTM options: Worth $0

This is why extrinsic value is sometimes called "time value"—it decays to zero over time.

---

## Extrinsic Value Factors

### The Main Drivers

1. **Time to expiration** (more time = more value)
2. **Implied volatility** (higher IV = more value)
3. **Distance from strike** (ATM has most extrinsic value)
4. **Interest rates** (minor effect)
5. **Dividends** (minor effect)

### Time Value

**More time = More uncertainty = More value**

The market pays for the possibility that the option could become profitable. More time means more opportunity for the underlying to move.

**Example (Stock at $50, $50 call):**

| Days to Expiration | Option Price | Extrinsic Value |
|-------------------|--------------|-----------------|
| 90 days | $4.50 | $4.50 |
| 60 days | $3.75 | $3.75 |
| 30 days | $2.75 | $2.75 |
| 7 days | $1.25 | $1.25 |
| 1 day | $0.30 | $0.30 |

### Time Decay Is Not Linear

**Key insight:** Time decay accelerates as expiration approaches.

- An option loses about 1/3 of its time value in the first half of its life
- It loses about 2/3 in the final half
- The last week sees dramatic decay

**Visual representation:**

```
Time Value
    |
    |****
    |    ****
    |        ****
    |            *****
    |                 *******
    |                        ************
    +---------------------------------------- Time
    90 days                            Expiration
```

---

## Implied Volatility (IV)

### What Is Implied Volatility?

**IV represents the market's expectation of future price movement.**

It's "implied" because it's derived from option prices—the market reveals its expectations through what people are willing to pay.

**Higher IV = Expectations of bigger moves = Higher option prices**
**Lower IV = Expectations of smaller moves = Lower option prices**

### How IV Affects Prices

**Example (Stock at $50, 30 days to expiration):**

| IV Level | $50 Call Price | $50 Put Price |
|----------|----------------|---------------|
| 20% | $1.50 | $1.50 |
| 30% | $2.25 | $2.25 |
| 40% | $3.00 | $3.00 |
| 50% | $3.75 | $3.75 |

**Doubling IV roughly doubles option prices** (for ATM options).

### IV vs. Historical Volatility

**Historical Volatility (HV):** How much the stock has actually moved in the past
**Implied Volatility (IV):** How much the market expects it to move in the future

**Relationship:**
- IV often exceeds HV (volatility risk premium)
- Before events (earnings), IV spikes
- After events, IV crushes

### IV Rank and IV Percentile

**IV Rank:** Where current IV stands relative to its 52-week range.
- IV Rank = (Current IV - 52wk Low IV) / (52wk High IV - 52wk Low IV)
- Range: 0-100%

**IV Percentile:** What percentage of days had lower IV than today.

**Example:**
- 52-week IV range: 20% to 60%
- Current IV: 30%
- IV Rank: (30-20)/(60-20) = 25%
- Meaning: IV is in the lower quarter of its range

### Using IV in Trading Decisions

**High IV (IV Rank > 50%):**
- Options are expensive
- Consider selling premium
- Expect IV to decrease (IV crush)

**Low IV (IV Rank < 30%):**
- Options are cheap
- Consider buying options
- Expect IV to increase

---

## The Black-Scholes Model

### Overview

The Black-Scholes model, developed in 1973, is the foundation of modern option pricing. It calculates theoretical option prices based on several inputs.

### Model Inputs

1. **Stock price (S)**
2. **Strike price (K)**
3. **Time to expiration (T)**
4. **Risk-free interest rate (r)**
5. **Volatility (σ)**
6. **Dividends (for dividend-paying stocks)**

### The Formula (Simplified Concept)

Without diving into calculus, Black-Scholes essentially calculates:
- The probability the option will be in-the-money at expiration
- The expected payoff if it is
- Discounts back to present value

### Limitations

**Black-Scholes assumes:**
- Constant volatility (not realistic)
- No early exercise (European-style)
- Efficient markets
- No transaction costs

**Reality:**
- Volatility changes constantly
- American options can exercise early
- Markets aren't perfectly efficient
- Costs exist

Despite limitations, it's the foundation that all option pricing builds upon.

---

## Volatility Smile and Skew

### The Volatility Smile

**Observation:** In reality, OTM options often trade at higher implied volatility than ATM options.

**Why:**
- Fat tails in return distributions
- Crash risk (OTM puts)
- Speculative demand (OTM calls)

### Volatility Skew

**In equity markets:** OTM puts typically have higher IV than OTM calls.

**Reason:** Investors pay more for downside protection (puts) because:
- Markets crash faster than they rally
- Fear of losses exceeds greed for gains
- Institutional hedging demand

**Example IV by strike (Stock at $100):**

| Strike | Call IV | Put IV |
|--------|---------|--------|
| $90 | 32% | 35% |
| $95 | 28% | 30% |
| $100 | 25% | 25% |
| $105 | 27% | 24% |
| $110 | 30% | 23% |

---

## Time Value Across Different Strikes

### Where Is Time Value Highest?

**ATM options have the most extrinsic value.**

| Moneyness | Intrinsic | Extrinsic | Total |
|-----------|-----------|-----------|-------|
| Deep ITM | High | Low | Mostly intrinsic |
| ITM | Medium | Medium | Mix |
| ATM | None | Highest | All extrinsic |
| OTM | None | Medium | All extrinsic |
| Deep OTM | None | Low | Low premium |

### Why ATM Has Most Time Value

**ATM options have:**
- Maximum uncertainty about expiring ITM or OTM
- Highest gamma (price sensitivity)
- Most time decay (theta)

**Deep ITM and OTM options:**
- Higher certainty of outcome
- Less uncertainty = less time value

---

## Put-Call Parity

### The Relationship

Put-call parity ensures calls and puts at the same strike are correctly priced relative to each other.

**Formula:**
Call + Cash = Put + Stock

Or rearranged:
Call - Put = Stock - Strike (present value)

### Why It Matters

**Arbitrage:** If put-call parity is violated, traders profit risk-free until prices align.

**For you:** Use it to verify option pricing makes sense.

### Example

Stock at $50, 30 days to expiration, $50 strike:
- $50 call = $2.50
- $50 put = $2.40

The prices should be very close for ATM options (slight difference for interest rates).

If $50 call = $3.00 but $50 put = $1.50, something is wrong—arbitrageurs would step in.

---

## Interest Rates and Dividends

### Interest Rate Effect

**Higher interest rates:**
- Increase call prices slightly
- Decrease put prices slightly

**Why:** Calls are like deferred stock purchases (benefit from interest on cash). Puts are like deferred sales (lose potential interest).

**Effect is small** except for long-dated options.

### Dividend Effect

**Expected dividends:**
- Decrease call prices
- Increase put prices

**Why:** Dividends reduce stock price on ex-date, hurting call holders and helping put holders.

**Important for:**
- Stocks with large dividends
- Options near dividend dates
- Understanding early exercise risk

---

## Practical Pricing Insights

### What Makes Options Expensive?

1. **High implied volatility** (biggest factor for extrinsic)
2. **More time to expiration**
3. **ATM strikes** (max extrinsic value)
4. **High-priced stocks** (absolute premium higher)
5. **Event expectations** (earnings, FDA decisions)

### What Makes Options Cheap?

1. **Low implied volatility**
2. **Near expiration**
3. **Deep ITM or OTM** (relative to ATM)
4. **After events** (IV crush)
5. **Low-volatility stocks**

### Reading Option Prices

**When evaluating an option ask:**
- How much am I paying for time value?
- Is IV high or low relative to history?
- How much of my premium is at risk to time decay?
- What probability does this price imply?

---

## IV Crush

### What Is IV Crush?

**The rapid decline in IV after an anticipated event** (usually earnings).

**Before earnings:**
- Uncertainty is high
- IV elevated
- Options expensive

**After earnings:**
- Uncertainty resolved
- IV drops sharply
- Options lose value even if stock moves as expected

### Example

**Before earnings:**
- Stock at $100
- 30% IV
- $100 call = $5.00

**After earnings (stock still at $100):**
- IV drops to 20%
- $100 call = $3.50

**Result:** Even though stock didn't move, you lost $1.50 per share on the call.

### Implications

**For option buyers:** You need the stock to move MORE than the market expects to profit.
**For option sellers:** IV crush is your friend—sell before events, profit from IV decline.

---

## Key Takeaways

- **Option price = Intrinsic value + Extrinsic value**
- **Intrinsic value is real** - It's what you'd get if you exercised now
- **Extrinsic value decays to zero** - Time is working against buyers
- **IV is the key variable** - High IV = expensive options, low IV = cheap options
- **Time decay accelerates** - Most decay happens in the final weeks
- **ATM options have most extrinsic value** - And most time decay
- **IV crush is real** - Expect IV to drop sharply after events
- **Put-call parity keeps pricing consistent** - Arbitrage ensures fair pricing

---

## What's Next

In [Chapter 31: The Greeks](31-the-greeks.md), we'll explore delta, gamma, theta, and vega—the risk metrics that help you understand how option prices change with various factors.

---

*Remember: Understanding how options are priced helps you identify good value and avoid overpaying. Always know what you're paying for time and volatility.*
