# Mina SDK Documentation Plan

## Overview

This document outlines the comprehensive documentation structure for the `@siphoyawe/mina-sdk` - a cross-chain bridge SDK for Hyperliquid enabling bridging assets from 40+ chains with automatic deposit to trading accounts.

---

## Documentation Structure

### Navigation Tabs

1. **Guides** - Getting started, concepts, tutorials
2. **API Reference** - Complete method and type documentation
3. **React** - React hooks and provider documentation
4. **Examples** - Real-world integration examples

---

## Tab 1: Guides

### Group: Getting Started

| Page | File | Description |
|------|------|-------------|
| Introduction | `index.mdx` | SDK overview, features, supported chains |
| Installation | `installation.mdx` | npm/yarn/pnpm installation, peer dependencies |
| Quick Start | `quickstart.mdx` | 5-minute getting started guide |
| Configuration | `configuration.mdx` | MinaConfig options, RPC URLs, defaults |

### Group: Core Concepts

| Page | File | Description |
|------|------|-------------|
| Chains | `concepts/chains.mdx` | Chain discovery, supported chains, HyperEVM |
| Tokens | `concepts/tokens.mdx` | Token discovery, bridgeable tokens, native tokens |
| Quotes | `concepts/quotes.mdx` | Quote generation, price impact, route preferences |
| Execution | `concepts/execution.mdx` | Bridge execution flow, steps, status tracking |
| Auto-Deposit | `concepts/auto-deposit.mdx` | USDC arrival detection, L1 deposit, confirmation |
| Slippage | `concepts/slippage.mdx` | Slippage settings, constraints, presets |

### Group: Advanced

| Page | File | Description |
|------|------|-------------|
| Caching | `advanced/caching.mdx` | Cache management, TTLs, invalidation |
| Custom RPCs | `advanced/custom-rpcs.mdx` | Custom RPC URL configuration |
| Standalone Functions | `advanced/standalone.mdx` | Using services without Mina client |

---

## Tab 2: API Reference

### Group: Client

| Page | File | Description |
|------|------|-------------|
| Mina Class | `api/mina.mdx` | Main client class, constructor, all methods |

### Group: Services

| Page | File | Description |
|------|------|-------------|
| Chain Service | `api/services/chain.mdx` | getChains, getDestinationChains, etc. |
| Token Service | `api/services/token.mdx` | getTokens, getBridgeableTokens, etc. |
| Balance Service | `api/services/balance.mdx` | getBalance, getBalances, etc. |
| Quote Service | `api/services/quote.mdx` | getQuote, getQuotes, estimatePriceImpact |
| Execute Service | `api/services/execute.mdx` | execute, validateQuote |
| Deposit Service | `api/services/deposit.mdx` | detectUsdcArrival, executeDeposit, monitorL1 |

### Group: Types

| Page | File | Description |
|------|------|-------------|
| Configuration | `api/types/config.mdx` | MinaConfig, SlippagePreset, RoutePreference |
| Chain & Token | `api/types/chain-token.mdx` | Chain, Token, ChainsResponse, TokensResponse |
| Quote & Execution | `api/types/quote-execution.mdx` | QuoteParams, Quote, ExecuteOptions, ExecutionResult |
| Status | `api/types/status.mdx` | StepStatusPayload, TransactionStatusPayload |
| Balance | `api/types/balance.mdx` | Balance, BalanceParams, BalancesResponse |

### Group: Events

| Page | File | Description |
|------|------|-------------|
| Event System | `api/events.mdx` | SDKEventEmitter, SDK_EVENTS, event payloads |

### Group: Errors

| Page | File | Description |
|------|------|-------------|
| Error Classes | `api/errors.mdx` | All error classes, recovery actions, type guards |

### Group: Constants

| Page | File | Description |
|------|------|-------------|
| Constants | `api/constants.mdx` | Chain IDs, addresses, timeouts, thresholds |

---

## Tab 3: React

### Group: Setup

| Page | File | Description |
|------|------|-------------|
| Installation | `react/installation.mdx` | React-specific setup, peer deps |
| MinaProvider | `react/provider.mdx` | Provider setup, context value |

### Group: Hooks

