# Enemies of the Realm

A Rare Friends strategy game built on FriendSDK v0.1.2.

March your Rare Friend out of its Realm, raid other players' Realms, mine resources, and defend your own. Powered entirely by $RAREFRIENDS (RF). No separate token.

## The loop

1. **Signup** — email in via Privy, one RF airdropped as a permanent play-pass. Your Friend materializes.
2. **Build** — spend RF above the reserve floor to recruit troops, expand your Realm, and upgrade defenses.
3. **Raid** — march your army to another player's Realm, loot resources, and bring them home.
4. **Mine** — send scouts to unexplored tiles to find gold, lumber, and rare nodes.
5. **Defend** — fortify walls and traps so raiders come home empty-handed.

## Reserve floor

The airdropped RF is a permanent play-pass. Game logic never lets your spendable balance drop below **1 RF**, so your Friend never vanishes mid-session. All purchases debit from the balance above the floor. Hit the floor and the game nudges you to top up — the V-Bucks moment.

## Run locally

```sh
git clone https://github.com/spokesz/friendsdk.git
cd friendsdk && npm ci
# then point dev:game at this game, or install the package and run:
npx friendsdk dev ./games/enemies-of-the-realm
```

Open the displayed URL (normally http://localhost:4173), connect a wallet on Robinhood mainnet (chain 4663) holding a hardwired Generations NFT, and play.

## Economy (game.json)

| Action | Cost | Notes |
| --- | --- | --- |
| Recruit 1 troop | 1 RF | Spendable above floor |
| Expand Realm tile | 5 RF | Permanent build |
| Raid a Realm | 2 RF | Loot scales with target size |
| Mine a node | 1 RF | Rewards gold/lumber/rare |

All simulated in preview mode. Live mode requires a deployed contract.

## Visual style

Hand-painted, fog-of-war minimap, isometric isometric worlds — nodding to classic Warcraft II (1995) and the original Rare Friends on-chain art.

## Status

MVP scaffold. Next: Privy email signup, airdrop + reserve floor enforcement, raid/mine/defend UI, and onramp for RF top-ups.