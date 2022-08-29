# Smart Contracts -- Joint Savings Account

To create a Joint Savings Account Contract in Solidity

open the Solidity file named joint_savings.sol in the Remix IDE.

Define a new contract named JointSavings.

Define the following variables in the new contract:

Two variables of type address payable named accountOne and accountTwo

A variable of type address public named lastToWithdraw

Two variables of type uint public named lastWithdrawAmount and contractBalance

Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:

Define a require statement that checks if recipient is equal to either accountOne or accountTwo. If it isn’t, the require statement returns the “You don't own this account!” text.

Define a require statement that checks if balance is sufficient for accomplishing the withdrawal operation. If there are insufficient funds, it returns the “Insufficient funds!” text.

Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

Call the transfer function of the recipient, and pass it the amount to transfer as an argument.

Set lastWithdrawAmount equal to amount.

Set the contractBalance variable equal to the balance of the contract by using address(this).balance to reflect the new balance of the contract.

Define a public payable function named deposit. In this function, code the following:

Set the contractBalance variable equal to the balance of the contract by using address(this).balance.
Define a public function named setAccounts that takes two address payable arguments, named account1 and account2. In the body of the function, set the values of accountOne and accountTwo to account1 and account2, respectively.

Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.

Step 2: Compile and Deploy Your Contract in the JavaScript VM
Compile your smart contract. If an error occurs, review your code, and make the necessary changes for a successful compilation.

In the Remix IDE, navigate to the “Deploy & Run Transactions” pane, and then make sure that “JavaScript VM” is selected as the environment.

Click the Deploy button to deploy your smart contract, and then confirm that it successfully deployed.

Step 3: Interact with Your Deployed Smart Contract
Now that your contract is deployed, it’s time to test its functionality! After each step, capture a screenshot of the execution, and then save it in a folder named Execution_Results. You’ll share this folder with your final submission.

To interact with your deployed smart contract, complete the following steps:

Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.