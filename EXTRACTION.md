# Extraction status

Source: [`apps/contracts`](https://github.com/walletchan/walletchan/tree/1ad4346e5d20994fa7457facaef7e389244d6290/apps/contracts) from `walletchan/walletchan` at `1ad4346e5d20994fa7457facaef7e389244d6290`.

This is a fresh repository with a source snapshot, not a history rewrite. Only committed source and example environment files were copied; no live credentials, databases, generated builds, or deployment state were copied.

## Deployment boundary

The main repo is unchanged. Existing Railway services remain connected to `walletchan/walletchan`. This repo has not been connected to any Railway service, and no domains, secrets, database schemas, volume contents, or running processes were changed.

Source is at this repository's root. Its Dockerfile and Railway config use root-relative paths. Existing copied implementation/deployment docs may describe historical monorepo paths; use these extraction notes for the standalone layout.

Before cutover: verify builds, configure repo access, preserve current environment variables and database/volume bindings, update Railway's source/config/watch paths explicitly, and confirm service health and API behavior. Keep the previous deployment available for rollback. Never start signing bots locally against a production wallet during validation.

## Shared dependencies

See `package.json` for dependencies. External services and public contract addresses remain runtime boundaries even when no workspace package is imported.

## Related documentation

- [EXTRACTION.md](./EXTRACTION.md)
- [IMPLEMENTATION.md](./IMPLEMENTATION.md)
- [LICENSE.md](./LICENSE.md)
- [_docs/ASSET_CHANGES_SIMULATION.md](./_docs/ASSET_CHANGES_SIMULATION.md)
- [_docs/DRIP_APY_UI_INFO.md](./_docs/DRIP_APY_UI_INFO.md)
- [_docs/SECURITY_AUDIT_PROMPT.md](./_docs/SECURITY_AUDIT_PROMPT.md)
- [_docs/VAULT_APY_INDEXING_INFO.md](./_docs/VAULT_APY_INDEXING_INFO.md)
- [ipfs/tokenURI-ipfs-CID.md](./ipfs/tokenURI-ipfs-CID.md)

Shared product/integration docs remain in the [main repo](https://github.com/walletchan/walletchan/tree/1ad4346e5d20994fa7457facaef7e389244d6290/_docs). Copies here retain their original context; they do not authorize a deployment.