| Page | File | Description |
|------|------|-------------|
| useMina | `react/hooks/use-mina.mdx` | Access SDK instance |
| useQuote | `react/hooks/use-quote.mdx` | Fetch bridge quotes with debounce |
| useTokenBalance | `react/hooks/use-token-balance.mdx` | Fetch token balances |
| useTransactionStatus | `react/hooks/use-transaction-status.mdx` | Track transaction status |

---

## Tab 4: Examples

### Group: Basic Examples

| Page | File | Description |
|------|------|-------------|
| Simple Bridge | `examples/simple-bridge.mdx` | Basic bridge transaction |
| Token Selection | `examples/token-selection.mdx` | Chain/token selection UI |
| Quote Display | `examples/quote-display.mdx` | Displaying quote details |

### Group: Advanced Examples

| Page | File | Description |
|------|------|-------------|
| Full Integration | `examples/full-integration.mdx` | Complete bridge widget |
| Error Handling | `examples/error-handling.mdx` | Robust error handling patterns |
| Event Tracking | `examples/event-tracking.mdx` | Real-time status updates |

---

## Page Content Templates

### Getting Started Pages

Each page should include:
- Clear title and description in frontmatter
- Overview paragraph
- Prerequisites (if any)
- Step-by-step instructions with code blocks
- Next steps with card links

### API Reference Pages

Each page should include:
- Function/class signature
- Parameters table with types
- Return value description
- Code example
- Related methods/types

### Example Pages

Each page should include:
- Use case description
- Complete working code
- Step-by-step explanation
- Common variations

---

## Branding Configuration

### Colors (docs.json)
```json
{
  "colors": {
    "primary": "#00D4AA",
    "light": "#00E6BB",
    "dark": "#00B899"
  }
}
```

### Metadata
- **Name**: Mina SDK
- **Description**: Cross-chain bridge SDK for Hyperliquid
- **Logo**: Light and dark variants needed

---

## File Structure

```
mina-documentation/
├── docs.json
├── index.mdx
├── installation.mdx
├── quickstart.mdx
├── configuration.mdx
├── concepts/
│   ├── chains.mdx
│   ├── tokens.mdx
│   ├── quotes.mdx
│   ├── execution.mdx
│   ├── auto-deposit.mdx
│   └── slippage.mdx
├── advanced/
│   ├── caching.mdx
│   ├── custom-rpcs.mdx
│   └── standalone.mdx
├── api/
│   ├── mina.mdx
│   ├── events.mdx
│   ├── errors.mdx
│   ├── constants.mdx
│   ├── services/
│   │   ├── chain.mdx
│   │   ├── token.mdx
│   │   ├── balance.mdx
│   │   ├── quote.mdx
│   │   ├── execute.mdx
│   │   └── deposit.mdx
│   └── types/
│       ├── config.mdx
│       ├── chain-token.mdx
│       ├── quote-execution.mdx
│       ├── status.mdx
│       └── balance.mdx
├── react/
│   ├── installation.mdx
│   ├── provider.mdx
│   └── hooks/
│       ├── use-mina.mdx
│       ├── use-quote.mdx
│       ├── use-token-balance.mdx
│       └── use-transaction-status.mdx
└── examples/
    ├── simple-bridge.mdx
    ├── token-selection.mdx
    ├── quote-display.mdx
    ├── full-integration.mdx
    ├── error-handling.mdx
    └── event-tracking.mdx
```

---

## Implementation Priority

### Phase 1: Foundation
1. Update docs.json configuration
2. Create index.mdx (landing page)
3. Create installation.mdx
4. Create quickstart.mdx

### Phase 2: Core Guides
5. Create configuration.mdx
6. Create concepts/ pages (6 pages)

### Phase 3: API Reference
7. Create api/mina.mdx (main client)
8. Create api/services/ pages (6 pages)
9. Create api/types/ pages (5 pages)
10. Create api/events.mdx and api/errors.mdx
11. Create api/constants.mdx

### Phase 4: React Documentation
12. Create react/ pages (6 pages)

### Phase 5: Examples
13. Create examples/ pages (6 pages)

### Phase 6: Polish
14. Add code snippets
15. Verify navigation
16. Test with Mintlify CLI

---

## Total Pages: 37

- Guides: 10 pages
- API Reference: 14 pages
- React: 6 pages
- Examples: 6 pages
- Landing: 1 page
