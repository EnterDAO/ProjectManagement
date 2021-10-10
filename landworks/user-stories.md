# User Stories

**Legend**

- **Lender** - User that has already connected his wallet & either wants or already has properties that he provided for renting at LandWorks. All user stories specified for normal users are applicable to lenders.
- **Renter** - User that has already connected his wallet & either wants or already has properties that he rents at LandWorks. All user stories specified for normal users are applicable to renters.
- **Property** - A single parcel or a single Estate (LAND/Estate in the case of Decentraland)

## General

1. As a user, I must be able to see a list of all properties listed in LandWorks
2. As a user, I must be able to filter & sort properties:
    1. Sort by rent price
    2. Filter by availability - when it can be rented & for how long in the future
    3. Filter by Metaverse (only Decentraland for now)
3. As a user, I must be able to see the details of a given property:
    1. Title/Description
    2. Location (Metaverse + Coordinates)
    3. Who is the Lender
    4. Is the property currently available or if not, the start time at which the user can rent it
    5. The maximum time a user can rent the property
    6. The minimum time use can rent the property
    7. Current rent price & price history
        1. Diagram of the rent price history (if present)
    8. Rent history
        1. History of renters of the property, for how long and how much
    9. Pooling
        1. List of other properties that are listed and are adjacent to the property being viewed
4. As a user, I must be able to update the ruler for a given property

## Connecting Wallet

1. As a user, I must be able to "Sign In" by connecting a wallet through:
    1. Metamask
    2. Ledger
    3. Portis
    4. Trezor
    5. Coinbase
    6. WalletConnect

## Lender User Stories

1. As a lender, I must be able to "List Property" by specifying the following details:
    1. From which Metaverse is the property?  (for now only Decentraland)
    2. The property he wants to lend (the UI will automatically show all properties owned by the user for the specified metaverse)
    3. The minimum rent period  (measured in blocks, but for simplicity, there will be an approximation to days f.e)
    4. The maximum rent period (measured in blocks, but for simplicity, there will be an approximation to days f.e)
    5. The maximum time in the future that the property can stay rented (the delta after which the protocol will not allow for the property to be rented). Useful for property owners to restrict the renting time and have their property "liquid" (to be removed from the marketplace) (measured in blocks, but for simplicity, there will be an approximation to days f.e)
    6. Payment options - ETH or a whitelisted set of ERC20 tokens (configured in the protocol by EnterDAO)
    7. Rent price - the price of the property per block (measured in blocks, but for simplicity, there will be an approximation to days f.e)
2. As a lender, I must be able to see all my listed properties
3. As a lender, I must be able to see my unclaimed rent for a given property
4. As a lender, I must be able to claim my accrued rent for a given property
5. As a lender, I must be able to claim my accrued rent for multiple properties
6. As a lender, I must be able to update my lending conditions.
    1. Minimum rent period
    2. Maximum rent period
    3. Maximum time in the future that the property can stay rented
    4. Payment option
    5. Rent price

## Renter User Stories

1. As a renter, I must be able to "Rent" a property by specifying:
    1. The period of time for which I am renting it
    2. (Optional) the `operator` address that will be authorised to deploy scenes to the rented land
2. As a renter, when I am at the point of renting a property, I must be able to see "Pooling" information, that is if there are any adjacent properties listed / available that I can rent as well in order to make my overall rented property bigger.
3. As a renter, I must be able to see all my rented properties
4. As a renter, I must be able to change my `operator` address for a given rented property