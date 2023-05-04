# Order Receive Amount Simulation

### Instant Swap

Instant swap receive amount is calculated using [Jupiter API](https://docs.jup.ag/integrating-jupiter-1/start-with-the-jupiter-api).

### TWAP

TWAP order receive amount is impossible to calculate. Therefore, the UI displays an estimate amount assuming the **exchange rate (price) of the pair remains static during execution period.**

The amount is estimated by dividing the order size by the time interval to get the suborder size per crank epoch which is calculated as follows.

```tsx
// Define Constants
const tifPeriod = 300; // if execution period is 5 minutes (≈300 seconds)
const crankInterval = 5; // crank interval
const tokenA = 10000; // 10000 Token A to be swapped to Token B
const epochs = tifPeriod / crankInterval; // total amount of epochs of trade

// Slice orders
const tifAccountedTokenA = tokenA / intervals; // est amount of token A to be swapped per epoch
const tokenB = fetchFromJupiter(tifAccountedTokenASize); // fetch exchange rate

// Final calculation
const tifAccountedTokenB = tokenB * epochs; // total token B out amount
```

The TWAP order receive amount is a metric to estimate reduction of price impact as the execution period increases. However, lack of arbitrage activities could result in price impact. It is important to select a conservative execution period for larger size.

Following is the assumptions fo the simulations

* Price remains constant throughout the trade
* No counterparty settlement (all orders via [Jupiter](https://jup.ag))
