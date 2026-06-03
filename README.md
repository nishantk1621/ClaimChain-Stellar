contract address :
<img width="1883" height="881" alt="image" src="https://github.com/user-attachments/assets/8d96b807-8877-42b8-9b45-9bc0f4f5987e" />

UI Screenshot :
<img width="1254" height="708" alt="image" src="https://github.com/user-attachments/assets/41b694ff-c54b-4959-80d6-74d6027368b7" />



# 🛡️ ClaimChain — Decentralized Insurance Claims System

## 📌 Project Description  
Traditional insurance is plagued by centralized gatekeepers — adjusters, administrators, and executives who decide whether your claim gets paid, and when. ClaimChain eliminates all of that.  

Built on *Stellar Soroban*, ClaimChain is a decentralized application (DApp) where insurance claims are filed, reviewed, and paid out entirely on-chain through community consensus. There is no owner, no admin role, and no privileged address — the smart contract is permissionless by design.  

Claimants stake a small amount of XLM when filing, which deters spam. The broader community votes on claim validity. Once voting ends, anyone can trigger resolution and payout — the contract enforces the outcome automatically.  

---

## ⚙️ What It Does  
- Fund the insurance pool — anyone can contribute XLM  
- File a claim with title, description, evidence URI, and amount  
- Vote on claims (approve/reject) during a 3-day window  
- Resolve claims once voting ends and quorum is met  
- Execute payouts for approved claims  
- Reclaim 50% stake for rejected claims  

---

## ✨ Features  

### Core  
- 🔓 Fully permissionless (no owner, no admin)  
- 🗳️ Community voting with quorum & threshold  
- ⚡ Trustless automatic payouts  
- 🛡️ Stake-based spam deterrence  
- 🎁 Voter rewards (1% of claim)  
- 📎 Evidence via IPFS/URLs  
- 🌐 Open funding pool  

### DApp Frontend  
- 🦊 Freighter wallet integration  
- 📊 Live on-chain data via Soroban RPC  
- 🧾 Explorer links (Stellar Expert)  
- 🎨 Terminal-style UI (IBM Plex Mono)  
- 📱 Responsive design  

### Contract Mechanics  
- Voting Period: 3 days  
- Minimum Quorum: 3 votes  
- Approval Threshold: 60%  
- Claimant Stake: 0.01 XLM  
- Max Claim Amount: 10,000 XLM  
- Voter Reward: 1% (split equally)  
- Rejected Stake Returned: 50%  

---

## 🔄 How It Works  
1. User files a claim with 0.01 XLM stake  
2. 3-day voting window starts  
3. Community votes approve/reject  
4. After voting ends, anyone calls resolve_claim()  
5. If ≥60% approve → payout executed  
6. If <60% approve → 50% stake returned  

---

## 📜 Smart Contract  
 
- *Contract Address:*  
  CAY57LW6Q4KS3BXRNDHC37UJB6LKKA4TGJLQ3KNRG4PTBFOJ3FABBXMK  

- *Freighter Address:*  
  GD3KADPLFNCKMGLTJS2AXUU3KWSSNJH3C3MA3OC3PGOAMAYC35S5SFWQ  

---

## 🛠 Tech Stack  
- Rust · Soroban SDK  
- Stellar Mainnet  
- Soroban RPC (soroban.stellar.org)  
- Vanilla JS · HTML · CSS  
- @stellar/stellar-sdk v12  
- Freighter Wallet  
- IPFS  
- Stellar Expert  

---

## 🚀 Getting Started  

### Prerequisites  
- Freighter wallet installed  
- Stellar Mainnet account with XLM  
- Modern browser  

### Run Locally  
git clone https://github.com/your-org/claimchain  
cd claimchain  
open ClaimChain_Stellar.html  

Or:  
npx serve .  

---

## 📐 Contract Functions  

### Read Functions  
- get_all_claims()  
- get_claim(id)  
- get_pool_balance()  
- get_voters(id)  
- get_voting_status(id)  

### Write Functions  
- contribute()  
- file_claim(title, description, evidence_uri, amount)  
- vote(claim_id, approve)  
- resolve_claim(claim_id)  
- execute_payout(claim_id)  
- reclaim_stake(claim_id)  

---

## 🔓 Permissionless Design  
- No owner or admin roles  
- No whitelist system  
- Anyone can resolve claims  
- Anyone can execute payouts  
- Anyone can reclaim stake  
- Economic incentives replace moderation  
- Time-based rules enforced by smart contract
