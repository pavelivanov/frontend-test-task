# frontend-test-task

### Business story

We'd like to build an app where users can put their tokens (USDT) to the project's contract for future rewards. Users should be able to connect their wallets and add / remove tokens using a form in the app. We'd like to show users a list of last 10 transactions from all users. Also connected user should be able to see his account balance and balance of tokens that he provided to the contract.

### What nees to be done

- Add a button to connect wallet. When connected the button should be replaced with block containing account address. Optional: add "disconnect" button that disconnects
- Add a form (title: Provide tokens) with input (placeholder: Amount), account balance and submit button (title: Submit). Using this form user should be able to put tokens 
- Add same form to withdraw tokens (instead of account belance we should show balance on the contract).
- Add list of transactions (to receive transactions use contract Events). Each item of the list should contain: sender address, amount of tokens, action (provide / withdraw), date (MM/DD/YYYY HH:mm:ss). Show only last 10 transactions.

### Example how forms might look

![image](https://user-images.githubusercontent.com/966176/135583164-0cb5c748-de42-4735-961a-2657eda04f6b.png)

### Requreiments

- Use Next.js framework, deploy to Vercel
- Use TypeScript
- Use typechain library to generate types from contracts ABI
- Use Rinkeby network
- Use Ethers.js library
- Use @web3-react/core to connect wallet (only MetaMask)
- UI design is not evaluated, here you have complete freedom
