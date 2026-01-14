# Chapter 35: Options Risk Management

## Overview

Options offer powerful leverage and flexibility, but that same power can lead to significant losses if risk isn't managed properly. This chapter consolidates everything we've learned about options into a comprehensive risk management framework. Good risk management is what separates successful options traders from those who blow up their accounts.

---

## The Cardinal Rules

### Rule 1: Define Risk Before Entry

**Never enter a trade without knowing your maximum loss.**

For every options position, know:
- Maximum possible loss
- Probability of that loss
- Point at which you'll exit

### Rule 2: Size Positions Based on Max Loss

**Position size = Account Risk / Maximum Loss per Contract**

**Not:** "I want to buy 10 contracts"
**Instead:** "I can risk $500. Max loss is $200/contract. I can buy 2 contracts."

### Rule 3: Never Risk More Than 1-5% Per Trade

**Conservative:** 1-2% of account per trade
**Moderate:** 2-3% per trade
**Aggressive:** 3-5% per trade (maximum)

**Example ($50,000 account):**
- 2% risk = $1,000 max loss per trade
- If max loss on iron condor is $400/contract
- Maximum position: 2-3 contracts

### Rule 4: Diversify Strategies and Underlyings

**Don't concentrate risk:**
- Multiple underlyings, not all in one stock
- Multiple strategies, not all iron condors
- Multiple expirations, not all same date
- Balance long and short premium

---

## Position Sizing

### The Math

**Step 1:** Determine account risk percentage (1-3%)
**Step 2:** Calculate dollar risk amount
**Step 3:** Determine max loss per contract
**Step 4:** Divide to get position size

### Example Calculations

**Long Call:**
- Account: $50,000
- Risk tolerance: 2% = $1,000
- Call premium: $3.00 ($300 per contract)
- Max loss: $300 (100% of premium)
- Position size: $1,000 / $300 = 3 contracts

**Credit Spread:**
- Account: $50,000
- Risk tolerance: 2% = $1,000
- Credit received: $1.00
- Spread width: $5.00
- Max loss: $5 - $1 = $4.00 ($400 per contract)
- Position size: $1,000 / $400 = 2 contracts

**Iron Condor:**
- Account: $50,000
- Risk tolerance: 3% = $1,500
- Credit received: $1.50
- Spread width: $5.00
- Max loss: $5 - $1.50 = $3.50 ($350 per contract)
- Position size: $1,500 / $350 = 4 contracts

### Never Use Margin for Naked Options

**Margin magnifies losses.** A naked put on margin can lose far more than your account if the stock gaps down.

If you sell options, use defined-risk strategies or cash-secured positions only.

---

## Managing the Greeks

### Delta Risk Management

**Portfolio delta:** Sum of all position deltas

**Example portfolio:**
- 5 long calls (+260 delta)
- 3 credit spreads (-90 delta)
- 2 long puts (-100 delta)
- **Net delta:** +70 (slightly bullish)

**Guidelines:**
- Keep net delta proportional to account size
- Consider delta as "equivalent shares"
- Don't let delta become unbalanced unintentionally

### Gamma Risk

**High gamma = Explosive moves near expiration**

**Management:**
- Close positions before expiration week (especially short positions)
- Be cautious with ATM options near expiration
- Size smaller when gamma is high

### Theta Management

**For theta-positive positions (sellers):**
- Collect time decay daily
- Monitor for adverse moves
- Close at 50% of max profit to reduce risk

**For theta-negative positions (buyers):**
- Be aware of decay rate
- Don't hold too long without movement
- Consider longer-dated options to slow decay

### Vega Risk

**Before events (earnings):**
- IV is elevated
- Long vega positions expensive
- Short vega positions can profit from IV crush

**Management:**
- Know your vega exposure before events
- Avoid being long vega into binary events
- Use IV rank to guide buying/selling

---

## Setting Stop Losses

### The Challenge with Options

**Options don't move linearly with stock price.** A stop on the option price may trigger too early or too late.

### Stop-Loss Approaches

