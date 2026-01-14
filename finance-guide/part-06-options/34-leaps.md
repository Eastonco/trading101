# Chapter 34: LEAPS - Long-Term Options

## Overview

LEAPS (Long-Term Equity Anticipation Securities) are options with expiration dates of one year or more into the future. They offer unique opportunities for long-term investors: stock replacement with less capital, leveraged long-term positions, and hedging strategies that last beyond typical options timeframes.

---

## What Are LEAPS?

### Definition

**LEAPS are options contracts with more than one year until expiration.**

- Standard options: Days to months
- LEAPS: 1-3 years

### Key Characteristics

**Compared to short-term options:**
- Much slower time decay initially
- Higher absolute premium (more time value)
- Lower gamma (less sensitive to short-term moves)
- Higher vega (more sensitive to IV changes)
- More time for thesis to play out

### Availability

**LEAPS are available on:**
- Most large-cap stocks
- Major ETFs (SPY, QQQ, etc.)
- Typically added in September for next year's January

**Expiration:** Usually January (third Friday)

---

## LEAPS vs. Short-Term Options

### Time Decay Comparison

| Days to Expiration | Daily Theta (ATM) |
|-------------------|-------------------|
| 730 (2 years) | -$0.01 |
| 365 (1 year) | -$0.02 |
| 180 (6 months) | -$0.04 |
| 90 (3 months) | -$0.06 |
| 30 (1 month) | -$0.10 |
| 7 (1 week) | -$0.30 |

**LEAPS lose time value slowly**, making them suitable for longer holding periods.

### The Greeks for LEAPS

| Greek | LEAPS Characteristic |
|-------|---------------------|
| Delta | Similar to shorter-term at same strike |
| Gamma | Lower (price less sensitive to small moves) |
| Theta | Much lower (slow decay) |
| Vega | Higher (more sensitive to IV changes) |

---

## Stock Replacement Strategy

### The Concept

**Use LEAPS calls instead of buying stock to gain similar exposure with less capital.**

### How It Works

**Buy a deep ITM LEAPS call (0.80+ delta):**
- Acts like owning stock
- Costs fraction of stock price
- Leverages your capital

### Example: Stock Replacement

**Traditional stock purchase:**
- Buy 100 shares of XYZ at $100 = $10,000

**LEAPS replacement:**
- Buy 1 XYZ Jan 2027 $70 call (2 years out)
- Delta: 0.85
- Price: $35
- Cost: $3,500

**Capital comparison:**
- Stock: $10,000
- LEAPS: $3,500
- Capital freed: $6,500 (65%)

### Outcome Scenarios

**Stock rises to $120 (+20%):**
- Stock gain: $2,000 (20% return)
- LEAPS gain: ~$17 × 100 = $1,700 (49% return)
- Dollar gain similar, percentage return higher

**Stock stays at $100:**
- Stock: No gain/loss
- LEAPS: Loses ~$5-8 in time value (~15-23% loss)

**Stock falls to $80 (-20%):**
- Stock loss: -$2,000 (20% loss)
- LEAPS loss: ~-$1,800 (51% loss)
- Dollar loss similar, but $3,500 vs $10,000 at risk

### Key Considerations

