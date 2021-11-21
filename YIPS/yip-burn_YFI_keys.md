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

The YFI token has a supply of 36,666 tokens and there is no emissions schedule to release more.  The power to mint more YFI is available to YFI holders subject to a successful governance vote and execution by the multisig.  This proposal is to forever remove the ability to create more YFI by burning the mint keys, creating a fixed cap on YFI supply of 36,666 tokens.

## Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the YIP is implemented, not *why* it should be done or *how* it will be done. If the YIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->



## Motivation

<!--This is the problem statement. This is the *why* of the YIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the YIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the YIP will address the issue!-->

A Brief History of YFI Supply:
YFI was created by the Andre Cronje and the Yearn team to hand control of the Yearn ecosystem over to the community.  30,000 YFI tokens were minted and distributed to liquidity providers in the yEarn, Balancer, and Governance pools.  These tokens gave holders the right to vote on Yearn governance proposals and claim a share of rewards earned by the yearn.finance ecosystem.  Initially, the supply of YFI was not fixed as the token included a mint function. The first proposal under the new distributed governance model (YIP-1 <insert footnote ref>) proposed to increase the supply of YFI, with a future vote required to decide the model for distribution.  YIP-1 was passed, but there were no subsequent successful proposals to determine the distribution model.  

The debate around YFI supply evolved around two key themes - how to compensate and retain key Yearn contributors, and a growing movement for a fixed or reduced supply cap.  Further proposals were submitted to modify the YFI supply, some inflationary and some deflationary , none of which were successful <ref yip57>.  There was, however, a successful signalling poll to burn the minting keys and fix the supply of YFI.  This did not progress to a binding proposal and was not implemented.  <ref https://gov.yearn.finance/t/burn-yfi-minting-ability-permanently/5377>

YIP-57 proposed to deal with these issues via increasing the supply of YFI by 6,666 tokens.  One third of these would be vested to reward & retain key Yearn contibuters, and the remaining two thirds allocated to the Yearn treasury for deployment via the Governance process.  Against the backdrop of a small treasury and intense competition for contributors, YFI holders voted 83% to 17% to increase the supply of YFI to 36,666.  Whilst most opponents were not opposed to rewarding contributors, it was clear that token dilution and a fixed supply cap were key concerns from many YFI holders.  Against the backdrop of the earlier poll supporting burning the mint keys, YIP-57 was seen as a divergence from the fixed supply cap meme which had evolved around YFI.  

A further major leap forward in Yearn Governance occured with YIP-61 - Governance 2.0.  This established the framework for governing, organising and operating Yearn.  With this model and a strong treasury  <https://twitter.com/bantg/status/1461910717494398983>, Yearn is in the position to continue operating and innovating without further requirement for supply expansion.  This is the opportunity to codify

## Specification

<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

### Overview

<!--This is a high level overview of *how* the YIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->



### Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->



### Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Yearn Finance currently exposes or the creations of new ones.-->



### Test Cases

<!--Test cases for an implementation are mandatory for YIPs but can be included with the implementation..-->



## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
