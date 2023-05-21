# Integrate TWAMM

### Unified TWAMM Liquidity on Solana

LP Finance TWAMM allows users to create TWAP orders, which _does not_ get processed by an underlying AMM but via internal matching or Jupiter orders.

The architecture performs best when there is sufficient liquidity on both side of the orders as the trade can happen without paying fees to AMM LPs.&#x20;

To maximize this efficiency, LP Finance TWAMM can be integrated by **"any"** frontend providers that can earn 100% of the fees generated.

### Integrating TWAMM (twamm-lite)

TODO

### Use Cases

* **General Frontend Integration:** Integrate TWAMM to your frontend to earn 100% of generated fees
* **DAOs:** Process large swaps without worrying about slippage
* **Protocols / Communities:** Register your token on TWAMM and enable TWAP trading
