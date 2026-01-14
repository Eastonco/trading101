# Chapter 40: Futures Contracts Explained

## Overview

Futures contracts are agreements to buy or sell an asset at a predetermined price on a specific future date. Originally developed for agricultural hedging, futures now cover everything from stock indices to oil to currencies. They offer leverage, liquidity, and unique market access—but also carry substantial risks that make them unsuitable for most retail investors.

---

## What Is a Futures Contract?

### Definition

**A futures contract is a standardized agreement to buy or sell a specific quantity of an asset at a predetermined price on a set future date.**

### Key Characteristics

**Standardized:** Exchange-traded with fixed specifications
**Obligatory:** Unlike options, both parties MUST fulfill the contract
**Leveraged:** Control large value with small capital (margin)
**Marked-to-market:** Profits and losses settled daily
**Expiration:** Each contract has a specific end date

### Futures vs. Options

| Feature | Futures | Options |
|---------|---------|---------|
| Obligation | Both parties obligated | Only seller obligated |
| Premium | No premium; margin only | Buyer pays premium |
| Risk | Unlimited both sides | Buyer: premium only |
| Settlement | Typically daily MTM | At exercise/expiration |
| Leverage | Very high | Variable |

---

## How Futures Work

### The Basic Mechanism

**Example: Corn Futures**

**Farmer (Seller):**
- Has corn to sell at harvest (September)
- Worried prices might fall
- Sells September corn futures at $5.00/bushel
- **Locked in price:** Will receive $5.00 regardless of market

**Food Company (Buyer):**
- Needs corn for production
- Worried prices might rise
- Buys September corn futures at $5.00/bushel
- **Locked in price:** Will pay $5.00 regardless of market

### At Expiration

**If market price is $4.50:**
- Farmer sells at $5.00 (better than market)
- Food company pays $5.00 (worse than market)
- Both got certainty, which was their goal

**If market price is $5.50:**
- Farmer sells at $5.00 (worse than market)
- Food company pays $5.00 (better than market)
- Both got certainty

---

## Contract Specifications

### Understanding Contract Details

Every futures contract specifies:
- **Underlying asset:** What's being traded
- **Contract size:** Quantity per contract
- **Tick size:** Minimum price movement
- **Tick value:** Dollar value of one tick
- **Expiration months:** When contracts settle
- **Settlement:** Physical delivery or cash settlement

### Example: E-mini S&P 500 Futures

| Specification | Value |
|---------------|-------|
| Symbol | ES |
| Underlying | S&P 500 Index |
| Contract size | $50 × Index |
| Tick size | 0.25 points |
| Tick value | $12.50 |
| Trading hours | Nearly 24 hours |
| Settlement | Cash settled |

**At S&P 500 = 4,500:**
- Contract value: $50 × 4,500 = $225,000
- One tick move (0.25 points): $12.50

### Example: Crude Oil Futures

| Specification | Value |
|---------------|-------|
| Symbol | CL |
| Underlying | Light Sweet Crude Oil |
| Contract size | 1,000 barrels |
| Tick size | $0.01/barrel |
| Tick value | $10 |
| Settlement | Physical delivery |

**At oil = $75/barrel:**
- Contract value: 1,000 × $75 = $75,000
- One cent move: $10

---

## Margin in Futures

### How Margin Works

**Futures margin is NOT borrowing money.** It's a performance bond/good faith deposit.

### Margin Types

**Initial margin:** Amount required to open a position
**Maintenance margin:** Minimum amount to keep position open
**Variation margin:** Daily settlement of gains/losses

### Example

**E-mini S&P 500:**
- Contract value: ~$225,000
- Initial margin: ~$12,000 (varies)
- Maintenance margin: ~$11,000

**Leverage:** $225,000 / $12,000 = ~19:1

### Daily Settlement (Mark-to-Market)

**End of each day:**
- Your position is "marked" to the current price
- Gains credited to your account
- Losses debited from your account
- If account falls below maintenance margin: **margin call**

### Margin Call Example

**Day 1:**
- Buy 1 ES contract at 4,500
- Initial margin: $12,000
- Account balance: $15,000

**Day 2:**
- ES falls to 4,480 (down 20 points)
- Loss: 20 × $50 = $1,000
- Account balance: $14,000 (still above maintenance)

**Day 3:**
- ES falls to 4,420 (down 60 more points)
- Loss: 60 × $50 = $3,000
- Account balance: $11,000 (at maintenance)

**Day 4:**
- ES falls to 4,400 (down 20 more points)
- Loss: $1,000
- Account balance: $10,000 (below maintenance)
- **Margin call:** Must deposit funds or position liquidated

---

## Futures Markets

### Major Exchanges

**CME Group (US):**
- Chicago Mercantile Exchange (CME)
- Chicago Board of Trade (CBOT)
- New York Mercantile Exchange (NYMEX)
- Products: Indices, currencies, commodities, interest rates

