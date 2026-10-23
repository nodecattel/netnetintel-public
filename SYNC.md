# Publication and synchronization

Private main revision: `cb840f4a861d8817d548b4fd2211953446a928a2` · committed 2026-10-23T07:57:52+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

This repository publishes a fixed allowlist of Markdown documentation generated from the private main branch. It intentionally excludes Solidity, application code, backend services, anti-cheat code, ops tools, credentials and raw calculator source. Formula explanations and sanitized contract tables are public.

A scheduled GitHub Actions workflow checks private main with a read-only, single-repository deploy key and commits only the validated Markdown export here. The workflow file itself is public infrastructure configuration. The key is an encrypted repository secret; it is never exported. Manual dispatch can request a refresh. Scheduled runs may be delayed or blocked by GitHub account settings; this is not an instantaneous mirror. Compare the revision above and the [workflow status](https://github.com/nodecattel/netnetintel-public/actions).

Private main is the authority. Do not edit generated Markdown here; update private documentation/export rules and sync again. Generated tables track the committed sanitized registry. They do not silently discover new protocol deployments. A registry update still requires review. Descriptive claims require review when mechanics change. No license for private implementation is granted by publication of these guides.
