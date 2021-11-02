# The Sandbox Metaverse Report

By Ben Alistair

The Sandbox is a virtual world where users can create, own, and monetize their own metaverse experience built on the
Ethereum blockchain. Sandbox gives users tools to create their own custom voxel models, trade in-game assets, and even
build and share their own games with other users of Sandbox - all of which can be monetized. Sandbox offers customizable
behaviors and parameters for an immersive experience. Users can create an unlimited amount of NFTs and have complete
ownership over their creations. With a number of ways to build and explore within the metaverse, Sandbox offers a unique
platform for anyone looking to get involved. While the metaverse is not live yet, you can currently buy land and create
your own games and custom NFT assets with their free Game Maker and VoxEdit software. Once Sandbox is live, gaming
experiences and custom NFT assets can be deployed and utilized within the metaverse.

Sandbox has a native marketplace to buy and trade user created NFT assets. Users can purchase NFTs with the native
currency $SAND. There are plans to utilize meta-transactions which will allow users to interact with the Ethereum
blockchain without owning any Ethereum. Users will eventually have the ease of paying fees in $SAND. To date, there is
no option to rent Sandbox land natively, although the Sandbox documents state that “in the future LAND owners will be
able to rent out any LANDs they own to other creators in The Sandbox” (Sandbox Gitbook). Land owners will be able to
decide how much they want to rent their land for, but will need to consider several factors like proximity to popular
areas, locations near large partners' land, and the size of the land itself. Once live, this will enable owners of the
land to authorize renters (other addresses) to deploy scenes themselves.

Sandbox is based on the Ethereum blockchain although they are currently working on integrating Polygon as well. $SAND is
the native ERC-20 token and serves as the utility token of the Sandbox ecosystem as well as a governance token. $SAND
can be used to purchase land, in-game assets, gems, and catalysts. $SAND can also be used to stake on land to earn
rewards in GEMs.

Gems are an ERC-20 utility token that define your ASSETs’ attributes, and Catalysts are an ERC-20 utility token that
define your in-game assets’ tier and scarcity. Both are burnt upon usage. Gems can be acquired by staking $SAND on land
or can be bought in the Sandbox marketplace from other users. Catalysts can be obtained several different ways in the
metaverse with more information on how to do so coming in the future.

All land and in-game assets are currently built on Ethereum utilizing both ERC-721 and ERC-1155 tokens. According to a
Medium post from Sandbox, Polygon is being integrated for the VoxEdit NFT builder, the Marketplace, and the Game Maker
tool. Contracts are not live for Polygon to date, but the active Ethereum contracts for Sandbox can be found below.

Land plots known as LANDs are ERC-721 tokens and user created NFTs called ASSETs can be minted as ERC-1155 and ERC-721
tokens depending on the supply; ERC-1155 is the standard for anything over one token of a given creation and ERC-721 is
used for unique 1/1 NFTs.

Sandbox land is certainly scarce. Multiple public sales have been completed and sold out along with a number of other
special event land sales. Land is available through secondary markets via OpenSea and the Sandbox marketplace with plans
for more public sales in the near future. There is a hard cap of 166,464 plots of land within a square map of 408 x 408.
Approximately 100,000 plots of land have been minted. Each plot of land is 96m x 96m and allows owners to create any
game or experience they wish to build out. Estates can be created by combining multiple lands together and districts can
be formed by creating a collective with other estate owners. Land plots must be adjacent, and two landowners must be
staking $SAND in order to form a district. Along with that, approval of a district has to pass through a majority vote
within the DAO. You can find the number of plots for estates or districts within the smart contract transaction
information. (I wasn’t able to find this myself when looking into this, but a Sandbox staff member said it was available
with custom tools)

If you own two adjacent parcels/estates, you will be able to deploy scenes to both of the parcels without them being
combined. If you form a district with another adjacent estate, then you will only be able to deploy scenes to the
district you formed.

Once the metaverse client is live, scene/game experience publishing will require Sandbox’s servers/nodes to request a
signed message from the owner to verify they either own land or have rental permission to publish experiences and
utilize said land. According to Discord moderators of Sandbox, more information regarding the metaverse client will be
coming to fruition soon.

Currently there are no `operator` roles that have permission to deploy scenes to the land. The Sandbox team has it as a
concept but haven't released it yet.

When it comes to custom icons on the metaverse map, any land can have preview images, but you will need to have an
estate (3x3 or larger) to upload a map icon. If someone rents an estate, they should be able to upload a custom map icon
during the duration of their rental (yet to be confirmed from the Sandbox). There are no details on how this process
will be implemented, but further information regarding this topic should be announced in the near future.

Addresses and source code of important contracts:

- $SAND (ERC-20) contract
  address: [0x3845badade8e6dff049820680d1f14bd3903a5d0](https://etherscan.io/address/0x3845badade8e6dff049820680d1f14bd3903a5d0#code)
- LANDs (ERC-721) contract
  address: [0x50f5474724e0Ee42D9a4e711ccFB275809Fd6d4a](https://etherscan.io/address/0x50f5474724e0ee42d9a4e711ccfb275809fd6d4a#code)
- ASSETs (ERC-1155/ERC-721 NFTs made by users) contract
  address: [0xa342f5D851E866E18ff98F351f2c6637f4478dB5](https://etherscan.io/address/0xa342f5d851e866e18ff98f351f2c6637f4478db5#code)
  (I believe the ASSETs contract and source code with correlate with the marketplace as that is the only thing available
  in the native marketplace currently)

Sources:

- [https://sandboxgame.gitbook.io/the-sandbox/](https://sandboxgame.gitbook.io/the-sandbox/)
- [https://medium.com/sandbox-game/the-sandbox-gets-greener-reducing-nft-carbon-footp](https://medium.com/sandbox-game/the-sandbox-gets-greener-reducing-nft-carbon-footp)
- [https://github.com/thesandboxgame](https://github.com/thesandboxgame)

# Actionable Items (Core Team input)

The only hurdle integrating Sandbox is the fact that they do not have a `contributor/consumer/operator` role build in
the contracts. Since they are currently under development and havent released their client yet, it would be wise to
contact the development team with proposal to
utilise [EIP4400](https://ethereum-magicians.org/t/erc-4400-erc721consumer-extension/7371) or contribute to them the
implementation needed.


