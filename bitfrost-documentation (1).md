# Bitfrost Platform Documentation

![Bitfrost Navigation Menu](uploads/Screenshot_2026-01-29_at_11_01_17.png)

## Table of Contents

### 1. BITFROST PRIME
- [1.1 Initialize Your Account](#11-initialize-your-account)
  - [1.1.1 Funding the Account](#111-funding-the-account)
  - [1.1.2 Exchange Selection](#112-exchange-selection)
  - [1.1.3 Capital Allocation](#113-capital-allocation)
  - [1.1.4 Sub-Account Initialization](#114-sub-account-initialization)
- [1.2 Deposits](#12-deposits)
  - [1.2.1 Supported Network and Asset](#121-supported-network-and-asset)
  - [1.2.2 Deposit Flow](#122-deposit-flow)
  - [1.2.3 Post Deposit Allocation](#123-post-deposit-allocation)
- [1.3 Withdrawals](#13-withdrawals)
  - [1.3.1 Withdrawal Source](#131-withdrawal-source)
  - [1.3.2 Supported Network and Asset](#132-supported-network-and-asset)
  - [1.3.3 Withdrawal Flow](#133-withdrawal-flow)
  - [1.3.4 Withdrawal Processing](#134-withdrawal-processing)
- [1.4 Transfers](#14-transfers)
  - [1.4.1 Transfer Scope](#141-transfer-scope)
  - [1.4.2 Supported Asset](#142-supported-asset)
  - [1.4.3 Transfer Flow](#143-transfer-flow)
  - [1.4.4 Transfer Constraints](#144-transfer-constraints)
  - [1.4.5 Use in Withdrawals](#145-use-in-withdrawals)

### 2. EXPLORE
- [2.1 Funding Rate Comparison](#21-funding-rate-comparison)
  - [2.1.1 Overview](#211-overview)
  - [2.1.2 Data Aggregation](#212-data-aggregation)
  - [2.1.3 Interaction and Selection](#213-interaction-and-selection)
  - [2.1.4 Capacity Weighted Selection](#214-capacity-weighted-selection)
  - [2.1.5 Use in Trade Construction](#215-use-in-trade-construction)

### 3. AGGREGATOR
- [3.1 Overview](#31-overview)
  - [3.1.1 Market Context](#311-market-context)
  - [3.1.2 Trade Construction](#312-trade-construction)
  - [3.1.3 Exchange Selection](#313-exchange-selection)
- [3.2 Execution Strategies](#32-execution-strategies)
  - [3.2.1 Impact Minimization](#321-impact-minimization)
  - [3.2.2 Time Constant (TWAP)](#322-time-constant-twap)
  - [3.2.3 Target Participation Rate](#323-target-participation-rate)
  - [3.2.4 Market Maker](#324-market-maker)
  - [3.2.5 Aggressive Maker](#325-aggressive-maker)
  - [3.2.6 Aggressive Taker](#326-aggressive-taker)
  - [3.2.7 Target Time](#327-target-time)
  - [3.2.8 Custom](#328-custom)
  - [3.2.9 Simple Orders](#329-simple-orders)
- [3.3 Exit Conditions](#33-exit-conditions)
  - [3.3.1 Take Profit](#331-take-profit)
  - [3.3.2 Stop Loss](#332-stop-loss)
  - [3.3.3 Urgency](#333-urgency)
  - [3.3.4 Scope and Behavior](#334-scope-and-behavior)
- [3.4 Scale Orders](#34-scale-orders)
  - [3.4.1 Price Range](#341-price-range)
  - [3.4.2 Price Skew](#342-price-skew)
  - [3.4.3 Size Skew](#343-size-skew)
  - [3.4.4 Number of Orders](#344-number-of-orders)
  - [3.4.5 Execution Behavior](#345-execution-behavior)
- [3.5 Advanced Settings](#35-advanced-settings)
  - [3.5.1 Trajectory](#351-trajectory)
  - [3.5.2 Participation Controls](#352-participation-controls)
  - [3.5.3 Strategy Parameters](#353-strategy-parameters)
  - [3.5.4 Execution Constraints](#354-execution-constraints)
  - [3.5.5 Defaults](#355-defaults)
- [3.6 Template Strategies](#36-template-strategies)
  - [3.6.1 Save Template](#361-save-template)
  - [3.6.2 Load Template](#362-load-template)
  - [3.6.3 Manage Templates](#363-manage-templates)
  - [3.6.4 Scope](#364-scope)

### 4. MARKET MAKER
- [4.1 Advanced](#41-advanced)
  - [4.1.1 Overview](#411-overview)
  - [4.1.2 Basic Configuration](#412-basic-configuration)
  - [4.1.3 Market Making Parameters](#413-market-making-parameters)
  - [4.1.4 Risk Management](#414-risk-management)
  - [4.1.5 Participation Rate](#415-participation-rate)
  - [4.1.6 Auto Repeat](#416-auto-repeat)
  - [4.1.7 Strategy Summary and Estimates](#417-strategy-summary-and-estimates)
  - [4.1.8 Execution and Scope](#418-execution-and-scope)
- [4.2 Vaults](#42-vaults)
  - [4.2.1 Overview](#421-overview)
  - [4.2.2 Vault Access and Operators](#422-vault-access-and-operators)
  - [4.2.3 Capital Deployment](#423-capital-deployment)
  - [4.2.4 Returns and PnL Distribution](#424-returns-and-pnl-distribution)
  - [4.2.5 Transparency and Reporting](#425-transparency-and-reporting)
  - [4.2.6 Risk Considerations](#426-risk-considerations)
  - [4.2.7 Scope](#427-scope)
- [4.3 Multi-Strategy](#43-multi-strategy)
  - [4.3.1 Overview](#431-overview)
  - [4.3.2 Strategy Configuration](#432-strategy-configuration)
  - [4.3.3 Strategy Aggregation and Global View](#433-strategy-aggregation-and-global-view)
  - [4.3.4 Shared Risk Context](#434-shared-risk-context)
  - [4.3.5 Strategy Management](#435-strategy-management)
  - [4.3.6 Simulation](#436-simulation)
  - [4.3.7 Deployment](#437-deployment)
  - [4.3.8 Execution and Risk Scope](#438-execution-and-risk-scope)
- [4.4 Exchange Points](#44-exchange-points)
  - [4.4.1 Overview](#441-overview)
  - [4.4.2 Supported Exchanges](#442-supported-exchanges)
  - [4.4.3 Points Attribution](#443-points-attribution)
  - [4.4.4 Use Cases](#444-use-cases)
  - [4.4.5 Portfolio Context](#445-portfolio-context)

### 5. ENTERPRISE MARKET MAKERS
- [5.1 Custom Strategies](#51-custom-strategies)
  - [5.1.1 Overview](#511-overview)
  - [5.1.2 Execution Model](#512-execution-model)
  - [5.1.3 API Configuration](#513-api-configuration)
  - [5.1.4 Strategy Configuration Upload](#514-strategy-configuration-upload)
  - [5.1.5 Vault Integration](#515-vault-integration)
  - [5.1.6 Risk and Isolation](#516-risk-and-isolation)
  - [5.1.7 Status and Control](#517-status-and-control)
- [5.2 Vault Creation](#52-vault-creation)
  - [5.2.1 Overview](#521-overview)
  - [5.2.2 Minimum Initial Deposit](#522-minimum-initial-deposit)
  - [5.2.3 Minimum TVL Commitment](#523-minimum-tvl-commitment)
  - [5.2.4 Profit Distribution](#524-profit-distribution)
  - [5.2.5 Example](#525-example)
  - [5.2.6 Execution and Control](#526-execution-and-control)
  - [5.2.7 Transparency](#527-transparency)
- [5.3 Vault Management](#53-vault-management)
  - [5.3.1 Overview](#531-overview)
  - [5.3.2 Vault State](#532-vault-state)
  - [5.3.3 Minimum Capital Commitment](#533-minimum-capital-commitment)
  - [5.3.4 Capital Withdrawal](#534-capital-withdrawal)
  - [5.3.5 Performance Fee Settlement](#535-performance-fee-settlement)
  - [5.3.6 Vault Metrics](#536-vault-metrics)
  - [5.3.7 Administrative Controls](#537-administrative-controls)

### 6. FUNDING RATE ARBITRAGE
- [6.1 Make A Carry Trade](#61-make-a-carry-trade)
  - [6.1.1 Overview](#611-overview)
  - [6.1.2 Strategy Overview](#612-strategy-overview)
  - [6.1.3 Trade Construction](#613-trade-construction)
  - [6.1.4 Funding Rate Calculation](#614-funding-rate-calculation)
  - [6.1.5 Funding PnL Time Series](#615-funding-pnl-time-series)
  - [6.1.6 Strategy Parameters](#616-strategy-parameters)
  - [6.1.7 Monitoring and Lifecycle](#617-monitoring-and-lifecycle)
- [6.2 Funding Rate Arbitrage Bot](#62-funding-rate-arbitrage-bot)
  - [6.2.1 Overview](#621-overview)
  - [6.2.2 Configuration](#622-configuration)
  - [6.2.3 Position and Exposure Management](#623-position-and-exposure-management)
  - [6.2.4 Funding Tracking](#624-funding-tracking)
  - [6.2.5 Control and Lifecycle](#625-control-and-lifecycle)

### 7. PORTFOLIO
- [7.1 Overview](#71-overview)
- [7.2 Equity and Distribution](#72-equity-and-distribution)
- [7.3 Performance Tracking](#73-performance-tracking)
- [7.4 Balances and Positions](#74-balances-and-positions)

### 8. EXCHANGE MANAGEMENT
- [8.1 Overview](#81-overview)
- [8.2 Exchange Detail View](#82-exchange-detail-view)
- [8.3 Adding an Exchange Account](#83-adding-an-exchange-account)
- [8.4 Removing an Exchange Account](#84-removing-an-exchange-account)
- [8.5 Funding Distribution](#85-funding-distribution)
- [8.6 Exchange Level Actions](#86-exchange-level-actions)

### 9. ORDER HISTORY
- [9.1 Overview](#91-overview)
- [9.2 Filters and States](#92-filters-and-states)
- [9.3 Displayed Fields](#93-displayed-fields)
- [9.4 Scope and Aggregation](#94-scope-and-aggregation)

### 10. MARKET MAKER MANAGEMENT
- [10.1 Overview](#101-overview)
- [10.2 Strategy Types](#102-strategy-types)
  - [10.2.1 Advanced Strategies](#1021-advanced-strategies)
  - [10.2.2 Vault Based Strategies](#1022-vault-based-strategies)
  - [10.2.3 Multi Strategy Portfolios](#1023-multi-strategy-portfolios)
- [10.3 Active Strategy Set](#103-active-strategy-set)
- [10.4 Exposure and Performance Aggregation](#104-exposure-and-performance-aggregation)

### 11. POSITION MANAGEMENT
- [11.1 Execution](#111-execution)
  - [11.1.1 Overview](#1111-overview)
  - [11.1.2 Execution Configuration](#1112-execution-configuration)
  - [11.1.3 Execution Progress](#1113-execution-progress)
  - [11.1.4 Execution Metrics](#1114-execution-metrics)
  - [11.1.5 Exposure Tracking](#1115-exposure-tracking)
  - [11.1.6 Market Context](#1116-market-context)
  - [11.1.7 Execution Controls](#1117-execution-controls)
- [11.2 Status](#112-status)
  - [11.2.1 Overview](#1121-overview)
  - [11.2.2 Position State](#1122-position-state)
  - [11.2.3 Funding Performance](#1123-funding-performance)
  - [11.2.4 Price and PnL Metrics](#1124-price-and-pnl-metrics)
  - [11.2.5 Exposure Monitoring](#1125-exposure-monitoring)
  - [11.2.6 Controls](#1126-controls)
  - [11.2.7 Final State](#1127-final-state)
- [11.3 Market Making Strategy Monitor](#113-market-making-strategy-monitor)
  - [11.3.1 Overview](#1131-overview)
  - [11.3.2 Summary Metrics](#1132-summary-metrics)
  - [11.3.3 Profit and Loss Over Time](#1133-profit-and-loss-over-time)
  - [11.3.4 Position and Exposure](#1134-position-and-exposure)
  - [11.3.5 Volume and Trading Activity](#1135-volume-and-trading-activity)
  - [11.3.6 Order Book Imbalance](#1136-order-book-imbalance)
  - [11.3.7 Spread Capture](#1137-spread-capture)
  - [11.3.8 Fill Rate Performance](#1138-fill-rate-performance)
  - [11.3.9 Current Positions](#1139-current-positions)
  - [11.3.10 Risk Metrics](#11310-risk-metrics)
  - [11.3.11 Strategy Status](#11311-strategy-status)
  - [11.3.12 Relationship to Other Strategy Types](#11312-relationship-to-other-strategy-types)

### 12. MORE
- [12.1 Transaction Explorer](#121-transaction-explorer)
  - [12.1.1 Overview](#1211-overview)
  - [12.1.2 Search and Filtering](#1212-search-and-filtering)
  - [12.1.3 Transaction Records](#1213-transaction-records)
  - [12.1.4 Transaction Status States](#1214-transaction-status-states)

---

## 1. BITFROST PRIME

### 1.1 Initialize Your Account

Initializing a Bitfrost account follows a defined, sequential process.

![Account Initialization Flow](Group_1__1_.svg)

#### 1.1.1 Funding the Account

The user must first deposit funds from an external wallet.

- All deposits are received in USDC on HyperEVM
- These funds are credited to the user's Bitfrost parent account
- The parent account acts as the control layer for all exchange sub-accounts and governs balance allocation, trading permissions, and execution

#### 1.1.2 Exchange Selection

After the parent account is funded, the user must select a minimum of two exchanges on which sub-accounts will be created.

![Exchange Selection Interface](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FLJq8BS4Fi75m9lPpze58_2FScreenshot_202026-01-25_20at_2014_25_37_png_alt_media_token_b6a37e81-4fe9-4f20-a4ec-a06777feebca.png)

In the initial release, supported exchanges are:
- Hyperliquid
- Paradex

Each selected exchange will receive a dedicated sub-account linked to the parent account.

#### 1.1.3 Capital Allocation

The user specifies how the parent account balance is distributed across the selected exchanges.

- For the initial release, the system applies a default allocation of 50 percent per exchange
- This allocation can be modified by the user before confirmation

#### 1.1.4 Sub-Account Initialization

Once allocation is confirmed, funds are transferred from the parent account to each exchange sub-account.

- This step completes account initialization and enables trading across multiple exchanges using a single Bitfrost account
- Sub-account funding may take up to 60 minutes to complete

### 1.2 Deposits

Deposits are used to fund the Bitfrost parent account and may be made during initial setup or at any time after the account is active.

#### 1.2.1 Supported Network and Asset

All deposits are made in USDC on HyperEVM. Only deposits sent on this network and in this asset are supported.

#### 1.2.2 Deposit Flow

![Deposit Interface](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FlIrPIt6oB838qEff6pZt_2FScreenshot_202026-01-17_20at_2010_35_30_png_alt_media_token_af7d0658-fa58-4cbc-ac5d-f637089b08b1.png)

1. The user initiates a deposit from an external wallet
2. USDC is transferred on HyperEVM to the user's Bitfrost deposit address
3. After on-chain confirmation, funds are credited to the Bitfrost parent account
4. The parent account functions as the primary balance and control layer for all exchange sub-accounts

#### 1.2.3 Post Deposit Allocation

After confirmation, deposited funds may be allocated to exchange sub-accounts according to the user's chosen distribution or transferred manually using the transfer function to fund specific exchanges.

### 1.3 Withdrawals

Withdrawals allow users to remove funds from their Bitfrost account to an external wallet.

#### 1.3.1 Withdrawal Source

- Withdrawals can only be initiated from the Bitfrost parent account
- Direct withdrawals from exchange sub-accounts are not supported
- To withdraw funds held on an exchange, the user must first transfer the balance from the exchange sub-account back to the Bitfrost parent account

#### 1.3.2 Supported Network and Asset

All withdrawals are made in USDC on HyperEVM. Only this network and asset are supported.

#### 1.3.3 Withdrawal Flow

![Withdrawal Interface](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FcxT3AdGQhNh4FskoxVuH_2FScreenshot_202026-01-17_20at_2010_37_10_png_alt_media_token_dd15035c-e25a-464d-bd45-79cbb236444a.png)

1. The user transfers funds from one or more exchange sub-accounts to the Bitfrost parent account, if required
2. The user submits a withdrawal request from the parent account to an external wallet
3. USDC is sent on HyperEVM to the specified destination address

#### 1.3.4 Withdrawal Processing

Withdrawals do not alter the configuration or status of existing exchange sub-accounts.

### 1.4 Transfers

Transfers move funds between the Bitfrost parent account and exchange sub-accounts. This mechanism is used to fund exchanges, rebalance capital, and prepare funds for withdrawal.

![Transfer Interface](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FBQPdeDsCAELKz116iW97_2FScreenshot_202026-01-17_20at_2010_38_07_png_alt_media_token_0df1fe0a-2a48-4304-ad25-99033f6f1da4.png)

#### 1.4.1 Transfer Scope

Transfers are supported in both directions:
- From the Bitfrost parent account to an exchange sub-account
- From an exchange sub-account back to the Bitfrost parent account

Transfers do not move funds to or from external wallets.

#### 1.4.2 Supported Asset

All transfers are denominated in USDC.

#### 1.4.3 Transfer Flow

1. The user selects the source and destination (either the Bitfrost parent account or an exchange sub-account)
2. The user specifies the transfer amount or selects a percentage of the available balance
3. The transfer is submitted and processed internally
4. The destination balance is updated once the transfer completes

#### 1.4.4 Transfer Constraints

Only free and available capital may be transferred:

- **On the Bitfrost side**: Transfers are limited to the available balance held in the Bitfrost vault
- **On exchange sub-accounts**: Only capital that is not required for margin, open positions, or risk constraints may be transferred
- Funds reserved for margin, maintenance requirements, or pending settlement are not transferable

#### 1.4.5 Use in Withdrawals

- Funds held on an exchange must be transferred back to the Bitfrost parent account before a withdrawal can be initiated
- Transfers do not affect open positions or account configuration on supported exchanges such as Hyperliquid

---

## 2. EXPLORE

### 2.1 Funding Rate Comparison

The Funding Yield Explorer provides a consolidated view of funding rate yields across supported exchanges. It allows users to compare funding conditions across markets using normalized data.

#### 2.1.1 Overview

The explorer displays funding rate yields for perpetual markets across multiple exchanges.

Funding rates are:
- Normalized to a common basis
- Aggregated across consistent time windows
- Presented as annualized percentage yields

Users may switch between day, week, month, and year views to assess short-term and long-term funding dynamics.

#### 2.1.2 Data Aggregation

For each exchange and trading pair, funding rates are:
- Collected at the native exchange interval
- Normalized to a comparable yield format
- Averaged over the selected time period

This enables direct comparison of funding yields across venues with differing funding schedules.

#### 2.1.3 Interaction and Selection

Users may:
- Search for tokens and perpetual pairs
- Mark pairs as favorites for quick access
- Select individual cells to identify attractive funding opportunities

Selecting a funding cell automatically populates the trade construction interface with the corresponding exchange, pair, and directional context.

#### 2.1.4 Capacity Weighted Selection

Capacity Weighting represents the maximum notional that can be deployed at the observed funding rate before it degrades due to liquidity limits, position size constraints, or risk controls.

#### 2.1.5 Use in Trade Construction

The Funding Yield Explorer serves as the primary discovery tool for funding-based strategies.

It allows users to:
- Identify funding rate differentials across exchanges
- Compare relative yield opportunities over time
- Pre-fill trade parameters for manual or automated funding arbitrage execution

---

## 3. AGGREGATOR

### 3.1 Overview

The Aggregator page provides a unified interface for executing trades across multiple exchanges using configurable execution strategies.

![Aggregator Interface - Order Book View](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FaRGTy2DKFIjqIXBK5mT8_2FScreenshot_202026-01-25_20at_2014_22_36__1__png_alt_media_token_04b31978-3f81-498e-ba90-8631d9c5f4cf.png)

The Aggregator is designed to optimize execution quality by aggregating liquidity, improving price discovery, and reducing market impact relative to single-venue execution.

The Aggregator allows a user to submit a single trade instruction that may be executed across multiple exchanges and sub-accounts. The user defines the trade intent and constraints. Execution is then distributed across eligible exchanges according to the selected strategy and prevailing market conditions.

#### 3.1.1 Market Context

The main view displays real-time market data for the selected instrument, including:
- Price and recent price action
- Funding rate and open interest
- Volatility and reference price metrics
- Order book depth across exchanges

This data provides context for execution decisions and strategy selection.

#### 3.1.2 Trade Construction

To construct a trade, the user specifies:
- Instrument and direction
- Target quantity or notional
- Eligible exchanges for execution
- Execution strategy
- Optional execution parameters

These inputs define a single logical trade.

#### 3.1.3 Exchange Selection

Users may select one or more exchanges as execution venues. Selected exchanges are treated as eligible liquidity sources. Execution may be split across exchanges to improve fill quality, reduce slippage, and manage available depth.

### 3.2 Execution Strategies

The Aggregator supports multiple execution strategies, each designed to optimize a specific objective.

Strategies determine:
- How orders are sized and sequenced
- Whether execution is time-based, liquidity-seeking, or price-sensitive
- How aggressively orders interact with the order book

Only one strategy is active per trade.

#### 3.2.1 Impact Minimization

Executes the trade gradually using smaller orders distributed over time.

- Designed to reduce market impact and slippage while targeting completion within a fixed duration
- Best suited for larger orders where execution quality is prioritized over immediacy

#### 3.2.2 Time Constant (TWAP)

Executes the trade at a consistent rate over a fixed time window.

- Order sizes and timing are evenly distributed regardless of short-term market conditions
- Best suited for predictable execution where timing consistency is preferred

#### 3.2.3 Target Participation Rate

Adjusts execution dynamically to maintain a fixed share of observed market volume.

- Order flow scales up or down based on liquidity conditions until the target quantity is completed
- Best suited for liquid markets where participation relative to volume is the primary constraint

#### 3.2.4 Market Maker

Places passive limit orders that rest on the order book.

- Orders do not cross the spread and aim to earn maker rebates while providing liquidity
- Best suited for non-urgent execution where cost efficiency is prioritized

#### 3.2.5 Aggressive Maker

Uses passive limit orders with higher participation targets.

- Balances faster execution with cost efficiency while still avoiding spread crossing
- Best suited for moderately urgent trades where taker fees are undesirable

#### 3.2.6 Aggressive Taker

Executes using market or aggressively priced orders.

- Prioritizes speed and certainty of execution over price optimization
- Best suited for urgent trades requiring immediate liquidity

#### 3.2.7 Target Time

Concentrates execution around a specified future time or event.

- Execution intensity increases as the target time approaches
- Best suited for event-driven strategies or time-sensitive positioning

#### 3.2.8 Custom

Allows manual control over execution trajectory through advanced settings.

- Provides maximum flexibility for bespoke execution logic
- Enabled through Template Strategies

#### 3.2.9 Simple Orders

Simple execution modes bypass advanced scheduling logic:

- **Market**: Executes immediately at available prices
- **Limit**: Executes passively at a specified price
- **Iceberg**: Splits a large order into smaller visible portions to reduce signaling
- **IOC**: Executes immediately for available liquidity and cancels any unfilled quantity

### 3.3 Exit Conditions

Exit Conditions define automated rules for closing or reducing a position once predefined profit or loss thresholds are reached. These are optional and apply only to the trade or execution in which they are configured.

![Exit Conditions Configuration](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FFMjeHwJEPGCfUcHK5ARQ_2FScreenshot_202026-01-25_20at_2014_24_28_png_alt_media_token_423f388b-90af-4bd0-b924-e1355ec929ae.png)

#### 3.3.1 Take Profit

Take Profit specifies the level at which execution is triggered to lock in gains.

The user may define the take profit threshold as:
- A percentage change from the entry price
- An absolute profit amount in quote currency

When the take profit condition is met, an exit order is generated according to the selected urgency. Displayed estimates such as maximum profit and probability of fill are indicative and depend on market conditions.

#### 3.3.2 Stop Loss

Stop Loss specifies the level at which execution is triggered to limit losses.

The user may define the stop loss threshold as:
- A percentage change from the entry price
- An absolute loss amount in quote currency

When the stop loss condition is met, an exit order is generated according to the selected urgency. Displayed estimates such as maximum loss and probability of fill are indicative and depend on market conditions.

#### 3.3.3 Urgency

Urgency controls how aggressively exit orders are executed once triggered.

- Available levels range from very low to very high
- Higher urgency prioritizes speed and certainty of execution
- Lower urgency prioritizes price and reduced market impact
- Urgency affects order type selection, pricing behavior, and execution timing

#### 3.3.4 Scope and Behavior

- Exit conditions are evaluated continuously while the trade is active
- Once triggered, exit execution is handled independently of the original entry strategy

### 3.4 Scale Orders

Scale Orders allow a single trade to be split into multiple orders distributed across a defined price range.

![Scale Orders Configuration](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FGmKclAdA8m9k8pof5Zvd_2FScreenshot_202026-01-25_20at_2015_06_22_png_alt_media_token_7787a509-e391-4645-832a-4341550738b0.png)

This feature is used to improve execution quality by spreading orders over price and size rather than executing at a single level. When Scale Orders are enabled, the target quantity is divided into multiple child orders. Each order is placed at a different price within the specified range and may have a different size depending on configuration.

Scale Orders may be used with supported execution strategies.

#### 3.4.1 Price Range

The user defines a price range over which orders will be placed:

- **From Price**: The starting price of the range
- **To Price**: The ending price of the range

The range may be specified as a percentage relative to the reference price or as an absolute price range.

#### 3.4.2 Price Skew

Price Skew controls how orders are distributed within the price range:

- A neutral setting distributes orders evenly across the range
- Positive skew concentrates orders closer to the more aggressive end of the range, nearer to the current market price
- Negative skew concentrates orders closer to the more passive end of the range, further from the current market price

This allows users to bias execution toward more aggressive or more passive price levels.

#### 3.4.3 Size Skew

Size Skew controls how the total order size is allocated across the scaled orders:

- A neutral setting assigns equal size to each order
- Positive skew allocates larger order sizes closer to the more aggressive price levels, nearer to the current market price
- Negative skew allocates larger order sizes closer to the more passive price levels, further from the current market price

This allows users to concentrate size where fill probability or pricing is preferred.

#### 3.4.4 Number of Orders

The number of orders determines how finely the total quantity is split:

- Higher values result in more, smaller orders spread across the range
- Lower values result in fewer, larger orders

#### 3.4.5 Execution Behavior

Scale Orders are executed according to the selected execution strategy and market conditions. Orders may fill partially or fully and do not guarantee execution of the full range.

### 3.5 Advanced Settings

Advanced Settings provide fine-grained control over execution behavior and risk constraints.

#### 3.5.1 Trajectory

Trajectory defines the execution path used to distribute orders over time.

- Trajectory selection is available only when the execution strategy is set to Custom
- For non-custom strategies, trajectory is defined by the selected strategy and cannot be modified

#### 3.5.2 Participation Controls

**Participation Rate Target**: The desired percentage of observed market volume that execution should represent.

**Participation Rate Limit**: The maximum allowable participation rate. Execution will not exceed this threshold even if market conditions change.

Participation controls apply only to strategies that support volume-based execution.

#### 3.5.3 Strategy Parameters

- **Passiveness**: Controls how aggressively orders interact with the order book. Higher values favor resting orders and lower fees. Lower values favor faster execution.
- **Discretion**: Allows flexibility in timing and price placement within defined bounds
- **Alpha Tilt**: Applies a controlled bias within the execution logic to improve expected outcomes
- **Max OIC Percentage**: Limits the maximum proportion of open interest or visible liquidity that execution may consume
- **Max Clip Size**: Sets the maximum size for any single child order. If not specified, clip size adapts to order book conditions

#### 3.5.4 Execution Constraints

- **Passive Only**: Restricts execution to passive limit orders. Orders will not cross the spread
- **Active Limit**: Allows limit orders to be priced aggressively within defined bounds
- **Reduce Only**: Ensures execution can only reduce existing positions
- **Strict Duration**: Enforces a hard execution window. Orders are canceled if execution is not completed within the specified duration

#### 3.5.5 Defaults

Advanced settings may be reset to default values at any time.

### 3.6 Template Strategies

Templates allow users to save an execution configuration and reuse it for future trades.

A template stores strategy setup, selected exchanges, and execution parameters so the same workflow can be applied consistently without reconfiguring each field.

#### 3.6.1 Save Template

After configuring a trade, the user may select Save Template.

Saving a template captures the current configuration, including:
- Selected instrument and direction
- Selected exchanges
- Execution strategy
- Limit handling and duration settings
- Exit conditions, scale orders, and advanced settings where applicable

The user assigns a template name and saves it for later use.

#### 3.6.2 Load Template

Selecting Load Template displays saved templates.

![Load Template Interface](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FB9vJ3j9Rp8ByH5ehyVvz_2FScreenshot_202026-01-25_20at_2014_44_57_png_alt_media_token_f9f738ed-d4e5-4581-82bf-1856fb2cd165.png)

Each template entry summarizes key configuration details, including:
- Instrument
- Exchanges
- Strategy selection

Loading a template applies the saved configuration to the current trade ticket. Templates update inputs and parameters only. They do not submit orders automatically.

#### 3.6.3 Manage Templates

Templates may be deleted at any time. Deleting a template removes the saved configuration and does not affect account balances, positions, or historical executions.

#### 3.6.4 Scope

Templates are designed for repeatable execution. They provide a consistent baseline for recurring trades while allowing the user to modify any field before submitting a new order.

---

## 4. MARKET MAKER

### 4.1 Advanced

The Advanced Market Maker module allows users to configure and deploy automated market making strategies on supported exchanges.

#### 4.1.1 Overview

A market making strategy continuously places bid and ask orders around the prevailing market price.

It is designed to provide continuous liquidity while managing spread placement, inventory exposure, and execution cadence within defined risk constraints.

Orders are refreshed at a configurable interval to maintain competitiveness in the order book while adapting to price movements and inventory imbalance. Each strategy operates independently and contributes to the aggregated portfolio and account metrics.

#### 4.1.2 Basic Configuration

To deploy a market making strategy, the user configures the following:

- **Exchange**: The exchange on which the strategy will operate
- **Trading Pair**: The instrument for which liquidity will be provided
- **Margin**: Capital allocated to the strategy
- **Leverage**: Leverage applied to the allocated margin (defined by the underlying exchanges)
- **Target Volume**: The notional trading volume the strategy aims to generate

These parameters define the capital allocation and operating scope of the strategy.

#### 4.1.3 Market Making Parameters

- **Base Spread**: The initial distance between bid and ask quotes, expressed in basis points
- **Order Levels**: The number of bid and ask levels placed on each side of the order book
- **Order Amount**: The size of each individual order at each level
- **Refresh Time**: The frequency at which existing orders are canceled and replaced
- **Inventory Skew**: Adjusts quote placement based on current inventory. Positive values bias quoting toward buying. Negative values bias quoting toward selling
- **Minimum Spread**: The tightest spread the strategy is permitted to quote
- **Maximum Spread**: The widest spread the strategy is permitted to quote

#### 4.1.4 Risk Management

- **Stop Loss**: Automatically halts the strategy if losses exceed the specified threshold
- **Take Profit**: Automatically exits the strategy once profit targets are reached

Risk controls apply at the strategy level and do not affect other positions or strategies.

#### 4.1.5 Participation Rate

Participation rate defines how actively the strategy interacts with available market liquidity:

- **Passive**: Lower participation and reduced turnover
- **Neutral**: Balanced participation between speed and cost
- **Aggressive**: Higher participation and faster inventory turnover

#### 4.1.6 Auto Repeat

Auto repeat allows the strategy to restart automatically after each completed run.

When enabled, the strategy will continue to redeploy until either:
- The maximum number of runs is completed, or
- A configured PnL tolerance threshold is breached

If a PnL tolerance is set, auto repeat will continue only while realized PnL remains within the defined bounds.

Because auto repeat may extend execution beyond a 24-hour window, total executed volume may exceed estimated 24-hour volume figures.

#### 4.1.7 Strategy Summary and Estimates

A strategy summary panel displays:
- Allocated margin and leverage
- Spread and order configuration
- Estimated trading volume
- Indicative fees and returns

All estimates are indicative and depend on market conditions and execution behavior.

#### 4.1.8 Execution and Scope

Market making strategies run continuously until stopped manually or terminated by risk controls. All activity is reflected in portfolio, exchange, and history views.

### 4.2 Vaults

Market Maker Vaults provide access to professionally managed market making strategies operated by verified and permissioned operators.

#### 4.2.1 Overview

Vaults allow users to deploy capital into active strategies without managing execution or configuration directly.

Each vault represents an independent market making strategy operated by a specific manager. Vault operators deploy and manage their own strategies, including exchange selection, execution logic, and risk controls.

Users interact with vaults only through capital allocation and do not require specialized knowledge of market making mechanics.

#### 4.2.2 Vault Access and Operators

Vaults are created and operated by verified participants.

Operators are permissioned and are responsible for:
- Strategy design and execution
- Risk management and monitoring
- Operational maintenance

Vault strategies are not exposed to users.

#### 4.2.3 Capital Deployment

Users may allocate capital to a selected vault by depositing funds. Deployed capital is pooled within the vault and used by the operator to execute the strategy. Capital allocation is subject to vault-specific parameters, including leverage and drawdown limits.

#### 4.2.4 Returns and PnL Distribution

Vault performance is reflected through realized and unrealized PnL. Users receive returns proportional to their share of the total vault capital. PnL is aggregated and distributed according to the vault's accounting logic.

#### 4.2.5 Transparency and Reporting

Vault summaries display high-level performance metrics, including:
- Historical PnL
- Trading volume
- Total value locked
- Indicative yield metrics

Underlying strategy logic, execution details, and order flow are not visible to users.

#### 4.2.6 Risk Considerations

Vault performance is subject to market conditions and operator execution. Users are exposed to strategy-level risk but are insulated from direct execution decisions. Vault participation does not grant control over individual orders or positions.

#### 4.2.7 Scope

Vault allocations are independent of user-managed strategies and aggregated within the overall portfolio view.

### 4.3 Multi-Strategy

Multi-Strategy Market Making allows users to configure, simulate, and deploy multiple independent market making strategies simultaneously across different exchanges and instruments.

#### 4.3.1 Overview

Each strategy operates independently with its own parameters, while monitoring and risk management are coordinated at a global strategy level.

The Multi-Strategy interface enables parallel deployment of multiple market making strategies from a single configuration view.

Strategies may differ by:
- Exchange
- Trading pair
- Capital allocation
- Leverage
- Market making parameters
- Risk controls

All configured strategies are executed concurrently once deployed.

In addition to individual strategy views, users can monitor the combined behavior of all strategies as a single aggregated strategy.

#### 4.3.2 Strategy Configuration

Each strategy is defined independently and includes:

- **Strategy Name**: A user-defined identifier for clarity and tracking
- **Exchange and Trading Pair**: Specifies where and on which instrument the strategy operates
- **Margin and Leverage**: Capital allocated to the strategy and the leverage applied
- **Market Making Parameters**: Including base spread, order levels, order size, refresh cadence, inventory skew, and spread bounds
- **Risk Controls**: Stop loss, take profit, participation rate, and auto repeat parameters

Each strategy executes independently and contributes its own exposure and PnL to the overall strategy.

#### 4.3.3 Strategy Aggregation and Global View

All configured strategies are aggregated into a single global strategy view.

This provides visibility into:
- Total margin allocated across all strategies
- Total notional exposure
- Aggregate PnL and ROI
- Per-strategy performance contribution
- Exchange-level exposure and concentration

This allows users to understand how individual strategies interact and contribute to the overall outcome.

#### 4.3.4 Shared Risk Context

While execution logic remains isolated per strategy, risk is also evaluated at the aggregated strategy level.

Global monitoring enables users to assess:
- Combined exposure across strategies
- Portfolio-level drawdown
- Exchange concentration risk
- Strategy interaction and correlation indicators

This shared risk context provides a clearer understanding of overall risk without coupling execution logic between strategies.

#### 4.3.5 Strategy Management

Users may:
- Add multiple strategies
- Edit or remove individual strategies
- Upload strategy configurations via JSON
- Expand or collapse strategies for review

A strategy must be fully configured before it can be deployed.

#### 4.3.6 Simulation

Before deployment, users may run a multi-strategy simulation.

![Multi-Strategy Simulation Results](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2F9dQzYoojg4KqEEY9DICu_2FScreenshot_202026-01-25_20at_2014_58_57_png_alt_media_token_04b2f275-ab71-4cbf-a82c-40d07cc8f1c9.png)

The simulation provides projected performance metrics based on the previous 7 days' market metrics across all configured strategies, including:
- Total projected PnL
- Total exposure
- Aggregate ROI
- Risk metrics such as drawdown
- Per-strategy performance breakdown
- Exchange-level exposure and PnL
- Strategy correlation and interaction indicators

Simulation results are indicative and based on historical data and current market conditions.

#### 4.3.7 Deployment

Once configured, all strategies are deployed simultaneously.

![Multi-Strategy Deployment Confirmation](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FA5nEmOPry0yRmT8wT5zB_2FScreenshot_202026-01-25_20at_2014_59_17_png_alt_media_token_fc612a3a-33a6-4323-8687-f2b6613f2749.png)

A confirmation step summarizes:
- Number of strategies
- Total margin allocated
- Total notional exposure
- Per-strategy capital and leverage

Upon confirmation, each strategy begins execution immediately on its respective exchange.

#### 4.3.8 Execution and Risk Scope

Strategies execute independently and do not share order logic. Individual risk controls apply at the strategy level.

Exposure, PnL, and risk metrics are also tracked at the aggregated strategy level for global oversight. Stopping or modifying one strategy does not directly affect the execution of others.

### 4.4 Exchange Points

Exchange Points provides a unified view of reward points earned across connected exchanges.

#### 4.4.1 Overview

The Exchange Points interface aggregates points earned across all supported exchanges into a single dashboard.

This section is designed to help users track, compare, and manage incentive programs that reward trading activity such as volume, liquidity provision, or market making participation.

For each exchange, users can see:
- Whether a points or incentives program is active
- Total points earned to date
- Program status: active, concluded, or unavailable

This allows users to monitor incentive accumulation without needing to log into each exchange individually.

#### 4.4.2 Supported Exchanges

Each exchange entry displays its current points status:

- **Points Program Active**: The exchange is currently running an incentives or rewards program. Points continue to accrue based on eligible activity
- **Points Program Concluded**: The exchange previously ran a points program, but it is no longer active. Earned points are still displayed for reference
- **No Points Program**: The exchange does not currently offer a points-based incentives program. No points are tracked

If an exchange does not support points, the interface clearly indicates this.

#### 4.4.3 Points Attribution

Points shown reflect rewards earned through activity executed via Bitfrost, including:
- Market making strategies
- Aggregated execution strategies
- Volume-generating activity eligible under each exchange's program rules

Bitfrost tracks and displays points at the exchange level but does not modify or control how points are calculated by the underlying exchange.

#### 4.4.4 Use Cases

Exchange Points enables users to:
- Track incentive accumulation across venues
- Compare effectiveness of strategies across exchanges
- Identify which exchanges currently offer active rewards
- Factor points into strategy and capital allocation decisions

This is particularly useful for users running market making or high-volume strategies where points materially contribute to overall returns.

#### 4.4.5 Portfolio Context

Exchange points are displayed independently from PnL and portfolio equity. They represent non-cash rewards issued by exchanges and should be evaluated separately from realized trading performance.

All points data is informational and reflects exchange-reported metrics.

---

## 5. ENTERPRISE MARKET MAKERS

### 5.1 Custom Strategies

Custom Strategies enable enterprise users to execute proprietary, off-chain trading logic across exchanges while using Bitfrost as the execution and capital coordination layer.

![Enterprise Features Dashboard](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2FGI1xjgsY22cuTW8dJjm9_2FScreenshot_202026-01-25_20at_2015_00_41_png_alt_media_token_f12c38b5-6f43-40fb-9682-ff7ac60b4620.png)

#### 5.1.1 Overview

Custom Strategies are designed for operators who maintain their own signal generation, models, or trading systems.

Strategy logic remains external to Bitfrost. Only execution instructions and risk-bounded actions are transmitted to the platform.

Bitfrost acts as:
- An execution gateway
- A vault coordination layer
- A risk-constrained deployment environment

This enables deployment across multiple exchanges without exposing intellectual property or internal logic.

#### 5.1.2 Execution Model

Custom Strategies operate using an off-chain execution model.

Strategy logic runs externally and communicates with Bitfrost via authenticated API calls.

Bitfrost receives:
- Execution instructions
- Position sizing parameters
- Risk constraints
- Timing and direction signals

Bitfrost does not receive or evaluate underlying strategy logic.

#### 5.1.3 API Configuration

To enable execution, the user generates a Strategy API Key.

This key authenticates requests sent to the Bitfrost execution endpoint. Each API key is scoped to the associated enterprise account and vault configuration.

API keys must be stored securely.

#### 5.1.4 Strategy Configuration Upload

Users upload a strategy configuration JSON file defining execution boundaries and risk parameters.

![Custom Strategy API Configuration](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2Fh7uTXkEbBdYokX3zHXqL_2FScreenshot_202026-01-25_20at_2014_25_17_png_alt_media_token_e8a54358-39d3-4031-bb53-ab5dd06342a1.png)

![Strategy JSON Upload](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2F78Q3EIgoLnyXMggBL90m_2FScreenshot_202026-01-25_20at_2014_23_50_png_alt_media_token_be3a536e-0fdd-4da6-a0f4-28fd5ff56b74.png)

Uploaded configurations include:
- Strategy identifier and description
- Execution parameters
- Risk limits
- Position sizing constraints
- Rebalance and refresh behavior

Configurations are provided as JSON files and validated upon upload. This configuration governs how incoming signals are interpreted and applied.

#### 5.1.5 Vault Integration

Custom Strategies may be linked to one or more market making vaults.

Vaults execute actions based on received signals while enforcing predefined constraints. Vault participants receive proportional PnL based on vault performance.

Vault users do not have visibility into:
- Strategy logic
- Signal generation methods
- Internal parameters

Only aggregate performance metrics are exposed.

#### 5.1.6 Risk and Isolation

Custom Strategies are subject to platform-level and vault-level risk controls.

This includes:
- Maximum exposure limits
- Drawdown constraints
- Slippage tolerance
- Exchange-specific restrictions

Execution is isolated per vault and per account. Failure or modification of one custom strategy does not affect others.

#### 5.1.7 Status and Control

Each custom strategy maintains an explicit execution status.

Strategies may be inactive, configured, or actively executing. Execution can be paused or disabled without removing configuration or API credentials.

### 5.2 Vault Creation

Vault Creation enables approved market makers to create capital pools that aggregate user deposits for executing market making strategies.

#### 5.2.1 Overview

A vault allows a verified market maker to deploy deposited user capital into their own market making strategies. The vault creator controls execution and risk. Users participate passively and receive a proportional share of the vault's performance. Underlying strategy logic is not visible to depositors.

#### 5.2.2 Minimum Initial Deposit

The vault creator must deposit a minimum of 100 USDC to initialize the vault.

This deposit is a one-time requirement to create the vault and does not represent capital committed to trading or profit and loss participation. The deposit is not included in vault TVL and is not exposed to trading risk.

#### 5.2.3 Minimum TVL Commitment

The vault creator must maintain at least 5% of the total vault value at all times.

This capital is committed alongside user deposits and is subject to the same profit and loss dynamics as the vault's trading activity. The requirement ensures ongoing alignment between the vault creator and depositors.

#### 5.2.4 Profit Distribution

Profits generated by the vault are distributed based on realized PnL:

- 10% of realized profits are allocated to the vault creator as a performance fee
- 90% of realized profits are distributed to users, proportional to their share of vault capital

Fees apply only to profits. Principal is not subject to fees.

#### 5.2.5 Example

If the vault holds 10,000 USDC and generates 1,000 USDC in profit:
- The vault creator receives 100 USDC
- Depositors receive 900 USDC
- The vault creator must maintain at least 500 USDC in the vault

#### 5.2.6 Execution and Control

The vault creator determines:
- Strategy design
- Exchange selection
- Order execution
- Risk parameters

Depositors cannot modify strategy behavior or execution parameters.

#### 5.2.7 Transparency

**Depositors can view:**
- Total vault value
- Aggregate performance
- Historical profit and loss

**Depositors cannot view:**
- Strategy logic
- Execution rules
- Signal inputs

Once all requirements are met, the vault can be created and opened for deposits.

### 5.3 Vault Management

Vault management governs the ongoing operation of an active market making vault after creation and deployment.

#### 5.3.1 Overview

This interface allows the vault creator to monitor performance, manage required capital commitments, and claim earned fees, while maintaining alignment with depositor capital.

All actions taken here affect only the vault creator's capital and permissions. Depositor funds remain segregated and governed by vault rules.

#### 5.3.2 Vault State

- **Total TVL**: Represents the aggregate capital deposited into the vault by all participants
- **Creator deposit**: Represents the capital committed by the vault creator, expressed both as an absolute value and as a proportion of total TVL
- **Vault PnL**: Represents cumulative profit and loss generated by vault trading activity
- **Creator earnings**: Represent accumulated performance fees generated by the vault and available for settlement
- **Vault status**: Indicates whether the vault is active and accepting new deposits

#### 5.3.3 Minimum Capital Commitment

Vault creation and operation require the vault creator to maintain a minimum capital commitment equal to 5% of total vault TVL.

As depositor capital increases, the required minimum commitment increases proportionally. Additional capital may be deposited by the vault creator to maintain compliance with the minimum commitment requirement.

Failure to maintain the required commitment may restrict vault operations or prevent additional deposits.

#### 5.3.4 Capital Withdrawal

Vault creator capital may be withdrawn provided the remaining deposit satisfies the minimum 5% TVL requirement.

The maximum withdrawable amount represents capital in excess of the required minimum commitment. Withdrawals affect only the vault creator's exposure to vault performance and do not impact depositor balances.

#### 5.3.5 Performance Fee Settlement

Performance fees accrue as a fixed percentage of realized vault profits. Accrued fees are tracked independently of vault capital and may be settled without modifying vault TVL or depositor balances.

Only realized profits are subject to performance fees.

#### 5.3.6 Vault Metrics

Vault metrics provide aggregated visibility into vault activity and participation:

- **Total user deposits**: Reflect capital contributed by depositors
- **Number of users**: Reflects active depositors within the vault
- **Average user deposit**: Represents mean depositor exposure
- **Total fees earned**: Reflects cumulative performance fees accrued by the vault creator over the lifetime of the vault

These metrics are informational and do not influence vault mechanics.

#### 5.3.7 Administrative Controls

Vault controls define administrative actions available to the vault creator:

- Vault visibility may be modified to restrict new deposits
- Deposits may be paused without affecting existing positions or strategies
- Strategy configurations may be updated subject to platform constraints
- Transaction records and performance reports may be exported for auditing or reporting purposes

Administrative controls do not permit retroactive modification of depositor outcomes or historical performance.

---

## 6. FUNDING RATE ARBITRAGE

### 6.1 Make A Carry Trade

Funding Rate Arbitrage is Bitfrost's cornerstone product offering.

#### 6.1.1 Overview

The Carry Trade Terminal provides users with a structured interface to construct, execute, and manage funding rate arbitrage strategies by maintaining offsetting long and short positions across exchanges.

![Carry Trade Interface - Initial Setup](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2F5oQYKgfQKQZJvXbj7gcB_2FScreenshot_202026-01-25_20at_2013_50_09_png_alt_media_token_03eb7166-8e19-4f7c-9f83-e60b2cc54d54.png)

Bitfrost does not impose a proprietary trading strategy. Instead, the product enables users to implement their own strategies by selecting venues, instruments, position sizing, and execution parameters.

Users may optionally introduce controlled directional exposure through configurable parameters, allowing the strategy to range from pure arbitrage to partially directional positioning based on user preference.

![Carry Trade Interface - Active Position](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2F6isCapdfHstYzHrRByvC_2FScreenshot_202026-01-25_20at_2013_53_41_png_alt_media_token_d376ab38-1f83-49a4-b0ab-889adefeaa52.png)

#### 6.1.2 Strategy Overview

A funding rate arbitrage trade consists of two linked positions:
- A long position on a selected exchange and asset pair
- A short position on a selected exchange and asset pair

Positions are constructed to be directionally neutral by default. Profit and loss is primarily derived from net funding payments rather than price movement.

#### 6.1.3 Trade Construction

To create a trade, the user defines:
- The exchange and trading pair for the long position
- The exchange and trading pair for the short position
- The notional value of each position

These inputs define a single funding rate arbitrage strategy executed across the user's exchange sub-accounts.

#### 6.1.4 Funding Rate Calculation

Each position accrues funding independently based on the funding rate of the selected exchange and pair.

The system calculates:
- Funding earned on the long position
- Funding paid on the short position

These values are netted to produce the gross funding rate return. The headline value displayed at the top of the interface represents the gross funding rate received, defined as funding earned minus funding paid.

#### 6.1.5 Funding PnL Time Series

A time series chart displays the cumulative funding rate PnL of the combined position.

The chart reflects:
- Changes in funding rates on each exchange
- Net funding accrual over time
- Stability of the funding spread

The chart excludes mark-to-market price PnL and isolates funding performance.

#### 6.1.6 Strategy Parameters

Users may adjust parameters to optimize execution quality and net PnL.

| Parameter | Description | Effect on Strategy |
|-----------|-------------|-------------------|
| **Exposure Tolerance** | Defines the maximum allowable imbalance between long and short notional exposure | Lower values enforce tighter market neutrality and reduce directional risk |
| **Passiveness** | Controls how aggressively orders are placed relative to the order book | Higher values favor maker execution, lower fees, and reduced market impact |
| **Discretion** | Allows flexibility in execution timing and price placement within defined bounds | Higher values improve fill probability during volatile conditions |
| **Alpha Tilt** | Applies a controlled weighting toward the leg with more favorable funding rates | May increase funding yield while introducing limited directional exposure |
| **Directional Bias** | Allows explicit net exposure in one direction when enabled | Converts the strategy from pure arbitrage to a partially directional trade |
| **Minimum Clip Size** | Sets the minimum order size used during execution | Reduces order book signaling and mitigates market impact |
| **Passive Only** | Restricts execution to maker orders only | Eliminates taker fees at the cost of slower fills |
| **Active Limit** | Allows limit orders to cross the spread within defined bounds | Improves execution speed while maintaining price control |
| **Reduce Only** | Ensures orders can only reduce existing positions | Prevents accidental increases in exposure |
| **Cooldown Pause** | Temporarily halts execution after defined conditions are met | Limits over-trading during unstable market periods |
| **Soft Pause** | Gradually slows execution without fully stopping the strategy | Preserves position stability during short-term disruptions |
| **Strict Duration** | Enforces a fixed execution and holding window | Ensures the strategy exits after a defined time horizon |

#### 6.1.7 Monitoring and Lifecycle

Once active, positions are continuously monitored. Funding accrual, exposure, and execution metrics are updated in real time.

Trades may be adjusted, reduced, or closed without impacting other active strategies or account configuration on supported exchanges such as Hyperliquid and Paradex.

### 6.2 Funding Rate Arbitrage Bot

The Automated Funding Arbitrage Bot allows users to automate funding rate arbitrage strategies across exchanges.

#### 6.2.1 Overview

The bot operates by monitoring funding rates and position balances across the selected exchanges and perpetual pairs.

Its primary function is to maintain a directionally neutral exposure while capturing funding rate differentials over time. The bot maintains paired long and short positions according to predefined configuration and continuously manages exposure, sizing, and funding accrual.

#### 6.2.2 Configuration

Before activation, the user selects:
- Exchanges and perpetual pairs for long and short positions
- Target notional size per position
- Leverage
- Duration of Execution

These inputs define the operating bounds of the bot.

#### 6.2.3 Position and Exposure Management

The bot enforces directional neutrality at all times. Positions are rebalanced automatically to maintain matched long and short exposure within defined tolerances.

Directional exposure is not supported.

#### 6.2.4 Funding Tracking

Funding is accrued independently on each exchange. Net funding performance is calculated as funding earned minus funding paid and is presented as a cumulative time series and aggregate value.

Price-based PnL is tracked separately and does not influence bot behavior.

#### 6.2.5 Control and Lifecycle

The bot may be started, paused, or stopped at any time. Pausing or stopping the bot prevents further actions and does not automatically close positions unless explicitly requested.

---

## 7. PORTFOLIO

### 7.1 Overview

The Portfolio page provides an aggregated view of the entire Bitfrost account. All metrics represent the combined state of the Bitfrost parent account and all associated exchange sub-accounts.

![Portfolio Overview](https___files_gitbook_com_v0_b_gitbook-x-prod_appspot_com_o_spaces_2Fvha7vMBPD2xjgyDUGRDe_2Fuploads_2F4d01M0KFY3y16fk6i6Pl_2FScreenshot_202026-01-25_20at_2015_37_14_png_alt_media_token_ce412737-66a2-4775-8076-243f8be4e940.png)

The overview section displays account-wide metrics aggregated across all balances and positions.

Specifically:
- **Total Equity** represents the sum of equity held in the Bitfrost parent account and all exchange sub-accounts
- **PnL** represents cumulative realized profit and loss across all sub-accounts and strategies
- **Unrealized PnL** represents mark-to-market PnL across all open positions on all exchanges
- **Directional Bias** represents net directional exposure aggregated across all positions

These values reflect the global state of the user's Bitfrost account.

### 7.2 Equity and Distribution

| Metric | Definition |
|--------|------------|
| **Unlocked Vault Equity** | Equity held in the Bitfrost parent account that is not assigned to any exchange sub-account |
| **Exchange Equity** | Equity held across all exchange sub-accounts. Calculated as total equity minus unlocked vault equity |
| **Locked Margin Equity** | Equity held on exchanges that is not transferable because it is reserved as margin for open positions or exchange risk requirements |
| **Unlocked Margin Equity** | Equity held on exchanges that is transferable and not currently used as margin for any positions |

Exchange distribution views reflect the relative allocation of equity across connected exchanges.

### 7.3 Performance Tracking

Performance charts display aggregated PnL over selectable time horizons.

Charts reflect:
- Funding-based returns
- Realized trading outcomes
- Unrealized position changes

All performance data is calculated at the account level rather than per strategy or per exchange.

### 7.4 Balances and Positions

Tables display records across all exchanges.

Values include:
- Asset balances by exchange
- Open Positions by exchange
- Rebalancing history
- Funding rate payment history
- Deposits & withdrawals

---

## 8. EXCHANGE MANAGEMENT

The Exchange Management view provides visibility into each exchange sub-account linked to a Bitfrost account.

### 8.1 Overview

Each active exchange is listed under the accounts list. Each account displays its equity, exposure, and status.

For each exchange sub-account, the view shows:
- Current exchange equity
- Short-term performance indicators
- Account update status

Exchange-level values contribute to the aggregated portfolio metrics.

Selecting an exchange opens an exchange-specific view with detailed metrics scoped to that sub-account.

This page also allows users to manage sub-account configuration by adding or removing exchange sub-accounts via Configure Accounts.

### 8.2 Exchange Detail View

The exchange detail view provides a breakdown of the selected sub-account only.

It includes:
- Total equity held on the exchange
- Directional exposure of open positions
- Unrealized profit and loss
- Time series charts for equity, notional exposure, and PnL

All values in this view are isolated to the selected exchange and do not include balances or positions from other sub-accounts.

### 8.3 Adding an Exchange Account

To add a new exchange sub-account, the user opens Configure Accounts and enables the desired exchange.

A new exchange account is initialized by transferring funds from the Bitfrost parent account. The account becomes active once it has been funded.

Initial funding amount determines the starting equity of the exchange sub-account and may be adjusted later using transfers.

### 8.4 Removing an Exchange Account

Removing an exchange sub-account requires the account to be fully settled.

Before an exchange can be removed:
- All open positions must be closed
- All funds must be transferred back to the Bitfrost parent account
- The exchange sub-account balance must be 0

Removing an exchange with a non-zero balance may result in loss of funds.

### 8.5 Funding Distribution

Users may set a default distribution for allocating newly deposited funds across exchanges.

This setting applies only to new deposits and does not move existing balances unless the user performs a transfer.

### 8.6 Exchange Level Actions

From the exchange detail view, users may:
- Deposit funds into the selected exchange sub-account
- Transfer transferable funds between the exchange sub-account and the Bitfrost parent account
- Prepare funds for withdrawal by transferring them back to the parent account

All exchange-level actions are reflected in the aggregated portfolio view.

---

## 9. ORDER HISTORY

The Order History view provides a complete record of execution activity across the Bitfrost account. All entries shown are aggregated across the Bitfrost parent account and all exchange sub-accounts.

### 9.1 Overview

The table displays historical and active execution records for all strategies initiated through Bitfrost.

Each row represents a single execution instance, which may consist of one or multiple coordinated orders.

### 9.2 Filters and States

Orders may be filtered by status, including:
- Active
- Finished
- Paused
- Scheduled
- Canceled
- Conditional

Additional filters allow grouping by execution type.

### 9.3 Displayed Fields

For each execution, the following fields are shown:

- **Pair**: The trading pair associated with the execution
- **Side**: Indicates whether the execution represents a single order or a multi-leg strategy
- **Target Quantity**: The intended notional or asset quantity specified at execution time
- **Filled**: The percentage of the target quantity that has been executed
- **Time Start**: The timestamp at which the execution was initiated
- **Strategy**: The execution method used, such as time-weighted execution
- **Status**: The current or final state of the execution

### 9.4 Scope and Aggregation

Order history reflects execution activity across all exchanges and sub-accounts.

Execution records remain available after completion and form part of the permanent account history.

---

## 10. MARKET MAKER MANAGEMENT

Market Maker Management provides a consolidated, account-level view of all active market making activity executed through the platform.

### 10.1 Overview

Market Maker Management provides a unified supervisory view over all market making activity executed within the account.

This includes standalone strategies, vault-based strategies, and multi-strategy portfolios that aggregate multiple independent strategies across venues. All execution remains strategy-scoped while monitoring and analysis are performed at the account level.

### 10.2 Strategy Types

Market making activity may be deployed through three distinct strategy constructs.

#### 10.2.1 Advanced Strategies

Advanced strategies represent single market making deployments operating on a specific exchange and trading pair.

Each advanced strategy maintains its own:
- Capital allocation
- Leverage configuration
- Market making parameters
- Risk controls

Advanced strategies execute independently and contribute discrete exposure and profit and loss to the account.

#### 10.2.2 Vault Based Strategies

Vault strategies represent pooled capital deployments operated by permissioned market makers.

User-deposited capital is aggregated into a vault and deployed through proprietary strategies that are not publicly disclosed.

Vault strategies operate across one or more venues and generate profit and loss that is distributed proportionally to depositors after performance fees.

From a management perspective, vault strategies are treated as a single execution unit with internal strategy abstraction.

#### 10.2.3 Multi Strategy Portfolios

Multi-strategy portfolios aggregate multiple independent strategies into a single coordinated deployment.

Each underlying strategy within a multi-strategy portfolio may differ by:
- Exchange
- Trading pair
- Capital allocation
- Leverage
- Market making configuration
- Risk parameters

All underlying strategies execute independently but are monitored collectively as part of a unified portfolio construct.

Aggregate exposure, profit and loss, and risk metrics are computed across all constituent strategies to provide a holistic view of portfolio behavior.

### 10.3 Active Strategy Set

The active strategy set includes:
- Standalone advanced strategies
- Vault strategy positions
- Multi-strategy portfolios

Each entry represents an execution grouping rather than an individual order stream.

Status, deployment timing, venue scope, and realized performance are tracked continuously.

### 10.4 Exposure and Performance Aggregation

Exposure and performance data may be analyzed across multiple dimensions including venue, asset, and strategy type.

Venue-level aggregation consolidates all strategies executing on the same exchange, including strategies that belong to multi-strategy portfolios or vaults.

Exposure reflects gross notional exposure and does not imply shared margin or risk limits unless explicitly configured.

---

## 11. POSITION MANAGEMENT

### 11.1 Execution

The Execution view describes how a submitted order or strategy was executed across exchanges.

#### 11.1.1 Overview

The Execution summary provides a complete, time-ordered record of fills, exposure management, and market interaction during the execution window.

Each execution represents a single submission and its resulting activity until completion, cancellation, or pause.

#### 11.1.2 Execution Configuration

The execution configuration reflects the parameters defined at submission time and remains fixed for the lifetime of the execution.

This includes:
- Trading pairs and exchanges per leg
- Buy or sell direction per leg
- Target notional per leg
- Execution method and duration
- Exposure and tolerance constraints

#### 11.1.3 Execution Progress

Execution progress is displayed per leg and in aggregate.

For each leg, the view shows:
- Target notional
- Executed notional
- Average execution price
- Fill percentage
- Execution state

#### 11.1.4 Execution Metrics

Execution metrics describe how the order interacted with the market during execution.

Displayed metrics include:

- **Minimal Exposure**: The lowest observed net exposure during execution
- **Slippage**: Difference between reference price and achieved execution price
- **Spread**: Average bid-ask spread observed over the execution window
- **Exchange Fees**: Total fees incurred across all exchanges
- **Realization Rate**: Rate at which target notional was converted into executed notional

#### 11.1.5 Exposure Tracking

Exposure tracking charts show the evolution of exposure during execution.

They include:
- Maker-executed volume
- Taker-executed volume
- Net exposure over time
- Target exposure
- Exposure tolerance bands

This view illustrates how exposure was constrained and corrected throughout execution.

#### 11.1.6 Market Context

Market context charts show reference market data during execution.

These include:
- Mid-price of the traded instrument
- Observed spread over time

#### 11.1.7 Execution Controls

While execution is active, the following controls may be available:
- Pause execution
- Cancel execution

Pausing or cancelling prevents further execution but does not revert completed fills.

Once an execution is finished, the record becomes final and read-only.

### 11.2 Status

The Status view describes the state of an active or completed funding rate arbitrage position.

#### 11.2.1 Overview

It provides a consolidated view of the position configuration, current exposure, and performance metrics.

#### 11.2.2 Position State

The status view reports the current state of the position.

Displayed fields include:
- Open or closed status
- Time the position was opened
- Current leg balances
- Net exposure across legs

This section reflects the live state of the position.

#### 11.2.3 Funding Performance

The funding section displays funding-related performance metrics for the position.

This includes:
- Funding earned on the long leg
- Funding paid on the short leg
- Net funding accrued
- Funding rate time series

Funding metrics update continuously while the position is open.

#### 11.2.4 Price and PnL Metrics

Price-based metrics are displayed separately from funding metrics.

These include:
- Unrealized price PnL per leg
- Aggregate unrealized PnL
- Mark-to-market valuation of the position

Price PnL does not define the strategy outcome but is shown for completeness.

#### 11.2.5 Exposure Monitoring

Exposure charts show how long and short exposure has evolved over the lifetime of the position.

These charts illustrate:
- Leg-level exposure
- Net exposure drift
- Adherence to directional neutrality

#### 11.2.6 Controls

While the position is open, the user may:
- Reduce the position
- Close the position

Controls operate at the position level and affect both legs.

#### 11.2.7 Final State

Once closed, the status view reflects the final realized funding and price PnL.

### 11.3 Market Making Strategy Monitor

The Market Making Strategy Monitor provides detailed execution, performance, and risk visibility for active market making strategies.

#### 11.3.1 Overview

For multi-strategy portfolios, the monitor exposes both aggregated portfolio behaviour and granular analytics for each underlying sub-strategy operating across multiple exchanges and instruments.

Advanced strategies and vault strategies expose aggregated analytics only and do not include sub-strategy level decomposition as these do not exist.

#### 11.3.2 Summary Metrics

The summary metrics section provides a consolidated view of portfolio performance and execution quality.

Metrics include:
- Total profit and loss across realized and unrealized positions
- Cumulative traded volume
- Net directional exposure after offsetting long and short positions
- Average spread captured across executions
- Order fill rate as a measure of execution efficiency
- Average order book imbalance encountered
- Maximum observed drawdown
- Risk-adjusted performance expressed as a Sharpe ratio

These metrics reflect the combined behaviour of all active sub-strategies within the portfolio.

#### 11.3.3 Profit and Loss Over Time

The profit and loss chart displays portfolio performance through time.

It includes:
- Realized profit and loss from closed executions
- Unrealized profit and loss from open positions
- Net profit and loss representing the combined effect

This view is used to assess performance stability, drawdown behaviour, and recovery characteristics across the full strategy set.

#### 11.3.4 Position and Exposure

The position and exposure chart visualises inventory distribution over time.

It shows:
- Aggregate long exposure
- Aggregate short exposure
- Net exposure after offsetting positions

This view enables monitoring of directional bias, inventory accumulation, and hedging effectiveness across sub-strategies and venues.

#### 11.3.5 Volume and Trading Activity

The volume and trading activity chart reflects cumulative executed notional.

It provides insight into:
- Strategy participation intensity
- Execution pacing
- Changes in market interaction over time

Steeper increases indicate periods of higher trading activity or increased aggressiveness.

#### 11.3.6 Order Book Imbalance

The order book imbalance chart represents market pressure during execution.

- Positive values indicate buy-side dominance
- Negative values indicate sell-side dominance

This metric is used to evaluate adverse selection risk and the impact of market conditions on inventory management.

#### 11.3.7 Spread Capture

The spread capture chart reflects the effective bid-ask spread captured by executions, measured in basis points.

This metric indicates:
- Quoting competitiveness
- Pricing efficiency
- Market making edge under prevailing liquidity conditions

Sustained compression may indicate increased competition or reduced inefficiency.

#### 11.3.8 Fill Rate Performance

The fill rate performance chart shows execution efficiency over time.

- Higher values indicate improved order placement and liquidity interaction
- Lower values may indicate overly passive quoting or reduced available liquidity

#### 11.3.9 Current Positions

The current positions section lists all open positions across sub-strategies.

Each position includes:
- Instrument and exchange
- Position direction
- Position size
- Entry price
- Current price
- Notional exposure
- Unrealized profit and loss

Positions are grouped to support rapid inspection of live exposure and risk concentration.

#### 11.3.10 Risk Metrics

The risk metrics section summarizes key portfolio-level risk indicators.

These include:
- Maximum drawdown observed since deployment
- Risk-adjusted performance
- Execution efficiency indicators
- Pricing and imbalance metrics

These metrics are informational unless explicitly linked to automated risk controls.

#### 11.3.11 Strategy Status

The strategy status section reflects the operational state of the portfolio.

It includes:
- Execution status
- Total runtime since deployment
- Total executed trades
- Win rate across executions

This section is used to confirm strategy health and operational continuity.

#### 11.3.12 Relationship to Other Strategy Types

- **Multi-strategy portfolios** expose both aggregated and sub-strategy level analytics as described above
- **Advanced strategies** expose the same execution and performance metrics
- **Vault strategies** expose aggregate vault-level performance and risk metrics without visibility into internal strategy logic or execution details

---

## 12. MORE

### 12.1 Transaction Explorer

The Transaction Explorer provides a real-time, system-wide view of all on-chain and off-chain actions processed through Bitfrost Prime.

#### 12.1.1 Overview

The explorer streams live transaction activity as it is processed and settled.

It is designed to serve as an operational audit layer, enabling verification, traceability, and monitoring of all account activity across deposits, withdrawals, trading, and protocol interactions.

Each record represents a discrete system action initiated by an account, strategy, or vault and propagated through the Bitfrost execution and settlement pipeline.

The explorer supports operational monitoring, reconciliation, and post-trade analysis.

#### 12.1.2 Search and Filtering

The search interface allows querying by transaction hash, action type, or account identifier.

Status filters enable isolation of successful, pending, or failed transactions.

This supports rapid identification of execution issues, settlement delays, or anomalous behaviour.

#### 12.1.3 Transaction Records

Each transaction entry includes:

- **Transaction hash**: A unique identifier referencing the underlying on-chain or internal execution event
- **Action**: The operation performed, such as deposit, withdrawal, transfer, or trade execution
- **Block**: The block height at which the transaction was confirmed or recorded
- **Time**: The timestamp indicating when the transaction was processed
- **Account**: The originating account or sub-account responsible for the action
- **Status**: The current execution state of the transaction

#### 12.1.4 Transaction Status States

Transactions may exist in one of the following states:

- **Success**: The transaction has been fully executed and settled
- **Pending**: The transaction has been submitted but is awaiting confirmation or finalisation
- **Failed**: The transaction did not complete due to execution, validation, or settlement failure

Status is updated in real-time as transactions progress through the system.

---

*End of Documentation*
