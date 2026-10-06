# Public contract addresses

Public TypeScript address artifact used by WalletChan's vault indexer. Generated from this repo's `addresses.json` with `pnpm sync:addresses`. No private repository or credential is needed to build this package.

Consumers pin this repository commit and include `packages/contract-addresses` as a workspace package. Import `@walletchan/contract-addresses` as before. This package is not published to npm as part of extraction.

The main repo and private shared repo retain their original address snapshots during the Railway transition. Propagate reviewed address changes deliberately; do not treat source extraction as a production configuration update.
