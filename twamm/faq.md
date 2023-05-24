# FAQ

1. **Why is the order not being filled frequently?**

Orders are normally filled by cranks, which matches orders internally or execute swap on Jupiter. If there are no counterparties and the order execution amount is too small, cranks would skip the order until it can be executed via Jupiter.&#x20;

2. **Why is there a smal portion of USDC left after order is complete?**

As some AMMs leave dusts on input if the decimals of input and output token is different, small portion (≈0.00001 USDC) could be left as dust.

Read more on [Jupiter docs.](https://hub.jup.ag/docs/additional-topics/cpi-smart-contract-integration)

<figure><img src="../.gitbook/assets/Screenshot 2023-05-24 at 6.48.22 PM.png" alt=""><figcaption></figcaption></figure>

3. **How can I add my tokens to TWAMM?**

Feel free to contact our team on [telegram or discord](../links/links.md) to discuss the listing process.&#x20;

Generally, there are no listing fees. However, SOL for running oracles and crank (RPC cost) might be required).

4. **I want to submit TWAP orders for a time period  or token not available on the website**.

Feel free to contact our team on [telegram or discord](../links/links.md) to set up a custom program for your requirements.

Fees can deviate (higher or lower) regarding to the size of trade, which could be discussed internally.
