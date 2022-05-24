# What is a DEX?

A decentralized exchange – or DEX – is a marketplace for trading cryptocurrencies without a middleman. Unlike with a traditional exchange (Binance, Coinbase, etc.), **you never give up custody of your funds**. Trades involve only you and a handful of blockchain-based smart contracts, and can be performed directly from your wallet.\


It isn’t hard to see why these venues have exploded in popularity in recent years. By sidestepping the centralized exchanges that make up the crypto industry today, you:

1. Don’t put your funds at risk of getting stolen if a centralized body is hacked
2. Don’t sacrifice your privacy by providing identifying information
3. Can verify the open-source code that underpins your DEX

Of course, there are some shortcomings here. Fiat-to-crypto and crypto-to-fiat transactions aren’t possible – DEXs are designed for crypto-to-crypto swaps on the same blockchain.

For example, Ethereum has [Uniswap](https://uniswap.org/), BSC has [PancakeSwap](https://pancakeswap.finance/), and Solana has [Solape](https://solapeswap.io/#/swap).





### How a DEX works <a href="#_h0z66owijf65" id="_h0z66owijf65"></a>

In today’s ecosystem, two models dominate the decentralized exchange game. By far the most popular on other blockchains is the **Automated Market Maker (AMM)** system, but Solana does things a little differently with Serum’s **on-chain order book**. Let’s talk about how each of these work.

#### The Automated Market Maker (AMM) <a href="#_p117jpfwsq4e" id="_p117jpfwsq4e"></a>

On centralized exchanges, an order book is used to pair buyers with sellers. A user posts what they want to buy or sell and for what price, and the exchange says _hey, this other user is happy with those terms_ and carries out the trade. The ‘list’ of these orders is, fittingly, called an **order book**.

You _could_ replicate this on a blockchain (as has been done in the past), but it isn’t efficient. Users would need to pay a fee to list their order and more to cancel or update it to reflect rapidly changing prices. Besides, most blockchain simply aren’t equipped to facilitate high-throughput trading due to scalability limitations.

Enter **liquidity pools**. When a market maker wants to create a new market, they deposit two types of tokens into a pool. For our purposes, let’s use SOLAPE and USDC as examples.

To kick things off, the market maker (or _liquidity provider_, as they’re known in this new paradigm) deposits these tokens in **equivalent values**. So, if SOLAPE is currently worth $2, you might expect the liquidity provider to deposit one of the following combinations:

* 10,000 USDC and 5,000 SOLAPE
* 5,000 USDC and 2,500 SOLAPE
* 1,000 USDC and 500 SOLAPE

It doesn’t matter which they go with, so long as the value of the SOLAPE deposited is equal to that of the USDC deposited. The liquidity provider will then receive a certain amount of LP tokens which, once cashed in, entitle them to their share of the pool’s value as well as a cut of the trading fees collected from users that traded using the pool. Soon, other LPs want in on this action and begin to deposit their own SOLAPE+USDC to the pool.

Now, here’s where things get interesting. Suppose that our pool has 100,000 USDC and 50,000 SOLAPE currently, meaning that SOLAPE is worth 2 USDC (or $2). If a user makes a purchase of 5,000 SOLAPE, they’re removing SOLAPE from the pool in exchange for USDC.

Now, the pool holds 105,000 USDC and 45,000 SOLAPE. Since we’re working on the assumption that each is held in equal value, this pushes the price of SOLAPE to $2.3.

We’re omitting some of the more technical details, but the idea behind this system is that the **pools can dynamically price their assets based on the market activity**. If discrepancies exist between these venues and other exchanges, users are incentivized to exploit them until prices reach equilibrium with the wider market.

Also worth highlighting is that the larger the value held in the pool, the lesser the price impact of swaps: in our example above, withdrawing 5,000 SOLAPE from a pool of 10,000,000 SOLAPE wouldn’t shift its price as much as if we withdrew it from our pool of 50,000.

The AMM model has been a revolutionary introduction to the world of DeFi – making it easy to swap between currency pairs within seconds, all without the intervention of a centralized exchange.

#### On-chain order books <a href="#_9pnphhabuv1f" id="_9pnphhabuv1f"></a>

On-chain order books store limit orders on the blockchain. As we touched on above, this has traditionally been a cost-prohibitive solution as it requires the entire network to store a record of the order (and, therefore, for the user to pay a fee). What’s more, it leaves orders vulnerable to _front running_, where other users can spot an order before it gets added to the blockchain and act on that information.

For years, the limitations on this model (largely imposed by chains struggling with scalability) prevented it from gaining meaningful traction. But when Serum was launched on Solana, the protocol demonstrated the true potential of the on-chain order book model. With near-instant confirmations and low fees, Solana proved to be the ideal testing ground for this new iteration.

Today, Serum is arguably one of the most important components in the Solana DeFi space. Its protocol is used by a vast range of different trading venues (Solape included), each of which taps into the order book to achieve deep, ecosystem-wide liquidity.\


### To Sum It Up <a href="#_xqilow45nth0" id="_xqilow45nth0"></a>

The DEX concept is nothing new, but it’s only over the past couple of years that we’ve seen what it’s capable of. The advent of new scaling technologies and innovative implementations have resulted in decentralized exchanges becoming the backbone of a fast-growing DeFi ecosystem across a range of blockchains.

With Solape DEX, you can enjoy everything the Serum DEX has to offer. Trade with nominal fees and seamless access to over 95 pairs today.\
