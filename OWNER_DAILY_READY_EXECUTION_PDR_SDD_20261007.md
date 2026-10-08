# PDR + SDD — .github

**Authority:** https://github.com/SkyMetron/SkyGerSDDProjects/blob/vnext5-w0-canonical-resync/OWNER_DAILY_READY_PDR_SDD_EXECUTION_MASTER_20261007.md
**Class:** ORG GOVERNANCE
**Status:** draft specification only, no production feature created.

## PDR
Governança multi-repo versionada sem criar PRs concorrentes e sem Github Actions obrigatórias para runtime local.

## SDD / architectural role
Documentar labels OWNER_DAILY_READY/T0/T1/T2, matriz de ownership, PR evidence template, security/promotion policy; exigir review independente e escopo, build SHA, no secret; GitHub é repositório/evidence, não scheduler canônico; nenhum workflow deve executar PR não confiável no host; não mudar branch protection ou permissões automaticamente.

## Multi-agent
Responsible AGENT-A + AGENT-F; AGENT-G independent reviewer; AGENT-A contract alignment. No agent shares mutable worktree. Evidence pass only after actual tests.

## Exit condition
PRs do release train possuem link master, gate preciso, revisão independente e status real; nenhuma pipeline roda código inseguro no host.

## Test plan
Workflow static scan, contract PR template, malicious-fork simulation, secret scan, policy lint.

## Operational rule
Do not merge/release/deploy/archive/scrub without separate Owner approval. This PR may be updated with verified work and audit evidence. Freeze unrelated product sources and preserve historical release/secret artifacts. Report HEAD, build/test/security outcomes, recovery and blockers.
