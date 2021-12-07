# YFI Tokenomics Non-Binding Poll
This poll is a non-binding temperature check to sharpen the direction of proposed changes to the YFI tokenomics that are being worked on right now.  Five proposals have been developed and guidance is sought from YFI holders before more substantial design work is undertaken.  Whilst the vote is non-binding on the multisig, it will direct the future work of the tokenomics group.  Note that the listed proposals require much more work to progress to a successful governance vote.  Consider each proposal a general direction and not a final product - any reservations with particular details can be overcome in future iterations.

This snapshot poll will be by weighted voting.  You can split your YFI between the different options you are interested in Yearn going forwards with. For example, if your favourite is A, you think C, D are ok but don’t like B and E, then you’d perhaps vote half your YFI on A with 25% on each of C and D.

## Option A - ySplit
The YFI token is limited to 36,666 tokens on issue.  At the time of this proposal, 1 YFI is valued at 6 ETH or $25,000 USDC.  Unit bias is a common psychological phenomenon whereby the number of tokens received for a given investment has value to the investor which is not related to any of the underlying characteristics of the token.  

The ySplit token proposal is simply to remove the perceived impact of unit bias from investors by issuing a significant multiple (10,000 to 1,000,000) of new YFI tokens proportionately to YFI token holders.  This proposal will have a once-off cost (development, outreach, communications, audits, gas) and will likely require holders to migrate their holdings to a new contract.

The ySplit proposal is compatible with all other proposals in this poll, however it will likely need to be done before any other proposal if it is approved with one or more others.  In particular, this proposal must be done prior to BurnKeYs if both proposals are approved.

The full text of the draft proposal is here:  [ySPLIT](https://docs.google.com/document/d/1dAWTkS_ZsXNy7mKKjOFUjILSlLsLz9KhGfLrwVu0GUg/)

## Option B - veYFI
Treasury earnings are accumulated and used to buy and hold YFI tokens, with the option of spending these on the development of the yearn.finance ecosystem.  This was approved in YIP-56 (BABY) which had the goals of removing YFI from circulation and providing the means to fund ecosystem growth.  These goals are only both fulfilled if the amount of YFI removed from circulation is greater than the amount spent on growth.  So far this has been the case, but there are no guarantees that the treasury YFI will not make it back onto the open market.

The veYFI option proposes a token locking mechanism modelled from veCRV.  YFI holders can stake and lock their tokens for a period of up to 4 years, and in return will receive voting rights (via veYFI tokens) on the distribution of treasury earnings to yearn vaults.  The BABY mechanism continues to buy YFI using treasury earnings but the deployment of the earnings is altered as follows:
- An operational treasury is maintained in stablecoins with a minimum balance of $30m to fund operations and growth of the ecosystem
- Excess treasury revenue surplus to this requirement is directed back into vaults as gauge rewards, with the gauge weight determined by veYFI holders in weekly voting rounds.

It is anticipated that this mechanism will trigger accumulation of veYFI voting rights to direct gauge rewards, removing YFI from circulating supply.  It is also expected that aggregators like Convex will be incentivised, as will bribing mechanisms to direct gauge rewards in a similar manner to the Curve ecosystem.

The YFI protocol returns (treasury revenue / market cap) is around 9.5% APR and this may fall as TVL grows.  It is recognised that this revenue stream may not be sufficient to incentivise locking of YFI for multi-year periods, and further issuance of YFI tokens (similar to Curve emissions) to supplement the gauge rewards may be required to see this proposal meet its full potential.  Further modelling and discussion on this point will be undertaken if this proposal proceeds.

The veYFI proposal is mutually exclusive with the xYFI proposal, and if token emissions are required it will be incompatible with BurnKeYs also.  If veYFI proceeds along with ySplit, ySplit will need to be executed first.

The full text of the draft proposal is here: [veYFI draft proposal WIP](https://docs.google.com/document/d/1hoi-IVccOB6iUJYzuApVbyjbQBx8-M0UuzZosb9wlWM)

## Option C - xYFI
xYFI is similar to veYFI, however instead of vote locking tokens, the xYFI option proposes a YFI staking vault (xYFI) to which excess treasury revenue is directed as vault rewards.  YFI holders deposit their YFI into the vault, receiving xYFI in return. The BABY mechanism continues to buy YFI using treasury earnings but the deployment of earnings is altered as follows:
- An operational treasury is maintained in stablecoins with a minimum balance of $30m to fund operations and growth of the ecosystem
- The vault operates in a similar manner to a Yearn vault, however instead of strategies the revenue comes as YFI from the BABY buybacks.  When users withdraw, they receive a greater amount of YFI than they deposited, depending on time held and treasury revenue.

The purpose of the xYFI vault is to reward stakers for removing their YFI from circulation by giving them a share of protocol revenue.  The intent is to positively impact YFI price by removing a portion of circulating supply.

The xYFI proposal is mutually exclusive with the veYFI proposal.  If xYFI proceeds along with ySplit, ySplit will need to be executed first to avoid complexity when implementing xYFI.  xYFI is independent of the BurnKeYs proposal.

The full text of the draft proposal is here: [xYFI proposal draft](https://docs.google.com/document/d/1ev16BXu3bDC8zMSBvHmxMWIeD82ptZck6SJAO5frV5g/)

## Option D - BurnKeYs

The YFI token supply is 36,666 tokens.  30,000 were minted at when the token was created and an additional 6,666 were minted with YIP-57 to ensure the sustainability of the protocol.  There is nothing preventing YFI holders from voting to mint more tokens at any point in the future and this creates a perception that the YFI supply is not limited.

The BurnKeYs option proposes to permanently disable the mint functionality of the YFI token contract, permanently capping the supply to the number of tokens issued at the time.

The BurnKeYS option is mutually exclusive with veYFI in the event that veYFI requires further token emissions.  BurnKeYs is compatible with all other tokenomics proposals, but may need to be executed last if other proposals are also approved.

The full text of the draft proposal is here: [BurnKeYs](https://docs.google.com/document/d/1BqmRsfdfCIaCtNZULdhKqUJzpKdaHE1XOGQlVp2nuSc)

## Option E - Status Quo

This proposal keeps the YFI tokenomics as they are now, and proposes a campaign to inform YFI holders and potential investors of the benefits of the current tokenomics system. Discussion for new ideas to increase excitement for YFI and Yearn overall will continue. Ideas discussed in #status-quo included adding more explicit ownership of the Treasury to YFI holders through a possible withdrawal mechanism, using the Treasury to provide liquidity in yvTokens, and increasing focus to appeal to DAOs, possibly with custom DAO treasury vaults.

### Acknowledgements
This proposal is the result of lots of input and work from the community. A few of those are mentioned here:
0x_bear, onlylarping, BraveNewDefi + Iguana & Owl, HatTip3675, Reese, defiglenn, bobe, J-yhelper, bfs, Vany, scottincrypto & fin4dao

