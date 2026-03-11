# Decentralized KYC Project - TODO List (PRD v3.0)

## Phase 1: Smart Contract Upgrade (Multi-Entity) [COMPLETE]
- [x] Define `EntityType` enum (BANK, CRYPTO_EXCHANGE, INSURANCE, GOVERNMENT, etc.)
- [x] Add `EntityInfo` struct and `entityRegistry` mapping
- [x] Implement `registerEntity()` and `removeEntity()` (Admin only)
- [x] Refactor `checkDocumentHash()` to:
    - [x] Require the calling address to be a registered entity
    - [x] Accept and log the `EntityType`
    - [x] Emit updated events including the entity type
- [x] Add `userEntityAccess` mapping to track history on-chain

## Phase 2: Backend Integration & Role Expansion [IN PROGRESS]
- [x] Implement 'Entity' role in User model
- [x] Create Entity registration flow (Signup)
- [x] Enhance Entity API:
    - [x] Validate entity's on-chain registration status before processing requests
    - [x] Logic for entities to "pull" approved data from user vault (currently partial)
- [x] User Approval Flow in Vault

## Phase 3: Frontend - Multi-Entity UI [COMPLETE]
- [x] **Entity Selector**: Update institutional pages to allow users to select specific entity types/instances
- [x] **Public Status Checker**: Implement a page where any wallet address can be checked for KYC status on-chain
- [x] **Admin Dashboard**: Add UI for managing the on-chain Entity Registry
- [x] **Branding & Consistency**: Ensure the "Monochrome Premium" theme is applied to all new v3 components

## Completed Features (v2 -> v3 Transition)
- [x] Client-side SHA-256 Hashing (No document transmission)
- [x] MetaMask Wallet Integration
- [x] Basic User/Verifier/Admin roles
- [x] Document Vault with IPFS (Pinata) backup
- [x] Basic Entity Request & Approval logic
- [x] Stable Node.js/Express/MongoDB Backend
