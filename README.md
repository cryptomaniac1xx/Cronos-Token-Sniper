# Cronos-Token-Sniper for cro network

## How to use it:
1. Deploy contract using http://remix.ethereum.org/ on Cronos Network
2. Send at least 1000 CRO to contract for tokens to buy
3. Call function 'Action' to start sniping

## How it works:
By default contract is looking for 'pair created' event which is when new LP is created to new tokens.
Contract then proceed to buy tokens for 10 CRO , approve it to sell and try to sell 1% of tokens in one transaction. If it fails to sell or approve then whole transaction is reverted. That way it avoids honeypots.
Later it waits until price of 20% tokens is worth more then 100 CRO. When price reach that limit contract sells tokens and send CRO to your wallet.
