# GigLend
![GigLend logo](assets/logo.png)

**Undercollateralized microloans for gig workers backed by on-chain income history**

## Overview
GigLend is a Solana protocol that turns verified stablecoin income into an on-chain reputation score, letting gig workers borrow small working-capital loans without collateral. DeFi yield seekers fund these loans by depositing USDC into a pooled lending vault.

## Problem
Gig workers, drivers, freelancers, and creators, are increasingly paid in stablecoins, but they have no credit history banks recognize and no collateral to offer DeFi protocols. As a result, they are excluded from both traditional and most on-chain lending markets, even when their income is real, regular, and verifiable.

## Solution
GigLend aggregates a worker's stablecoin payment history and runs it through an on-chain credit scoring contract that evaluates payment frequency and consistency. This score becomes a reputation asset: workers use it, instead of collateral, to borrow small loans from a shared lending pool. Lenders deposit USDC into that pool and earn yield as loans are repaid.

## Features (MVP)
- On-chain income verification by aggregating stablecoin payment history
- Simple credit score smart contract based on payment frequency and consistency
- Lending pool vault where users deposit USDC and earn yield
- Borrower dashboard to request and repay micro-loans
- Basic default handling via score penalty and repayment incentives

## Tech Stack
- Anchor, Rust (on-chain programs)
- USDC (lending and repayment asset)
- Pyth (price feeds)
- React (frontend)
- PostgreSQL indexer (off-chain payment history aggregation)

## How It Works

```
Stablecoin payouts
      |
      v
PostgreSQL indexer  --->  aggregates payment history
      |
      v
Credit Score Program (Anchor, Solana)
      |
      v
Reputation Score  --->  Borrower Dashboard  --->  Loan Request
      |
      v
Lending Pool Vault (USDC) <--- Lender Deposits
      |
      v
Loan Disbursement / Repayment  --->  Score Update
```

1. A worker's stablecoin payment history is indexed off-chain and submitted for verification.
2. An on-chain credit score contract scores the history for frequency and consistency.
3. Lenders deposit USDC into a pooled vault, earning yield as the vault funds loans.
4. Workers use their score to request a micro-loan through the borrower dashboard.
5. Repayment or default updates the score on-chain, reinforcing good repayment behavior.

## Roadmap
- Integrate with real gig platforms' payout APIs for verified income data
- Build a more robust credit scoring model incorporating historical loan performance
- Pursue partnerships with gig platforms to offer embedded lending

## Pitch
See our full pitch deck at [docs/pitch.pdf](docs/pitch.pdf) and the spoken pitch script at [docs/pitch-script.md](docs/pitch-script.md).

## Team
- [Name] — Role (placeholder)
- [Name] — Role (placeholder)
- [Name] — Role (placeholder)

Built for the Colosseum hackathon.

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)


## Prototype

Live prototype: https://ytakahashi2020.github.io/giglend/

The source is [docs/index.html](docs/index.html) (served with GitHub Pages from the /docs folder). All data is simulated.
