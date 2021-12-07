# YFI Tokenomics Non-Binding Poll
This poll is a non-binding temperature check to sharpen the direction of proposed changes to YFI tokenomics. As each option requires more development work, please consider each proposal a general direction and not a final product.

This poll will be by weighted voting - you can split your YFI between the different options.


## Option A - ySplit
The YFI token is limited to 36,666 tokens, with 1 YFI is valued at 6 ETH or $25k USDC. There is a perception that unit bias is a barrier to token investors.

The ySplit proposal removes the impact of unit bias by issuing a multiple (10,000 to 1,000,000) of new YFI tokens proportionately to YFI token holders. This proposal will have a once-off cost (development, comms, audits, gas) and will a token contract migration.

More detail here:  [ySPLIT](https://docs.google.com/document/d/1dAWTkS_ZsXNy7mKKjOFUjILSlLsLz9KhGfLrwVu0GUg/)

## Option B - veYFI
Treasury earnings are accumulated and used to buy and hold YFI tokens, with the option of spending these on the development of the yearn.finance ecosystem. This reduces circulating supply if spending is less than earnings but there are no guarantees that these holdings will not be spent.

The veYFI option proposes a token locking mechanism modelled from veCRV. YFI holders can stake and lock their tokens for a period of up to 4 years, and in return will receive voting rights (via veYFI tokens) on the distribution of treasury earnings to yearn vaults. The BABY mechanism continues to buy YFI using treasury earnings but the deployment of the earnings is altered as follows:

- An operational treasury is maintained in stablecoins with a minimum balance of $30m
- Excess treasury revenue is directed back into vaults as gauge rewards, with the gauge weight determined by veYFI holders in weekly voting rounds.

It is anticipated that this will incentivise accumulation of veYFI for voting rights, and spawn a Curve-like ecosystem with bribes and entities like Convex.

With YFI protocol returns at around 9.5% APR, there may be a requirement for further issuance of YFI tokens (Curve-like emissions) to properly incentivise locking of YFI for multi-year periods.  This will be subject to future analysis if this proposal proceeds.

More detail here: [veYFI draft proposal WIP](https://docs.google.com/document/d/1hoi-IVccOB6iUJYzuApVbyjbQBx8-M0UuzZosb9wlWM)

## Option C - xYFI
xYFI is similar to veYFI, however instead of vote locking tokens, there is a YFI staking vault (xYFI) to which excess treasury revenue is directed. The BABY mechanism continues to buy YFI using treasury earnings but the deployment of earnings is altered as follows:
- An operational treasury is maintained in stablecoins with a minimum balance of $30m
- The vault operates in a similar manner to a Yearn vault, however instead of strategies the revenue comes as YFI from the BABY buybacks.

The purpose of the xYFI vault is to reward stakers for removing their YFI from circulation by giving them a share of protocol revenue. 

More detail here: [xYFI proposal draft](https://docs.google.com/document/d/1ev16BXu3bDC8zMSBvHmxMWIeD82ptZck6SJAO5frV5g/)

## Option D - BurnKeYs

The YFI token supply is 36,666 tokens. There is nothing preventing YFI holders from voting to mint more tokens at any point in the future leading to a perception that the YFI supply is not limited.

The BurnKeYs option proposes to permanently disable the mint functionality of the YFI token contract, permanently capping the supply to the number of tokens issued at the time.

More detail here: [BurnKeYs](https://docs.google.com/document/d/1BqmRsfdfCIaCtNZULdhKqUJzpKdaHE1XOGQlVp2nuSc)

## Option E - Status Quo

This proposal keeps the YFI tokenomics as they are now, and proposes a campaign to inform YFI holders and potential investors of the benefits of the current tokenomics system. Many of these ideas have been discussed in #status-quo.

### Interactions

If ySplit proceeds, it will occur before any other successful proposal.  BurnKeYs will occur after any other proposal.  veYFI and BurnKeYs may be mutually exclusive if further emissions are required.  veYFI and xYFI are mutually exclusive.

### Acknowledgements
This proposal is the result of lots of input and work from the community:
0x_bear, onlylarping, BraveNewDefi + Iguana & Owl, HatTip3675, Reese, defiglenn, bobe, J-yhelper, bfs, Vany, scottincrypto & fin4dao
