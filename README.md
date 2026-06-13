# Ninetailed

Ninetailed (now known as Contentful Personalization) is an API-first personalization and experimentation platform for content-rich applications. Acquired by Contentful in 2023, it provides digital teams with tools to define audience segments, run A/B tests, and deliver personalized experiences at the edge without requiring deep developer involvement for each campaign.

## APIs

### Experience API

The core REST API deployed on Cloudflare Workers for edge performance. It manages visitor profiles and resolves which experience variant to serve based on configured audience rules.

Base URL: `https://experience.ninetailed.co/v2/organizations/{organizationId}/environments/{environmentSlug}`

Key endpoints:
- `POST /profiles` — Create a new visitor profile with events
- `POST /profiles/{profileId}` — Update an existing profile
- `GET /profiles/{profileId}` — Retrieve a visitor profile
- `DELETE /profiles/{profileId}` — Remove a profile
- `POST /events` — Batch upsert profiles (synchronous, max 200 events)
- `POST /import/events` — Batch upsert profiles (asynchronous)

## Authentication

Authentication uses a **Client ID** found under the SDK Keys section on the Optimization tab within your Contentful account.

## SDKs

- JavaScript SDK (`@ninetailed/experience.js`)
- React SDK
- Next.js SDK
- Node.js SDK
- React Native SDK (experimental)
- Shared SDK (`@ninetailed/experience.js-shared`)

GitHub organization: https://github.com/ninetailed-inc

## Rate Limits

- Maximum 200 events per batch request
- Maximum 50 identify events per batch request
- Maximum 50 unique profiles per batch request
- HTTP 429 (`ERR_PROFILE_OVERLOAD`) returned on concurrent request overload

## Links

- Website: https://www.contentful.com/products/personalization/
- Documentation: https://www.contentful.com/developers/docs/ninetailed/
- Experience API: https://www.contentful.com/developers/docs/ninetailed/experience-api/
- GitHub: https://github.com/ninetailed-inc
- Status: https://ninetailedstatus.com/
- Changelog: https://www.contentful.com/developers/docs/ninetailed/ninetailed-changelog/
- LinkedIn: https://www.linkedin.com/company/ninetailed
- X: https://x.com/ninetailedhq

## Pricing

Quote-based enterprise pricing, available as an add-on via the Contentful Apps Marketplace. Three tiers: Start, Core, and Scale. No free plan or self-serve signup. Contact Contentful sales for pricing.

## Notes

Ninetailed was founded in Germany and acquired by Contentful in 2023. Contentful announced a definitive agreement to be acquired by Salesforce in January 2025.
