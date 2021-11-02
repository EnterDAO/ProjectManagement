# CryptoVoxels Metaverse Report

By caju

CryptoVoxels (CV) is a virtual world, built on the Ethereum blockchain (ERC721 Token), where players can explore, create
avatars, buy land, build art galleries, stores, and any other type of buildings or installations. The aesthetic of CV is
voxel art - a type of art form where 3D models are constructed entirely out of 3D cubes called voxels.

The world consists of Origin City, the capital and the main island, and smaller surrounding islands. Origin city is
split into multiple districts varying in sizes, with streets and parcels. Parcels are owned by individual people, and
anyone with an Ethereum wallet can buy one.

The world has neighborhoods, where each suburb was originally built with a theme in mind, however, these themes are not
enforced and players are free to build what they want. This led to suburbs with an amazing diversity of builds! There
are also multi-suburb player-made districts that result from the collaboration of builders.

Anyone with a browser can explore CV. You don't need an Ethereum wallet or a parcel, and it's compatible with VR (Oculus
Quest, Oculus Rift, and HTC Vive).

Cryptovoxels doesn't have a native Marketplace. Instead, it has a UI Marketplace for wearables and land, that links back
to Opensea for purchases.

For primary sales, you can purchase a Cryptovoxels parcel by hopping onto the Opensea Cryptovoxels page and sorting by "
Recently Created". A parcel being sold in a primary sale will be owned by bnolan. If it is not owned by him, it is a
secondary sale!

There are usually about 15 to 30 parcels listed for auction every Wednesday. Often, bnolan will randomly accept bids on
new parcels just before the auctions start.

You can buy multiple parcels next to each other, but they will act independently of each other (different names, their
own limit of objects, etc). If this is something you would want to see in CV, the team accepts ideas on the forum. They
read everything and are very close with the community. At the moment there is no technical support for renting parcels (
although that's something the team might be looking into). Right now, the best way to rent is by adding someone as a
contributor on a parcel, for a specific period.

This contributor (or multiple ones) don’t have access to sell the land, and they will be there indefinitely until you
remove their access. As we know, a temporary feature is very useful, especially for renting out, and already have shared
this idea with the team. Parcels have different sizes, and there's a max of 48 height, 60 width, and 106 depth.

To edit and publish on the Land, there's no need for signed transactions. The only requisite is to be the owner or
contributor of the parcel.

At the moment, there’s no way to access contributors through Smart Contract, only manually (or scraping) through the
website. One thing that may be a solution for this is to move the parcel into a multi-sig, and by doing that, the tenant
would be able to edit the land, but not sell/trade without the multi-sig.

CryptoVoxels is based on the Ethereum blockchain. CV properties are ERC721 tokens.

- [Parcel](https://etherscan.io/address/0x79986af15539de2db9a5086382daeda917a9cf0c)
    - [code](https://github.com/cryptovoxels/contracts/blob/master/contracts/Parcel.sol)
- [Other Contracts Source Code](https://github.com/cryptovoxels/contracts)

## My thoughts (bonus section):

### Why integrate CryptoVoxels with Landworks

1. It's one of the first Metaverses (alongside Decentraland), and has probably the best onboarding experience, certainly
   the most straightforward one, since you just need a browser and the link to the coordinates you want to spawn. No
   need for a wallet, making an avatar, or inputting any data like username or email.
2. It is extremely easy to build on the world. You just open the build menu with TAB and build intuitively like
   Minecraft. Any new player/metaverse user will have a much easier time building on Cryptovoxels vs other Metaverses (
   at least for now). This helps a user be more creative, and so it leads to my next point.
3. The world is filled with content. Artists from all around the world have created galleries and installations. To
   follow art and business events one needs to be part of each micro-community to know when and where they are taking
   place. At the moment I would say this is one of the most artistic/free metaverses.

### How hard would it be to integrate Landworks with CryptoVoxels + design proposal

At the moment, there’s no way to access contributors through Smart Contract, only manually (or scraping) through the
website. One thing that may be a solution for this is to move the parcel into a multi-sig. The owner would be the smart
contract, and that contract would have ownership represented by tokens or NFTs.

The website requires a signed message from the owner to log in, and once logged in, the owner gets a temporary cookie
that is used in place of signatures. To log into the website, the multi-sig would sign a message, then the user would be
signed as the multisig contract, without owning the key, and they would have that cookie which would let them do the
off-chain activities like editing the land, but wouldn't be able to transfer ownership.

We can also try to talk with the team and check if it’s possible to develop a better system for them, or if they are
thinking about building one in the near future.

# Actionable Items (Core Team input)

Unfortunately if we cannot get the `contributor` through a smart contract and if its purely off-chain solution, we won't
be able to utilise that role. The suggestion provided is to make the renter partial `owner` without permissions to
transfer the land, however this has problems as-well. When deploy scenes, you need to provide a signature to provide a
proof that you are the owner of the land and if we are using a multi-sig wallet, we cannot provide a signature signed by
a multi-sig.

There is no such feature in the EVM that allows you to sign a message through a smart contract since smart contracts do
not have private keys as EOA do. That means that the viable option would be to approach the team and pitch them the idea
of the
[EIP4400](https://ethereum-magicians.org/t/erc-4400-erc721consumer-extension/7371) proposal and hopefully get them
onboard.

