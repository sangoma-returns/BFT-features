 # Bitfrost Prime

## Contents

### Bitfrost Prime
- [Initialize your account](#initialize-your-account)
- [Deposits](#deposits)
- [Withdrawals](#withdrawals)
- [Transfers](#transfers)

### Explore
- [Funding Rate Comparison](#funding-rate-comparison)

### Aggregator
- [Aggregator Overview](#aggregator)
- [Strategies](#strategies)
- [Exit Conditions](#exit-conditions)
- [Scale Orders](#scale-orders)
- [Advanced Settings](#advanced-settings)
- [Template Strategies](#template-strategies)

### Market Maker
- [Advanced](#advanced)
- [Vaults](#vaults)
- [Multi-Strategy](#multi-strategy)
- [Exchange Points](#exchange-points)

#### Enterprise Market Makers
- [Custom Strategies](#custom-strategies)
- [Vault Creation](#vault-creation)
- [Vault Management](#vault-management)

### Funding Rate Arbitrage
- [Make A Carry Trade](#make-a-carry-trade)
- [Funding Rate Arbitrage Bot](#funding-rate-arbitrage-bot)

---

## Initialize your account

Initializing a Bitfrost account follows a defined, sequential process.

### 1. Funding the Account

The user must first deposit funds from an external wallet.  
All deposits are received in USDC on HyperEVM.  
These funds are credited to the user’s Bitfrost parent account.  
The parent account acts as the control layer for all exchange sub-accounts and governs balance allocation, trading permissions, and execution.

### 2. Exchange Selection

After the parent account is funded, the user must select a minimum of two exchanges on which sub-accounts will be created.

In the initial release, supported exchanges are:

Hyperliquid  
Paradex  

Each selected exchange will receive a dedicated sub-account linked to the parent account.

### 3. Capital Allocation

The user specifies how the parent account balance is distributed across the selected exchanges.  
For the initial release, the system applies a default allocation of 50 percent per exchange.  
This allocation can be modified by the user before confirmation.

### 4. Sub-Account Initialization

Once allocation is confirmed, funds are transferred from the parent account to each exchange sub-account.  
This step completes account initialization and enables trading across multiple exchanges using a single Bitfrost account.  
Sub-account funding may take up to 60 minutes to complete.

---

## Deposits

Deposits are used to fund the Bitfrost parent account and may be made during initial setup or at any time after the account is active.

### Supported Network and Asset

All deposits are made in USDC on HyperEVM.  
Only deposits sent on this network and in this asset are supported.

### Deposit Flow

The user initiates a deposit from an external wallet.  
USDC is transferred on HyperEVM to the user’s Bitfrost deposit address.  
After on chain confirmation, funds are credited to the Bitfrost parent account.  
The parent account functions as the primary balance and control layer for all exchange sub-accounts.

### Post Deposit Allocation

After confirmation, deposited funds may be allocated to exchange sub-accounts according to the user’s chosen distribution or transferred manually using the transfer function to fund specific exchanges.

---

## Withdrawals

Withdrawals allow users to remove funds from their Bitfrost account to an external wallet.

### Withdrawal Source

Withdrawals can only be initiated from the Bitfrost parent account.  
Direct withdrawals from exchange sub-accounts are not supported.  
To withdraw funds held on an exchange, the user must first transfer the balance from the exchange sub-account back to the Bitfrost parent account.

### Supported Network and Asset

All withdrawals are made in USDC on HyperEVM.  
Only this network and asset are supported.

### Withdrawal Flow

The user transfers funds from one or more exchange sub-accounts to the Bitfrost parent account, if required.  
The user submits a withdrawal request from the parent account to an external wallet.  
USDC is sent on HyperEVM to the specified destination address.

### Withdrawal Processing

Withdrawals do not alter the configuration or status of existing exchange sub-accounts.

---

## Transfers

Transfers move funds between the Bitfrost parent account and exchange sub-accounts. This mechanism is used to fund exchanges, rebalance capital, and prepare funds for withdrawal.

### Transfer Scope

Transfers are supported in both directions:

From the Bitfrost parent account to an exchange sub-account  
From an exchange sub-account back to the Bitfrost parent account  

Transfers do not move funds to or from external wallets.

### Supported Asset

All transfers are denominated in USDC.

### Transfer Flow

The user selects the source and destination, either the Bitfrost parent account or an exchange sub-account.  
The user specifies the transfer amount or selects a percentage of the available balance.  
The transfer is submitted and processed internally.  
The destination balance is updated once the transfer completes.

### Transfer Constraints

Only free and available capital may be transferred.  
On the Bitfrost side, transfers are limited to the available balance held in the Bitfrost vault.  
On exchange sub-accounts, only capital that is not required for margin, open positions, or risk constraints may be transferred.  
Funds reserved for margin, maintenance requirements, or pending settlement are not transferable.

---

## Explore

## Funding Rate Comparison

The Funding Yield Explorer provides a consolidated view of funding rate yields across supported exchanges.

### Overview

Funding rates are normalized, aggregated across consistent time windows, and presented as annualized percentage yields.

Users may switch between day, week, month, and year views.

### Data Aggregation

Funding rates are collected at native exchange intervals, normalized, and averaged over the selected period.

### Capacity Weighted Selection

Capacity Weighting represents the maximum notional deployable before funding degrades due to liquidity or risk constraints.

---

## Aggregator

The Aggregator provides a unified interface for executing trades across multiple exchanges.

### Market Context

Displays price, funding rate, volatility, open interest, and cross-exchange order book depth.

### Trade Construction

Users specify instrument, direction, notional, eligible exchanges, and execution strategy.

---

## Strategies

Execution strategies define how a trade is broken into orders and routed across exchanges.

Includes:

Impact Minimization  
TWAP  
Target Participation Rate  
Market Maker  
Aggressive Maker  
Aggressive Taker  
Target Time  
Custom  

---

## Exit Conditions

Automated rules for closing or reducing a position.

Includes:

Take Profit  
Stop Loss  
Urgency  

---

## Scale Orders

Splits a trade across multiple price levels within a defined range.

Includes:

Price Range  
Price Skew  
Size Skew  
Number of Orders  

---

## Advanced Settings

Fine grained control over execution trajectory, participation, and risk constraints.

---

## Template Strategies

Save and reuse execution configurations.

---

## Advanced

Advanced Market Maker module for automated liquidity provision.

---

## Vaults

Professionally managed market making strategies operated by verified operators.

---

## Multi-Strategy

Deploy and monitor multiple market making strategies concurrently.

---

## Exchange Points

Unified dashboard of incentive points earned across exchanges.

---

## Custom Strategies

Execute proprietary off chain trading logic using Bitfrost as the execution layer.

---

## Vault Creation

Create market maker vaults with minimum deposit and TVL commitments.

---

## Vault Management

Manage vault capital, performance fees, and operational controls.

---

## Make A Carry Trade

Construct funding rate arbitrage strategies using paired long and short positions.

---

## Funding Rate Arbitrage Bot

Automated bot for maintaining directionally neutral funding arbitrage positions.

