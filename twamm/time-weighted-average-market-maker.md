# Time-weighted Average Market Maker

TWAMM, short for time-weighted average market maker is a service that allows traders on Solana to efficiently execute large orders.

TWAMM pools large orders together, breaks them down into small pieces, and executes them over a specified time interval. Orders with opposite sides are internally matched using the oracle price, and net outstanding liquidity is settled via the best possible execution route available with Jupiter.

Additionally, market makers (or literally anyone) have the opportunity to settle the outstanding net balance at the oracle price (i.e. perform a swap against TWAMM pools), saving on swap fees for themselves and the protocol.

By using TWAMM, following are acheived

1. Reduce price impact of large orders
2. Fill orders close to the average price over the specified time window.
3. Reduce complexity and lower execution fees compared to the manual approach.
4. Let users retain full custody of their tokens while orders are executed.
5. Reduce adverse selection by providing full transparency.

The original idea belongs to [Paradigm](https://www.paradigm.xyz/2021/07/twamm). But instead of relying on internal pools that may lack liquidity, this project leverages Jupiter to settle the net outstanding balance as well as opens the opportunity to any liquidity providers to settle trades at the oracle price.

\
