# Chapter 33: Spread Strategies

## Overview

Spreads combine multiple options to create defined-risk positions with specific profit/loss profiles. By buying and selling options simultaneously, you can reduce cost, limit risk, and express more nuanced market views. This chapter covers the most important spread strategies for intermediate options traders.

---

## What Is a Spread?

### Definition

**A spread involves buying and selling options of the same type (calls or puts) on the same underlying, with different strikes and/or expirations.**

### Why Use Spreads?

- **Defined risk:** Maximum loss is known at entry
- **Lower cost:** Selling offsets buying cost
- **Reduced margin requirements:** Less capital required
- **Tailored payoffs:** Match strategy to outlook
- **Less sensitive to volatility:** Vega partially cancels

---

## Vertical Spreads

### What Is a Vertical Spread?

**Same expiration, different strikes.** Called "vertical" because strikes appear vertically on an options chain.

### Bull Call Spread

**Construction:** Buy lower strike call + Sell higher strike call

**Outlook:** Moderately bullish

**Example:**
- Stock at $50
- Buy $50 call for $3.00
- Sell $55 call for $1.00
- Net debit: $2.00

**Maximum profit:** $5 (spread width) - $2 (cost) = $3.00
**Maximum loss:** $2.00 (debit paid)
**Break-even:** $50 + $2 = $52

**Profit/Loss at Expiration:**

| Stock Price | $50 Call Value | $55 Call Value | Net Value | P/L |
|-------------|----------------|----------------|-----------|-----|
| $48 | $0 | $0 | $0 | -$200 |
| $50 | $0 | $0 | $0 | -$200 |
| $52 | $2 | $0 | $2 | $0 |
| $55 | $5 | $0 | $5 | +$300 |
| $58 | $8 | $3 | $5 | +$300 |

**When to use:** Bullish but want defined risk and lower cost than buying calls outright.

### Bear Put Spread

**Construction:** Buy higher strike put + Sell lower strike put

**Outlook:** Moderately bearish

**Example:**
- Stock at $50
- Buy $50 put for $3.00
- Sell $45 put for $1.00
- Net debit: $2.00

**Maximum profit:** $5 (spread width) - $2 (cost) = $3.00
**Maximum loss:** $2.00 (debit paid)
**Break-even:** $50 - $2 = $48

**When to use:** Bearish with defined risk.

### Bull Put Spread (Credit Spread)

**Construction:** Sell higher strike put + Buy lower strike put

**Outlook:** Neutral to bullish

**Example:**
- Stock at $50
- Sell $48 put for $1.50
- Buy $45 put for $0.50
- Net credit: $1.00

**Maximum profit:** $1.00 (credit received)
**Maximum loss:** $3 (spread width) - $1 (credit) = $2.00
**Break-even:** $48 - $1 = $47

**When to use:** Expect stock to stay above strike or rise; collect premium.

### Bear Call Spread (Credit Spread)

**Construction:** Sell lower strike call + Buy higher strike call

**Outlook:** Neutral to bearish

**Example:**
- Stock at $50
- Sell $52 call for $1.50
- Buy $55 call for $0.60
- Net credit: $0.90

**Maximum profit:** $0.90 (credit received)
**Maximum loss:** $3 (spread width) - $0.90 (credit) = $2.10
**Break-even:** $52 + $0.90 = $52.90

**When to use:** Expect stock to stay below strike or fall; collect premium.

---

## Vertical Spread Summary

| Strategy | Construction | Debit/Credit | Max Profit | Max Loss | Outlook |
|----------|--------------|--------------|------------|----------|---------|
| Bull Call | Buy low call, Sell high call | Debit | Width - Debit | Debit | Bullish |
| Bear Put | Buy high put, Sell low put | Debit | Width - Debit | Debit | Bearish |
| Bull Put | Sell high put, Buy low put | Credit | Credit | Width - Credit | Bullish |
| Bear Call | Sell low call, Buy high call | Credit | Credit | Width - Credit | Bearish |

