# UBounty.ai - End-to-End Demo

> **Create & fund a GitHub bounty in 15 seconds** — no account, no KYC, no friction.

---

## Table of Contents

1. [What is UBounty?](#what-is-ubounty)
2. [Quick Demo: Create a Bounty in 15 Seconds](#quick-demo-create-a-bounty-in-15-seconds)
   - [Step 1: Enter Issue Details & AI Analysis](#step-1-enter-issue-details--ai-analysis-7s)
   - [Step 2: Pay with x402 Protocol](#step-2-pay-with-x402-protocol-8s)
   - [Step 3: Creator Allocates Payment](#step-3-creator-allocates-payment)
   - [Step 4: Developer Connects Wallet & Gets Paid](#step-4-developer-connects-wallet--gets-paid)
3. [How Developers Claim Bounties](#how-developers-claim-bounties)
4. [Payment Scenarios](#payment-scenarios)
5. [Technical Details](#technical-details)
6. [FAQ](#faq)
7. [Get Started](#get-started)
8. [Resources](#resources)

---

## What is UBounty?

**UBounty.ai** is an automated cryptocurrency bounty platform for GitHub issues. Fund any public GitHub issue and pay developers instantly when they solve it.

**Key Features:**
- ⚡ **15-second bounty creation** with AI-powered analysis
- 🔗 **Works with ANY public GitHub repo** (no permission needed)
- 💰 **Instant USDC payments** on Base blockchain via x402 protocol
- 🤖 **Automatic settlement** when PRs are merged
- 🔒 **Trustless escrow** - funds locked in smart contracts
- 💵 **9% platform fee** - transparent pricing

---

## Quick Demo: Create a Bounty in 15 Seconds

### Step 1: Enter Issue Details & AI Analysis (7s)

<img src="./01.create-bounty.png" alt="Create Bounty Form" width="700"/>

1. **Login with GitHub** → Click "Create Bounty"
2. **Paste GitHub issue URL**: `https://github.com/ubounty-app/ubounty-demo/issues/3`
3. **Click "AI Analyze"** → Claude AI suggests pricing, difficulty, and requirements
4. **Set amount**: $10.00 USDC (+ $0.50 fee = $10.50 total)
5. **Add labels & deadline** (optional)
6. **Click "Fund & Create Bounty"**

**AI Analysis provides:**
- Type: Feature / Bug Fix / Enhancement
- Difficulty: Easy / Medium / Hard
- Estimated time: 8-16 hours
- Suggested price range: $200-$600
- Detailed requirements breakdown

---

### Step 2: Pay with x402 Protocol (8s)

<img src="./02.x402payment.png" alt="x402 Payment Modal" width="600"/>

1. **x402 payment modal opens** showing:
   - Your wallet: `0x3828...f344`
   - Amount: `$10.5 USDC`
   - Network: `Base`
2. **Click "Pay now"**
3. **Approve in your wallet** (MetaMask/Coinbase Wallet/Rainbow)
4. **Funds locked on-chain** in 3-5 seconds

✅ **Bounty is now live!** UBounty automatically:
- Verifies transaction on Base blockchain
- Posts bounty comment on GitHub issue ([see example](https://github.com/ubounty-app/ubounty-demo/issues/3))
- Lists bounty on [ubounty.ai/bounties](https://ubounty.ai/bounties)

**Real example:** [Transaction on BaseScan](https://basescan.org/tx/0x9d992a57654d54c644fc5ae99959b4436e5373cfcb197255f465c1ba84837550)

---

### Step 3: Creator Allocates Payment

<img src="./03.making-payment-decision.png" alt="Payment Decision" width="800"/>

**After developer submits PR and maintainer merges:**

1. **Bounty creator reviews** all merged PRs
2. **Allocates payment** percentage to each contributor:
   - In this example: **@1bcMax** gets **100%** ($10.0 USDC)
3. **Clicks "Confirm Payment Decision"**

The page shows:
- Bounty details, requirements, and acceptance criteria
- All merged PRs with contributor names
- Allocation interface (adjust % for multiple contributors)
- Protection: Auto-split after 7 days if creator doesn't decide

---

### Step 4: Developer Connects Wallet & Gets Paid

<img src="./04.dev-Wallet-setting.png" alt="Wallet Settings" width="700"/>

**Developer connects wallet to receive payment:**

1. **Visit Settings** at [ubounty.ai/settings](https://ubounty.ai/settings)
2. **Enter wallet address** (starting with `0x...`)
3. **Click "Save Wallet"**
4. **Payment executes automatically** (3-5 seconds)

**Important:**
- ⚠️ Funds sent to Base Mainnet only
- Double-check wallet address (payments are irreversible)
- No deadline to connect wallet - approved payments wait indefinitely
- Once saved, USDC arrives instantly

---

## How Developers Claim Bounties

### 1. Discover Bounty
- Browse [ubounty.ai/bounties](https://ubounty.ai/bounties)
- See UBounty bot comment on GitHub issues
- Filter by price, difficulty, or tech stack

### 2. Submit Solution
```bash
# Fork repo and create PR
git checkout -b fix-issue-3
# ... make changes ...
git commit -m "Fix issue"
git push
```

**Important:** Include `Fixes #3` in PR description to link to bounty!

### 3. Creator Allocates Payment

![Payment Decision](./03.making-payment-decision.png)

When your PR is merged, the bounty creator sees all merged PRs and decides allocation:

- **Single developer**: Allocate 100% to one contributor
- **Multiple developers**: Split payment by contribution (e.g., 70%/30%)
- **Reject**: Allocate 0% if work doesn't meet requirements

In this example:
- Developer: **@1bcMax** (PR #4)
- Allocation: **100%** = **$10.0 USDC**
- Creator clicks **"Confirm Payment Decision"**

**Protection:** If creator doesn't decide within 7 days, payment auto-splits equally among all merged PRs.

### 4. Get Paid
1. **Connect wallet** at [ubounty.ai/settings](https://ubounty.ai/settings)
2. **Receive USDC instantly** (3-5 seconds after approval)

---

## Payment Scenarios

**Single Developer:**
- Your PR merged → You get 100%

**Multiple Developers:**
- Creator allocates % to each contributor
- Example: Alice 70% ($70), Bob 30% ($30)

**Auto-Split (if creator doesn't decide):**
- After 7 days, funds split equally among all merged PRs
- Your protection against negligent creators

---

## Technical Details

| Component | Technology |
|-----------|-----------|
| **Blockchain** | Base (Ethereum L2) |
| **Currency** | USDC stablecoin |
| **Protocol** | x402 (instant payments) |
| **Settlement** | 3-5 seconds |
| **Platform Fee** | 9% (paid by creator) |
| **Gas Fees** | Free (sponsored by platform) |
| **Min Bounty** | $10 USDC |

**Architecture:**
```
User Wallet → x402 Protocol → Base Blockchain Escrow
                                      ↓
                           (Locked until approved)
                                      ↓
                    Creator Approves → Developer Wallet (3-5s)
```

---

## FAQ

**Q: Do I need to own the repo to create a bounty?**
No! Create bounties on ANY public GitHub issue.

**Q: Can multiple developers earn from one bounty?**
Yes! Creator can split payment among multiple contributors.

**Q: What if creator never approves payment?**
Auto-split after 7 days protects developers.

**Q: Are payments reversible?**
No. Cryptocurrency payments are final and on-chain.

**Q: What wallets are supported?**
Any wallet with Base network: MetaMask, Coinbase Wallet, Rainbow, WalletConnect.

**Q: Do developers pay fees?**
No! Developers receive 100% of allocated amount. Gas fees paid by platform.

---

## Get Started

**For Creators:** [ubounty.ai/create](https://ubounty.ai/create)
**For Developers:** [ubounty.ai/bounties](https://ubounty.ai/bounties)
**View Example:** [Issue #3 with live bounty](https://github.com/ubounty-app/ubounty-demo/issues/3)

---

## Resources

- **Website:** [ubounty.ai](https://ubounty.ai)
- **Full Docs:** [ProductFeatures](https://github.com/ubounty-app/ProductFeatures)
- **BaseScan:** [basescan.org](https://basescan.org)
- **Support:** support@ubounty.ai

---

*Powered by x402 protocol | Built on Base | Instant USDC payments* ⚡

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
