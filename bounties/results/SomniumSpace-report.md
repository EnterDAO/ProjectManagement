# Somnium Space Metaverse Report

By @sgrasmann

Primary goals of this exercise for EnterDAO:

- Have a feasibility report on the Metaverse
- Asses the effort required and prioritize its integration. Best case scenario would be the integration of the Metaverse
  as part of LandWorks Version 1 release.

Tasks:

1. General Description / Overview of the metaverse Whether the metaverse has a native Marketplace and whether it
   provides renting/lending natively
2. Where is the metaverse based? (Is it deployed on an EVM network/Rollup or other? Ethereum/Polygon/Side-chain etc)
3. Addresses + source code of important contracts
   (ERC20/721/Marketplace/Registry etc.)
4. Is Land scarce in the metaverse or anyone can mint new properties?
5. How do scene publishing works? Is it authenticated (f.e metaverse servers/nodes are requesting signed messages from
   the owner/operator)?
    1. Whether the metaverse has a concept of "operators". Is there a way for the "owner" of Land to authorize other
       addresses to publish scenes?

Bonus tasks (out of scope for now):

1. Provide your thoughts on how important it is to integrate with the specified metaverse (reason for important does not
   include "you have land there, and you want to rent it out through LandWorks").
2. Provide your thoughts on how hard it would be to integrate with the Metaverse? Assume that LandWorks protocol will
   become the owner of deposited land and renters must be able to use it (deploy scenes)
3. Propose a design for Integrating

## General Description

### Introduction

Somnium Space main is a persistent 3D world where you can currently find 5000 land parcels owned by individuals users.
In addition, of the “main world”, you can find an important amount of parallel worlds also owned by users. Each land
parcel and each world is defined on the Ethereum blockchain in addition to a lot of other content (Avatars, art pieces,
worlds, cars, kayaks and more).

With your own parcel, you can build anything to your imagination’s content: an art structure, a business meeting office,
an art gallery, an event room, a place to socialize, a showroom for your work and more.

This universe is actually accessible from 3 platforms: VR, PC and Web. With the most focus on the VR experience, Somnium
Space is an alternative to real life to connect with your customers, your friends and/or even your fans!

With a very rich community all over the Earth, Somnium Space is growing and proposes more and more activities and
opportunities. There is no target public in this universeeveryone is welcome and can participate in the future of this
social platform!

### Useful Links

