<div align="center">
  <br />
  <p>
    <a href="https://financial.js.org"><img src="/static/logo.svg" width="546" alt="finance.io" id="djs-logo" /></a>
  </p>
  <br />
  <p>
    <a href="https://discord.gg/bRCvFy9"><img src="https://img.shields.io/discord/793118787460399154?color=7289da&logo=discord&logoColor=white" alt="Discord server" /></a>
    <a href="https://www.npmjs.com/package/discord.js"><img src="https://img.shields.io/npm/v/finance.io.svg?maxAge=3600" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/discord.js"><img src="https://img.shields.io/npm/dt/finance.io.svg?maxAge=3600" alt="NPM downloads" /></a>
    <a href="https://travis-ci.org/discordjs/discord.js"><img src="https://travis-ci.org/discordjs/finance.io.svg" alt="Build status" /></a>
    <a href="https://david-dm.org/discordjs/discord.js"><img src="https://img.shields.io/david/discordjs/finance.io.svg?maxAge=3600" alt="Dependencies" /></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/finance.io/"><img src="https://nodei.co/npm/finance.io.png?downloads=true&stars=true" alt="NPM info" /></a>
  </p>
</div>

# Welcome!

Welcome to the finance.io v0.1.0 documentation.


```
$ npm install finance.io@latest
```

### Define finance.io


```
const stock = require('finance.io')
```


## Version 

- v0.1.4@latest

- v0.1.3

- v0.1.2

- v0.1.1

- v0.1.0

- v0.0.9 <




## Usage

> Recommend Using Version 0.1.0 And Above

#### Formats

```
// Example

stock.getInfo("GOOGL").then( (data) => {
   // You May Modify The Output
   // default : console.log(JSON.stringify(data, null, 4)
   // note : Please Use "JSON.stringify(data, null, 4)" // In Every Output
});
```

### Get Stock Quote Data

To Get Stock Quote Of GOOGL Use The Code Snippet Below.

```
// v0.1.0 and above

stock.getInfo("GOOGL").then( (data) => {
    console.log(JSON.stringify(data, null, 4));
});


// v0.1.0 below

stock.get("GOOGL") // returning the data in console.log


// Returning Data 

[
  { quote: 'GOOGL',
  currentPrice: 1734.16,
  targetHighPrice: 2250,
  targetLowPrice: 1420,
  targetMeanPrice: 1911.79,
  targetMedianPrice: 1950,
  recommendationMean: 1.8,
  recommendationKey: 'buy',
  numberofAnalystOpinions: 36,
  totalCash: 132595998720,
  totalCashFormat: '132.6B',
  totalCashPerShare: 196.024,
  ebitda: 48075001856,
  ebitdaFormat: '48.08B',
  totalDebt: 27541999616,
  quickRatio: 3.28,
  currentRatio: 3.41,
  totalRevenue: 171703992320,
  totalRevenueFormat: '171.7B',
  debtToEquity: 12.935,
  revenuePerShare: 250.985,
  returnOnAssets: 0.07745,
  returnOnAssetsFormat: '7.74%',
  returnOnEquity: 0.17511,
  returnOnEquityFormat: '17.51%',
  grossProfits: 89961000000,
  grossProfitsFormat: '89.96B',
  freeCashFlow: 28147499008,
  freeCashFlowFormat: '28.15B',
  operatingCashFlow: 56874000384,
  operatingCashFlowFormat: '56.87B',
  earningsGrowth: 0.62,
  revenueGroth: 0.14,
  revenueGrothFormat: '14.00%',
  grossMargins: 0.53599,
  grossMarginsFormat: '53.60%',
  ebitdaMargins: 0.27999002,
  ebitdaMarginsFormat: '28.00%',
  operatingMargins: 0.2029,
  profitMargins: 0.20798999,
  profitMarginsFormat: '20.80%',
  financialCurrency: 'USD' }
  
  ] 

```

### Get Company Data

Get Specific Company Data

