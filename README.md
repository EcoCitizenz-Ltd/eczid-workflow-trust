# ECZ-ID Workflow Trust

Review GitHub workflow dependencies, permissions and currentness facts without uploading source or inventing a safety score.

## Outcome

Inventory workflow dependencies and review mutable references, permissions, trigger posture, OIDC, runner and attestation evidence.

## Quick start

```yaml
- uses: EcoCitizenz-Ltd/eczid-workflow-trust@v1
  with:
    report-path: eczid-workflow-trust.json
```

## Inputs

| Input | Required | Default | Description |
|---|---:|---|---|
| `report-path` | No | `eczid-workflow-trust.json` | Path for the JSON evidence report. |

## Outputs

| Output | Description |
|---|---|
| `result-state` | OBSERVED, REVIEW_RECOMMENDED or NOT_APPLICABLE. |
| `workflow-count` | Number of supported GitHub Actions workflow files reviewed. |
| `finding-count` | Number of deterministic observations emitted. |
| `report-path` | Generated JSON report path. |
| `next-action-url` | One contextual ECZ-ID next step, or empty when none is warranted. |

## Permissions, secrets and data

- The Action itself does not require repository write permission.
- No ECZ-ID secret or API key is required for this public Action.
- Supported workflow/configuration files are read locally inside the GitHub Actions workspace; repository source is not uploaded to ECZ-ID.
- See [PRIVACY.md](./PRIVACY.md), [SECURITY.md](./SECURITY.md) and [SUPPORT.md](./SUPPORT.md) for the complete public boundary.

## Version pinning

The examples use the stable `@v1` compatibility tag. For policies that require an immutable third-party reference, pin this Action to the full commit SHA of the reviewed release. GitHub Actions does not support action-name redirects as a substitute for a stable reference.

## Trust boundary

- Bounded deterministic evidence/current-state processing.
- No hidden telemetry.
- No repository code execution.
- Missing ECZ-ID or missing evidence never means unsafe, non-compliant or untrusted.
- No automatic ownership inference.
- No pay-to-pass.
- No global safety/certification/compliance/approval verdict.
- Local policy decides.

## ECZ-ID identity model

A free Declared Business Passport is the organisation Parent gateway for the seven free machine Passport families: Agent, MCP, Plugin, API, IoT / Device, SDK, and Service & Workload. Verified or Assured strengthens the same Parent ECZ-ID; it does not automatically independently verify a child Passport.

When an identity/currentness next step is warranted, ECZ-ID returns at most one neutral route. Payment never changes the technical result.

## Works with GitHub, not against it

ECZ-ID complements GitHub-native controls with persistent identity, accountable operator context, declared authority, current state, change and re-checkable evidence. It does not replace CodeQL, secret scanning, dependency review, workflow dependency lockfiles or artifact attestations.

## Support and security

Use the repository issue tracker only for reproducible product defects that contain no secrets or customer-private evidence. Follow [SECURITY.md](./SECURITY.md) for vulnerability reporting and [SUPPORT.md](./SUPPORT.md) for private/commercial support routes.
