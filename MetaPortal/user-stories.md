# User Stories

The app will be built with Electron.

## [EPIC-01] Authentication and Login

Description: Once this epic is complete the user will be able to sign up/sign in with a wallet.

Related to: EPIC-02, EPIC-03, EPIC-04

### [S01] As a user I want to be able to login into the application via creating a new in-app wallet

Description: Once the user opens up the application, they should be able to login with "New MetaPortal In-app Wallet". This should generate a new wallet, cache it in the local persistent storage and display the user mnemonic seed-phrase for them to backup. Once the process is complete I want to be redirected to the app homescreen.

### [S02] As a user I want to be able to login into the application via previously created in-app wallet

Description: Once the user opens up the application, they should be able to login with "Existing MetaPortal In-app Wallet". This should allow the user to input seed-phrase, private key or json file+password and login with the wallet. The wallet should be cached in the local persistent storage. Once the process is complete the user should be redirected to the app homescreen.

### [S03] As a user I want to be able to login into the application via WalletConnect

Description: Once the user opens up the application, they should be able to login with "Wallet Connect". This should allow the user to connect their mobile wallet with the app and use the mobile wallet for authentication and further transactions.

### [S04] As a user I want to be redirected immediately to the homescreen if I have local wallet cached.

Description: If the user has local wallet cached, they should be directly cached until they logout

## [EPIC-02] Settings & Profile

Description: Once this epic is complete the user will be able to add information about their profile and change the application settings.

Related to: EPIC-03

### [S05] As a user I want to be able to access my profile and settings screen

Description: The user should have a button or menu allowing them to enter the profile an settings screen

### [S06] As a user I want to be able to see information about my wallet and blockchain connection

Description: Once the user opens up the profile screen they should be able to see section/tab about their wallet and blockchain connection. The user should be able to see their address, their crypto balance for selected coins/tokens (starting with ETH and $ENTR) and see information about the network they are connected to (ETH Mainnet, Polygon, etc).

### [S07] As a user I want to be able to backup my wallet from the wallet section of the profile screen

Description: The user should have two options of backing up their wallet. First option allows them to see their private key and copy it. Second option is enabling them to download their wallet in the form of json file encrypted by a password of their choosing.

### [S08] As a user I want to be able to change the network I am connected to in the profile screen

Description: The user should be able to change the network they are connected to via the profile screen. Once the network is changed he user should see their updated balances. At first only the Ethereum Mainnet will be supported.

### [S09] As a user I want to be able to link my email and username to my wallet

Description: The user should be able to link their email and username to their wallet address from the profile page. This should create a record in the local persistence layer. This should also create a record in a remote service that can use the email for notifications.

### [S10] As a user I want to be able to upload an avatar for my profile

Description: The user should be able to upload an avatar image for their profile. The avatar should be linked to the user wallet and be stored in decentralised storage (Areweave, IPFS, etc).

### [S11] As a user I want to be able to logout

Description: The user should be able to log out of the application through the settings and profile screen.

## [EPIC-03] Wallet Connection

Description: Once this epic is complete the user will be able to use Native wallet or Wallet connect for sign in, recover their wallet and see information about their wallet.

Related to: EPIC-01

### [S12] As a developer I want to have an abstract wallet connection

Description: We should create an abstract wallet connection interface that can be implemented by the specific wallet connections - in-app wallets and wallet connect.

### [S13] As a user I want to be able to connect via my in-app wallet

Description: The user should be able to connect to dApps via the in-app wallet of the application. The dapp required interactions (signing messages for login, sending transactions) should happen via the user confirming in the app (UI flow analysis is required).

### [S14] As a user I want to be able to connect via WalletConnect

Description: The user should be able to connect to dApps via WalletConnect. The dapp required interactions should happen via the user confirming through the mobile app.

#### [Research] Find possible ways to connect with Metamask

Description: Research if there is any way to connect with the user browser metamask as wallet connection

## [EPIC-04] Homescreen

Description: Once this epic is complete the user will be able to see the Homescreen of the application and see games and events.

Related to: EPIC-05

