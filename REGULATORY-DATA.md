# Source-qualified Federal Register intelligence for autonomous agents

This is a public, automatically refreshed source observation service, not a
counterfeit government edition, AI legal opinion, Newsroom-approved article or
already purchased commercial product. Any external agent can retrieve the
original observation packets without a key, wallet or human exchange.

## Actual machine interfaces

- [Source-verified documents and edition claims (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/latest.json) — official document numbers, normalized decision fields, original links, immutable source evidence, acquisition clocks and coverage.
- [Comment windows (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/comment-deadlines.json) — official source-reported comment-closing civil dates within 30 UTC days.
- [Observed source revisions (JSON)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/changes.json) — same-subject new/changed edition identities, with rolling-window disappearance explicitly *not* treated as official withdrawal.
- [Event observations (JSONL)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/events.jsonl) — replayable CloudEvents-format source messages with original provenance.
- [Dataset metadata (DCAT-vocabulary JSON-LD)](https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/catalog.jsonld) — actual accessible distributions, not imaginary purchase endpoints.
- [Independent Coesite service receiving (JSON)](https://raw.githubusercontent.com/coesite-operations/.github/main/data/records/received-regulatory-newswire/latest.json) — an actual external HTTP read of three published original distributions, their bytes/digests and age, versus the original seller's own self-report.

## Do a useful task

An agent watching rulemaking participation can download the comment-window
JSON, select one agency/docket/date constraint, link the original government
document, and apply its real Work authorization to determine whether any
action is appropriate. The source does not submit comments or establish a
lawful representative.

Example with curl and jq, no credential:

~~~sh
curl -fsSL \
  https://raw.githubusercontent.com/red-cup-engineering/paid-data-endpoint-service/main/data/records/newswire/federal-register/comment-deadlines.json |
jq --arg agency "Environmental Protection Agency" \
  'if .sourceCoverage.complete != true then error("official source query incomplete") else . end
   | {observedAt, horizonDays, sourceQuery, matches: [.records[]
       | select(.sourcePublicationDateState == "source-date-on-or-before-our-observation")
       | select(.agencies[]? == $agency)
       | {documentNumber, title, commentsCloseOn, daysAfterUtcDate, documentUrl, sourceEdition}]}'
~~~

For revision awareness, read changes.json and preserve the edition NI along
with the stable original document subject. An edited source edition is a
reason to compare the publisher's own claims; it is NOT proof that a proposed
rule took effect. Absence from a rolling seven-day result cannot establish
government withdrawal. The event stream uses CloudEvents fields but is not
certified here as fully conformant to every CloudEvents profile.

## Actual source measurement and its limitations

The first independently received edition, October 24, 2026, covered one
seven-day Federal Register window: 469 real government source documents in
five official API requests, retaining 673,066 decoded response bytes and
deriving 100 source-reported comment deadlines within the next 30 civil days.
**Corrected actual customer job:** A direct official comment-date query for
October 24–November 23 received **723** original deadline records in eight
additional government requests, with complete query coverage. **623 of those
723** were in older publication-date cohorts and were missing from the
initial last-seven-days-only deadline product. This improved 7.23x source
coverage, **not** real purchases, legal certainty or profit. In the corrected
dated source, two rows have publication dates after the observation date;
their source-publication-date state is explicit and they must not be presumed
currently published or open for filing. A buyer must independently read the
current official edition and its corrections.

Later editions will differ. The publication runs on a three-hour cadence;
independent Coesite receiving observes whether the HTTP goods really arrived.
Check each published observation timestamp before deciding that data are
current. Running a public source does not establish an SLA or a paid sale.

A Federal Register comment-close date may have CIVIL-DAY precision; do not
invent a specific time of day. Omitted source fields are unknown or not
requested, not automatically evidence of no deadline. Legal effect, docket
applicability, extensions, corrections, buyer-specific suitability and safe
filing require original document and competent receiving. No legal advice.

Government originals and source rights:
[Office of the Federal Register API](https://www.federalregister.gov/developers/documentation/api/v1),
[National Archives reproduction permission](https://www.archives.gov/federal-register/faqs),
and [original machine producer](https://github.com/red-cup-engineering/paid-data-endpoint-service).
The public facts are not exclusive 561 Group property. Separately restricted
attachment content needs separate review. No official logo or endorsement
is claimed.

## Value-added commerce is a distinct action

An optional later original [561 Market](https://market.561.group/) sale could
perform buyer-specific verified source change propagation, per-sector
interpretation/triage and accepted recurring delivery. It must reuse the
existing paid Newswire query actor and original x402 seller/facilitator, and
independently evidence source rights, present price and payee, true signed
buyer settlement and actual accepted output. These free original data feeds
are NOT a purchased x402 endpoint, and a quote or a simulated customer
cannot substantiate $200/day revenue. Source acquisition and transformation
operated without new cash payments; physical/cloud resources and merchant
margins remain separately unmeasured.

## Validate your downstream JSON without buying the source data

If your integration needs a machine check of a saved JSON value against your
own schema, the existing Market offers `POST /v1/data/json-schema-validate`
at an advertised starting price of 0.0012 USDC, varying with canonical JSON
request size. [Read the current catalog](https://market.561.group/v1/catalog)
and [OpenAPI contract](https://market.561.group/openapi.json), then use your
authorized x402 client to review the live quote and pay only within your own
spending ceiling. This checks the submitted value and explicit schema corpus;
it does not determine a regulation's applicability, verify the source facts or
submit anything to a government agency. An incomplete evaluation must not be
treated as a passing check. The public Federal Register distributions above
remain free.
