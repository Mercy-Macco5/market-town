# MarketTown Game Design

## 1. Overview

MarketTown is a 2D pixel-art town simulation where the economy is the main game mechanic. Players gather resources, trade with merchants, complete supply requests, and gradually influence the town's economy.

The first version should be small enough to build and test during the hackathon. It should still show a complete economic loop that judges can understand by playing or watching a short demo.

Current status: design document. The mechanics below are planned, not yet implemented.

## 2. Main player goal

Start as a new arrival with limited resources. Learn what the town needs, gather or buy useful goods, sell them at the right time, and build enough wealth and trust to take part in running a business.

The player should have meaningful choices:
- Sell an item now for a quick return, or hold it because demand may rise.
- Gather a resource that is scarce, or focus on a merchant request.
- Invest in a struggling merchant, or save money for a future shop.
- Buy low when a merchant has excess stock, then sell when another merchant needs that item.

## 3. Core loop

### Every 30 seconds

The player should be able to:
- Move around the town.
- Gather a nearby resource.
- Enter a shop or open its trading interface.
- Check an item's price and stock.
- Buy or sell a small amount of goods.

The short loop should always offer a clear action without forcing the player to read long instructions.

### Every 5 minutes

The player should be able to:
- Complete a merchant's supply request.
- Make a larger trade based on price differences or changing demand.
- Compare stock across the three merchants.
- See whether a merchant is low on funds or goods.
- Invest in a struggling merchant when that option is available.

This loop should create short-term goals and reward players who pay attention to the economy.

### Every session

The player should:
- Build up money, resources, and useful items.
- Learn which goods are in demand.
- Influence merchant stock and prices through trading.
- Help keep important shops open.
- Progress towards opening or owning a shop.

The town should continue to feel active as merchants restock, trade, and react to changing conditions.

## 4. First playable town

The first map should be one compact town with:
- A central square.
- A resource-gathering area.
- A blacksmith shop.
- A farm or produce stall.
- A general store.

Keep the map small and easy to navigate. The goal is to make the economy playable, not to build a huge world.

## 5. Resources and goods

Initial gatherable resources:
- Wood
- Stone
- Iron
- Food

Initial trade goods:
- Basic tools
- Metal goods
- Farm produce
- Everyday supplies

The exact item list and quantities will be narrowed during implementation so the first version stays achievable.

## 6. Merchant agents

Each merchant should have:
- An identity and role.
- An inventory with stock limits.
- A wallet or tracked balance.
- A list of goods they buy and sell.
- Pricing rules based on stock and recent demand.
- A simple record of recent transactions.
- A state such as open, low on funds, or closed.

Initial merchants:

### Blacksmith
Trades iron, tools, and metal goods. The blacksmith needs iron to produce or restock tools.

### Farmer
Trades food and agricultural goods. Food availability should change with deliveries and player purchases.

### General Merchant
Trades everyday supplies and can act as a link between goods produced by the other merchants.

## 7. Pricing rules

Merchant prices should change in response to supply and demand. A simple first model is preferable to a complicated system that is hard to explain or balance.

Possible inputs:
- Current stock compared with a target stock level.
- Recent purchases and sales.
- Merchant cash balance.
- A minimum and maximum price for each item.

A merchant with excess stock should lower its selling price. A merchant running low on an item that players want should raise its price within configured limits.

All pricing logic should live in one readable file. The trading interface should show a short explanation, for example: "Iron is cheaper because the blacksmith has more stock than usual."

Exact formulas and limits will be selected and documented before the pricing system is coded.

## 8. Merchant finances and investment

Merchants should spend and earn money through trades. If a merchant runs out of money or cannot maintain its shop, it may close.

A player should be able to invest in a closed or struggling shop under clear rules. Investment should give the merchant enough funds or stock to reopen, and the player should see what the investment changed.

The first version should avoid promising real-world financial returns. Investments are a game mechanic.

## 9. Town Time

Town Time is a fast-forward simulation that compresses one in-game week into roughly 60 seconds.

During the simulation, the player should be able to observe:
- Merchants buying and selling goods.
- Inventory levels changing.
- Prices moving as supply and demand change.
- Merchant balances rising or falling.
- A shop struggling, closing, or reopening after investment.

The simulation should be repeatable so a judge can trigger it and see the economy respond.

## 10. NEAR and digital ownership

Planned NEAR integration:
- NEP-245 multi tokens for item types.
- Social or email sign-in so players do not need to manage seed phrases or approve routine wallet popups during normal play.
- Merchant wallet-backed agents or an equivalent testable wallet model.
- Testnet-first development.

The game should keep blockchain activity out of the way during ordinary movement and trading. The chain should support the economy rather than interrupt the player.

Implementation details, contract methods, and transaction boundaries must be confirmed against current NEAR documentation before coding.

## 11. First-version scope

Must have:
- One compact town.
- Basic player movement.
- Resource gathering.
- Three merchants.
- Inventory and trading.
- Dynamic prices.
- Merchant balances and shop status.
- Investment to reopen a struggling merchant.
- Town Time simulation.

NEAR requirements to integrate and demonstrate:
- NEP-245 item tokens.
- Social or email sign-in.
- Wallet-backed merchant agents.

Can wait until after the core loop works:
- Large maps.
- Multiplayer.
- Complex crafting trees.
- Many merchant types.
- Cosmetic collections.
- Real-money rewards or token incentives.

## 12. Design principles

- Make the game understandable within the first minute.
- Give players a useful action every 30 seconds.
- Make economic changes visible, not hidden in code.
- Explain why prices change.
- Keep the first town small and polished.
- Never label a planned feature as complete before it has been tested.