### [S15] As a user I want to be able to see the Homescreen once I've logged in

Description: Once the user has logged in they should be able to see the homescreen. The user should see two distinct sections - for games and for events.

### [S16] As a developer I want to be able to fetch a list of supported games from a backend service

Description: The app should be able to fetch a list of the supported games from a backend service. The backend service will be populated from an admin in the content management section.

### [S17] As a user I want to be able to see a list of supported games in my homescreen

Description: The games fetched from S16 should be seen in the homescren UI where the user can interact with them based on their state.

### [S18] As a user I want to be able to start a web based game from the homescreen

Description: When the user clicks the play button of a web based game in the games list, the game should immediately launch in separate fullscreen window and be connected with their connected wallet.

### [S19] As a developer I want to be able to detect if a desktop game is installed or not

Description: As a developer I need to know if a certain game is installed or not so that I know If I should install it or launch it.

### [S20] As a user I want to be able to install a desktop game from the homescreen

Description: When the user clicks the install button of a desktop game in the games list, the game should walk them through downloading and installing the game. If the desktop game is already installed no install button shall appear, but rather a play one.

### [S21] As a user I want to be able to start a desktop game from the homescreen

Description: When the user clicks the play button of an install desktop game in the games list, the game should immediately launch in separate window.

### [S22] As a developer I want to be able to fetch a list of relevant metaverse based events from a backend service

Description: The app should be able to fetch a list of the relevant events for the user wit htheir information like links and time. The backend service will be populated from an admin in the content management section.

### [S23] As a user I want to be able to see a list of metaverse based events

Description: The user should be able to see a list of upcoming metaverse based events they can participate in.

### [S24] As a user I want to be able to see the information of a metaverse based event

Description: The user should be able to see the detailed information about metaverse based event from the events list.

### [S25] As a user I want to be able to add the information about metaverse based event to my callendar

Description: The user should be able to add a reminder for this event to their calender.

### [S26] As a user I want to be able to enter a metaverse based event

Description: The user should be able to choose to Enter (cool pun on the ENTER DAO name would be good here) an event of their choosing from the list. If the game this event is hosted in is a web-based the user should directly go to the event coordinates if possible. If the game this event is hosted in is desktop based the game should be launched.

## [EPIC-05] Content Management

Description: Once this epic is complete the admins of the MetaPortal will be able to add games and events to be displayed in the app. It is good idea in the future for this to be curated via Token Curated Registries.

### [S27] As an admin I need to be able to authenticate

Description: The admin should be able to authenticate in order to perform list management operations. This should happen through a website.

### [S28] As an admin I want to be able to modify the displayed metaverse games list

Description: The admin should be able to add meta add/remove metaverse games that can be displayed in the application.

### [S29] As an admin I want to be able to modify the events list

Description: The admin should be able to add/remove events to be displayed in the application.

## [EPIC-06] Delight

Description: Once this epic is complete, the application will be delightfully sensory pleasing!

### [S30] As a user I want to experience pleasing audio effects in the application

Description: The application should have pleasing, game-type experiences through audio cues.

### [S31] As a user I want to experience pleasing animation effects in the application

Description: The application should have pleasing, game-type experiences through animations and motion graphics.

## [EPIC-07] Download webpage

Description: Once this epic is complete the user will be able to download the installation file for the application for their OS.

### [S32] As a user I want to be able to download an installer for my OS

Description: The user should be able to go to a webpage that allows them to download the installer package for their OS

### [S33] As an admin I want to be able to upload new version of the installer for certain OS

Description: The admin should be able to upload new version of the installer for given OS.

## [EPIC-08] Auto update

Description: Once this epic is complete the application should be able to autoupdate.

### [S34] As a developer I want my application to detect if a newer version is available

Description: The application should be able to detect if there is an update to be installed.

### [S35] As a user I want my application to ask me if I want to update

Description: The user should be able to proceed or not with an auto-update

### [S36] As a developer I want an update to the application to be applied

Description: The application should be able to get updated

---

- Filters
- Rethink the experience of creating account
- Link to metamask account through message signing - like the gods unchained thing - to link your metapass and real account