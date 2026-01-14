# Chapter 15: Technical Indicators

## Overview

Technical indicators are mathematical calculations based on price and/or volume that help traders identify trends, momentum, and potential reversal points. While hundreds of indicators exist, a handful of core indicators provide the foundation for most technical analysis.

This chapter covers the essential indicators—moving averages, RSI, MACD, and Bollinger Bands—and how to use them effectively.

---

## Moving Averages

Moving averages smooth out price data to identify trends. They're the foundation of technical analysis.

### Simple Moving Average (SMA)

**Calculation:** Average of closing prices over N periods.

**Formula:** SMA = (P₁ + P₂ + ... + Pₙ) / N

**Example (10-day SMA):** Sum of last 10 closing prices ÷ 10

### Exponential Moving Average (EMA)

**Calculation:** Weighted average giving more weight to recent prices.

**Key difference:** EMA reacts faster to price changes than SMA.

### Common Moving Average Periods

| Period | Timeframe | Use |
|--------|-----------|-----|
| 9-10 EMA | Short-term | Fast signals, day trading |
| 20-21 EMA | Short-term | Swing trading |
| 50 SMA/EMA | Medium-term | Intermediate trend |
| 100 SMA | Medium-term | Support/resistance |
| 200 SMA | Long-term | Major trend, institutional reference |

### Moving Average Signals

**Price vs. Moving Average:**
- Price above MA = Bullish
- Price below MA = Bearish

**Moving Average Crossovers:**
- **Golden Cross:** 50-day crosses above 200-day (bullish)
- **Death Cross:** 50-day crosses below 200-day (bearish)
- Shorter MA crossing longer MA signals potential trend change

**Moving Average as Support/Resistance:**
- In uptrends, price often bounces off rising MAs
- In downtrends, price often rejects at falling MAs

### Practical Application

**Trend identification:**
- All MAs sloping up, price above = strong uptrend
- All MAs sloping down, price below = strong downtrend
- MAs flat, price crossing back and forth = range/consolidation

**Entry timing:**
- Buy pullbacks to rising 20 EMA in uptrends
- Sell bounces to falling 20 EMA in downtrends

---

## Relative Strength Index (RSI)

RSI measures momentum on a scale of 0-100, indicating overbought and oversold conditions.

### Calculation

RSI = 100 - (100 / (1 + RS))

Where RS = Average Gain / Average Loss over N periods

Standard period: 14

### Reading RSI

| RSI Level | Interpretation |
|-----------|----------------|
| Above 70 | Overbought (potentially overextended) |
| 50-70 | Bullish momentum |
| 50 | Neutral |
| 30-50 | Bearish momentum |
| Below 30 | Oversold (potentially overextended) |

### RSI Signals

**Overbought/Oversold:**
- RSI > 70: Stock may be due for pullback
- RSI < 30: Stock may be due for bounce
- **Warning:** In strong trends, RSI can stay overbought/oversold for extended periods

**Divergence:**
- **Bullish divergence:** Price makes lower low, RSI makes higher low → Potential reversal up
- **Bearish divergence:** Price makes higher high, RSI makes lower high → Potential reversal down

**Failure Swings:**
- RSI breaks above 70, pulls back, then makes lower high without reaching 70 = Bearish
- RSI breaks below 30, bounces, then makes higher low without reaching 30 = Bullish

### RSI Best Practices

- Don't blindly buy oversold or sell overbought
- Use divergence for counter-trend setups
- In strong trends, use RSI for pullback entries (buy when RSI pulls back to 40-50 in uptrend)
- Adjust period for your timeframe (shorter period = more signals, more noise)

---

## MACD (Moving Average Convergence Divergence)

MACD shows the relationship between two EMAs and is one of the most popular momentum indicators.

### Components

1. **MACD Line:** 12 EMA - 26 EMA
2. **Signal Line:** 9 EMA of the MACD Line
3. **Histogram:** MACD Line - Signal Line

### Reading MACD

**MACD Line vs. Zero:**
- MACD above zero = 12 EMA above 26 EMA = Bullish
- MACD below zero = 12 EMA below 26 EMA = Bearish

**MACD Line vs. Signal Line:**
- MACD crosses above signal = Bullish signal
- MACD crosses below signal = Bearish signal

**Histogram:**
- Positive and growing = Bullish momentum increasing
- Positive and shrinking = Bullish momentum waning
- Negative and growing = Bearish momentum increasing
- Negative and shrinking = Bearish momentum waning

### MACD Signals

**Crossovers:**
- Buy when MACD crosses above signal line
- Sell when MACD crosses below signal line
- More reliable when crossing near zero line

**Zero Line Cross:**
- MACD crossing above zero = Bullish trend confirmation
- MACD crossing below zero = Bearish trend confirmation

**Divergence:**
- Price makes new high, MACD makes lower high = Bearish divergence
- Price makes new low, MACD makes higher low = Bullish divergence

### MACD Limitations

- Lagging indicator (uses moving averages)
- Generates false signals in ranging markets
- Works best in trending conditions

