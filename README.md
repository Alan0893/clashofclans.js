# clashofclans.js
**API Wrapper for official Clash of Clans API.**

## Before you Start
➤ To control traffic and access to the API, you will be required to obtain a API Token [here](https://developer.clashofclans.com/#/).

## Getting Started
1. To install this package, in your console run: `git clone https://github.com/Alan0893/clashofclans.js.git` 
2. In your package.json, add `"clash": "file:clashofclans.js"` in your dependencies
3. You have now installed the package!

### Problems with `git`
> **'git' is not recognized as an internal or external command, operable program or batch file.**
If you get the error stated above, follow the instructions below:
1. Open VS Code
2. Hit `ctrl + ,`
3. In the seach bar, type `git path`
4. Click `add this path`
5. You should now be able to use `git` in VS Code

## Example
```javascript
const clash       = require("clash")             //includes the brawlchart module
const token       = "Your Token"                 //your unique API token
const client      = new clash.Client(token)      //creates a new brawlchart Client

;(async() => {
  const player     = await client.getPlayer("#PLAYERTAG") //Fetches a player stats as given in the parameter  
  const playerClub = await client.getClub("#CLUBTAG")     //Fetches a club stats as given in the parameter
})()
```
More examples pertaining to player and club data can be found in the official API documentation.
