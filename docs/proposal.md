# GigLend

_Undercollateralized microloans for gig workers backed by on-chain income history_

## Summary

GigLend lets gig workers (drivers, freelancers, creators) build a verifiable on-chain income reputation from stablecoin payment history, then borrow small working-capital loans against that reputation instead of collateral. Lenders earn yield by funding a pooled vault scored by an on-chain credit model.

## Target users

Gig economy workers needing short-term working capital, and DeFi yield seekers

## Problem

Gig workers often lack credit history and collateral, so they're excluded from traditional and most DeFi lending.

## Solution

An on-chain reputation score built from verified stablecoin payment inflows enables undercollateralized micro-lending from a pooled vault.

## MVP features

- On-chain income verification by aggregating stablecoin payment history
- Simple credit score smart contract based on payment frequency/consistency
- Lending pool vault where users deposit USDC and earn yield
- Borrower dashboard to request and repay micro-loans
- Basic default handling via score penalty and repayment incentives

## Chains

Solana

## Tech

Anchor, Rust, USDC, React, Pyth (price feeds), PostgreSQL indexer

## Category

DeFi

## Why now

Gig work and stablecoin payouts are rapidly converging, but no credit infrastructure exists yet to unlock capital for this growing on-chain-paid workforce.

## Roadmap

- Integrate with real gig platforms' payout APIs for verified income data
- Build a more robust credit scoring model with historical loan performance
- Pursue partnerships with gig platforms to offer embedded lending
