# Redemption

The contract is a direct copy of https://github.com/aptos-labs/aptos-core/pull/15019
that's developed by Aptos Labs engineers and audited by OtterSec.

## Deployment

**Important**: the contract is deployed as immutable (see [Move.toml](./Move.toml)).

See [0xd47ead75b923422f7967257259e7a298f029da9e5484dc7aa1a9efbd4c3ae648](https://explorer.aptoslabs.com/account/0xd47ead75b923422f7967257259e7a298f029da9e5484dc7aa1a9efbd4c3ae648?network=mainnet).

To verify, there are 2 ways:

1. compare [onchain code](https://explorer.aptoslabs.com/account/0xd47ead75b923422f7967257259e7a298f029da9e5484dc7aa1a9efbd4c3ae648/modules/code/redemption?network=mainnet)
with [code in this repo](./sources/redemption.move)

2. run the below `verify-package` command

```
> aptos move verify-package --account 0xd47ead75b923422f7967257259e7a298f029da9e5484dc7aa1a9efbd4c3ae648 --url https://fullnode.mainnet.aptoslabs.com
Compiling, may take a little while to download git dependencies...
UPDATING GIT DEPENDENCY https://github.com/aptos-labs/aptos-core.git
INCLUDING DEPENDENCY AptosFramework
INCLUDING DEPENDENCY AptosStdlib
INCLUDING DEPENDENCY MoveStdlib
BUILDING redemption
{
  "Result": "Successfully verified source of package"
}
```
