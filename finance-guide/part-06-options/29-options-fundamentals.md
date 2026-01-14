# Chapter 29: Options Fundamentals

## Overview

Options are financial contracts that give the buyer the right—but not the obligation—to buy or sell an underlying asset at a specific price before a certain date. They offer unique capabilities: leverage, hedging, income generation, and speculation. Understanding options fundamentals is essential before exploring strategies.

---

## What Is an Option?

### The Basic Concept

**An option is a contract between two parties:**
- **Buyer:** Pays premium, receives the right to act
- **Seller (Writer):** Receives premium, takes on the obligation

**Key distinction:** The buyer has a choice. The seller must comply if the buyer chooses to exercise.

### Call Options

**A call option gives the buyer the right to BUY the underlying stock at the strike price.**

**Example:**
- Stock ABC trades at $50
- You buy the $55 call option for $2
- You have the right to buy ABC at $55 anytime before expiration
- If ABC rises to $65, you can buy at $55 (saving $10, minus $2 premium = $8 profit)
- If ABC stays below $55, you lose your $2 premium

**Who buys calls:** Bullish traders expecting price to rise
**Who sells calls:** Traders willing to sell stock at strike price for premium

### Put Options

**A put option gives the buyer the right to SELL the underlying stock at the strike price.**

**Example:**
- Stock ABC trades at $50
- You buy the $45 put option for $2
- You have the right to sell ABC at $45 anytime before expiration
- If ABC falls to $35, you can sell at $45 (gaining $10, minus $2 premium = $8 profit)
- If ABC stays above $45, you lose your $2 premium

**Who buys puts:** Bearish traders expecting price to fall
**Who sells puts:** Traders willing to buy stock at strike price for premium

---

## Key Option Terms

### Strike Price

**Definition:** The price at which the option buyer can buy (call) or sell (put) the underlying.

**Example strikes for $50 stock:**
- $45 strike (in-the-money for calls)
- $50 strike (at-the-money)
- $55 strike (out-of-the-money for calls)

### Expiration Date

**Definition:** The last day the option can be exercised.

**Common expirations:**
- Weekly (Friday)
- Monthly (third Friday)
- Quarterly
- LEAPS (1-2+ years out)

**After expiration:** Options expire worthless or are exercised automatically.

### Premium

**Definition:** The price paid to buy an option.

**Components:**
- Intrinsic value (real value if exercised now)
- Extrinsic value (time value + volatility premium)

### Contract Multiplier

**Standard:** 1 option contract = 100 shares

**Example:**
- Option premium: $2.00
- Cost to buy 1 contract: $2.00 × 100 = $200
- 10 contracts: $2,000

---

## In-the-Money, At-the-Money, Out-of-the-Money

### Definitions

**For Calls:**
- **In-the-money (ITM):** Stock price > Strike price
- **At-the-money (ATM):** Stock price ≈ Strike price
- **Out-of-the-money (OTM):** Stock price < Strike price

**For Puts:**
- **In-the-money (ITM):** Stock price < Strike price
- **At-the-money (ATM):** Stock price ≈ Strike price
- **Out-of-the-money (OTM):** Stock price > Strike price

### Example (Stock at $50)

| Strike | Call Status | Put Status |
|--------|-------------|------------|
| $45 | ITM by $5 | OTM by $5 |
| $50 | ATM | ATM |
| $55 | OTM by $5 | ITM by $5 |

### Why It Matters

**ITM options:**
- Have intrinsic value
- More expensive
- Higher delta (move more with stock)
- Lower percentage return, higher probability of profit

**OTM options:**
- Only extrinsic value
- Cheaper
- Lower delta
- Higher percentage return potential, lower probability

---

## Intrinsic and Extrinsic Value

### Intrinsic Value

**Definition:** The value if the option were exercised right now.

**Calculation:**
- Call: Stock Price - Strike Price (if positive)
- Put: Strike Price - Stock Price (if positive)
- If negative: Intrinsic value = $0

