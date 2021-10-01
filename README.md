# frontend-test-task

## Business story

We'd like to build an app where users can put their tokens (USDT) to the project's contract for future rewards. Users should be able to connect their wallets and add / remove tokens using a form in the app. We'd like to show users a list of last 10 transactions from all users. Also connected user should be able to see his account balance and balance of tokens that he provided to the contract.

<br />

## What nees to be done

- Add a button to connect wallet. When connected the button should be replaced with block containing account address. Optional: add "disconnect" button that disconnects
- Add a form (title: Provide tokens) with input (placeholder: Amount), account balance and submit button (title: Submit). Using this form user should be able to put tokens 
- Add same form to withdraw tokens (instead of account belance we should show balance on the contract).
- Add list of transactions (to receive transactions use contract Events). Each item of the list should contain: sender address, amount of tokens, action (provide / withdraw), date (MM/DD/YYYY HH:mm:ss). Show only last 10 transactions.

<br />

## Example how forms might look

![image](https://user-images.githubusercontent.com/966176/135583164-0cb5c748-de42-4735-961a-2657eda04f6b.png)

## Requreiments

- Use Next.js framework, deploy to Vercel
- Use TypeScript
- Use typechain library to generate types from contracts ABI
- Use Rinkeby network
- Use Ethers.js library
- Use @web3-react/core to connect wallet (only MetaMask)
- UI design is not evaluated, here you have complete freedom

<br />

## TestTask Contract

```
address: 0x02cB34d293e74D3328321c0E32898e42D8594895
```

### API

Read `balance(address)`<br />
Write `provide(amount)`<br />
Write `withdraw(amount)`<br />
Event `Withdraw(address to, uint amount)`<br />
Event `Provide(address from, uint amount)`

**Note:** use events to receive data to render list of past transactions.

<br />

## USDT Contract

```
address: 0x18696aE68855e95674765d4Dbbc54dF6F8a66290
```

### API

Read `balanceOf(address)`<br />
Read `allowance(address)`<br />
Write `approve(address, amount)`<br />

**Note:** you can read about approve and allowance [here](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#IERC20-approve-address-uint256-) and [here](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#IERC20-allowance-address-address-).

<br />

## Accounts (with tokens on balance)

```
address: 0x63ab10e2262b685acfc25c02ff688bc15d325deb
privateKey: 0xb4b0f4d42079badfcd0f92273494e09f53cf0c7889ae5f7e8c1dd73899f5a044

address: 0x1b6ff534d723d8a9c8494d0337b98b2ec9c13e16
privateKey: 0x9690b165466ac84e7e7ec9dcda000c7b4ff55d79ba31255a6f7fb6489801cdb8
```

Use these accounts to test the DApp.
