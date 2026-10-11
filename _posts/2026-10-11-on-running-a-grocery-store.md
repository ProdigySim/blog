---
layout: post
title: "On running a grocery store"
---

Running a Magic: The Gathering singles selling shop has been quite interesting. There are a lot of other people running similar operations, and yet there is still room for me to be successful here. I think this is primarily owed to two factors: 

1. The game is in a boom cycle right now, with more players than ever getting into the game and record amounts of new cards being released.
2. Wizards of the Coast's choice to use randomized distrubtion of cards in packs--which is unfortunately a "loot box" mechanic--directly enables a healthy secondary market for cards.

The latter of these two points is vastly intriguing to me. At face value, especially as a younger player, this type of system feels predatory. My puritanical midwestern roots may be showing, but these gacha mechanics inherently feel anti-consumer to me.

However, in contrast to other gaming communities I've been in, this random-pack business model provides very easy avenues for people to build businesses around the game. One of the constant struggles in other competitive gaming spaces (especially esports) is building a sustainable, positive community around the game. There are small pockets of money available in other games: running tournaments, doing content creation, selling accessories or tools. But it's incredibly hard to make any of those sustainable without significant scale.

I've long felt like there is value in creating positive spaces through gaming. Whether you're [playing an FPS to increase neuroplasticity and visual attention ability](https://direct.mit.edu/jocn/article-abstract/24/6/1286/27781/Playing-a-First-person-Shooter-Video-Game-Induces), or analyzing options in a card game with [fully disjunctive reasoning](https://www.psychologicalscience.org/news/were-only-human/uncommon-sense-toward-an-rq-test.html), there are real cognitive benefits to gaming--particularly when playing competitively. And I believe there can be great social developmental benefits as well when the environment is positive. Maybe a future blogpost can be "Top Five things I gained from playing Left 4 Dead 2".

That digression aside, the slightly more practical problem I find myself focusing on today is "What value does a Magic card sellling business provide?" I want to understand why running a TCG business works, what roles it plays for different people, and where it can evolve and grow. 

My experience primarily as a software developer leads me to think about this in terms of use cases and scenarios. But more plainly, I think about what function the business serves to different groups of people:

1. Providing a place to meet people and play the game.
2. Providing tournaments / organized play events to players.
  - This also serves Wizards of the Coast by helping legitimize and standardize play experiences.
3. Providing retail packs or decks of cards to players.
4. Providing individual cards players are seeking for their decks or collections.
5. Providing liquidity to players or other businesses who have cards they do not want by buying cards.
6. Providing a marketplace for cards to help with valuation and data collection for WotC, businesses, players, to make informed decisions.

As I've grown a bit and found new purchase opportunities, I've started to understand more how we serve not just the players, but also WotC in terms of solving the last mile distribution problem for them. We figure out the "most efficient" way to distribute cards to players, and ensure players can find the cards or products they need.

I don't currently have desires to operate a game store--I worked retail very early on in my life and was quite bad at it. It's only now after having a real income for many years that I understand what consumers expect from businesses for customer service. So, my focuses are primarily on the **Providing individual cards to players** portion.

Even this category has a wide variety of use cases hidden within:

1. Commander players seek a wide variety of unique cards, to add 1x each to their decks.
2. Constructed 60-card format players generally seek 4x of a smaller set of meta-relevant cards.
3. Collectors or deck-blingers seek a small number of specific printings of cards.
4. Professional deck builders seek large quantities of a wide variety of cards to resell as a unit.
  - Cube makers probably fall into this category as well
5. Speculators seek large quantities of single cards to make bets on their future value.
6. Other TCG shops seek moderate quantities of a wide variety of cards to shore up their own inventory.

These are my primary customers. They generally are happy to pay market rates for their cards, and they're happy for the service we provide. We take on the risk and logistics of inventorying large quantities of cards and making them available. As long as [The Prof keeps telling people to just buy singles](https://www.youtube.com/watch?v=YdX5vRkZvJ4), this seems like a happy compromise. Players avoid the gambling aspects of the game, and people like me who enjoy sorting and sifting can operate as Banks, turning capital into specific cardboard when the market demands it. When players ask for more high-powered cards for their decks, the Expected Value of a MH3 booster box goes up, and we can purchase the packs, open them, and redistribute the cards for a small profit.

But I don't primarily think of my operation as a bank. Instead, I think it's more like a grocery store. Players come in to buy Produce, Meat, and Dairy (Sol Ring, Command Tower, Llanowar Elves), and also pick up their favorite cereal, some frozen goods, and laundry detergent (random other cards) while they're here. Since I operate within [Manapool](https://manapool.com/shop/psimtcg), almost every order I receive is a subset of a large list of cards a player gives to a [Cart Optimizer](https://manapool.com/add-deck). I only win a sale if I can provide the best price on a significant list of cards, after shipping costs are taken into account.

This leads to a delicate balance: If I don't have enough staples available, players will primarily seek other stores. If I don't have enough variety of cards available, I will only sell the staples, sell out fast, and be left with large quantities of low-demand cards I'm unable to move. A grocery store with only milk and eggs would find it hard to maintain a profit, but a grocery store with only non-perishable boxed goods would find it hard to attract foot traffic.

This probably isn't true for every magic shop--some have distribution from WotC that changes a lot of the math. Some have established card-buying operations where they can get cards from players for cheap. But for me, for now, my primary strategy is to provide a wide variety of cards--to be a large grocer like a Walmart or Kroger, where you can go in and expect to find everything you need.

There are **over 33,000 unique cards** in Magic, and over 100,000 when you count alternate printings. This is actually a lower number than I expected. As of this writing, my shop's inventory has between $10-20k of cards, and currently covers 7,805 unique cards, and just over 10,000 when you count alternative printings.

```ts
const myinv = await mySinglesByScryfallId(manapoolPublic, { useCached: true });

const withCards = await Array.fromAsync(retrieveManyScryfall(Object.keys(myInv)));

const oracleIds = new Set(withCards.map(x => x.oracle_id));

const totalCardboardPieces = Object.values(myinv).flatMap(i => i.map(l => l.quantity)).reduce((acc, next) => acc+next, 0);

console.log("Total:", totalCardboardPieces, "Printings:", Object.keys(myinv).length, "Unique:", oracleIds.size);

// Total: 41031 Printings: 10075 Unique: 7805
```

I would consider this "not bad!" I have no estimate for how many cards are actively sought by players, but having just under a quarter of all cards at my scale seems great. I doubt I'll ever get to 100%, but I would bet some of the larger stores are near that if not full.

So, as far as the challenge of maintaining an inventory goes, I feel pretty on top of it. This is a largely illiquid business--PSim TCG has far more in cardboard than in cash. Being able to stay on top of inventory health in spite of this feels like a good accomplishment.

There are a lot more nebulous problems still to tackle though, especially currently being a 1-man operation. How should I prioritize what software I build? How do I track profitability? What larger role can my operation play, and how should I get there? Should I diversify? There's a good amount of learning and soul-searching I will need to even start on these. Maybe some opportunities for future blog posts. I need to spend some time doing some real hacking, too :)

PSim Out
