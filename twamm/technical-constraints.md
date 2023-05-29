# Technical Constraints

### Order Routing Constraints

LP Finance TWAMM utilizes Jupiter Aggregator SDK to find best routes for the trade. However, as TWAMM program detects the output token of the instruction, it only supports "direct-routes".

If there is a token that has most liquidity in SOL but the token pair is "token-USDC", the trade is likely to cause higher slippage. Therefore, LP Finance creates token pair accordingly to available liquidity of the tokens.

Development is ongoing to solve the order routing constraint to allow any routes from the Jupiter Aggregator SDK. Feel free to create a PR on our repository for contribution.&#x20;

{% embed url="https://github.com/LP-Finance-Inc/twamm" %}
