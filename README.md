# Bridge Transfer Status API

API contract for the service that reports the status of BTC L1 → L2 bridge transfers and issues the proofs needed to complete them. The bridge frontend consumes this API.

## Contract

The source of truth is [`bridge-status-openapi.yaml`](./bridge-status-openapi.yaml) (OpenAPI 3.0).

| Endpoint | Purpose |
|---|---|
| `GET /transfers/{id}` | Get a single bridge transfer and its current status |
| `POST /proofs` | Request the proof needed to complete a transfer |

## Changing the contract

1. Create a branch from `main`.
2. Edit `bridge-status-openapi.yaml`.
3. Open a pull request and request review from the frontend lead. Contract changes affect frontend integration.