- [Official Website Official](https://somniumspace.com/)
- [Discord Server](https://discord.com/invite/somniumspace)
- [Official Twitter](https://twitter.com/somniumspace)
- [Somnium Space Web](https://somniumspace.com/parcel/)
- [Official YouTube channel](https://www.youtube.com/channel/UCabT6LiDZv4cXQRPDwY1-DA)
- [Official Twitch channel](https://www.twitch.tv/somniumspace)
- [Somnium Times community website](https://somniumtimes.com/)

### NFT Types

- Spaces ("parcels") are offered in S (200m2), M (600m2) and XL (1500m2) sizes and have 3 dimensions (also height) and
  also have additional properties like "roadside" or "waterfront".
- Worlds also exist in different sizes like S (125 MB), M (300 MB) and XL (750 MB). The size describes the complexity of
  the 3D worlds which can be created in tools like Unity and loaded onto ones parcel. They are hosted on Somnium Space
  servers.
- There also exist "Teleportation hubs" as NFTs to travel between parcels (and worlds loaded onto these parcels).
- Special Avatars were created as NFTs for special events like e.g.NFT.NYC.

All in all the NFT types don't seem to be very well-designed to be distinguished on OpenSea if we compare them to other
projects' assets.

### Marketplaces

SomniumSpace seems to rely heavily on OpenSea: https://opensea.io/collection/somnium-space

Trading happens mainly with parcels and avatars. Few trades, but still relatively high
prices: https://nonfungible.com/market/history/somniumspace

There is a community page SomniumTimes, which also wraps
OpenSea: https://somniumtimes.com/somnium-space-vr-market-place/

Additional info from the community manager (I asked via Discord):
"Lending and renting are possible now under landlord management in the PC client. There's currently no smart contract
integration, but I believe that is being considered/worked on in the background."

### Where is the metaverse based?

It's running on Ethereum mainnet.

According to a chat (2021-10-25) on their Discord, Polygon will be supported "soon"
(according to user "Artur | Founder & CEO")

I asked for further support of rollups on Discord (no response yet).

Interesting new announcements for support for NFTs from Solana and Near:
https://somniumspace.medium.com/somnium-space-is-building-the-future-of-an-open-immersivemetaverse-announces-new-investments-95c8ae1cb5a7

### Important Contracts

- Token Cube: https://www.coingecko.com/en/coins/somnium-space-cubes
- Contract: https://etherscan.io/token/0xdf801468a808a32656d2ed2d2d80b72a129739f4
- Uniswap: https://v2.info.uniswap.org/pair/0xf6c3595cbd6858b47e93c83312cef89750cea3a4
- Parcel NFT: https://etherscan.io/address/0x913ae503153d9a335398d0785ba60a2d63ddb4e2
- World NFTs: https://etherscan.io/address/0xf980759616a795b2d692a5c0a0f1bad651984bc1
- Item NFTs: https://etherscan.io/address/0x595f279de4b5df1e47ca55b65175d8a9a935a0fa
- Avatars: https://etherscan.io/address/0x2a378c8d96e7d994fb9bec6adb7c6af2fe772c3b

### Is Land scarce in the metaverse or anyone can mint new properties?

Yes, land is scarce and gets sold in certain batches over time - similar to Sandbox. There have been three "land
offerings" as far as I can tell.
See [this announcement](https://somniumspace.medium.com/%EF%B8%8Froad-2-tlo-auction-dates-creators-fund-buildersdk-%EF%B8%8F-live-worlds-sdk-technical-e4e1021e3c1e)
from summer 2021.

### Concept of Operator/Contributor/Consumer

The whole system seems to be run on servers hosted by Somnium Space LTD (the company). So, they are the operators.
Buying world (measured in MB) means buying hosting space on their servers. On their website's FAQ you can find some info
like: "Lastly, we are a team of +-12 VR fanatics with experience in coding, management and finance. We are also a UK
registered limited company. You can contact us anytime at Discord, Twitter and LinkedIn."

I've asked for plans to decentralize operations in the future to become more permissionless. Their CEO Artur answered on
Discord:

"Hi, we are running on Azure as we are partners with Microsoft. Decentralization of cloud computing is not an easy task
and so far all services and games are running in a centralized way. We are planning to invest more into our
decentralization in the future."

### Additional Info

My question: "Let's say I own some land/parcel. Is it possible to let a creative partner upload their world into my
parcel (from their wallet)? E.g. "whitelist" their wallet address for a certain amount of time. This could be the
foundation for interesting B2B use cases."

Answer by CEO Artur:
"Just rent them your parcel, and it will allow them to build and place any objects on it."

The most comprehensive info can be found in this document (hint from Somnium's Discord):
https://metaverse.properties/wp-content/uploads/2021/09/Metaverse-Report-Series_-Part-2-Somnium-1.pdf

https://metaverse.properties/ is a partner of [GDA Group](https://gda.group/) and is already offering renting land on
Decentraland, Sandbox, Somnium, Cryptovoxels and Upland. Metaverse Properties seems like an interesting partner,
competitor or client for EnterDAO building a real estate business model on top of the Metaverse. I suggest EnterDAO to
get in touch with them.

### How do scene publishing works?

Somnium Space works with two main NFTs: parcels (land) and worlds. The latter get created interactively in the Somnium
Space Builder (on your land) or via the Builder SDK via Unity - a 3D modeling engine with advanced possibilities. Worlds
can be created and edited offline/off-chain and then uploaded onto a land. This separation opens many interesting
business use cases for partners or temporary events: Load a world onto a parcel, have an event, take it down afterwards.
I don't own land - so I couldn't try it out, but I'm pretty sure that land owner need to sign messages to upload a world
onto their land.

# Actionable Items (Core Team input)

`Metaverse Property` - We noticed them a couple of weeks ago, but they seem to be a "web2" company. Meaning that
anything related to buying/selling/renting is done the old web2 way. They do not have any contracts to serve as a
trustless layer for buying/selling/renting properties.

The only hurdle integrating Somnium Space is the fact that they do not have a `contributor/consumer/operator` role **on-chain**. We should contact the development team with proposal to
utilise [EIP4400](https://ethereum-magicians.org/t/erc-4400-erc721consumer-extension/7371) or contribute to them the
implementation needed.