```
// v0.1.0 and above

stock.getCompany("AAPL").then( (data) => {
    console.log(JSON.stringify(data, null, 4));
});


// v0.1.0 below

stock.get.company("AAPL")


// Returning Data

[
  { quote: 'GOOGL',
  address1: '1600 Amphitheatre Parkway',
  city: 'Mountain View',
  state: 'CA',
  zipCode: '94043',
  country: 'United States',
  contactNumber: '000-000-000', 
  website: 'http://www.abc.xyz',
  industry: 'Internet Content & Information',
  sector: 'Communication Services',
  businessSummary:
   '--something--',
  fullTimeEmployees: 132121,
  headCompanyOfficers: 'Mr. Sundar  Pichai' }
]
```

### Get Filtered Financial Data

```

// v0.1.0 and above

stock.getFinancial("GOOGL").then( (data) => {
    console.log(JSON.stringify(data, null, 4));
});


// v0.1.0 below

stock.get.financial("GOOGL")


// Returning Data 

[
  { quote: 'GOOGL',
  fiftyTwoWeekRange: '1008.87 - 1843.83',
  fiftyTwoWeekLow: 1008.87,
  fiftyTwoWeekHigh: 1843.83,
  trailingPE: 33.509045,
  epsTrailingTwelveMonths: 51.752,
  epsForward: 61.25,
  epsCurrentYear: 51.61,
  priceEpsCurrentYear: 33.601242,
  sharesOutstanding: 300644000,
  bookValue: 314.169,
  marketCap: 1174577872896,
  forwardPE: 28.312817,
  priceToBook: 5.5198317,
  fullExchangeName: 'NasdaqGS' }
  ]
```


### Get netSharePurchaseActivity

```
// v0.1.0 and Above

stock.nspa("GOOGL").then( (data) => {
  console.log(JSON.stringify(data, null, 4));
});



// v0.1.0 below
stock.netSharePurchaseActivity("GOOGL") 


// Returning Data

[
  { quote: 'GOOGL',
  buyInfoCount: 1,
  buyInfoShares: 1459,
  buyPercentInsiderShares: 0.002,
  sellInfoCount: 6,
  sellInfoShares: 334,
  netInfoCount: 7,
  netInfoShares: 1125,
  netPercentInsiderShares: 0.001,
  totalInsiderShares: 825240 }
]
```

### Outside NYSE (stock.getFinancial)

> v0.1.0 and below will not work as the same way


Stocks Outside NYSE Require A Corresponding Argument.
What You Need Is Just Adding A Comma And A Value.

```
// Karex, 5247.KL

// v0.1.0 and above
stock.getFinancial('5247', 'KL')
.then( (data) => {
  console.log(JSON.stringify(data, null, 4))
});


// v0.1.0 below

stock.get.financial("5247.KL")

// Returning Data

{
    "symbol": "5247",
    "data": "financial",
    "fiftyTwoWeekRange": "0.26 - 1.23",
    "fiftyTwoWeekLow": 0.26,
    "fiftyTwoWeekHigh": 1.23,
    "trailingPE": 10.985915,
    "epsTrailingTwelveMonths": 0.071,
    "sharesOutstanding": 1002370000,
    "bookValue": 0.464,
    "marketCap": 781848576,
    "priceToBook": 1.6810344,
    "fullExchangeName": "Kuala Lumpur"
}

```

### Test finance.io functions

```
stock.test()
```

## Extra Features

### Get A Random Number

Value Is Require. For Example : `stock.random(1,8)`
The Returning Data Should Be `1` to `8`

```
stock.random(1,8)

// Display The Data By Doing 

console.log(stock.random(1,8))


// Returning Data 

Example : `1.0246939366192591`
```


## Author 

- [@joeleeofficial](https://github.com/joeleeofficial)


### Contributors 

- [Joe Lee Official](mailto:tojoeleeofficial@gmail.com)


### Need Help ? 

[Join stock.js Discord Community Now](https://discord.gg/hZMCwDXfQb)


<a href="https://discord.gg/hZMCwDXfQb"><img src="https://discordapp.com/api/guilds/793118787460399154/embed.png?style=banner2"></a>

