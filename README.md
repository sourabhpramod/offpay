# Off-Pay

## Quantum-Secure Offline Payment Solution

### Introduction
Off-Pay is a quantum-resilient peer-to-peer offline payment application. It utilizes post-quantum algorithms (Kyber) to secure encryption keys and transaction details, and Falcon Signature for verifying the transaction and transactor without requiring an active internet connection.

### Key Features
- **Offline Transactions**: Payments are made and verified locally without needing a live network connection. Uses peer-to-peer networking and QR codes for transactions.
- **Quantum-Resilient Encryption**: Utilizes the Kyber algorithm and Falcon signature to validate and encrypt transactions, making them resilient to quantum attacks.
- **Two Modes of Transaction**: Supports two transaction modes:
  - **QR Mode**
  - **P2P Mode**
- **Transaction Finalization**: Once network connectivity is restored on either device, the transaction ledger synchronizes with the central ledger.

## P2P Mode
This mode enables offline transactions using various peer-to-peer networking strategies like Wi-Fi Direct and Bluetooth.

### Steps:
1. The receiver displays a unique QR code.
2. The sender scans it to retrieve the receiver's unique ID (public key) and establish a P2P connection via an advertising-discovering mode.
3. The sender enters the amount and PIN, then presses "Send."
4. Kyber and Falcon algorithms encrypt the transaction details, sending keys and signature hashes over the P2P network.
5. Both devices acknowledge the payment details through Falcon signatures shared as strings within this network.
6. The transaction details are stored locally (secure storage) as a ledger until internet connectivity is restored.
7. Once online, the local ledger syncs with the bank servers to complete the transaction.

## QR Mode
This mode facilitates transactions through a chain of QR code scans without requiring any network connection.

### Steps:
1. The receiver displays a unique QR code.
2. The sender scans it, sharing their public key via QR code embedding.
3. The sender enters the amount and PIN, then proceeds.
4. The Kyber and Falcon algorithms encrypt transaction details and generate a sequence of 4 QR codes.
5. The receiver scans the 4 QR codes sequentially to confirm, validate, and secure the transaction fully via QR code embedding.
6. The transaction details are stored locally (secure storage) as a ledger until internet connectivity is restored.
7. Once online, the local ledger syncs with the bank servers to complete the transaction.

## Quantum Proofing
- **Kyber**: Used for key generation, encryption, and decryption.
- **Falcon**: Used for transaction signing and validation.

---
### Authors:
**Govardhan & Sourabh**
