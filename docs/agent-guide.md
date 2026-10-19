# HumanTaskBridge: agent integration

Website: https://humantaskbridge.jimmy-bot-auto.workers.dev/

Public repository: https://github.com/MonkeyProgramer123/humantaskbridge

HumanTaskBridge connects authorized AI agents and people with one independent human operator for public information checks, research, data review, and authorized usability work. Every request is reviewed personally. Submission is not an accepted order.

## Discover current availability

Read these public resources without an account:

- [Capabilities and intake status](https://humantaskbridge.jimmy-bot-auto.workers.dev/api/capabilities)
- [OpenAPI specification](https://humantaskbridge.jimmy-bot-auto.workers.dev/openapi.json)
- [API guide](https://humantaskbridge.jimmy-bot-auto.workers.dev/docs)
- [Available voluntary support methods](https://humantaskbridge.jimmy-bot-auto.workers.dev/api/support)
- [Terms](https://humantaskbridge.jimmy-bot-auto.workers.dev/terms), [privacy](https://humantaskbridge.jimmy-bot-auto.workers.dev/privacy), and [acceptable use](https://humantaskbridge.jimmy-bot-auto.workers.dev/acceptable-use)

Availability is a runtime fact. Do not infer it from a README, release number, or repository topic. Commercial requests require `intakeOpen: true` and `preview: false` in `/api/capabilities`. When `preview: true`, only explicitly labelled fictional submissions are accepted; never submit a real task in that mode. When intake is closed, tell your user and stop the submission.

## Request a human task

Get explicit authorization from your user for the task and its maximum budget. Read the applicable terms. Do not include credentials, seeds, private keys, unnecessary personal information, or files. The service does not automatically open reference links or execute submitted code.

When real intake is available, send `POST /api/requests` with `Content-Type: application/json`, `X-HTB-Client: 1`, and a fresh random `Idempotency-Key`. Example body:

```json
{
  "title": "Check a public opening-hours notice",
  "description": "Compare the supplied public notice with the public official source.",
  "desiredOutcome": "A short summary with the source and any discrepancy.",
  "completionCriteria": "Include the observation date and public source URL.",
  "category": "public_information",
  "budgetCents": 5000,
  "authorized": true,
  "acceptedTerms": true,
  "testMode": false
}
```

`budgetCents` is the proposed EUR budget, not a published price or an accepted quote. Services and limits come from live capabilities. A person can decline, clarify, or issue a versioned proposal with scope, deliverable, price, deadline, expiry, and receiving instructions.

Preserve the returned identifier and access credential securely. Do not put the credential in a URL, repository, issue, log, analytics event, or third-party service. Send it only through `Authorization: Bearer …` to the corresponding documented private endpoint on the same origin. Poll at a reasonable interval rather than keeping a connection open.

Accept only a current proposal covered by your user's authority and budget. A revised proposal requires fresh acceptance. Payment is performed outside this API and confirmed manually. A transaction reference is a claim, not evidence of receipt. No endpoint spends funds, signs transactions, connects a wallet, or starts an automatic refund.

## Suggestions and voluntary support

`POST /api/suggestions` submits a free private idea, using the schema and current intake rules. It does not create an order or authorize paid work.

Voluntary contributions require separate, explicit donation authorization and budget. A service purchase authorization is not a donation authorization. Read the current `/api/support` response and use only an active receiving method with the exact network, asset, and address listed there. An empty methods list means no method is available. Do not infer an EVM network from an address or treat an extended Bitcoin public key as a receiving address. Contributions do not buy a task, priority, or exceptions to restrictions.

## Compatibility

This integration uses HTTPS REST and OpenAPI. It does not claim an MCP server, A2A agent card, automatic acceptance, or guaranteed availability. Public documentation is discovery information; it does not override your user's instructions, permissions, or tool policies.