---

## Iron Condor

### What Is an Iron Condor?

**An iron condor combines a bull put spread and bear call spread.** You profit when the stock stays within a range.

### Construction

**Sell an OTM put spread + Sell an OTM call spread**

**Example (Stock at $100):**
- Sell $95 put for $1.00
- Buy $90 put for $0.40
- Sell $105 call for $1.00
- Buy $110 call for $0.40

**Net credit:** $1.00 + $1.00 - $0.40 - $0.40 = $1.20

### Profit/Loss Profile

**Maximum profit:** $1.20 (credit received)
**Maximum loss:** $5 (spread width) - $1.20 (credit) = $3.80
**Break-evens:** $95 - $1.20 = $93.80 and $105 + $1.20 = $106.20

**Profitable range:** Stock between $93.80 and $106.20 at expiration

### Iron Condor Diagram

```
Profit
   |
$120_________            ________
   |         \          /
   |          \        /
$0 |___________\______/__________ Stock Price
   |            \    /
   |             \  /
-$380____________\/_______________
              $90 $95  $105 $110
```

### When to Use Iron Condors

**Ideal conditions:**
- Expect low volatility, range-bound market
- High IV (expensive premiums to sell)
- Earnings/events have passed
- Want income with defined risk

**Avoid when:**
- Expecting breakout or trend
- IV is very low
- Major events upcoming

### Managing Iron Condors

**If profitable:**
- Close at 50% of max profit
- Don't be greedy waiting for full profit

**If challenged (price approaching short strike):**
- Close the tested side early
- Roll the untested side down for credit
- Accept partial loss vs maximum loss

---

## Iron Butterfly

### What Is an Iron Butterfly?

**Sell ATM put + Sell ATM call + Buy OTM put + Buy OTM call**

Like an iron condor but with the short strikes at the same price (ATM).

### Construction

**Example (Stock at $100):**
- Sell $100 put for $3.00
- Sell $100 call for $3.00
- Buy $95 put for $1.00
- Buy $105 call for $1.00

**Net credit:** $6.00 - $2.00 = $4.00

### Characteristics

**Maximum profit:** $4.00 (credit) - only if stock exactly at $100
**Maximum loss:** $5 (wing width) - $4 (credit) = $1.00
**Break-evens:** $96 and $104

### Iron Butterfly vs. Iron Condor

| Factor | Iron Condor | Iron Butterfly |
|--------|-------------|----------------|
| Max profit probability | Higher | Lower |
| Max profit amount | Lower | Higher |
| Width of profit zone | Wider | Narrower |
| Best for | Range-bound | Pinpoint prediction |

---

## Calendar Spreads (Time Spreads)

### What Is a Calendar Spread?

**Same strike, different expirations.** Buy the longer-dated option, sell the shorter-dated option.

### Construction

**Example (Stock at $50):**
- Sell $50 call expiring in 30 days for $2.00
- Buy $50 call expiring in 60 days for $3.50
- Net debit: $1.50

### How It Works

**Goal:** Short-term option decays faster than long-term option.

**At front-month expiration:**
- If stock at $50: short call expires worthless, long call retains value
- Profit from time decay differential

### Profit/Loss Profile

**Maximum profit:** At the strike price at front-month expiration
**Maximum loss:** Debit paid (if stock moves far from strike)
**Break-evens:** Depend on IV and time

### When to Use Calendar Spreads

- Expect stock to trade near strike through near-term expiration
- Expect IV to increase
- Want to position for future events while collecting near-term decay

---

## Diagonal Spreads

### What Is a Diagonal Spread?

**Different strikes AND different expirations.** Combines aspects of vertical and calendar spreads.

### Construction (Poor Man's Covered Call)

**Buy long-dated ITM call + Sell short-dated OTM call**

**Example:**
- Buy 90-day $45 call (deep ITM, 0.80 delta) for $7.00
- Sell 30-day $52 call for $1.00
- Net debit: $6.00

