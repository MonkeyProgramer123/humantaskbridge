# HumanTaskBridge

[Visit HumanTaskBridge](https://humantaskbridge.jimmy-bot-auto.workers.dev/) · [For agents](https://humantaskbridge.jimmy-bot-auto.workers.dev/docs) · [OpenAPI](https://humantaskbridge.jimmy-bot-auto.workers.dev/openapi.json)

**Independent human help for AI agents and their people.**

Request human assistance with public information checks, research, data review, or authorized usability work. One person reviews every request, agrees scope and price before payment, and delivers through a private tracking page and REST API.

## Start here

| Resource | Link |
| --- | --- |
| Website | [humantaskbridge.jimmy-bot-auto.workers.dev](https://humantaskbridge.jimmy-bot-auto.workers.dev/) |
| Live availability and supported services | [GET /api/capabilities](https://humantaskbridge.jimmy-bot-auto.workers.dev/api/capabilities) |
| Agent discovery | [/llms.txt](https://humantaskbridge.jimmy-bot-auto.workers.dev/llms.txt) |
| Agent integration guide | [Guide](docs/agent-guide.md) |
| REST contract | [OpenAPI](openapi.json) |
| Human task form | [Request a task](https://humantaskbridge.jimmy-bot-auto.workers.dev/request) |
| Private service ideas | [Suggest a task](https://humantaskbridge.jimmy-bot-auto.workers.dev/suggest) |
| Voluntary support | [Support](https://humantaskbridge.jimmy-bot-auto.workers.dev/support) |

## For agent developers

Read live capabilities before attempting a submission. Follow the [integration guide](docs/agent-guide.md) and the live OpenAPI contract. Commercial intake is available only when `intakeOpen` is true and `preview` is false. Availability may change independently of this repository.

User authorization is required to request work and spend funds. A separate authorization and budget are required for voluntary contributions. Keep private tracking credentials out of repositories, issues, logs, and URLs. Submitting a brief does not accept a contract, trigger a charge, or guarantee that the operator will accept it.

HumanTaskBridge provides an asynchronous REST workflow with versioned proposals, explicit acceptance, manual payment verification, and private delivery. This repository contains public discovery material and the API contract; operational source, administrative configuration, and customer records are maintained separately.

## Service boundaries

No wallet connection, automatic transfer, custody, automatic refund, or execution of submitted code. Do not submit passwords, private keys, seed phrases, or unnecessary sensitive information. Read [acceptable use](https://humantaskbridge.jimmy-bot-auto.workers.dev/acceptable-use), [terms](https://humantaskbridge.jimmy-bot-auto.workers.dev/terms), and [privacy](https://humantaskbridge.jimmy-bot-auto.workers.dev/privacy).

Report documentation errors through a GitHub issue without private task details. Use the private task conversation for customer work.
