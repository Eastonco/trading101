# Chapter 32: Basic Options Strategies

## Overview

Before diving into complex spreads, master the fundamental options strategies. These building blocks—covered calls, cash-secured puts, and protective puts—are the most common options trades used by both beginners and professionals. They offer defined risk profiles and practical applications for income generation and portfolio protection.

---

## Covered Calls

### What Is a Covered Call?

**A covered call = Own 100 shares + Sell 1 call option**

You sell someone the right to buy your shares at the strike price. In exchange, you collect premium.

### Why It's Called "Covered"

Your obligation to sell shares is "covered" by actually owning the shares. If assigned, you simply deliver shares you already own. No additional risk of having to buy at unfavorable prices.

### The Setup

**Example:**
- Own 100 shares of XYZ at $50
- Sell 1 XYZ $55 call for $1.50 premium
- Collect $150 (1 contract × 100 shares × $1.50)

### Possible Outcomes

**Scenario 1: Stock stays below $55 at expiration**
- Call expires worthless
- You keep your shares
- You keep the $150 premium
- **Result:** +$150 income

**Scenario 2: Stock rises above $55 at expiration**
- Call is exercised
- You sell shares at $55
- You keep the $150 premium
- **Result:** Profit capped at $5 (stock gain) + $1.50 (premium) = $6.50/share

**Scenario 3: Stock falls significantly**
- Call expires worthless
- You keep premium ($150)
- But shares lost value
- **Result:** Premium provides partial cushion against loss

### Profit/Loss Diagram

```
Profit
   |
   |              _______________
   |             /
   |            /
   |           /
   |----------/-------------------- Break-even
   |         /
   |        /
   |_______/________________________ Stock Price
         Strike
```

**Maximum profit:** Strike - Stock cost + Premium
**Maximum loss:** Stock goes to zero (minus premium collected)
**Break-even:** Stock cost - Premium received

### When to Use Covered Calls

**Ideal conditions:**
- Neutral to slightly bullish outlook
- Willing to sell shares at strike price
- Want to generate income while holding
- Stock in a range or slow uptrend

**Avoid when:**
- Strongly bullish (caps upside)
- Expect significant drop (better to sell)
- Not willing to part with shares

### Covered Call Example

**Setup:**
- Buy 100 shares XYZ at $48 = $4,800
- Sell $52.50 call for $1.25 = $125 received

**If stock at $50 at expiration:**
- Call expires worthless
- Stock gain: $200
- Premium: $125
- **Total profit: $325** (6.8% return)

**If stock at $55 at expiration:**
- Called away at $52.50
- Stock gain: $450
- Premium: $125
- **Total profit: $575** (12% return, but missed $250 above strike)

**If stock at $45 at expiration:**
- Call expires worthless
- Stock loss: -$300
- Premium: $125
- **Net loss: -$175** (better than -$300 without call)

---

## Cash-Secured Puts

### What Is a Cash-Secured Put?

**Cash-secured put = Sell 1 put option + Hold cash to buy shares if assigned**

You sell someone the right to sell you shares at the strike price. You collect premium and may be required to buy shares.

### Why "Cash-Secured"

You hold enough cash to buy 100 shares at the strike price. If assigned, you simply buy at the agreed price using reserved cash.

### The Setup

**Example:**
- XYZ trading at $50
- Sell 1 XYZ $47.50 put for $1.00
- Collect $100 premium
- Reserve $4,750 cash (strike × 100)

### Possible Outcomes

**Scenario 1: Stock stays above $47.50 at expiration**
- Put expires worthless
- You keep the $100 premium
- Cash remains available
- **Result:** +$100 income (2.1% return on cash reserved)

**Scenario 2: Stock falls below $47.50 at expiration**
- Put is exercised
- You buy 100 shares at $47.50
- You keep the $100 premium
- **Effective cost:** $47.50 - $1.00 = $46.50/share
- **Result:** Own shares at discount to where you sold the put

**Scenario 3: Stock falls significantly (say to $40)**
- You buy at $47.50 (obligation)
- Immediate paper loss of $750
- Premium offsets $100
- **Result:** -$650 loss (but you wanted to own the stock anyway)

### Profit/Loss Diagram

```
Profit
   |_____________
   |             \
   |              \
   |               \
   |------------------------------ Break-even
   |                 \
   |                  \
   |                   \
   |____________________\_________ Stock Price
                     Strike
```

**Maximum profit:** Premium received
**Maximum loss:** Strike price - Premium (if stock goes to zero)
**Break-even:** Strike price - Premium

### When to Use Cash-Secured Puts

**Ideal conditions:**
- Want to buy shares at lower price
- Neutral to bullish outlook
- Willing to wait or collect premium
- Have cash available

**Think of it as:** Getting paid to place a limit order below market.

### Cash-Secured Put Example

**Setup:**
- XYZ at $52
- Sell $50 put for $1.50
- Reserve $5,000 cash

**If stock stays above $50:**
- Keep $150 premium
- Return: 3% on reserved capital
- Repeat monthly: 36% annualized (if it works every time)

**If stock drops to $48:**
- Buy 100 shares at $50
- Effective cost: $50 - $1.50 = $48.50
- Stock is at $48, you're down $50 immediately
- But you wanted to own it anyway at ~$48.50

---

