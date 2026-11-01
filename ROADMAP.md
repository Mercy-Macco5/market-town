# MarketTown Development Roadmap

This roadmap tracks the planned work for the NEAR Hackathon 2026. Items are marked complete only when the work exists in the repository and has been checked.

## Stage 1: Design and setup

- [x] Create the public GitHub repository.
- [x] Write the initial project overview.
- [x] Document the 30-second, 5-minute, and session game loops.
- [ ] Review the NEAR hackathon instructions and Games With Real Economies requirements.
- [ ] Choose a suitable 2D game starter template and check its license.
- [ ] Set up the local development environment.
- [ ] Add a README setup section with steps that can be followed and verified.

## Stage 2: First playable game

- [ ] Start the game and show a basic town scene.
- [ ] Add player movement and collision.
- [ ] Add mobile-friendly touch controls and desktop keyboard controls.
- [ ] Add gatherable resources.
- [ ] Add player inventory.
- [ ] Add the three merchant shops.
- [ ] Add basic buying and selling.

## Stage 3: Living economy

- [ ] Add merchant stock and cash balances.
- [ ] Add a readable merchant pricing rules file.
- [ ] Make prices respond to stock and recent demand.
- [ ] Show players why a price changed.
- [ ] Add merchant trading and restocking behaviour.
- [ ] Add shop closure when a merchant can no longer operate.
- [ ] Add player investment and shop reopening.

## Stage 4: Town Time

- [ ] Add a control to start fast-forward mode.
- [ ] Simulate one in-game week in about 60 seconds.
- [ ] Show stock, prices, and merchant balances changing.
- [ ] Make the simulation repeatable for testing and judging.

## Stage 5: NEAR integration

- [ ] Confirm the NEAR contract and account architecture.
- [ ] Implement NEP-245 item tokens on testnet.
- [ ] Connect the game to the token contract.
- [ ] Add social or email sign-in.
- [ ] Implement and test merchant wallet-backed agents.
- [ ] Keep routine gameplay smooth without wallet popups or gas prompts.

## Stage 6: Testing and submission

- [ ] Test the full game loop from a fresh player session.
- [ ] Test mobile and desktop layouts.
- [ ] Test price changes, merchant bankruptcy, and investment.
- [ ] Add clear "do this, see this" test steps to the README.
- [ ] Record a short demo showing the economy changing.
- [ ] Publish the demo post on X and mention the NEAR Hackathon.
- [ ] Check the public repository for secrets and unfinished claims.
- [ ] Prepare the required hackathon submission details.

## Current milestone

Design and repository setup.

The next milestone is to choose and inspect the game starter template before adding game code. The starter should be suitable for a small 2D game, support mobile and desktop controls, and have a license that allows hackathon use.