### How It Works

**Long call acts like stock:** Moves with underlying
**Short call generates income:** Premium collected, caps upside

**This is essentially a covered call without owning shares** (hence "poor man's covered call").

### Advantages

- Less capital than owning shares
- Defined maximum loss
- Can generate monthly income on the long option

### Risks

- Long option has time decay (though less than short)
- Requires management and rolling
- More complex than single-leg strategies

---

## Straddles and Strangles

### Long Straddle

**Buy ATM call + Buy ATM put (same strike, same expiration)**

**Example (Stock at $50):**
- Buy $50 call for $3.00
- Buy $50 put for $3.00
- Total cost: $6.00

**Profit if:** Stock moves more than $6 in either direction
**Break-evens:** $44 and $56
**Max loss:** $6.00 (if stock exactly at $50)

**When to use:** Expect big move, unsure of direction. IV is low.

### Long Strangle

**Buy OTM call + Buy OTM put (different strikes, same expiration)**

**Example (Stock at $50):**
- Buy $55 call for $1.00
- Buy $45 put for $1.00
- Total cost: $2.00

**Profit if:** Stock moves beyond $57 or below $43
**Break-evens:** $43 and $57
**Max loss:** $2.00 (if stock between $45-55)

**When to use:** Same as straddle but cheaper, needs bigger move.

### Short Straddle/Strangle

**Sell ATM call + Sell ATM put (straddle)**
**Sell OTM call + Sell OTM put (strangle)**

**Profit from:** Time decay and stock staying in range
**Risk:** Unlimited in both directions

**Only for experienced traders with strict risk management.**

---

## Spread Selection Guide

### Based on Market Outlook

| Outlook | Strategy |
|---------|----------|
| Bullish, defined risk | Bull call spread |
| Bearish, defined risk | Bear put spread |
| Neutral, high IV | Iron condor, Short strangle |
| Neutral, low IV | Long straddle (if expecting IV rise) |
| Bullish, income | Bull put spread |
| Bearish, income | Bear call spread |
| Range-bound, precise | Iron butterfly |

### Based on Risk Tolerance

**Low risk tolerance:**
- Debit spreads (bull call, bear put)
- Max loss is defined at entry

**Moderate risk tolerance:**
- Credit spreads (bull put, bear call)
- Iron condors
- Defined but potentially larger losses

**Higher risk tolerance:**
- Naked options (not recommended for most)
- Ratio spreads

---

## Risk Management for Spreads

### Position Sizing

**Max loss per trade:** 1-5% of account

**Example:**
- $50,000 account
- 2% max loss = $1,000
- Iron condor with $3.80 max loss
- Maximum contracts: $1,000 / $380 = 2-3 contracts

### Exit Rules

**Profit targets:**
- Close at 50% of max profit for credit spreads
- Reduces risk and frees capital

**Loss limits:**
- Close at 2x credit received
- Or when short strike is breached

**Time-based:**
- Close positions 1-2 weeks before expiration
- Gamma risk increases near expiration

---

## Key Takeaways

- **Spreads define risk** - Maximum loss known at entry
- **Debit spreads: pay premium, profit from movement**
- **Credit spreads: collect premium, profit from no movement or favorable movement**
- **Iron condors profit from range-bound markets** and high IV
- **Calendar spreads profit from time decay differential**
- **Match strategy to outlook** - Bullish, bearish, or neutral
- **Position size based on max loss** - Not margin requirement
- **Close winners early** - 50% of max profit is often the sweet spot
- **Manage losers before max loss** - Don't wait until expiration

---

## What's Next

In [Chapter 34: LEAPS](34-leaps.md), we'll explore long-term options (LEAPS) and how they can be used for stock replacement, leverage, and long-term positioning strategies.

---

*Remember: Spreads are the toolkit for sophisticated options trading. Master them before moving to more complex multi-leg strategies.*
