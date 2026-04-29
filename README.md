# Fair Transaction Ordering

A static website summarizing state-of-the-art methods for fair transaction ordering in blockchain systems, with a focus on mitigating front-running and other forms of transaction-reordering manipulation in decentralized exchanges.

Live site: https://lucaspfingsten.github.io/my_website/

Maintained by the Distributed Computing Group at ETH Zürich.

## Methods covered

Each method has a dedicated page with a concise summary and discussion of its trade-offs:

- **Optimized Trade Execution** (`optimized-trade-execution.html`) — adjusts trade parameters to make front-running unprofitable; least invasive, limited in scope.
- **Professional Market Makers** (`professional-market-makers.html`) — replaces the AMM with a professional market maker that executes trades at market price, typically via off-chain agreements settled on-chain.
- **Trusted Third Party Ordering** (`trusted-third-party-ordering.html`) — delegates ordering to a trusted third party for efficiency, at the cost of decentralization and security.
- **Algorithmic Committee Ordering** (`algorithmic-committee-ordering.html`) — a committee agrees on a fair ordering through consensus, tolerating up to one third byzantine members.
- **On-Chain Commit & Reveal** (`on-chain-commit-and-reveal.html`) — two-phase ordering with encrypted commitments published on-chain and later revealed.
- **Off-Chain Commit & Reveal** (`off-chain-commit-and-reveal.html`) — a committee orders encrypted transactions off-chain and decrypts them via threshold signatures.
- **Randomized Ordering** (`randomized-ordering.html`) — collects transactions over a period and executes them in random order to prevent front-running.

The home page also includes an abbreviations reference (AMM, DEX, MEV, FairMM, MPTC, F3B, FairPoS, etc.).

## Structure

- `index.html` — landing page with method overview cards and abbreviations.
- One HTML page per method (see list above).
- `css/` — Webflow stylesheets (`normalize.css`, `webflow.css`, `basite-ecf154.webflow.css`).
- `js/webflow.js` — Webflow runtime.
- `images/` — illustrations and screenshots referenced from each page.

## Running locally

Open `index.html` in a browser, or serve the directory with any static HTTP server (e.g. `python3 -m http.server`).

## Disclaimer

The summaries are informational. The maintainers are not liable for any false information.