---

## Bollinger Bands

Bollinger Bands measure volatility and identify overbought/oversold conditions relative to recent price action.

### Components

1. **Middle Band:** 20-period SMA
2. **Upper Band:** Middle Band + (2 × Standard Deviation)
3. **Lower Band:** Middle Band - (2 × Standard Deviation)

### Reading Bollinger Bands

**Bandwidth:**
- Narrow bands = Low volatility, potential breakout coming (squeeze)
- Wide bands = High volatility, potential exhaustion

**Price vs. Bands:**
- Price touching upper band = Short-term overbought
- Price touching lower band = Short-term oversold
- Price outside bands = Extreme move, not sustainable

### Bollinger Band Strategies

**Mean Reversion:**
- Buy when price touches lower band (in range)
- Sell when price touches upper band (in range)
- Works in sideways markets

**Trend Following:**
- In uptrends, price "walks the band" (stays near upper band)
- In downtrends, price walks the lower band
- Don't fade these moves

**Bollinger Squeeze:**
- Bands contract significantly
- Signals low volatility
- Often precedes major move
- Trade the breakout direction

**Double Bottom:**
- Price touches lower band
- Bounces, then retests but doesn't touch band
- Second low holds above band = Bullish setup

### Bollinger Band Rules

- Bands don't predict direction, just volatility
- Price can ride bands for extended periods in trends
- Mean reversion works in ranges; trend following works in trends
- Use with other indicators for confirmation

---

## Stochastic Oscillator

Measures momentum by comparing closing price to price range over a period.

### Components

- **%K:** Main line (fast)
- **%D:** Signal line (slow, 3-period SMA of %K)

### Reading Stochastics

| Level | Interpretation |
|-------|----------------|
| Above 80 | Overbought |
| Below 20 | Oversold |

### Stochastic Signals

**Crossovers:**
- %K crosses above %D = Buy signal
- %K crosses below %D = Sell signal
- Best when occurring in overbought/oversold territory

**Divergence:**
- Works similarly to RSI divergence

### Stochastic vs. RSI

- Stochastic is faster, more signals (more noise)
- RSI is smoother, fewer signals
- Stochastic works well in ranging markets
- RSI works well in trending markets

---

## Volume Indicators

### Volume

**Basic interpretation:**
- Rising price + rising volume = Healthy uptrend
- Rising price + falling volume = Weakening uptrend
- Falling price + rising volume = Strong selling
- Falling price + falling volume = Selling exhaustion

### On-Balance Volume (OBV)

Running total of volume:
- Up day: Add volume to OBV
- Down day: Subtract volume from OBV

**Signals:**
- OBV confirming price trend = Healthy
- OBV diverging from price = Potential reversal

### Volume Moving Average

Compare current volume to average:
- Volume above average = Significant move
- Volume below average = Less conviction

---

## Using Multiple Indicators

### The Confluence Approach

Don't use indicators in isolation. Look for agreement between multiple signals:

**Example bullish confluence:**
- Price above 50 EMA
- RSI bouncing from 40-50 area
- MACD crossing above signal
- Price bouncing off lower Bollinger Band

### Avoiding Redundancy

Some indicators measure the same thing:
- RSI, Stochastic, CCI all measure momentum
- Multiple MAs all measure trend
- Using RSI and Stochastic together adds little value

**Better approach:** Use one trend indicator, one momentum indicator, one volume indicator.

### Suggested Combinations

**Trend Following:**
- Moving averages (trend)
- MACD (momentum)
- Volume

**Mean Reversion:**
- Bollinger Bands (volatility)
- RSI or Stochastic (momentum)

**Balanced:**
- 20/50/200 EMAs (trend)
- RSI (momentum)
- Volume

---

## Common Mistakes

### 1. Indicator Overload

Charts with 10+ indicators are impossible to read. Use 2-3 maximum.

### 2. Ignoring Price

Indicators derive from price. Price action is primary; indicators are secondary.

### 3. Treating Indicators as Holy Grail

No indicator works all the time. All have false signals.

### 4. Not Adjusting for Conditions

RSI overbought in a strong trend ≠ sell. Context matters.

### 5. Over-Optimizing

Changing indicator settings to fit historical data (curve fitting) doesn't help future trading.

---

## Key Takeaways

- **Moving averages identify trends** - 50/200 for major trends, 20 for short-term
- **RSI measures momentum** - Overbought/oversold and divergence signals
- **MACD shows momentum direction** - Crossovers and divergence
- **Bollinger Bands measure volatility** - Squeeze precedes big moves
- **Volume confirms moves** - High volume = conviction
- **Use indicators together** - Look for confluence, not single signals
- **Keep it simple** - 2-3 indicators maximum
- **Price is primary** - Indicators confirm, they don't predict

---

## What's Next

In [Chapter 16: Volume Analysis](16-volume-analysis.md), we'll take a deeper dive into reading volume—the "lie detector" of the market that confirms or denies price moves.

---

*Remember: Indicators are tools, not crystal balls. Always use proper risk management.*
