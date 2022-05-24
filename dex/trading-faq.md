# 🤔 Trading FAQ

### Jump to question:

* [What does “Your SOL balance is low” mean?](trading-faq.md#what-does-your-sol-balance-is-low-mean)
* [What fees do I pay when I trade or swap tokens on Solape? ](trading-faq.md#what-fees-do-i-pay-when-i-trade-or-swap-tokens-on-solape)
* [What is price impact?](trading-faq.md#what-is-price-impact)
* [Why did my transaction fail?](trading-faq.md#why-did-my-transaction-fail)
* [Why can't I see my tokens in my wallet after a trade?](trading-faq.md#why-cant-i-see-my-tokens-in-my-wallet-after-a-trade)
* [What is settlement? Why do I have to do it?](trading-faq.md#what-is-settlement-why-do-i-have-to-do-it)
* [I keep getting fail to fetch errors, errors loading markets, or balance flickering whenever I try to trade on the DEX or see my balance, what's going on?](trading-faq.md#i-keep-getting-fail-to-fetch-errors-errors-loading-markets-or-balance-flickering-whenever-i-try-to-t)
* [Why did my trade take a \~0.02 SOL fee? Am I being robbed blind? ](trading-faq.md#why-did-my-trade-take-a-0.02-sol-fee-am-i-being-robbed-blind)
* [Common Error Messages](trading-faq.md#common-error-messages)

### What does "Your SOL balance is low" mean?

**Your SOL balance is low**, surprisingly, tells you that you’re low on SOL.

Though Solana is cheap, it’s important to remember that each transaction requires a small amount of SOL to be paid as a fee. A small amount of SOL goes a long way, but we recommend keeping an eye on your balance – if you run out of SOL, you can’t move any of your tokens.&#x20;

### What fees do I pay when I trade or swap tokens on Solape?

**TL;DR**: not many.

Solape is built on [Serum](https://projectserum.com), a foundation that many Solana DEXs use to tap into ecosystem-wide liquidity.

When your order is **executed** on Solape, you pay **a fee to Serum** (the costs can be viewed [here](https://docs.projectserum.com/appendix/fees)), plus **a Solana network fee** (generally less than $0.01).

Another fee you may encounter is the **account creation fee**. This is only charged the first time you trade a new pair (for example, [SOLAPE/USDC](https://solapeswap.io)) and costs **0.02 SOL**. However, this is really more like a deposit, as you can reclaim it once you empty that account of tokens.

### What is price impact?

The price impact is the difference between the **market price of an asset** and **the price you’ll actually pay for it.**

Yep. Welcome to DeFi, bitch.

The reason this happens is due largely to how decentralized exchanges (DEX) work. Any time you buy or sell a token, you’re affecting the ‘pool’ of assets available for trading – when you buy SOLAPE in the SOLAPE/USDC pool, for example, you’re adding USDC to the pool and taking SOLAPE. When you sell, you’re depositing SOLAPE and withdrawing USDC. Both of these activities cause the pool to revalue the assets it holds.

The bigger your buy/sell, the more of an effect you have on the pool. With popular pairs this isn’t much of an issue (since the pool is so big, your impact is minimal). With less popular ones, however, even smaller transactions can have a large impact.

So, when you see a price impact of, say, **3%** to purchase a token whose market price is **$100**, you’ll end up paying an additional **3%** ($103 in total).

### Why did my transaction fail?

Transactions can fail for a handful of reasons:

_1) Insufficient SOL_&#x20;

As with all other blockchain, you pay a small fee to have your transactions validated on the Solana network. This fee is paid in Solana’s native currency, SOL.

If you don’t have enough SOL in your wallet, you can’t interact with Solape or any other dApp on the Solana network.

Sending additional SOL to your wallet can fix this issue.

_2) Slippage tolerance_&#x20;

When you place a market order, you tell the exchange to match your conditions with the orders that **other users have put on the books.**

As a result, if you want to sell a coin quickly, you’re limited by the orders that currently exist. Though you may want to sell your coin at the current price shown on CoinGecko or CoinMarketCap, there may not be enough demand from buyers on the platform you’re using.

For example, suppose that you’re trying to sell 10,000 coins for $10. Solape may have the following orders submitted by buyers:

* Buy 5,000 coins for $5&#x20;
* Buy 3,000 coins for $2&#x20;
* Buy 2,000 coins for $1

To sell all 10,000 coins at once, you’ll need to compromise by accepting to sell your coins at these rates. In the end, you’ll only receive $8 instead of the $10 you wanted.

Whether you’re happy with this kind of trade or not can be specified with your **slippage tolerance**. This is a percentage of how much difference you’re willing to accept. In this case, the difference was 20% – a pretty noticeable hit, but it’s the cost of doing business in illiquid markets.

If your transaction fails, it could be because your tolerance is too low. Try increasing it and retrying.

_3) Approving transactions_&#x20;

Unless you’ve set up auto-approve in your wallet, you’ll need to confirm your transaction in your Solana wallet when you perform a trade.

The **Making Transaction** notification in the lower left-hand corner of the screen is your cue to open your wallet to approve the transaction.

### Why can't I see my tokens in my wallet after a trade?

Not to panic, this is normal. You'll first need to **settle your balance**.

### What is settlement? Why do I have to do it?

When you trade a pair on Solape, your funds are routed through an intermediary account – regardless of whether the transaction is successful or not.

When your tokens are in this account, you can’t see them in your wallet, use them in other applications, or send them. So you need to settle them to regain access.

Note: some wallets will settle balances automatically if auto-approve is enabled.

### I keep getting fail to fetch errors, errors loading markets, or balance flickering whenever I try to trade on the DEX or see my balance, what's going on?

These errors can occur when Solana’s RPC nodes are overloaded and data can’t be effectively communicated between servers on the network.

In this case, you can do the following:&#x20;

* Try again later&#x20;
* Use another Serum-based GUI&#x20;
* Settle or cancel your trades via [Step Finance](http:step.finance)

### Why did my trade take a \~0.02 SOL fee? Am I being robbed blind?

When you trade a new pair, you pay a small fee to “rent” the space necessary to exchange those two assets. You’ll only pay this **once** per trading pair, and the amount can be later reclaimed if you no longer need to trade using a given pair.

Learn more about this fee [here](https://docs.solana.com/storage\_rent\_economics).

### Common Error Messages

* _Custom program error 0x1_&#x20;

This error tells us that there isn’t enough SOL in the wallet to complete a transaction.

A given trade _may_ require as much as 0.03-0.1 SOL to work, which is why **we recommend keeping at least 0.1 SOL in your wallet** to prevent these kinds of issues.

* _Custom program error 0x22_&#x20;

This error tells us that there aren’t enough tokens to perform a trade.

* _Initialize account_&#x20;

This error is shown when the wallet does not have the required SOL (\~0.02 SOL) to create an _open order account_. Check out [Why did my trade take a \~0.02 SOL fee?](trading-faq.md#why-did-my-trade-take-a-0.02-sol-fee) for more information.

* Fail to fetch&#x20;

This error means that there are RPC issues. It’s often solved by waiting for a short period and retrying.

* Signature verification failed&#x20;

This error indicates that the imported private key is not the correct one.

* Price must be an increment of X&#x20;

Serum-based markets have a tick size – a minimum amount by which prices can move. Any trade must be a multiple of that amount.



HAPPY TRADING!&#x20;
