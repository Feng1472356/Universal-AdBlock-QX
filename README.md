# Universal-AdBlock-QX

HAR-driven ad domain analysis and Quantumult X rule database.

## Repository layout

- `database/domains.csv`: observed-domain inventory, classification, evidence and block decision.
- `reports/`: sanitized per-capture analysis reports.
- `rules/rewrite/`: URL rewrite rules (`[rewrite_local]`) and their required MITM host declarations.
- `rules/filter/`: traffic-routing/filter rules (`[filter_local]`); keep separate from rewrite rules.

## Safety policy

- Never commit raw HAR files, authorization headers, cookies, tokens, full query strings, account identifiers or precise location data.
- Do not remove historical domains merely because they are absent from a new capture.
- Do not block a domain based only on its presence in a third-party blocklist.
- Keep uncertain domains out of active rules until evidence is sufficient.
- Preserve changes in Git history and review rule changes through pull requests.