**Option Price Stop:**
- Close if option loses 50-75% of value
- Simple but may trigger from normal volatility

**Stock Price Stop:**
- Close if underlying reaches certain level
- More logical for directional trades

**Time Stop:**
- Close after X days regardless of P&L
- Prevents holding losers too long

**Technical Stop:**
- Close if support/resistance is broken
- Aligns with chart-based analysis

### Practical Guidelines

**Long options:**
- Consider 50% loss as stop point
- Or set based on underlying price level
- Don't let winners become losers

**Short options (spreads):**
- Close at 2x credit received
- Or when short strike is breached
- Close early (50% profit) to avoid disaster

---

## Rolling Options

### What Is Rolling?

**Closing one position and opening another** to extend duration, adjust strike, or manage risk.

### Types of Rolls

**Roll Out (Time):**
- Close current position
- Open same strike, later expiration
- Buys more time

**Roll Up/Down (Strike):**
- Close current position
- Open different strike, same expiration
- Adjusts price exposure

**Roll Out and Up/Down:**
- Combines both adjustments
- Often used for credit spreads under pressure

### When to Roll

**Roll when:**
- Position is moving against you but thesis intact
- Near-term expiration approaching
- Want to collect additional credit

**Don't roll when:**
- Thesis is broken
- Would be better to accept loss
- Rolling creates worse risk/reward

### Example Roll

**Original position:** Sold $50 put for $1.50, stock at $52
**Stock falls to $49.50** (short strike breached)

**Options:**
1. Close for loss (~$2.00 loss)
2. Roll down and out:
   - Close $50 put for $2.50 (loss)
   - Sell $48 put 30 days out for $1.80 (credit)
   - Net: Still underwater but buying time

---

## Assignment Risk

### Understanding Assignment

**American-style options can be assigned any time** you're short an ITM option.

### When Assignment Is Likely

- **Deep ITM options** (intrinsic value > extrinsic)
- **Near expiration** (little extrinsic value)
- **Before dividends** (call assignment to capture dividend)

### Managing Assignment Risk

**For covered calls:**
- Assignment means selling shares at strike (usually fine)
- Close before expiration if you don't want to sell

**For cash-secured puts:**
- Assignment means buying shares at strike (be prepared)
- Have cash available

**For spreads:**
- Short leg can be assigned, leaving you with only long leg
- May create unhedged position temporarily
- Close spread if short leg goes deep ITM

### Early Assignment Scenarios

**Call spread example:**
- Short $50 call (ITM)
- Long $55 call (OTM)
- Assignment: You're now short 100 shares
- Risk: Stock gaps up, you have unlimited loss until market opens
- Solution: Close or exercise long call to cover

---

## Portfolio-Level Risk Management

### Total Account Risk

**Don't let total open risk exceed 15-20% of account.**

**Example ($50,000 account):**
- Max total risk: $10,000 (20%)
- 5 positions at $2,000 max loss each = at limit
- Don't add more positions until some close

### Correlation Risk

**Multiple positions on correlated underlyings = concentrated risk**

**Example of hidden concentration:**
- Long calls on AAPL
- Long calls on QQQ (heavy AAPL weight)
- Long calls on XLK (AAPL is top holding)
- **Appears diversified but all move with AAPL**

### Expiration Distribution

**Spread expirations to avoid "expiration cliffs":**
- Don't have 10 positions all expiring same day
- Stagger expirations across weeks/months
- Reduces gamma risk concentration

### Strategy Balance

**Balance premium buying and selling:**
- All long options: Bleeding theta, need moves to profit
- All short options: Collecting premium, exposed to big moves
- Balanced: More consistent returns

---

## Event Risk Management

### Earnings

**Earnings create binary risk:**
- Stock can gap 5-20% overnight
- IV crush after announcement
- Even correct direction may lose (IV crush > move)

**Guidelines:**
- Close positions before earnings
- Or size assuming worst-case gap
- Don't be long premium into earnings unless speculating

### Ex-Dividend Dates