**Example (Stock at $55):**
- $50 call intrinsic value: $55 - $50 = $5
- $60 call intrinsic value: $0 (out-of-the-money)
- $60 put intrinsic value: $60 - $55 = $5
- $50 put intrinsic value: $0 (out-of-the-money)

### Extrinsic Value (Time Value)

**Definition:** Premium above intrinsic value.

**Formula:** Extrinsic Value = Option Price - Intrinsic Value

**Example:**
- $50 call trading at $7
- Stock at $55
- Intrinsic value: $5
- Extrinsic value: $7 - $5 = $2

**Extrinsic value factors:**
- Time until expiration (more time = more value)
- Implied volatility (higher IV = more value)
- Interest rates and dividends (minor factors)

### The Decay of Extrinsic Value

**Key concept:** Extrinsic value decays to zero by expiration.

At expiration:
- Option value = intrinsic value only
- ITM options have value
- OTM options expire worthless

---

## The Options Chain

### Reading an Options Chain

**Components:**
- Strike prices (center column)
- Calls (left side)
- Puts (right side)
- Bid/Ask prices
- Volume and open interest
- Implied volatility
- Greeks

### Sample Options Chain (Stock at $50)

| Calls ||| Strike ||| Puts |
|-------|---|---|--------|---|---|-------|
| Bid | Ask | Vol | | Bid | Ask | Vol |
| 6.50 | 6.70 | 245 | $45 | 0.95 | 1.05 | 180 |
| 3.20 | 3.40 | 890 | $50 | 2.90 | 3.10 | 750 |
| 1.20 | 1.35 | 1,200 | $55 | 5.80 | 6.00 | 320 |

### Understanding Volume and Open Interest

**Volume:** Number of contracts traded today
**Open Interest:** Total outstanding contracts

**Significance:**
- High volume/OI = liquid, tight spreads
- Low volume/OI = illiquid, wide spreads, harder to exit
- Trade liquid options (bid-ask spread matters)

---

## Buying vs. Selling Options

### Buying Options (Long)

**You pay premium for:**
- Right to exercise
- Limited risk (max loss = premium paid)
- Unlimited profit potential (calls) or substantial (puts)
- Time working against you

**Best when:**
- You expect significant price movement
- Want defined risk
- Anticipate volatility increase

### Selling Options (Short)

**You receive premium for:**
- Obligation if exercised against
- Unlimited risk potential (naked calls) or significant (puts)
- Limited profit potential (premium received)
- Time working for you

**Best when:**
- You expect sideways or moderate movement
- Want to collect income
- Anticipate volatility decrease

### Risk Comparison

| Factor | Long Options | Short Options |
|--------|--------------|---------------|
| Max loss | Premium paid | Unlimited (calls) or strike price (puts) |
| Max profit | Unlimited (calls) | Premium received |
| Time decay | Enemy | Friend |
| Probability | Lower | Higher |

---

## Exercise and Assignment

### Exercise

**Definition:** Option buyer uses their right to buy/sell the underlying.

**Types:**
- **American-style:** Can exercise anytime before expiration (most stock options)
- **European-style:** Can only exercise at expiration (index options)

**When to exercise:**
- Usually only at expiration
- Early exercise rare (gives up extrinsic value)
- Exception: Deep ITM calls before dividend

### Assignment

**Definition:** Option seller is obligated to fulfill the contract when buyer exercises.

**For call sellers:** Must sell stock at strike price
**For put sellers:** Must buy stock at strike price

**Assignment risk:**
- Higher as option goes deeper ITM
- Higher near expiration
- Can happen anytime (American-style)

### Automatic Exercise

**At expiration:** ITM options are automatically exercised if:
- $0.01 or more ITM
- Unless you instruct broker otherwise

**Always monitor positions near expiration.**

---

## Options Leverage

### The Power of Leverage

