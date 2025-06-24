📦 Project: DMC with JANCTION
-----------------------------

### Overview

**DMC with JANCTION** is a decentralized music data storage and monetization platform built as a sidechain project of _JANCTION_, a public blockchain derived from Japan's IoT-focused **Jasmy** ecosystem.

The project's core philosophy is to "give value to your own data" by enabling content creators and consumers to store, share, and profit from audio data on-chain—without relying on centralized platforms like YouTube or Spotify.

### Key Features

*   **Decentralized Storage with IPFS**  
    All music data is permanently stored using IPFS, ensuring durability, censorship resistance, and decentralized access.
    
*   **Proof of Resource Blockchain**  
    JANCTION is built on a novel blockchain architecture where nodes contribute GPU resources to store and retrieve multimedia data.
    
*   **Token Economy (Watch/Listen to Earn)**  
    Users earn points and tokens simply by watching or listening to content. These points can be exchanged for products, services, or even cash via DMC Coin.
    
*   **Integrated Wallet**  
    A custom wallet solution bridges Web2 and Web3, allowing even non-crypto users to participate without installing special apps.
    
*   **Target Audience**  
    This project is especially beneficial for club DJs, music producers, and indie artists looking to share and monetize their work securely and independently.
    

* * *

🧩 IPFS Node Integration
------------------------

### Purpose

The IPFS Node is responsible for storing, pinning, and serving music data within the JANCTION ecosystem. It supports decentralized content delivery and works as a gateway between the user-facing frontend and the storage layer.

### Directory Structure

ipfs-node/

├── config/              # IPFS configuration files

├── scripts/             # Bash or Node scripts for pinning/uploading content

├── src/

│   ├── server.js        # REST API for upload/download operations

│   ├── pin-manager.js   # Pinning logic and content tracking

│   └── utils.js         # Helper functions for CID parsing, logging, etc.

├── package.json         # Dependencies and scripts

└── README.md            # Local guide for the IPFS Node

* * *

⚙️ Setup Guide (for IPFS Node)
------------------------------

> Requirements:
> 
> *   Node.js (v18 or higher)
>     
> *   IPFS CLI or Kubo Daemon
>     
> *   Linux or macOS (recommended)
>     

### 1\. Clone the Repository

`git clone https://github.com/your-org/dmc-with-janction.git
cd dmc-with-janction/ipfs-node` 

### 2\. Install Dependencies

`npm install` 

### 3\. Start IPFS Daemon (in separate terminal)

`ipfs init
ipfs daemon` 

### 4\. Launch the Node Server

`npm start` 

This will start the local server on `http://localhost:3000`, exposing endpoints like:

*   `POST /upload` — Upload audio and receive CID
    
*   `GET /file/:cid` — Retrieve stored file using CID
    

### 5\. (Optional) Pin Files Manually

`ipfs add ./music/track1.mp3
ipfs pin add ` 

* * *

📜 License
----------

This repository follows the same open-source license as the base IPFS Node implementation. See the `LICENSE` file for details.
