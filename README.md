# solana-jupiter-bot

> CAUTION! Use at Your own risk! This bot is currently being optimized 📊

> ⚠️ EPILEPSY WARNING - CLI UI is constantly refreshed and may be disruptive for sensitive people

# What is this?

It's a trading bot that can trade on Solana by utilizing the Jupiter Agregator SDK.
There are two parts:

- config wizard
- trading bot

With Config wizard, you can easly setup your trading strategy.

### CLI UI

📊 Bot have CLI UI which helps You monitor your trading strategy.

CLI UI currently displays a simulated profit chart and latency chart. The latency chart shows you the time taken to compute routes with Jupiter SDK.

All trades are stored in trades history and will be shown in the table. Table is limited to 5 entries, but history stores all trades.

💡 UI elements can be hidden or shown using hotkeys (read below).

> THIS README IS NOT COMPLETED YET.

![](https://github.com/arbprotocol/solana-jupiter-bot/blob/main/gif1.gif)
![](https://github.com/arbprotocol/solana-jupiter-bot/blob/main/gif2.gif)

## Install

```bash
$ git clone https://github.com/arbprotocol/solana-jupiter-bot && cd solana-jupiter-bot
$ yarn
```

Set Your wallet private key in `.env` file

```js
SOLANA_WALLET_PRIVATE_KEY =
	hgq847chjjjJUPITERiiiISaaaAWESOMEaaANDiiiIwwWANNAbbbBErrrRICHh;
```

\*[optionally] set default RPC (it can be also set in wizard)

```js
SOLANA_WALLET_PRIVATE_KEY=hgq847chjjjJUPITERiiiISaaaAWESOMEaaANDiiiIwwWANNAbbbBErrrRICHh
DEFAULT_RPC=https://my-super-lazy-rpc.gov
```

## USAGE

```
$ solana-jupiter-bot:

  Usage
    $ yarn start
      This will open Config Wizard and start bot

    $ yarn trade
      Start Bot and Trade with latest config
```

Have fun!

## Hotkeys

While the bot is running, you can use some hotkeys that will change the behaviour of the bot or UI

`[H]` - show/hide Help

`[CTRL] + [C]` - obviously it will kill the bot

`[E]` - force execution with current setup & profit

`[R]` - revert back last swap

`[L]` - show/hide latency chart (of Jupiter `computeRoutes()`)

`[P]` - show/hide profit chart

`[T]` - show/hide trade history table \*_table isn't working yet_

`[S]` - simulation mode switch (enable/disable trading)
