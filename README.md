# Peaceful Groupies Rarity
Provided without warranty. For ui visit [https://nftjoy.club/groupies](https://nftjoy.club/groupies)


# Important: rarity calculation
There are many ways to calculate rarity. I've used something inspired by the following: https://raritytools.medium.com/ranking-rarity-understanding-rarity-calculation-methods-86ceaeb9b98c. It is not guaranteed, and even unlikely, rarity.tools will use the exact same calculation.

The rarity is calculated as follows: 
- calculate the occurence of each trait across the entire set of groupies 
- add a new trait 'trait count' that accounts for groupies with 2, 8, or 9 traits.
- for each groupie, sum the occurrences of each trait – lower score = more rare, higher score = less rare

see `./scripts` and `./scripts/score.js` for the implementation.

## using rarity data

see `/data` directory for outputs
`metadata.json`: compiled metadata for each groupie (groupy?)
`traits.json`: aggregate rarity by trait
`score.json`: per token rarity score

## sample install and pipeline

```
git clone https://github.com/jtgi/groupies-rarity
cd ./groupies-rarity
npm install
cd ./scripts
node download.js
node compile.js
node traits.js
node score.js
```