**Advantages:**
- Less capital required
- Defined risk (can't lose more than premium)
- Frees capital for other investments
- Leveraged returns on capital deployed

**Disadvantages:**
- Time decay (stock doesn't decay)
- No dividends
- Must actively manage (roll or close before expiration)
- Limited time horizon

---

## Poor Man's Covered Call (PMCC)

### The Strategy

**Buy LEAPS call + Sell short-term OTM calls against it**

This replicates a covered call without owning stock.

### Setup

**Example:**
- Buy Jan 2027 $70 call (0.85 delta) for $35
- Sell monthly $105 call for $1.50

### How It Works

**Monthly income:** Sell calls against your LEAPS position
**If call expires worthless:** Keep premium, sell another call
**If call assigned:** Roll or close the LEAPS position

### Returns Comparison

**Traditional covered call (100 shares at $100):**
- Capital: $10,000
- Monthly premium: $1.50 × 100 = $150
- Return: 1.5%/month

**PMCC:**
- Capital: $3,500 (LEAPS cost)
- Monthly premium: $150
- Return: 4.3%/month on capital deployed

### Risks

- LEAPS has time decay (cost)
- If stock drops significantly, LEAPS loses value
- Short call can go ITM, creating management complexity
- More complex than traditional covered call

---

## Long-Term Portfolio Hedging

### Protective LEAPS Puts

**Buy LEAPS puts to protect portfolio for extended period.**

### Example

**Portfolio:** $100,000 in SPY (at $450)
**Protection:** Buy 2 SPY Jan 2027 $400 puts

**Cost:** ~$3,000 per contract × 2 = $6,000
**Protection:** If SPY falls below $400, puts offset losses

### Cost of Protection

**Protection cost as % of portfolio:**
- $6,000 / $100,000 = 6% over 2 years
- ~3% per year for downside protection

### When to Use

- Long-term holdings you don't want to sell
- Concentrated stock positions (company stock, founders)
- Retirement accounts approaching distribution

### LEAPS Put Collar

**Own stock + Buy LEAPS put + Sell LEAPS call**

**Example:**
- Own 100 shares at $100
- Buy Jan 2027 $85 put for $8
- Sell Jan 2027 $120 call for $6

**Net cost:** $2 per share for 2 years of protection
**Protection:** Guaranteed sale at $85 minimum
**Cap:** Upside limited to $120

---

## LEAPS as Speculation

### Leveraged Long-Term Bets

**Using LEAPS for directional speculation with defined risk.**

### ATM LEAPS Calls

**Example:**
- Stock at $50
- Buy Jan 2027 $50 call for $8

**Scenarios after 2 years:**

| Stock Price | Option Value | Return |
|-------------|--------------|--------|
| $40 | ~$0 | -100% |
| $50 | ~$3 (time value) | -62% |
| $60 | ~$12 | +50% |
| $70 | ~$21 | +163% |
| $80 | ~$31 | +288% |

**High leverage:** Stock up 60% = LEAPS up 288%
**High risk:** Stock down 20% = LEAPS possibly -100%

### OTM LEAPS (Higher Leverage)

**Example:**
- Stock at $50
- Buy Jan 2027 $60 call for $4

**Even more leverage but lower probability of profit.**

### Risk Considerations

- Can lose 100% of premium
- Needs significant move to profit
- Time decay works against you
- IV changes affect value

---

## Rolling LEAPS

### Why Roll?

**As LEAPS approach 6-12 months to expiration:**
- Time decay accelerates
- Gamma increases (more short-term volatility)
- Time to roll to a new LEAPS

### How to Roll

**Close existing LEAPS and open new longer-dated position.**

**Example:**
- Own Jan 2027 $70 call (now 9 months out)
- Sell for $33
- Buy Jan 2029 $75 call for $35
- Net cost: $2 to extend and possibly adjust strike

### When to Roll

**Timing considerations:**
- Roll when 6-12 months remain
- Roll when IV is favorable
- Roll to same or higher strike if stock has risen

### Maintaining the Position

**Track:**
- Original entry cost
- Roll costs (debits/credits)
- Total capital invested in the strategy
- Comparable stock performance

---

## Tax Considerations

### Long-Term Capital Gains

**LEAPS held > 1 year qualify for long-term capital gains rates** if profitable.

- Short-term: Taxed as ordinary income (up to 37%)
- Long-term: Taxed at 0%, 15%, or 20%

### Timing Strategy

**Buy LEAPS > 1 year from expiration:**
- Hold > 12 months for LTCG treatment
- Still have time value remaining at sale

**Example:**
- Buy 24-month LEAPS
- Sell after 13 months
- Qualifies for LTCG rates
- Still 11 months of time value left

### Losses

**LEAPS that expire worthless:**
- Capital loss
- Can offset gains
- $3,000 per year against ordinary income if excess

---

## LEAPS Strategy Selection

### Conservative: Stock Replacement

**Deep ITM calls (0.80+ delta):**
- Closest to stock behavior
- Highest capital efficiency for exposure
- Lower percentage leverage

**Best for:** Investors who want exposure with defined risk

### Moderate: Poor Man's Covered Call

**ITM LEAPS + Short calls:**
- Income generation on leveraged position
- Requires active management
- Higher return on capital

**Best for:** Active traders comfortable with management

### Aggressive: ATM/OTM LEAPS

**ATM or OTM calls for speculation:**
- Maximum leverage
- Lower probability of profit
- Can lose 100% of investment

**Best for:** Speculators with high risk tolerance

---

## Example: 2-Year LEAPS Investment

### Setup (January 2025)

**Stock:** ABC trading at $80
**Outlook:** Bullish over 2 years
**Strategy:** Stock replacement with PMCC

**Initial position:**
- Buy Jan 2027 $60 call for $25 (0.82 delta)
- Cost: $2,500 per contract (vs $8,000 for shares)

### Monthly Income (Year 1)

**Sell monthly OTM calls:**
- Average premium: $1.00/month
- Annual income: $1,200

### Results After 2 Years

**Scenario: Stock at $110 (+37.5%)**
- LEAPS value: ~$51 (at expiration, intrinsic only)
- Gain: $51 - $25 = $26 ($2,600)
- Plus monthly income: ~$2,400
- Total gain: $5,000 on $2,500 invested = 200%
- Stock gain would have been: $3,000 on $8,000 = 37.5%

**Scenario: Stock at $80 (flat)**
- LEAPS value: ~$20 (at expiration)
- Loss: $25 - $20 = $5 ($500)
- Plus monthly income: ~$2,400
- Total gain: $1,900 on $2,500 = 76%
- Stock gain: $0

**Scenario: Stock at $55 (-31%)**
- LEAPS value: $0 (expires worthless)
- Loss: $2,500 (100% of LEAPS)
- Plus monthly income: ~$1,500 (less as stock fell)
- Net loss: -$1,000
- Stock loss: -$2,500 (but still own shares)

---

## Key Takeaways

- **LEAPS have >1 year to expiration** - Much slower time decay than standard options
- **Stock replacement uses deep ITM LEAPS** - Similar exposure, less capital
- **PMCC generates income on LEAPS positions** - Leveraged covered call strategy
- **LEAPS puts provide long-term hedging** - Protect portfolios for years
- **Roll LEAPS when 6-12 months remain** - Avoid accelerating time decay
- **LEAPS can qualify for long-term capital gains** - Hold > 1 year
- **Higher vega means IV matters more** - Watch volatility levels
- **LEAPS require active management** - Not "set and forget" like stock

---

## What's Next

In [Chapter 35: Options Risk Management](35-options-risk-management.md), we'll tie together everything we've learned about options with comprehensive risk management strategies for options traders.

---

*Remember: LEAPS offer the power of options with the timeframe of investments. Use them wisely to leverage your capital and manage risk over longer horizons.*