## Protective Puts (Married Puts)

### What Is a Protective Put?

**Protective put = Own 100 shares + Buy 1 put option**

You buy insurance against your stock dropping. The put gives you the right to sell at the strike price, limiting downside.

### Why Use Protective Puts

- **Protect gains** on appreciated stock
- **Limit downside** while maintaining upside
- **Sleep better** during uncertain times
- **Define maximum loss** on position

### The Setup

**Example:**
- Own 100 shares of XYZ at $50
- Buy 1 XYZ $45 put for $1.50
- Pay $150 for protection

### Possible Outcomes

**Scenario 1: Stock rises to $60**
- Put expires worthless (-$150)
- Stock gain: +$1,000
- **Net profit: $850**

**Scenario 2: Stock stays at $50**
- Put expires worthless (-$150)
- Stock unchanged
- **Net loss: -$150** (cost of insurance)

**Scenario 3: Stock crashes to $35**
- Exercise put, sell at $45
- Stock loss limited to $5/share ($500)
- Put cost: $150
- **Total loss: -$650** (vs -$1,500 without put)

### Profit/Loss Diagram

```
Profit
   |
   |                    /
   |                   /
   |                  /
   |                 /
   |----------------/------------- Break-even
   |_______________/
   |
   |________________________________ Stock Price
              Strike
```

**Maximum profit:** Unlimited
**Maximum loss:** (Stock price - Strike) + Premium paid
**Break-even:** Stock price + Premium paid

### The Cost of Insurance

**Protective puts cost money:**
- Reduces returns in flat or up markets
- Premium is lost if not needed
- Must weigh cost vs. protection value

### When to Use Protective Puts

**Ideal conditions:**
- Large unrealized gains you want to protect
- Uncertain near-term outlook
- Want to maintain upside potential
- Can afford the premium cost

**Alternative:** Collar (covered call + protective put) reduces cost

---

## Comparing the Basic Strategies

### Strategy Comparison Table

| Strategy | Outlook | Max Profit | Max Loss | Premium |
|----------|---------|------------|----------|---------|
| Covered Call | Neutral/Mild Bullish | Limited (strike + premium) | Large (stock to 0) | Receive |
| Cash-Secured Put | Bullish/Neutral | Limited (premium) | Large (strike - premium) | Receive |
| Protective Put | Bullish (worried) | Unlimited | Limited | Pay |

### Risk/Reward Profiles

**Covered Call:**
- Enhances income on existing position
- Caps upside for premium
- Still exposed to significant downside

**Cash-Secured Put:**
- Income while waiting to buy
- May end up buying at higher than market
- Full downside exposure if assigned

**Protective Put:**
- Insurance has a cost
- Preserves unlimited upside
- Defines maximum loss

---

## Strategy Selection Guide

### Use Covered Calls When:

- [ ] You own shares you're willing to sell
- [ ] You're neutral to mildly bullish
- [ ] You want monthly income
- [ ] You're okay capping upside

**Don't use when:** You're strongly bullish or the stock is extremely volatile.

### Use Cash-Secured Puts When:

- [ ] You want to buy a stock at a lower price
- [ ] You'd be happy owning it if assigned
- [ ] You're neutral to bullish
- [ ] You have the cash to secure the put

**Don't use when:** You're bearish or wouldn't want to own the stock.

### Use Protective Puts When:

- [ ] You have significant gains to protect
- [ ] You're worried about near-term downside
- [ ] You want to maintain unlimited upside
- [ ] You can afford the premium

**Don't use when:** Cost exceeds your risk tolerance, or you'd rather just sell.

---

## Practical Considerations

### Strike Selection

**Covered Calls:**
- OTM for more upside potential, less premium
- ATM for maximum premium, capped at current price
- Typically 5-10% OTM is common

**Cash-Secured Puts:**
- OTM for lower chance of assignment, less premium
- ATM for maximum premium, higher assignment chance
- Typically 5-10% OTM (price you'd want to buy)

**Protective Puts:**
- ATM for maximum protection, highest cost
- OTM for cheaper insurance, more downside before protection
- Typically 5-15% OTM balances cost and protection

### Expiration Selection

**Shorter duration (weekly/monthly):**
- More frequent premium collection
- Higher annualized return if successful
- More management required

**Longer duration (45-60 days):**
- Less frequent management
- Captures most theta decay
- Common sweet spot for premium selling

### Managing Positions

**If winning:**
- Let expire or close early for profit
- Consider rolling to new expiration

**If losing:**
- Roll out (later expiration) for more time
- Roll down/up to different strike
- Accept assignment/loss based on thesis

---

## Key Takeaways

- **Covered calls generate income** on stocks you own by selling upside
- **Cash-secured puts earn premium** while waiting to buy at lower prices
- **Protective puts provide insurance** against downside while keeping upside
- **All three are "level 1" strategies** - approved for most accounts
- **These are building blocks** for more complex strategies
- **Strike and expiration selection** dramatically affect outcomes
- **Management is key** - know when to hold, roll, or close

---

## What's Next

In [Chapter 33: Spread Strategies](33-spread-strategies.md), we'll combine multiple options to create defined-risk strategies like vertical spreads, iron condors, and more sophisticated approaches.

---

*Remember: Master these basics before moving to spreads. Every complex strategy is built from these fundamental positions.*
