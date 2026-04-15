# Solia Network

> Solia is a programmable non-custodial escrow and settlement protocol on Solana for global payments, P2P trade, freelance transactions, and any workflow where trust between parties cannot be assumed.
>
> It combines on-chain escrow, a live devnet trading surface, and structured dispute resolution into one system, with public website, product app, and docs already live.

[![Status](https://img.shields.io/badge/status-active%20development-blue)]()
[![Network](https://img.shields.io/badge/network-Solana-14F195)]()
[![Category](https://img.shields.io/badge/category-P2P%20Escrow-0A7B83)]()
[![Hackathon](https://img.shields.io/badge/Colosseum-2026-orange)]()
[![Environment](https://img.shields.io/badge/environment-live%20on%20devnet-brightgreen)]()

## Live Product Links

- Website: [www.solia.network](https://www.solia.network)
- Escrow App: [escrow.solia.network](https://escrow.solia.network)
- Documentation: [docs.solia.network](https://docs.solia.network)

## At a Glance

Solia is building escrow and settlement infrastructure for peer-to-peer transactions where trust cannot be assumed.

Today, the Solia ecosystem already includes:

- a public website for product positioning and project overview
- a live escrow trading application on devnet
- a documentation portal for product documentation and future API usage

The escrow application currently supports order blocks for buying and selling and is already deployed live on devnet.

## Judge Checklist

- Visit the public website: [www.solia.network](https://www.solia.network)
- Open the live escrow app on devnet: [escrow.solia.network](https://escrow.solia.network)
- Review the docs portal: [docs.solia.network](https://docs.solia.network)
- Evaluate the buy and sell order flow
- Evaluate escrow-backed settlement flow
- Evaluate dispute escalation and evidence attribution workflow
- Evaluate the modular architecture across app, protocol, and Vera
- Evaluate whether Solia solves a real trust problem for P2P and freelance payments

## Why Solia Should Win

- Solia targets a real coordination problem: trust-minimized payments and settlement between parties that do not know each other.
- The product is not just a smart contract demo. It already has a public website, a live devnet escrow app, and a documentation surface.
- Disputes are treated as a first-class product and protocol concern, not an afterthought.
- The architecture is modular and credible: user experience, on-chain protocol, and dispute intelligence are clearly separated.
- Solana is used for the parts it is actually good at: fast settlement, low fees, and programmable on-chain escrow state.

## What Solia Is

Solia Network is a non-custodial escrow protocol built on Solana for peer-to-peer transactions where trust is weak and transaction risk is high.

Instead of sending funds directly to another party and hoping the transaction completes fairly, users lock funds into escrow. Funds are only released when trade conditions are met, both parties confirm completion, or a dispute is resolved through a structured workflow.

## The Problem

Peer-to-peer transactions still break down in the same places:

- Buyers fear paying before delivery.
- Sellers fear delivering before payment.
- Existing escrow systems are often centralized, opaque, slow, or expensive.
- Disputes are usually handled manually with weak evidence trails and poor accountability.

This is especially painful in freelance work, informal digital commerce, service delivery, and cross-border peer transactions.

## The Solia Approach

Solia replaces trust in the counterparty with verifiable escrow logic on Solana.

Core design goals:

- Non-custodial fund locking
- Clear trade state transitions
- Mutual confirmation before settlement
- Structured evidence submission during disputes
- Admin-led resolution workflow with Vera assisting dispute analysis

## Product Surfaces

### Main Website

`www.solia.network` is the public entry point for Solia. It presents the product thesis clearly: programmable escrow for global payments, P2P trade, and freelance settlement.

### Escrow Trading App

`escrow.solia.network` is the live product surface for escrow trades.

Current known scope:

- order blocks for buying and selling
- live deployment on devnet
- escrow-driven trade interaction flow

### Documentation Portal

`docs.solia.network` contains Solia documentation for builders, product understanding, and future API usage.

## How It Works

1. A trade is created with agreed terms between buyer and seller.
2. Funds are locked into escrow on-chain.
3. The counterparty accepts the trade.
4. The trade is completed when both sides confirm the outcome.
5. If something goes wrong, either side can trigger a dispute.
6. Evidence is submitted with clear attribution by role.
7. Vera helps structure and analyze the dispute workflow.
8. Resolution determines whether funds are released, refunded, or otherwise settled.

## Current Live Status

- Public website is live
- Escrow application is live on devnet
- Documentation portal is live
- Solia is actively being developed for the Colosseum Hackathon 2026

## Architecture Diagram

```mermaid
flowchart TD
    U[Users]
    W[www.solia.network<br/>Public Website]
    E[escrow.solia.network<br/>Live Escrow App on Devnet]
    D[docs.solia.network<br/>Developer Docs]
    A[Solia App<br/>Private Product Layer]
    P[Solia Protocols<br/>Private On-Chain Escrow Layer]
    V[Vera<br/>Private Dispute Intelligence Layer]
    S[Solana Devnet]

    U --> W
    U --> E
    U --> D

    E --> A
    A --> P
    P --> S

    A --> V
    V --> A
    V --> P

    W -. product overview .-> A
    D -. integration and future API usage .-> A
    D -. protocol understanding .-> P
```

## Architecture

Solia is organized into three connected components:

### 1. Solia App

Private mobile application for user-facing flows:

- trade creation and acceptance
- escrow interaction
- dispute submission
- user activity and transaction experience

Repository:
`https://github.com/Solia-Network/solia_app.git`

### 2. Solia Protocols

Private on-chain protocol layer for escrow execution:

- escrow account logic
- fund locking
- settlement rules
- dispute-triggered state transitions

Repository:
`https://github.com/Solia-Network/solia_protocols.git`

### 3. Vera

Private dispute intelligence layer for structured conflict handling:

- evidence processing
- dispute workflow support
- conflict analysis
- admin-facing decision support

Repository:
`https://github.com/Solia-Network/vera-solia.git`

## Current Progress

The following parts are already implemented in the current system:

- live website deployed at `www.solia.network`
- live escrow application deployed at `escrow.solia.network`
- live docs portal deployed at `docs.solia.network`
- order block trading flow for buying and selling
- dispute workflow implemented and tested with real scenarios
- evidence submission with explicit attribution for buyer, seller, and admin
- admin dispute initialization and queue handling
- Vera integration for structured dispute analysis

## Why Solana

Solana is a strong fit for Solia because it enables:

- fast transaction finality for real-time trade flows
- low fees for frequent escrow interactions
- on-chain state management for dispute-aware settlement logic
- scalable infrastructure for high-volume P2P transaction networks

## What Makes Solia Different

- Non-custodial by design: funds are controlled by protocol logic, not a centralized intermediary.
- Dispute-aware escrow: dispute handling is built into the product flow, not bolted on later.
- Evidence-first resolution: disputes are structured around attributable submissions, reducing ambiguity.
- Modular system design: app, protocol, and dispute intelligence are separated for clarity and extensibility.

## Repository Scope

This repository serves as the public project overview for Solia Network.

Because the product is still in active development, the main implementation repositories are private at this stage:

- `solia_app`
- `solia_protocols`
- `vera-solia`

For hackathon judging, this repo is meant to give clear public context around:

- the product vision
- the live surfaces already available
- the system architecture
- the escrow and dispute workflow
- the broader Solia ecosystem across private implementation repositories

## Why This Matters

Solia is not trying to be just another wallet-connected payments app.

It is building trust-minimized transaction infrastructure for real-world coordination problems:

- buyer and seller trust
- milestone-based settlement
- escrow-backed transactions
- evidence-driven dispute handling
- programmable settlement rails on Solana

## Demo and Judge Notes

Judges should evaluate Solia as a full escrow workflow, not just a smart contract:

- live product presence across website, app, and docs
- trade agreement
- buy and sell order flow
- escrow locking
- confirmation-based settlement
- dispute escalation
- evidence attribution
- Vera-assisted dispute analysis
- admin resolution path

This is the core product thesis: bring trust-minimized escrow and structured dispute handling into one Solana-native system.

## Screenshots

Add real screenshots in this section before final submission.

### 1. Landing Page

Caption: Solia's public website introducing programmable escrow for global payments, P2P trade, and freelance settlement.

Placeholder path:
`./assets/screenshots/landing-page.png`

### 2. Escrow Marketplace

Caption: Live devnet escrow trading interface showing buy and sell order blocks.

Placeholder path:
`./assets/screenshots/escrow-marketplace.png`

### 3. Trade Creation Flow

Caption: User flow for creating an escrow-backed trade with defined transaction terms.

Placeholder path:
`./assets/screenshots/trade-creation.png`

### 4. Trade Details and Escrow State

Caption: Trade detail view showing escrow status, counterparties, and current settlement state.

Placeholder path:
`./assets/screenshots/trade-details.png`

### 5. Dispute Submission

Caption: Structured dispute flow with role-based evidence submission.

Placeholder path:
`./assets/screenshots/dispute-submission.png`

### 6. Admin Dispute Queue

Caption: Admin workflow for reviewing, initializing, and resolving disputes.

Placeholder path:
`./assets/screenshots/admin-dispute-queue.png`

### 7. Documentation Portal

Caption: Solia documentation portal for builders, integration guidance, and future API usage.

Placeholder path:
`./assets/screenshots/docs-portal.png`

## Status

Solia Network is in active development as part of the Colosseum Hackathon 2026.

## Contact

If you plan to share a demo, judge access notes, or private repo access instructions, add them here before submission.
