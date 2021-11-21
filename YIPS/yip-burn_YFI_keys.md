---
yip: tba
title: Burn the YFI Keys
status: WIP
author: [@scottincrypto](https://twitter.com/scottincrypto), [@fin4dao](https://gov.yearn.finance/u/fin4dao)
discussions-to: <Create a new thread on https://gov.yearn.finance/ and drop the link here>

created: 2021-11-21
requires (*optional): <YIP number(s)>
implementation (*optional): <Added if YIP passes>
---

<!--You can leave these HTML comments in your merged YIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new YIPs. Note that an YIP number will be assigned by an editor. When opening a pull request to submit your YIP, please use an abbreviated title in the filename, `yip-draft_title_abbrev.md`. The title should be 44 characters or less.-->


## Simple Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

The YFI token has a supply of 36,666 tokens and there is no emissions schedule to release more.  The power to mint more YFI is available to YFI holders subject to a successful Governance vote and execution by the Multisig.  This proposal is to forever remove the ability to create more YFI by burning the mint keys, creating a fixed cap on YFI supply of 36,666 tokens.

## Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the YIP is implemented, not *why* it should be done or *how* it will be done. If the YIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

We propose to set the governer address of the YFI token contract to the burn address (0x0).  This will disable the mint functionality of the token contract, permanently capping the supply of the YFI token at the current supply of 36,666 tokens.


## Motivation

<!--This is the problem statement. This is the *why* of the YIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the YIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the YIP will address the issue!-->

### A Brief History of YFI Supply
YFI was created by Andre Cronje and the Yearn team to hand control of the Yearn ecosystem over to the community.  30,000 YFI tokens were minted and distributed to liquidity providers in the yEarn, Balancer, and Governance pools.  These tokens gave holders the right to vote on Yearn Governance proposals and claim a share of rewards earned by the yearn.finance ecosystem.  Initially, the supply of YFI was not fixed as the token included a mint function. The first proposal under the new distributed governance model ([YIP-1](https://gov.yearn.finance/t/proposal-0-yfi-supply/24)) proposed to increase the supply of YFI, with a future vote required to decide the model for distribution.  YIP-1 was passed, but there were no subsequent successful proposals to determine the distribution model.  The supply remained at 30,000 tokens.

The debate around YFI supply evolved around two key themes - how to compensate and retain key Yearn contributors, and a growing movement for a fixed or reduced supply cap.  Further proposals were submitted to modify the YFI supply, some inflationary and some deflationary, none of which were successful[^1].  There was, however, a successful signalling poll to burn the minting keys and fix the supply of YFI[^2].  This did not progress to a binding proposal and was not implemented.  

[YIP-57](https://gov.yearn.finance/t/yip-57-funding-yearns-future/9319) proposed to deal with these issues by increasing the supply of YFI by 6,666 tokens.  One-third of these would be vested to reward & retain key Yearn contributers, and the remaining two-thirds allocated to the Yearn treasury for deployment via the Governance process.  Against the backdrop of a small treasury and intense competition for contributors, YFI holders voted 83% to 17% to increase the supply of YFI to 36,666.  Whilst most opponents were not opposed to rewarding contributors, it was clear that token dilution and a fixed supply cap were key concerns from many YFI holders.  Against the backdrop of the earlier poll supporting burning the mint keys, YIP-57 was seen as a divergence from the fixed supply cap meme which had evolved around YFI.  

A major leap forward in Yearn Governance occurred with [YIP-61 - Governance 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460).  This established the framework for governing, organising, and operating Yearn.  With this model and a [strong treasury](https://twitter.com/bantg/status/1461910717494398983), Yearn is in the position to continue operating and innovating without a further requirement for supply expansion to fund operations.  The environment is now right to deliver on the previously unwritten expectation of a fixed supply cap for YFI by burning the YFI token mint keys.
  


## Specification

<!--The specification should describe the syntax and semantics of any new feature, there are five sections-->
### Powers to Approve and Execute this Proposal
[YIP-61 - Governance 2.0](https://github.com/yearn/YIPS/blob/master/YIPS/yip-61.md#decision-making-powers) is clear in that any changes to the YFI token contract, including burning the mint keys, is a power delegated to YFI holders.  YFI holders can implement this action via a successful vote on this proposal in accordance with [YIP-55](https://github.com/yearn/YIPS/blob/master/YIPS/yip-55.md).  The execution of this proposal, if approved, will be carried out by the Yearn Multisig.  The Multisig holds delegated veto power over any Governance decision, and thus execution of this proposal also requires the implicit consent of a majority of this team.
  
  
### Permanently Disable the Mint Functionality of the YFI Token Contract
Yearn Governance would need to:
  1. Ensure that there are no contracts listed in the `minters` variable of the YFI token contract. 
  2. Set the `governance` variable in the YFI token contract (currently set to the [TimelockGovernance contract](https://etherscan.io/address/0x026d4b8d693f6c446782c2c61ee357ec561dfb61)) to the zero address (0x0)


### Overview

<!--This is a high level overview of *how* the YIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->
Disabling the mint functionality of the YFI token contract will forever remove the ability of any party to call the `mint` function of the [YFI token](https://etherscan.io/address/0x0bc529c00C6401aEF6D220BE8C6Ea1667F6Ad93e).  This has the effect of capping the supply of the YFI token to the `totalSupply` variable at the time of implementation, which is currently 36,666 tokens.  The maximum supply of YFI will never exceed 36,666 tokens, but the future supply may be deflationary due to intentional burn operations or accidental loss of tokens or private keys.  This operation does not remove the ability of YFI holders to, via approved Governance proposals, reduce supply, issue new tokens (not YFI) on behalf of Yearn or, to migrate YFI to a new token contract without disabled mint functionality.


### Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

Following the passage of the signalling poll to burn the mint keys of the YFI token there was an expectation that the supply of YFI was capped. Some community members were under the impression that this decision had been implemented, which became evident during the YIP-57 debate[^3].  With the review of the YFI tokenomics there is an important decision to be made - after any modifications to the YFI token are made, or not made, will the changes be rendered permanent by burning the mint keys?  Stability in tokenomics is one requirement for long-term confidence in the success of Yearn.  Token holders express this confidence by holding YFI.  Regardless of the necessity of the supply inflation in YIP-57, this was a 22% dilution of the token holdings by YFI holders, and YFI holders retain the power to do this again in the future.  With the Yearn treasury in a strong position, and a sustainable Governance and funded operations model in place, YFI holders have the opportunity to prevent any future dilution by voting to burn the mint keys as per this proposal.  This will create on-chain verifiable trust that token supply will not be further increased by future Governance votes.  This can only increase the confidence in the success of Yearn further driving YFI value through token demand.
  
**Todo:**  Describe interactions with other tokenomics proposals currently being developed.  This proposal may be mutually exclusive with some or it may be critical to sequence the execution of this proposal after another has been executed.


### Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Yearn Finance currently exposes or the creations of new ones.-->

**Check:**  Is a technical specification needed in addition to Specification above?

### Test Cases

<!--Test cases for an implementation are mandatory for YIPs but can be included with the implementation..-->
**Todo:**  Need input from a technical/dev type person here on testing process

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

  
### References
  [^1]: [YIP-57 Funding Yearn's Future](https://github.com/yearn/YIPS/blob/master/YIPS/yip-57.md#previous-proposals), table with history of token supply proposals
  [^2]: [Burn YFI minting ability permanently](https://gov.yearn.finance/t/burn-yfi-minting-ability-permanently/5377) Governance Forum Post.  Snapshot poll appears to have been deleted and results are not available.  [IPFS link to Snapshot metadata](https://cloudflare-ipfs.com/ipfs/QmXywy67BG2rMwaMnfWWP5op6MWPdYUU3RPxD38WdxkN57)
  [^3]: [https://gov.yearn.finance/t/yip-57-funding-yearns-future/9319/15](https://gov.yearn.finance/t/yip-57-funding-yearns-future/9319/15)
