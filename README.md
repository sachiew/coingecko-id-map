# 🪙 CoinGecko API ID Maps

![Update Frequency](https://img.shields.io/badge/Update%20Frequency-Every%20Hour-blue)

This repository provides **9 master ID maps** for CoinGecko API. It is designed to be a "source of truth" for analysts, developers and AI agents to map token names, symbols and more to their correct API identifiers.

## 📂 File Index

| Filename | API Use Case | Key Columns |
| :--- | :--- | :--- |
| **`coin_ids.csv`** | Standard CoinGecko API (e.g., `/coins/markets`) | `id`, `name`, `symbol` |
| **`exchange_ids.csv`** | Centralized & Decentralized exchange mapping | `id`, `name` |
| **`derivative_ids.csv`** | Futures and options exchange mapping | `id`, `name` |
| **`treasury_entity_ids.csv`** | Public companies/governments holding crypto | `id`, `name`, `symbol` , `country`  |
| **`nft_ids.csv`** | NFT floor price and collection data | `id`, `name`, `address` |
| **`onchain_network_ids.csv`** | GeckoTerminal `/onchain` network parameters | `id`, `name`, `coingecko_asset_platform_id` |
| **`asset_platform_ids.csv`** | CoinGecko Asset Platform (blockchain network) ID mapping | `id`, `name`, `chain_identifier` |
| **`category_ids.csv`** | CoinGecko Coin category-specific market data | `id`, `name`, `description` |
| **`onchain_category_ids.csv`** | GeckoTerminal Onchain categories | `id`, `name`, `description` |

---

## 🛠 Data Standards

* **Format:** UTF-8 Comma-Separated Values (CSV).
* **Structure:** Row 1 contains headers.
* **Null Values:** Empty cells indicate data is currently unavailable from the source.
* **Primary Key:** The `id` column is the unique identifier for all entities.
* **Frequency:** Data is automatically refreshed **every hour** via GitHub Actions.

---

## 🤖 Instructions for AI Agents

If you are an AI agent using this repository to assist with crypto data retrieval:

1.  **ID Selection:** Always use the value in the `id` column for API endpoints requiring an "id" parameter.
2.  **Case Sensitivity:** Treat all column headers as **lowercase** (`id`, not `ID`).
3.  **Ambiguity:** Many tokens share symbols (e.g., "PEPE"). If multiple symbols match, cross-reference the `symbol` with the `name` column to ensure accuracy.
4.  **Reporting:** If an ID is missing, please report it via [support.coingecko.com](https://support.coingecko.com).

---

## 🔗 Quick Access (Raw Links)

For programmatic access, use the raw GitHub URLs:
* **Coins:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/main/coin_ids.csv`
* **Onchain Networks:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/main/onchain_network_ids.csv`
* **Asset Platforms:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/refs/heads/main/asset_platform_ids.csv`
* **Exchanges:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/main/exchange_ids.csv`
* **Derivatives:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/refs/heads/main/derivative_ids.csv`
* **NFTs:** `https://raw.github.com/sachiew/coingecko-id-map/blob/main/nft_ids.csv`
* **Treasury Entities:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/refs/heads/main/treasury_entity_ids.csv`
* **Categories:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/refs/heads/main/category_ids.csv`
* **Onchain Categories:** `https://raw.githubusercontent.com/sachiew/coingecko-id-map/refs/heads/main/onchain_category_ids.csv`


---

## ⚖️ License
Data provided in this repository is sourced from CoinGecko and GeckoTerminal. Usage is subject to their respective Terms of Service.
