[Uploading report.md…]()
# Investigation of Potential Informed Trading on Polymarket

## 1. Objective

The goal of this research is to identify Polymarket wallets whose trading behavior may be consistent with having better or earlier information than other market participants.

This analysis does **not** prove that any wallet belongs to an insider. Instead, I use the term **potentially informed trading** and treat the identified wallets as candidates for further investigation.

## 2. Data

I used publicly available Polymarket data.

Research period:

**November 1, 2025 – May 1, 2026**

First, I collected all markets that closed during this period. There were **1,161 markets**.

To keep the analysis manageable, I selected the **30 markets with the highest trading volume**.

For these markets, I collected around **1.33 million trades**.

After limiting the trades to the research period, the dataset contained:

- **383,615 trades**
- **96,039 unique wallets**

## 3. How I Looked for Suspicious Behavior

I used several simple signals.

### 3.1. Buying the Winning Outcome

First, I looked at purchases of the outcome that eventually won.

This signal alone does not mean much because successful traders are common. I therefore used it only as an initial filter.

### 3.2. Timing

I focused on purchases made **6–72 hours before the market closed**.

The idea is simple: if a trader repeatedly takes a large position shortly before an event is resolved, it can be more interesting than normal long-term trading.

### 3.3. Trade Size

To remove a large number of very small trades, I only considered purchases of at least **$1,000**.

### 3.4. Price Movement After the Trade

For each purchase, I looked at how much the price of the same outcome increased during the following 6 hours.

For example:

- a trader buys at 0.80;
- the price reaches 0.90 within the next few hours;
- the price movement is +10 percentage points.

This is **not the trader's actual profit**. It is only a way to measure whether the entry was well timed.

### 3.5. Repeatability

I also checked whether similar behavior appeared across multiple markets.

One successful trade can easily be luck.

If a wallet repeatedly makes similar trades across different markets, it becomes more interesting.

### 3.6. Bots and Very Frequent Trading

Some wallets make thousands of small trades and look more like bots or market makers.

For example, one wallet made more than 3,000 trades on a single market.

I did not treat this type of activity as strong evidence of insider trading and reduced its priority in the ranking.

## 4. Ranking

For each wallet, I considered:

- number of different markets;
- size of positions;
- time before market resolution;
- how often the price moved in the wallet's favor after entry;
- repeatability across markets;
- signs of bot-like trading.

The resulting score is only used to **prioritize wallets for further investigation**.

It should not be interpreted as the probability that a wallet is an insider.

## 5. Main Candidates

### 1. `0x24c8...`

One of the most interesting wallets in the dataset.

It made several large purchases around 8–12 hours before market resolution.

For example, on the Mamdani market, it made several purchases ranging from a few thousand dollars to tens of thousands of dollars. After these purchases, the price continued to move up by roughly 2–5 percentage points.

The behavior appears relatively repeatable, which is why this wallet received a high priority.

### 2. `0x7c3d...`

Another interesting candidate.

Across several markets, this wallet entered at relatively low prices and the price increased significantly afterwards.

The Trump UFO market was particularly interesting, with some purchases followed by price movements of around **+8–13 percentage points**.

This was one of the more noticeable patterns in the dataset.

### 3. `0xd218...`

This wallet stands out because of its trading volume and repeatability.

It traded across several markets and had around **$397K** in qualifying trades.

There is an important caveat, however: some of this volume was purchased at prices close to 0.999. These trades are less informative because the outcome was already considered almost certain.

Because of this, I consider the wallet interesting, but its results should be interpreted carefully.

### 4. `0x0c4b...`

This wallet made relatively large purchases across several markets.

The more interesting trades were earlier purchases at lower prices, followed by further price increases.

For example, on one market it bought at prices around 0.86–0.94, followed by several percentage points of upward movement.

The behavior is interesting, although there is not enough evidence to call it insider trading.

### 5. `0xbacd...`

This wallet had a smaller overall volume, but several particularly interesting trades.

For example:

- 0.60 → around +23 percentage points
- 0.66 → around +17 percentage points
- 0.84 → followed by further upward movement

Because of these trades, the wallet looks like one of the more interesting candidates for further investigation.

## 6. What Did We Find?

The research **does not allow us to say that we found actual insiders**.

Instead, we found several wallets that:

- frequently selected the correct outcome;
- made relatively large trades;
- sometimes entered shortly before resolution;
- showed favorable price movement after entry;
- repeated this behavior across multiple markets.

The main candidates are:

1. `0x24c8...`
2. `0x7c3d...`
3. `0xd218...`
4. `0x0c4b...`
5. `0xbacd...`

There may be completely normal explanations for this behavior, such as strong market analysis, faster access to public information, arbitrage, a specific trading strategy, or simply luck.

## 7. Limitations

There are several important limitations to this analysis.

First, the analysis is **retrospective**, so the final market outcome is already known.

Second, correctly predicting the outcome is not, by itself, evidence of insider trading.

Third, the price movement after a trade is not the trader's actual realized profit.

The dataset also contains related markets, such as multiple markets about the same candidate or different teams in the same sports event. Therefore, the markets cannot be treated as fully independent observations.

Finally, this research uses only public information and does not attempt to identify the real-world owner of any wallet.

## 8. Conclusion

The main result of this research is not proof of insider trading, but rather a **shortlist of wallets with unusually interesting trading behavior**.

The approach is intentionally simple and explainable: position size, timing, repeatability, and price movement after entry.

These signals make it possible to explain why a particular wallet received a higher investigation priority.

A useful next step would be to compare these wallets against a larger group of normal traders and study their activity immediately before specific real-world events.
