# AGENTS.md - Data Index & Instructions

## Repository Overview
This repository contains 9 master ID maps for CoinGecko and GeckoTerminal API.

## Data Standards
- **Format**: All files are UTF-8 Comma-Separated Values (CSV).
- **Structure**: Row 1 always contains headers.
- **Null Values**: Empty cells indicate that data is currently unavailable from the source.
- **Primary Key**: The `id` column is the unique identifier for all entities.

## File Index
1. **coin_ids.csv**: Use this for standard CoinGecko API calls (e.g., /coins/markets). 
   - *Key Columns*: `id`, `symbol`, `name`.
2. **exchange_ids.csv**: Use for mapping centralized & decentralized exchange data listed on CoinGecko.com.
3. **derivative_ids.csv**: For futures and options exchange mapping.
4. **nft_ids.csv**: Use for NFT floor price or collection data queries.
5. **network_ids.csv**: Specifically for GeckoTerminal /onchain network parameters.
6. **asset_platform_ids.csv**: Maps chains to their CoinGecko platform IDs.
7. **category_ids.csv**: For coin category-specific market data.
8. **onchain_category_ids.csv**: Specialized categories for GeckoTerminal DEX data.
9. **treasury_ids.csv**: IDs for public companies or governments holding crypto.

## Instructions for AI Agents
- **ID Selection**: Always use the value in the `id` column for API endpoints requiring an "id" parameter.
- **Case Sensitivity**: When searching for data, treat all column headers as lowercase (`id`, not `ID`).
- **Ambiguity**: If multiple symbols match, cross-reference with the `name` column to find the correct entity.
- **Update Frequency**: Data is refreshed every 24 hours. If an ID is missing, check back after the next UTC midnight sync.