**Intercontinental Exchange (ICE):**
- Energy, agriculture, financials
- Brent crude oil benchmark

### Trading Hours

**Nearly 24-hour markets:**
- E-mini S&P 500: Sunday 6pm - Friday 5pm ET (with breaks)
- Crude oil: Similar hours
- Allows reaction to global news anytime

### Liquidity

**Major contracts are highly liquid:**
- E-mini S&P 500: Millions of contracts daily
- Crude oil: Hundreds of thousands daily
- Tight bid-ask spreads

---

## Settlement Methods

### Physical Delivery

**The actual commodity is delivered:**
- Corn: Actual bushels of corn
- Crude oil: Actual barrels of oil
- Gold: Actual gold bars

**Most speculators exit before delivery** to avoid taking possession.

### Cash Settlement

**Cash difference is exchanged:**
- Stock index futures: Cash based on index value
- No physical delivery possible (can't deliver "the S&P 500")

**Example:**
- Buy ES at 4,500
- At expiration, S&P 500 = 4,550
- Receive: 50 × $50 = $2,500 (profit)

---

## Types of Futures Contracts

### Financial Futures

**Stock Index Futures:**
- E-mini S&P 500 (ES)
- E-mini Nasdaq-100 (NQ)
- E-mini Dow (YM)
- Russell 2000 (RTY)

**Interest Rate Futures:**
- Treasury bonds (ZB)
- Treasury notes (ZN)
- Eurodollars (GE)

**Currency Futures:**
- Euro (6E)
- Japanese Yen (6J)
- British Pound (6B)

### Commodity Futures

**Energy:**
- Crude Oil (CL)
- Natural Gas (NG)
- Heating Oil (HO)
- Gasoline (RB)

**Metals:**
- Gold (GC)
- Silver (SI)
- Copper (HG)
- Platinum (PL)

**Agriculture:**
- Corn (ZC)
- Wheat (ZW)
- Soybeans (ZS)
- Coffee (KC)
- Sugar (SB)

### Micro and Mini Contracts

**For smaller traders:**
- Micro E-mini S&P 500 (MES): 1/10th size of ES
- Micro Gold (MGC): 1/10th size of GC
- Lower margin requirements
- Lower risk per contract

---

## Who Trades Futures?

### Hedgers

**Commercial participants managing business risk:**
- Farmers hedging crop prices
- Airlines hedging fuel costs
- Companies hedging currency exposure
- Portfolio managers hedging market risk

### Speculators

**Traders seeking profit from price changes:**
- Institutional traders
- Proprietary trading firms
- Retail traders (small percentage)

### Arbitrageurs

**Exploiting price discrepancies:**
- Between futures and spot prices
- Between related markets
- Generally keeps markets efficient

---

## Risks of Futures Trading

### Leverage Risk

**Small moves = Large gains or losses**

**Example:**
- $12,000 margin controls $225,000 position
- 1% market move = $2,250
- That's 19% of your margin

### Margin Call Risk

**You can lose more than your initial deposit:**
- Position can move against you overnight
- Gap opens can exceed margin
- You may owe money beyond your deposit

### Volatility Risk

**Markets can move quickly:**
- Overnight news
- Economic reports
- Geopolitical events
- Flash crashes

### Unlimited Loss Potential

**Unlike buying options:**
- Long futures: Theoretically unlimited loss (price to infinity)
- Short futures: Theoretically unlimited loss (price to zero)
- No cap on how much you can lose

---

## Futures Are Not for Most People

### Who Should Avoid Futures

**Most retail investors should not trade futures:**
- Leverage is dangerous
- Requires constant monitoring
- Complex mechanics
- Can lose more than invested
- 24-hour markets challenging

### If You're Still Interested

**Before trading futures:**
1. Paper trade for months (at least 6)
2. Fully understand margin mechanics
3. Start with micro contracts only
4. Never use more than 2-3x leverage
5. Have strict risk management rules
6. Accept you'll likely lose money learning

---

## Key Takeaways

- **Futures are obligations, not rights** - Both parties must perform
- **Leverage is extremely high** - Control $225,000 with $12,000
- **Daily settlement (mark-to-market)** - Gains/losses settled daily
- **Margin calls can force liquidation** - Or require additional deposits
- **Loss can exceed deposit** - Unlike options, no maximum loss for buyers
- **Nearly 24-hour markets** - Global events affect prices anytime
- **Most retail traders lose money** - Due to leverage and complexity
- **Suitable for hedgers, not most speculators** - Professional tool, professional risks

---

## What's Next

In [Chapter 41: Commodities Investing](41-commodities.md), we'll explore how to gain exposure to commodities—including direct futures, ETFs, and other methods—along with the unique characteristics of commodity markets.

---

*Remember: Futures are powerful tools designed for hedging business risk. As speculative instruments, they've ruined many amateur traders. Approach with extreme caution or not at all.*
