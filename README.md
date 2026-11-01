# MarketTown

MarketTown is a 2D pixel-art economic simulation game being developed for the NEAR Hackathon 2026, Games With Real Economies track.

The idea is simple: explore a small town, gather useful materials, trade with merchants, and help shape the town's economy. Each merchant manages their own stock and money. Prices change as goods become scarce or abundant, and a merchant can run out of money and close their shop.

> Project status: planning and design. The playable game and blockchain features are not implemented yet.

## The idea

In many games, shops have fixed prices and unlimited stock. MarketTown is designed around a living economy. Merchants respond to what players buy and sell, so player activity can change the town.

The first version will focus on a small, understandable game loop rather than a large world.

## How the game is planned to work

1. Explore the town and gather resources such as wood, stone, iron, and food.
2. Visit merchant shops and check their current stock and prices.
3. Buy and sell items, or complete requests from merchants.
4. Watch prices respond to supply and demand.
5. Help a struggling merchant by investing in their shop.
6. Build up enough resources and money to work towards running a business of your own.

These are planned interactions. They will be updated as they are implemented and tested.

## The first merchants

- **Blacksmith:** trades iron, tools, and other metal goods.
- **Farmer:** trades food and agricultural goods.
- **General Merchant:** trades everyday supplies.

Each merchant is planned to have an independent wallet, inventory, and pricing rules. Their prices should respond to stock levels and recent demand. The game will explain why a merchant changed a price.

## The game loop

- **Every 30 seconds:** explore, gather a resource, check a shop, or make a small trade.
- **Every 5 minutes:** complete a supply request, make a larger trade, compare merchant stock, or decide whether to invest in a struggling shop.
- **Every session:** grow your inventory and wealth, influence the town's economy, and work towards a longer-term goal such as opening your own shop.

Merchants should continue making decisions as the town economy changes.

## Town Time

Town Time is a planned fast-forward feature. It will simulate one in-game week of trading in about one minute. Players and judges should be able to watch stock, prices, and merchant finances change during the simulation.

## NEAR integration

The project is being designed around the Games With Real Economies track requirements:

- Use NEP-245 multi tokens for game items, so one contract can represent different item types.
- Support social or email sign-in, keeping wallet setup out of the normal game loop.
- Give each merchant an on-chain wallet or wallet-backed agent as the implementation allows.
- Keep merchant pricing rules in one readable file and show the reason behind price changes.
- Include Town Time to make the economy easy to observe.

The exact contract and agent architecture will be documented before implementation. No blockchain feature should be described as complete until it is working and tested.

## Development status

- [x] Create the public project repository.
- [ ] Finalize the game design and first playable loop.
- [ ] Choose and set up the game starter template.
- [ ] Build the town scene and player controls.
- [ ] Add resources, inventories, and merchant shops.
- [ ] Implement supply-and-demand pricing.
- [ ] Add merchant finances and shop closure/reopening.
- [ ] Add Town Time simulation.
- [ ] Integrate NEAR testnet and NEP-245.
- [ ] Add social or email sign-in.
- [ ] Test the game on mobile and desktop.
- [ ] Record a demo and prepare the hackathon submission.

## Running the project

There is no playable build yet, so there are no run instructions at this stage. Setup and test instructions will be added once the game template and first build are in place.

## Project documents

- [Game design](GAME_DESIGN.md)
- [Development roadmap](ROADMAP.md)

## Built for

NEAR Hackathon 2026  
Track: Games With Real Economies
