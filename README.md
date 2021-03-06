# Babylon Finance On-chain SDK

This repository provides all the interfaces and helper contracts needed to start building on top of [Babylon Finance](https://babylon.finance) Gardens.

## Building on Babylon

Babylon provides a new DeFi lego building block. Babylon Gardens are the first **DeFi Investment DAO primitive (ERC-20)**.

Gardens are tokenized investment clubs/DAOs where users can deposit digital assets and receive a tokenized share (ERC-20) representing their ownership.

Developers can build on top of Babylon Gardens and benefit from all the following built-in features.

## Built-in Features

- Garden ERC-20 tokens are **fully composable and transferrable**.
- Gardens are **non-custodial and trust minimized**. Only users have access to their funds. Capital can only be allocated to approved strategies.
- Gardens also provide an **NFT Membership token (ERC-721)**. Members of a garden can mint their NFT.
- **Built-in light governance system with signature based voting**. Gas-free.
- No-hassle and **No code UI** to create strategies and deploy capital to +15 DeFi protocols including Aave, Compound, Uniswap, Curve and Convex.
- DeFi execution costs are automatically shared between all members of a Garden, increasing the capital efficiency.
- Garden UI where users & managers can deposit/withdraw and monitor the performance of their investment club.

You can read more in our [managers page](https://www.babylon.finance/managers).

## Architecture

![image](https://user-images.githubusercontent.com/541599/166601087-734a1c13-f979-4ec3-be8c-d1346e475c14.png)

Babylon uses several layers of abstraction. Every investment club aka Garden is its own smart contract. Every DeFi strategy within a garden is its own smart contract as well.

These layers of abstraction provide a high-level of isolation and composability. This ensures that potential bugs or hacks get isolated to specific strategies and clubs.

You have all the information in our [Litepaper](https://docs.babylon.finance/litepaper).

Babylon Finance uses [Hardhat](https://hardhat.org/) chain for testing and local development. Babylon Finance integrates with +15 DeFi protocols and therefore creating a full working deployment on testnests like Kovan or Ropsten is almost impossible. Hardhat lets you clone Ethereum Mainnet and use the contracts on the same addresses. That way you can build on top of mainnet with all the DeFi protocols with Ease.

## Prerequisites

You need to have node and yarn installed in your machine.

[NodeJS](https://nodejs.org/en/download/)
[Yarn](https://yarnpkg.com/)

## Tests and Samples

You can find a test with sample code to create gardens and strategies in the `test` folder. 

To run them, follow these steps

1. Install dependencies with yarn ```yarn```
2. Set `ALCHEMY_KEY` as an environment variable. You can grab a free key from [Alchemy](https://www.alchemy.com/).
3. Execute the following command ```yarn run test```

![image](https://user-images.githubusercontent.com/541599/167233003-ece57ab8-b736-4d48-b832-bb689f0497f6.png)

If you want to test with a live garden, you can use the Test WETH garden [0x2c4Beb32f0c80309876F028694B4633509e942D4](https://www.babylon.finance/garden/0x2c4Beb32f0c80309876F028694B4633509e942D4)

## Custom Integrations

Integrations are adapters that Babylon uses to connect with other DeFi & Web3 protocols. 

So far, Babylon has developed all these adapters in-house. You can see the whole list [here](https://docs.babylon.finance/protocol/integrations).

Starting today, anyone can develop an adapter, test it on a private garden and then submit it to be verified and audited by Babylon governance.

In the integrations folder, you'll find the base classes, a template, and an example of a custom integration developed to integrate with yearn.

You can find more documentation about custom integrations in our [docs](https://docs.babylon.finance/developers/custom-integrations).

## Smart Contracts API

You can see all the functions of our main contracts, their functions and paramaters documented here.

[API Docs](https://app.gitbook.com/o/-MU9cUI94K7ldAjpGj7S/s/-MU6ZbTQOlfV8oj9cw0O/developers/smart-contract-api)

## Deployed contracts

You can see all the deployed [open-sourced contracts here](https://docs.babylon.finance/developers/deployments).
