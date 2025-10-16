# ✍️ Chronicle

*The Verifiable History of Creation, Anchored On-Chain.*

---

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com)
[![Solidity](https://img.shields.io/badge/Solidity-^0.8.20-blueviolet)](https://soliditylang.org/)
[![React](https://img.shields.io/badge/React-18-blue)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18-green)](https://nodejs.org/)

## Abstract

**Chronicle** is a real-time, collaborative design tool that redefines creative ownership. By integrating a seamless design canvas with an immutable blockchain ledger, Chronicle allows teams to create, collaborate, and commit versions of their work to the chain. Each commit creates a permanent, tamper-proof, and timestamped record of the design's history, solving the critical problem of proving provenance and intellectual property in the digital age.

---

## The Problem 😟

In creative and professional fields, the history of a design is a chaotic mess of files like `logo_final_v4_real.psd` and ambiguous email chains. This creates significant problems:

* **No Single Source of Truth:** It's difficult to track changes and determine the authoritative version of a design.
* **Disputes Over Ownership:** Proving who designed what and when is nearly impossible, leading to intellectual property disputes.
* **Lack of Verifiability:** A file's "Date Created" metadata is easily alterable, making it an unreliable source of proof.

---

## The Solution ✨

Chronicle provides an unbreakable audit trail for the creative process by using the blockchain as a **time machine**.

* **Real-Time Collaboration:** A shared canvas, powered by WebSockets, allows teams to design together seamlessly, just like in Figma or Miro.
* **Immutable Commits:** At any point, a user can "commit" the current state of the canvas. This action uploads a snapshot of the design to IPFS and anchors its unique fingerprint (CID) to the Polygon blockchain.
* **Cryptographic Proof:** This creates a permanent, timestamped record that is cryptographically signed by the committer. The history can never be altered or deleted.
* **Instant Verification & Restoration:** Anyone can view the project's entire history and restore any previous version with 100% confidence in its authenticity.

---

## How It Works 🚀

1.  **Collaborate:** Users join a shared canvas "room" and begin designing in real-time. All changes are instantly synced to all participants.
2.  **Commit:** When a milestone is reached, a user clicks "Commit to Chain."
3.  **Snapshot & Anchor:** The application serializes the entire canvas state into a JSON file, uploads it to IPFS, and receives a unique Content Identifier (CID).
4.  **On-Chain Transaction:** The user signs a transaction with their wallet to call the `commitSnapshot` function on the smart contract, passing in the IPFS CID.
5.  **Verify & Restore:** The "History" panel instantly updates with the new version. Anyone can now view this historical snapshot or restore the entire canvas to that exact state.

---

## Features (Hackathon MVP)

* **Real-Time Collaborative Canvas:** A shared design space powered by `Fabric.js` and `socket.io`.
* **On-Chain Version History:** Immutable history of all committed snapshots, fetched directly from the blockchain.
* **One-Click Restore:** The ability to "time travel" and restore the canvas to any previously committed state.
* **Decentralized Storage:** All design snapshots are stored on IPFS, ensuring data persistence and decentralization.
* **Wallet Integration:** Secure and easy-to-use wallet connection for authentication and signing transactions.

---

## Tech Stack

* **Blockchain:** Solidity, Hardhat, OpenZeppelin
* **Network:** Polygon (Mumbai Testnet)
* **Frontend:** React (Next.js), `Fabric.js`, `ethers.js`/`wagmi`, Tailwind CSS
* **Backend & Real-Time:** Node.js, Express, `socket.io`
* **Decentralized Storage:** IPFS (via Pinata)

---

## Getting Started

Follow these instructions to set up and run the project locally.

#### Prerequisites

* Node.js (v18 or higher)
* Yarn or npm
* MetaMask browser extension

#### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/chronicle.git](https://github.com/your-username/chronicle.git)
    cd chronicle
    ```

2.  **Install Backend Dependencies:**
    ```bash
    cd server
    npm install
    ```

3.  **Install Frontend Dependencies:**
    ```bash
    cd ../client
    npm install
    ```

4.  **Deploy Smart Contract:**
    * Navigate to the `hardhat` directory.
    * Add your environment variables to a `.env` file.
    * Run `npx hardhat run scripts/deploy.js --network mumbai`.
    * Copy the contract address and ABI into the client and server.

5.  **Run the Application:**
    ```bash
    # Run the backend server from the /server directory
    npm run dev

    # Run the frontend from the /client directory
    npm run dev
    ```

---

## Demo & Presentation

* **Live App:** `[Link to Deployed Vercel/Render Site]`
* **Presentation Slides:** `[Link to Pitch Deck]`

---

## Team

* **Pikachu** - ThunderBolt⚡️
* **Charmaindar** - FlameThrower🔥
* **Squirtle** - WaterGun🌊
