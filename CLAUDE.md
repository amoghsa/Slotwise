<!-- agent-routing:begin -->
## Delegation policy

Keep bulk text out of this conversation's context — it is re-read on every
subsequent turn. Build logs, crash dumps, test transcripts, wide greps and
whole-file reads go to a subagent; take back only the digest.

| Work | Agent |
|---|---|
| Build, test, lint, install, git plumbing | `runner` |
| Find where something lives | `scout` |
| Digest a long log / crash / CI transcript | `log-digest` |
| Write code to a settled spec | `implementer` |
| Write or repair tests | `test-author` |
| README, changelog, PR text, store listings | `scribe` |
| Choose an approach, plan a change | `architect` |
| Root-cause an unknown failure | `debugger` |
| Review a diff before it ships | `reviewer` |

Handle directly what is cheaper to do than to delegate. Diagnosis and
implementation are separate steps: `architect`/`debugger` decide,
`implementer` writes.
<!-- agent-routing:end -->
