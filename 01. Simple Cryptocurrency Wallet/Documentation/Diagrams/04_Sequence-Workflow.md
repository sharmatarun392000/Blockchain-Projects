### Sequence Diagram 1: Wallet Creation

**Description**: This sequence diagram shows the steps involved when a user creates a new wallet.

#### Steps:
1. User initiates wallet creation via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service generates a new wallet (public-private key pair).
5. Wallet Service stores the wallet information in the Database.
6. Wallet Service sends wallet details back to the API Gateway.
7. API Gateway sends wallet details to the UI.
8. UI displays the wallet information to the user.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/a57f06b8-5dfe-4264-9862-195be61a3382)


### Sequence Diagram 2: Import Wallet

**Description**: This sequence diagram shows the steps involved when a user imports an existing wallet.

#### Steps:
1. User initiates wallet import via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service validates the private key and imports the wallet.
5. Wallet Service stores the wallet information in the Database.
6. Wallet Service sends wallet details back to the API Gateway.
7. API Gateway sends wallet details to the UI.
![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/735ba432-85a5-453f-bf87-527b34cffecf)


### Sequence Diagram 3: Send Ether

**Description**: This sequence diagram shows the steps involved when a user sends Ether.

#### Steps:
1. User initiates an Ether transfer via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Transaction Service.
4. Transaction Service creates and signs the transaction.
5. Transaction Service sends the transaction to the Ethereum Blockchain via Infura.
6. Infura processes the transaction and returns a transaction hash.
7. Transaction Service stores the transaction details in the Database.
8. Transaction Service sends the transaction hash back to the API Gateway.
9. API Gateway sends the transaction hash to the UI.
10. UI displays the transaction status to the user.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/7276e330-58b5-4a1c-aa28-501646a514f0)


### Sequence Diagram 4: Receive Ether

**Description**: This sequence diagram shows the steps involved when a user receives Ether.

#### Steps:
1. User checks wallet address via the UI.
2. UI retrieves the wallet address from the Wallet Service.
3. User shares wallet address to sender.
4. Sender sends Ether to the user's wallet address.
5. Transaction is processed by the Ethereum Blockchain.
6. Infura notifies the Transaction Service of the incoming transaction.
7. Transaction Service retrieves transaction details from Infura.
8. Transaction Service stores the transaction details in the Database.
9. Transaction Service sends transaction details to the API Gateway.
10. API Gateway sends transaction details to the UI.
11. UI updates the user's balance and transaction history.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/a4540b56-fd41-4969-985c-12343f3e67c3)

### Sequence Diagram 5: View Transaction History

**Description**: This sequence diagram shows the steps involved when a user views their transaction history.

#### Steps:
1. User requests to view transaction history via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Transaction Service.
4. Transaction Service retrieves transaction history from the Database.
5. Transaction Service retrieves additional transaction details from Etherscan.
6. Transaction Service compiles the transaction history and details.
7. Transaction Service sends the transaction history to the API Gateway.
8. API Gateway sends the transaction history to the UI.
9. UI displays the transaction history to the user.

```plaintext
User -> UI: View Transaction History
UI -> API Gateway: Request Transaction History
API Gateway -> Transaction Service: Retrieve Transaction History
Transaction Service -> Database: Retrieve Transaction History
Database -> Transaction Service: Return Transaction History
Transaction Service -> Etherscan: Retrieve Additional Details
Etherscan -> Transaction Service: Return Transaction Details
Transaction Service -> API Gateway: Send Transaction History
API Gateway -> UI: Send Transaction History
UI -> User: Display Transaction History
```

### Sequence Diagram 6: Balance Inquiry

**Description**: This sequence diagram shows the steps involved when a user checks their wallet balance.

#### Steps:
1. User requests to check wallet balance via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service retrieves the wallet balance from the Ethereum Blockchain via Infura.
5. Wallet Service sends the wallet balance to the API Gateway.
6. API Gateway sends the wallet balance to the UI.
7. UI displays the wallet balance to the user.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/25f225c3-18ea-4eed-bc22-873618bd1ad9)

### Sequence Diagram 7: Create Backup

**Description**: This sequence diagram shows the steps involved when a user creates a backup of their wallet.

Steps:
1. User initiates the backup creation process via the UI.
2. UI sends a request to the API Gateway to create a backup.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service retrieves the wallet data from the Database.
5. Wallet Service encrypts the wallet data.
6. Wallet Service generates a backup file.
7. Wallet Service sends the backup file to the API Gateway.
8. API Gateway sends the backup file to the UI.
9. UI provides the backup file to the user for download.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/8aa78dbe-ba1a-4791-9eb9-124564911a13)