**Example comparison (stock at $100):**

**Buying 100 shares:**
- Cost: $10,000
- Stock rises to $110
- Profit: $1,000 (10% return)

**Buying 1 call contract ($100 strike, $5 premium):**
- Cost: $500
- Stock rises to $110
- Option value: ~$10
- Profit: $500 (100% return)

**Same $1,000 move, 10x the percentage return.**

### The Risk of Leverage

**If stock stays at $100:**
- Shares: No gain, no loss
- Call option: -$500 (total loss of premium)

**If stock falls to $90:**
- Shares: -$1,000 loss
- Call option: -$500 (but only premium was at risk)

### Leverage Works Both Ways

Options amplify returns—both positive and negative. The same leverage that can create 100% gains can create 100% losses much more easily than stocks.

---

## Why Trade Options?

### Speculation

**Directional bets with defined risk:**
- Buy calls for bullish bets
- Buy puts for bearish bets
- Less capital than buying/shorting stock
- Maximum loss is premium paid

### Hedging

**Protecting existing positions:**
- Buy puts to protect stock holdings
- Create "insurance" against drops
- Collar strategies limit both up and downside

### Income Generation

**Selling premium:**
- Covered calls on stock you own
- Cash-secured puts on stock you'd buy
- Collect premiums while waiting

### Flexibility

**Options offer unique payoff structures:**
- Profit in any direction
- Profit in no direction (sideways)
- Define exact risk/reward
- Create complex probability profiles

---

## Risks of Options Trading

### Total Loss of Premium

**Buying options:** You can lose 100% of your investment if the option expires worthless.

### Time Decay

**Every day:** Options lose value due to time decay. Holding options is fighting against the clock.

### Complexity

**Options require understanding:**
- Greeks
- Volatility dynamics
- Exercise/assignment mechanics
- Strategy construction

**Mistakes can be expensive.**

### Leverage Cuts Both Ways

**Amplified losses:** The same leverage that creates big wins creates big losses.

### Liquidity Risk

**Illiquid options:**
- Wide bid-ask spreads
- Difficulty exiting positions
- Slippage costs

### Assignment Risk

**Selling options:** You can be assigned at any time, forced to buy or sell stock.

---

## Getting Started with Options

### Requirements

**Brokerage approval levels:**
- Level 1: Covered calls, protective puts
- Level 2: Long calls and puts
- Level 3: Spreads
- Level 4: Naked options (highest risk)

**You must apply for options trading and may need:**
- Minimum account balance
- Trading experience
- Risk acknowledgment

### Starting Recommendations

1. **Learn thoroughly before trading real money**
2. **Paper trade first** (at least 50 trades)
3. **Start with defined-risk strategies** (long options, spreads)
4. **Trade liquid options** (tight bid-ask spreads)
5. **Small position sizes** (never more than 2-5% of account per trade)
6. **Understand the Greeks** (next chapter)

### Common Beginner Mistakes

- Buying short-dated OTM options (low probability)
- Ignoring time decay
- Holding losing positions too long
- Oversizing positions
- Not understanding assignment
- Trading illiquid options

---

## Key Takeaways

- **Calls = right to buy, Puts = right to sell** at the strike price
- **Buyers pay premium for rights** - sellers receive premium for obligations
- **ITM options have intrinsic value** - OTM options are pure time value
- **Time decay erodes option value** - buyers fight it, sellers collect it
- **Options provide leverage** - amplifies gains AND losses
- **1 contract = 100 shares** - always think in 100-share lots
- **Options have defined risk for buyers** - max loss is premium paid
- **Selling options has significant risk** - unlimited for naked calls

---

## What's Next

In [Chapter 30: How Options Are Priced](30-options-pricing.md), we'll dive deeper into what determines option prices, including intrinsic value, time value, and the critical concept of implied volatility.

---

*Remember: Options are powerful tools, but they require education and respect. Take the time to understand them fully before risking capital.*
