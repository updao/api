### UPDAO API

This nodejs module for Token0x integration

Status: Implemented MVP

[Website](http://updao.org) | [Discuss](https://t.me/updao_platform)

#### Use API

```
npm i updao --save
```

```Javascript


var web3 = if window ? window.web3 : require('web3');

var nodeURI = "https://updao.org"

var updao = require('updao')(window.web3, nodeURI);

var showResult = function(err, result) {
    console.log(err, result);
}

// Add New Project

updao.addProject(project, showResult);


// Get list of public projects

updao.getProjects(showResult);


// Get project details

updao.getProjectDetails('BTC', showResult);


// Get tokensale contract

updao.tokensaleContractAt('0x....') //use contract methods


// Get token contract

updao.tokenContractAt('0x....') //use contract methods


// Claim tokens 
// You need to pass KYC bofore using this method

query = {
    contractAddress: '0x...',
    token: 'BTC'
};

updao.claimTokens(query, showResult);


// Whitelist Buy 
// You need to be registered in Whitelist before using this method

query = {
    contractAddress: '0x...',
    token: 'BTC',
    amountEthers: '1'
};

updao.whitelistBuy(query, showResult);

```


-----------------

updao.org