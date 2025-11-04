# Genesis 1.0 - GDrive3.0: Decentralized File Storage on Blockchain

A decentralized file storage and sharing platform built on Ethereum blockchain using IPFS for storage and Solidity smart contracts for access control.

## 🚀 Project Overview

Genesis 1.0 - GDrive3.0 is a blockchain-based alternative to traditional cloud storage services like Google Drive. It enables users to upload files (images) to IPFS (InterPlanetary File System) and manage access control through Ethereum smart contracts, ensuring true decentralization and user ownership of data.

## ✨ Key Features

- **Decentralized Storage**: Files stored on IPFS, ensuring no single point of failure
- **Blockchain Access Control**: Smart contracts manage file ownership and sharing permissions
- **User Ownership**: Complete control over your files with blockchain verification
- **Secure Sharing**: Grant or revoke access to specific users through smart contracts
- **Immutable Records**: All transactions and access changes are recorded on blockchain

## 🛠️ Tech Stack

- **Frontend**: React.js
- **Smart Contracts**: Solidity
- **Blockchain Framework**: Hardhat
- **Storage**: IPFS (via Pinata)
- **Blockchain**: Ethereum (Testnet/Mainnet)
- **Wallet Integration**: MetaMask

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MetaMask browser extension
- Pinata API keys (for IPFS)
- Ethereum testnet account (for testing)

## 🔧 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/StarkAg/decentralized-gdrive.git
cd "Genesis 1.0 - GDrive3.0"
```

### 2. Install Hardhat Dependencies

```bash
npm install
```

### 3. Compile Smart Contracts

```bash
npx hardhat compile
```

### 4. Deploy Smart Contract

```bash
# Deploy to local network
npx hardhat run scripts/deploy.js --network localhost

# Deploy to testnet (e.g., Sepolia)
npx hardhat run scripts/deploy.js --network sepolia
```

### 5. Install Frontend Dependencies

```bash
cd client
npm install
```

### 6. Configure Environment

1. Get Pinata API keys from [Pinata](https://pinata.cloud)
2. Update `FileUpload.js` in the client with your Pinata API keys:
   ```javascript
   const PINATA_API_KEY = 'your-api-key';
   const PINATA_SECRET_KEY = 'your-secret-key';
   ```

3. Update contract address in `App.js` after deployment:
   ```javascript
   const CONTRACT_ADDRESS = 'your-deployed-contract-address';
   ```

### 7. Run the Application

```bash
# Start React application
cd client
npm start
```

The application will open at `http://localhost:3000`

## 📖 Usage Guide

### Initial Setup

1. **Install MetaMask**: 
   - Install MetaMask browser extension
   - Create or import a wallet
   - Connect to Ethereum testnet (Sepolia, Goerli, etc.)

2. **Get Testnet ETH**:
   - Use a faucet to get testnet ETH for gas fees
   - Example: [Sepolia Faucet](https://sepoliafaucet.com/)

### Uploading Files

1. Connect your MetaMask wallet
2. Click "Upload Image" button
3. Select an image file
4. Wait for upload to IPFS
5. Transaction will be recorded on blockchain

### Sharing Files

1. Upload a file first
2. Use the "Share" function to grant access to specific addresses
3. Enter the recipient's Ethereum address
4. Confirm the transaction in MetaMask

### Accessing Shared Files

1. Click "Get Data" button
2. Enter the file owner's Ethereum address
3. If you have access, files will be displayed
4. If not, you'll see "You don't have access" error

### Important Notes

⚠️ **Important**: 
- Always upload an image BEFORE clicking "Get Data"
- "Get Data" will throw an error if no file is uploaded first
- You can only access files if the owner has granted you access
- Make sure contract address is updated after deployment

## 🏗️ Project Structure

```
Genesis 1.0 - GDrive3.0/
├── contracts/          # Solidity smart contracts
├── scripts/           # Deployment scripts
├── client/            # React frontend application
│   ├── src/
│   │   ├── App.js     # Main app component
│   │   └── FileUpload.js  # File upload component
│   └── package.json
├── hardhat.config.js  # Hardhat configuration
├── package.json
└── README.md
```

## 📚 Smart Contract Features

- **Upload Function**: Store file metadata and IPFS hash on blockchain
- **Access Control**: Grant/revoke access to specific addresses
- **Ownership Management**: Track file ownership
- **Access Verification**: Check if user has access to files

## 🔐 Security Considerations

- Private keys should never be exposed
- Always use testnet for development
- Verify smart contract code before mainnet deployment
- Use secure methods for API key storage

## 🧪 Testing

```bash
# Run Hardhat tests
npx hardhat test

# Run tests with coverage
npx hardhat coverage
```

## 📹 Demo Videos

- **English**: [Decentralize Google Drive](https://youtu.be/M-KRLlHG_zs?si=rD7I-fH-P8kGiwwf)
- **Hindi**: [Decentralize Google Drive](https://youtu.be/fghqq3-P3x0?si=CVMpHFTW3-fa3R3A)

## 🎯 Hackathon Details

- **Event**: Genesis 1.0 Hackathon
- **Project**: GDrive3.0 - Decentralized File Storage
- **Category**: Blockchain, Web3
- **Status**: Completed

## 🚀 Deployment

### Smart Contract Deployment

1. Configure network in `hardhat.config.js`
2. Add private key to `.env` file (never commit this)
3. Deploy:
   ```bash
   npx hardhat run scripts/deploy.js --network <network-name>
   ```

### Frontend Deployment

The React app can be deployed to:
- Vercel
- Netlify
- GitHub Pages
- Any static hosting service

## 🤝 Contributing

This is a hackathon project. For contributions:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is part of a hackathon submission. All rights reserved.

## 👥 Authors

- Developed as part of Genesis 1.0 hackathon project

## 🙏 Acknowledgments

- IPFS for decentralized storage
- Pinata for IPFS pinning service
- Hardhat for development framework
- Ethereum community

---

**Built with ❤️ for the decentralized web**
