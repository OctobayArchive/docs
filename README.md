# Docs

Documentation for the OctoBay project

For now this repository is just a collection of things worth writing down.

1. [Registration](https://octobay.github.io/docs/REGISTRATION.html)

# Overview

OctoBay is a decentralized bounty platform with promotional features, using the following technologies:

- Smart Contract and Token
- Chainlink Oracles
- The Graph
- Uniswap
- Gas Station Network

## Main Use Cases

### Bounty

![image](https://user-images.githubusercontent.com/6792578/107638409-d6739200-6c6f-11eb-9833-ff94dedb57bc.png)

Funds are deposited in the smart contract for an issue on GitHub. Once the issue is closed, the author/contributor can request a withdrawal on which the Chainlink oracles check if the required conditions are met.

Possible conditions:

- A pull request got **merged into the default branch**, closing the issue **automatically**. (Default behavior if not specified otherwise by the maintainer of the issue's repository.)
- A pull request, mentioning the issue (in its description or a commit message ) with a close command (e.g. `closes #12`), got merged into a branch specified by the maintainer and the issue is closed.
- The maintainer comments on the issue in the form: `@OctoBay release to @user`. (Overrides previous conditions.)

### Tipping/Inviting

Any Ethereum account can send funds to any GitHub user. If the user is new to OctoBay, one of our oracles will send an email invitation or mention the user on GitHub and Twitter, if no public email address is available. The user creates an Ethereum account and can withdraw the deposit via a gasless meta transaction, that is prepaid by the deposit and handled by our Gas Station Network relayer.

![image](https://user-images.githubusercontent.com/6792578/107778410-5539ff00-6d44-11eb-95a6-c3d652c180c0.png)

This process also works for issue bounties or repository funds. Those can also be accessed via gasless transactions for new users.
