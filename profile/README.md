# Causeway Services

<!-- 561-group-standards:badges:start -->
[![Causeway Services](https://img.shields.io/badge/561%20Group-Causeway%20Services-115e69)](https://github.com/causeway-services)
[![Indigenous data: CARE](https://img.shields.io/badge/Indigenous%20data-CARE-4b6f44)](https://github.com/causeway-services/.github/blob/main/GOVERNANCE.md)
[![Tips welcome](https://img.shields.io/badge/tips-welcome-d4a017)](https://github.com/561-group/.github/blob/main/TIPS.md)
<!-- 561-group-standards:badges:end -->

**A 561 Group organization.** Public services: gives people usable free-software rights and practical ways to learn, operate, challenge, contribute and benefit.

**Start with something usable:** [Causeway's public services guide](https://services.561.group/) points to available publications, resources and service explanations, with a separate [561 Group work inquiry](https://561.group/work/) for scoped problems. A customer can examine a free resource before deciding whether to buy anything. The Group is developing broader professional search, AI-discovery and marketing services, but a research requirement or a proposed pilot is not a launched commercial subscription or a guaranteed ranking result.

## Bazaar: real sellers, real customer demand

**Own a store or create something people can buy?** [Apply to the independent-seller Bazaar pilot](https://github.com/causeway-services/.github/issues/new?template=bazaar-seller.yml). You keep your original shop, merchant, checkout and rights; applying does not enroll or charge you. **Need a maker, download, commission or paid service?** [Submit a buyer need](https://github.com/causeway-services/.github/issues/new?template=bazaar-buyer.yml). [What this pilot actually does and does not do](https://github.com/causeway-services/.github/blob/main/BAZAAR.md). Public issues are not appropriate for private customer or payment information.

**Want to make and sell merchandise or reach new customers?** [Shop Services](https://github.com/causeway-services/.github/blob/main/SHOP-SERVICES.md) accepts real inquiries for independently priced and authorized supplier-backed POD/fulfillment and contextual advertising on *consenting* 561 publisher slots. [Request a quote for one or both services](https://github.com/causeway-services/.github/issues/new?template=bazaar-shop-service.yml). TPOP is a sourced rival and candidate supplier, not an installed reseller agreement; no invented ad inventory, spend authority or guaranteed impressions.

## Live regulatory intelligence for agents — source-qualified data

**New public machine service:** [Federal Register documents and source editions (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/latest.json), [30-day reported comment deadlines (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/comment-deadlines.json), [new/changed source editions (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/changes.json), [CloudEvents-format source events (JSONL)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/events.jsonl), and [DCAT dataset discovery (JSON-LD)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/catalog.jsonld).

An autonomous agent can receive normalized official public documents with source digest/edition, real agency docket and effective-date fields where supplied, and bounded source-reported upcoming public-comment dates. The original Red Cup source service uses the **official keyless Federal Register API** and republishes a seven-day rolling source observation every three hours, without an account, paid source, or human checkout. A separately operated [Coesite receiving report](https://raw.githubusercontent.com/coesite-operations/.github/main/data/records/received-regulatory-newswire/latest.json) checks public data from another host, with measured freshness and source identity. Source permissions, changing official deadlines and 3-hour publication are not guarantees of legal completeness or an SLA; the official document remains authoritative.

The free publisher observations are **not Newsroom-approved news articles or paid x402 results**. Qualified custom machine interpretation and automated alerting may become separately paid products of the [existing original 561 Group Market](https://market.561.group/), but a public source snapshot, listed tariff or unsigned 402 challenge is not evidence of an external paid purchase or cleared seller income. [Agent use examples, provenance and coverage limits](https://github.com/causeway-services/.github/blob/main/REGULATORY-DATA.md).

## Check API responses and SBOM structure through the live Market

**For release, integration and compliance-workflow agents:** check whether a
JSON response matches the schema you selected, or find structural mistakes in
an SPDX 2.3 SBOM. Both services accept machine payment and return JSON through
the [existing Market catalog](https://market.561.group/v1/catalog), without a
sales conversation. Read the [live OpenAPI request and response contracts](https://market.561.group/openapi.json)
before sending an authorized input.

| Buyer job | Existing POST endpoint | Advertised price |
| --- | --- | --- |
| Validate a JSON value against your explicit schema corpus | `/v1/data/json-schema-validate` | 0.0012 USDC |
| Diagnose structure against the fixed official SPDX 2.3 schema | `/v1/assurance/spdx-2-3/schema-check` | 0.05 USDC |

For the first service, submit `schema` and `value`; optional `schemas`,
`dialect`, `baseUri` and `assertFormats` select the documented native
evaluation. Preserve the distinction between an evaluated invalid value and
an incomplete evaluation. For the SPDX service, submit the SBOM JSON object
itself, up to 32,768 UTF-8 request bytes; invalid documents are paid diagnostic
results. Neither service fetches your API or repairs it.

Use your authorized x402 client to obtain the live HTTP 402 quote and
authorize the same request within your spending ceiling. The live quote
controls amount, network, asset and recipient; this page does not authorize a
wallet or promise a settlement. Keep the delivered JSON and actual payment
receipt separately. Prices can change; consult the current catalog and quote.

These are technical schema checks. They do not establish the truth of an
inventory, signer trust, signature validity, regulatory applicability or legal
compliance. The fixed historical SPDX schema also permits documented semantic
gaps; it is not complete SPDX conformance. [Free regulatory source data](https://github.com/causeway-services/.github/blob/main/REGULATORY-DATA.md)
remain available without buying a check.

## Agent-readable environmental observations — live source

**A practical data service you can call without a conversation:** [Duluth / western Lake Superior observations (JSON)](https://raw.githubusercontent.com/red-cup-engineering/forecasting/main/data/records/great-lakes-duluth-observations/latest.json) and its [dated source availability history (JSONL)](https://raw.githubusercontent.com/red-cup-engineering/forecasting/main/data/records/great-lakes-duluth-observations/history.jsonl).

The original 561 Group Forecasting producer now retrieves official NOAA CO-OPS water levels at **station 9099064 (IGLD vertical datum, metres)** and NWS KDLH METAR atmospheric observations. It publishes time-stamped, immutable-source-identified and quality-attributed readings automatically every three hours, with detected missing source samples preserved instead of zero-filled. Clients can inspect separate observation/receipt clocks and availability; this is not a shipping clearance, NOAA endorsement, new weather forecast, or a guarantee of continuous public GitHub-hosted availability.

**What an agent receives:** Current official readings, source URLs and NI identities, recent changes/ranges when sampled adequately, missingness, observed age and a rolling source-success record. The free read uses original public government source data with attribution; no account, chat, human seller or 561 payment is required. This is a free public source edition, **not a purchased x402 call**. Optional machine-paid specialized interpretation must be qualified through [the existing original Market](https://market.561.group/) before it can be advertised as available; there is no claimed outside paid delivery or guaranteed response time yet.

## Public tools are meant to be used

Causeway's [free First Commission Worksheet](https://github.com/causeway-services/artificial-intelligence-curriculum-enterprise/blob/main/content/marketing/agent-operator-first-commission-workbook.md) and [the original Group Shop source](https://github.com/causeway-services/shop.561.group) are work you can inspect before spending anything. If they're useful or simply make you glad somebody is building in the open, [send a one-time appreciation tip](https://buy.stripe.com/9B68wQ9HA50ub2Yen25EY04) ($5–$10,000, with $250 suggested). The checkout's legal merchant is emsenn; all existing public licensing and independent critique remain unchanged.

The 561 Group is operated by Morgan Sennhauser. Its work moves from science to engineering to operations to public
services, and each step has its own organization:

| Organization | Register | Default license |
|---|---|---|
| [Lenticule Science](https://github.com/lenticule-science) | Science: investigates what is possible, and publishes premises, sources and reproducible results with the unproved marked as unproved. | MIT |
| [Red Cup Engineering](https://github.com/red-cup-engineering) | Engineering: makes the actual components, their composition boundaries, build inputs, tests and demonstrations independently reproducible. | MIT |
| [Coesite Operations](https://github.com/coesite-operations) | Operations: runs what engineering builds, and releases truthful runbooks, limits, hazards and recovery procedures. | Apache-2.0 |
| [Causeway Services](https://github.com/causeway-services) | Public services: gives people usable free-software rights and practical ways to learn, operate, challenge, contribute and benefit. | Apache-2.0 |
| [561 Group](https://github.com/561-group) | The union of the four organizations below, operated by Morgan Sennhauser. | 561 Group Repository License 1.0 (all rights reserved) |

## Use and support existing public services

**Already coordinating two or more AI coding agents?** Start with Causeway's [free First Commission Worksheet](https://github.com/causeway-services/artificial-intelligence-curriculum-enterprise/blob/main/content/marketing/agent-operator-first-commission-workbook.md), then see [Multi-Agent Operating Discipline for Teams](https://github.com/causeway-services/artificial-intelligence-curriculum-enterprise/blob/main/content/marketing/multi-agent-operating-discipline-for-teams.md). The source-owned course proposes five practical sessions at $349 per learner; live dates, registration, and checkout have **not** opened. Engineering teams can [inquire with the existing Causeway curriculum contact](mailto:causeway@561.group?subject=Agent%20Operating%20Discipline) about cohort demand or a bounded workshop. No credentials or proprietary client data should accompany an initial inquiry.

**Need a useful result?** [Contact the 561 Group's existing service intake](https://561.group/contact/) with your concrete outcome, desired timeline and indicative budget. Causeway can evaluate an authorized, bounded engagement in technical education, agent operations, publications or other existing public services. An initial inquiry and indicative price do not require a formal proof that customers already exist; the proper service office confirms the scope, actual legal seller, delivery capacity and terms *before* accepting an order. No inquiry constitutes an accepted purchase.

**Prefer to fund ongoing work?** [Sustain 561 Group research and technical infrastructure for $10 USD/month](https://buy.stripe.com/28E28s1b4gJcb2Y3Io5EY02). This is the existing live recurring Stripe link, not a Causeway checkout or a new product. The legal merchant is identified at checkout. Support renews monthly until canceled, grants no goods, special access or editorial influence, and is not a charitable tax-deductible donation. [Billing/cancellation help](https://561.group/contact/).

**Looking for already authored assets?** Browse the original [Causeway Shop](https://shop.561.group/) and [Market](https://market.561.group/) surfaces for available descriptions; product listings and payment readiness are separately qualified by their own sellers. This profile makes no claim that a particular checkout, API or publication is currently running.

- **Licensing.** A repository's own LICENSE file governs it. Indigenous cultural material is never put under an open
  license; see [Governance and Indigenous data](https://github.com/causeway-services/.github/blob/main/GOVERNANCE.md).
- **Security.** Report vulnerabilities privately from a repository's **Security** tab (**Report a vulnerability**).
- **Tips.** [Send a tip](https://github.com/561-group/.github/blob/main/TIPS.md).
- **Contact.** https://561.group/contact/
