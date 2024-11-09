# coins-sdk

### Static config for cryptocurrency coins and tokens across different networks

## Goals
- Provide an "encyclopedia" of all relevant constants which are sprinkled throughout the MetaPouch stack.
- Separate static config data from dynamic config data.
- Strong typing for static config properties, with full type information for configuration items.
- Ability to export static configuration as JSON for consumption by non-javascript projects.

  ## Examples
  ### Get the number of decimal places in a cryptocurrency coin

  JavaScript
  ```
  import coins, { Network, Token, TokenType } from 'coins-sdk';

  const bitcoin = coins.get(Network.BITCOIN, Token.BITCOIN, TokenType.NATIVE);
  console.log(bitcoin.getDecimals() as number);

  const ethereum = coins.get(Network.ETHEREUM, Token.ETHEREUM);
  console.log(ethereum.getSymbol() as string);
  ```

  ```
  import coins, { COIN, TokenType } from 'coins-sdk';

  const usdt = coins.get(Network.ETHEREUM, Token.USDT, TokenType.ERC20);
  console.log(usdt.getContractAddress() as string);
  ```
