🏡 Land Registry Ledger Blockchain

A simple blockchain-based ledger system for property deeds.
This project demonstrates how blockchain concepts like immutability, proof-of-work, and ledger verification can be applied to land/property ownership records.

✨ Features

Register Deeds (ISSUE): Add a new property ownership record to the blockchain.

Transfer Ownership (TRANSFER): Securely transfer a property deed from one owner to another.

Revoke Deeds (REVOKE): Revoke ownership (e.g., due to legal disputes, fraud, or corrections).

Verify Deeds: Check the latest status of a deed, including validity and ownership.

Chain Validation: Ensure the blockchain is tamper-proof using hash verification and proof-of-work.

Persistent Storage: The ledger is stored in land_chain.json.

⚙️ How It Works

Each deed transaction (ISSUE, TRANSFER, REVOKE) is stored inside a block.
Blocks are linked using cryptographic hashes.
A proof-of-work requirement ensures no block can be altered without breaking the chain integrity.

📂 Project Structure
land-registry-ledger/
├── land_chain.json      # Blockchain data storage (auto-generated)
├── ledger.py            # Main blockchain & CLI implementation
└── README.md            # Project documentation

▶️ Running the Project

Clone the repository:

git clone https://github.com/your-username/land-registry-ledger.git
cd land-registry-ledger


Run the program:

python3 ledger.py

📋 Menu Options

When you run the script, you’ll see an interactive menu:

--- Land Registry Ledger ---
1) Register new deed
2) Transfer ownership
3) Revoke deed
4) Verify deed
5) Show chain length & validity
6) List last N blocks
0) Exit

Example Usage

Register a new property deed:

Select: 1
Deed ID: DEED-1001
Owner: John Smith
Property Address: 45 Lakeview Road
Registered on (YYYY-MM-DD): 2025-03-01
Registrar: City Registrar Office
[✓] Registered deed DEED-1001 in block #1.


Transfer ownership:

Select: 2
Deed ID to transfer: DEED-1001
New owner: Alice Johnson
Registrar confirming: City Registrar Office
[✓] Ownership of DEED-1001 transferred to Alice Johnson in block #2.


Verify a deed:

Select: 4
Deed ID to verify: DEED-1001
[INFO] DEED-1001: status=ISSUED (owner=Alice Johnson). VALID LINK=True, POW=True.


Revoke a deed:

Select: 3
Deed ID to revoke: DEED-1001
Registrar revoking: City Registrar Office
Reason/remarks: Court order
[✓] Revoked deed DEED-1001 in block #3.

🔒 Security

Each block is hashed with SHA-256.

Proof-of-Work ensures immutability.

Verification checks valid chain linkage and difficulty compliance.

🚀 Future Improvements

Web-based dashboard for deed management.

Multi-user authentication (registrar vs. owner).

Support for property metadata (size, survey number, documents).

Networking (peer-to-peer ledger synchronization).

📜 License

MIT License – free to use, modify, and distribute.
