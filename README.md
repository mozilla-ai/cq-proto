# cq-proto

Protocol buffer definitions for [cq](https://github.com/mozilla-ai/cq) — an
open standard for shared agent learning.

## Development

Requires [buf](https://buf.build/docs/installation).

    buf lint              # Lint proto files.
    buf breaking \        # Check for breaking changes against main.
      --against '.git#branch=main'
    buf convert . \       # Validate a fixture.
      --type cq.v1.KnowledgeUnit \
      --from fixtures/valid-unit.json

## Schema overview

| File | Contents |
|------|----------|
| `cq/v1/knowledge_unit.proto` | `KnowledgeUnit`, `Insight`, `Context`, `Evidence`, `Flag`, `Tier`, `FlagReason` |
| `cq/v1/scoring.proto` | `RelevanceWeights`, `ConfidenceConstants` |
| `cq/v1/api.proto` | `TeamAPIService`, `ProposeRequest`, `QueryRequest`, etc. |
| `cq/v1/review.proto` | `ReviewItem`, `ReviewQueueResponse`, `ReviewStatsResponse`, etc. |

## License

[Apache 2.0](LICENSE)
