# py3status-bittrex-module
A simple Bittrex module for py3status allowing the user to easily track account balances in real time on i3status bars.
![Sample Image 1](https://i.gyazo.com/9091e1d188179a333314e799c51b182d.png)
![Sample Image 2](https://i.gyazo.com/ef0790173530b92c69540130bde91f33.png)
## Dependencies:
This module requires [python-bittrex wrapper](https://github.com/ericsomdahl/python-bittrex) by ericsomdahl

## Installation:
Simply place "bittrex_module.py" in py3status default modules folder (~/.i3/py3status/) or any other folder specified with "--include" when launching.

## Configuration:
Make sure your Bittrex [API key](https://bittrex.com/Manage#sectionApi) has permission to read info!

You must add "bittrex_module" to your "order" in i3status config, like shown in [i3status tutorials](https://i3wm.org/i3status/manpage.html#_configuration)

bittrex_module configuration parameters are:

* `format_a` first output format *`(default: "{cursymbol} {fiat_bal:.2f}")`*
* `format_b` second output format *`(default: "{cursymbol} {btc_bal:.4f}")`*
* `format_c` third output format *`(default: "{cursymbol}Bittrex")`*
* `upsymbol` symbol for price raise since last update *`(default: "+")`*
* `downsymbol` symbol for price drop since last update *`(defaul: "-")`*
* `equalsymbol` symbol for same price since last update *`(default: "=")`*
* `api_key` your bittrex [API key](https://bittrex.com/Manage#sectionApi) - you **must** set this parameter!
* `api_secret` your bittrex [API secret](https://bittrex.com/Manage#sectionApi) - you **must** set this parameter!
* `fiat` the desired fiat currency used to calculate your balance *`(default: "USD")`*
* `cache_timeout` time in seconds for each update *`(default: "60")`*

Example of `fiat` parameters are `"USD"`, `"BRL"`, `"CAD"`, `"JPY"` or any other currencies supported by [Fixer.io](http://fixer.io/) API

bittrex_module format placeholders are:

* `{fiat_bal}` balance in selected fiat
* `{fiat_btc}` balance in bitcoin
* `{cursymbol}` current price change symbol according to last price
* `{show_mode}` current showing format


## Usage:
Once properly configured, bittrex_module can have it's showing formats alternated by clicking with the left mouse button, and updated by either clicking or scrolling.

A good setup is having a format showing your BTC worth in local fiat, another one showing the balance in BTC values and the third one hiding any values in case you need to publicly use the computer or in order to take screenshots/record the screen.

## Donations:
Thank you for using this module!
If you feel like helping out:
BTC 1KVUQB5QaRriSLRWPKWuqZaTEsaqzDAJHi
IOC iqmW3t5qfM2bNa2n8KFNvadWf2T962NJsV