**Risk for short calls:**
- Deep ITM calls may be assigned to capture dividend
- Check dividend dates before selling calls

### Economic Events

**Fed announcements, CPI data, etc.:**
- Can move entire market
- Consider reducing positions before major events
- Or ensure positions can survive 2-3% market move

---

## Emergency Procedures

### When to Exit Immediately

**Exit all or most positions when:**
- Position reaches max loss
- Account drawdown exceeds tolerance (e.g., 10%)
- You don't understand what's happening
- You're emotionally compromised

### Circuit Breakers

**Personal trading rules:**
- Daily loss limit: Stop trading after X% loss
- Losing streak limit: Stop after 3-5 consecutive losses
- Take a day off after hitting limits

### Recovery Mode

**After significant drawdown:**
- Reduce position sizes by 50%
- Trade only highest-probability setups
- Rebuild confidence and capital slowly
- Review what went wrong

---

## Record Keeping

### Trade Journal Essentials

**For every trade, record:**
- Date, underlying, strategy
- Entry and exit prices
- Greeks at entry
- Thesis and expected outcome
- Actual outcome and P&L
- What went right/wrong
- Screenshot of position

### Performance Tracking

**Track metrics:**
- Win rate by strategy
- Average winner vs. average loser
- Profit factor (gross profits / gross losses)
- Return on capital
- Max drawdown

### Monthly Review

**Questions to answer:**
- Which strategies are profitable?
- Which strategies are costing money?
- Are position sizes appropriate?
- Is total risk being managed?
- What needs to change?

---

## Common Risk Management Failures

### Failure 1: No Plan

**Trading without defined entries, exits, and size.**

Solution: Write the plan before every trade.

### Failure 2: Oversizing

**Risking too much per trade or total.**

Solution: Stick to 1-3% per trade, 15-20% total.

### Failure 3: Hoping and Holding

**Refusing to exit losers, waiting for recovery.**

Solution: Set stops and honor them without exception.

### Failure 4: Ignoring Correlation

**Multiple positions with same underlying risk.**

Solution: Track portfolio Greeks and correlation.

### Failure 5: Event Ignorance

**Holding through earnings without sizing for gap.**

Solution: Close before or size for worst case.

### Failure 6: Emotional Trading

**Increasing size after losses, revenge trading.**

Solution: Circuit breakers and cooling-off periods.

---

## Risk Management Checklist

### Before Every Trade

- [ ] What is my maximum loss?
- [ ] What percentage of my account is this?
- [ ] What are my exit criteria (profit target, stop loss)?
- [ ] What are the Greeks exposure (delta, vega especially)?
- [ ] Any events before expiration (earnings, dividends)?
- [ ] Does this trade fit my overall portfolio risk?

### Daily Review

- [ ] What is my total portfolio delta?
- [ ] What is my total risk if everything goes wrong?
- [ ] Any positions approaching stop levels?
- [ ] Any upcoming events affecting positions?

### Weekly Review

- [ ] What is my win/loss ratio this week?
- [ ] Am I following my trading plan?
- [ ] Any adjustments needed to strategies?
- [ ] Am I emotionally balanced?

---

## Key Takeaways

- **Define max loss before entering every trade**
- **Size positions based on max loss, not desired profit**
- **Never risk more than 1-3% per trade, 15-20% total**
- **Manage Greeks at portfolio level** - Know your delta, gamma, theta, vega exposure
- **Close positions before earnings** or size for worst-case gaps
- **Roll or exit before max loss** - Don't hope and pray
- **Keep records and review** - Continuous improvement
- **Use circuit breakers** - Stop trading after hitting daily/weekly limits
- **The goal is survival** - Protect capital to trade another day

---

## What's Next

With options fundamentals complete, we move to [Part 7: Cryptocurrency](../part-07-cryptocurrency/36-crypto-fundamentals.md), exploring digital assets, blockchain technology, and the unique risks and opportunities in the crypto market.

---

*Remember: In options trading, risk management isn't just about avoiding losses—it's about staying in the game long enough to let your edge compound. Protect your capital above all else.*
