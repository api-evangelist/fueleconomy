# FuelEconomy.gov

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

FuelEconomy.gov is the official U.S. government source for fuel economy information, providing free REST web services exposing EPA fuel economy ratings, vehicle specifications, CO2 emissions data, current fuel prices, and community-contributed real-world MPG data. The API covers passenger cars and light trucks from 1984 through the current model year and is administered by Oak Ridge National Laboratory for the U.S. Department of Energy and the U.S. Environmental Protection Agency.

## API

- **Base URL**: `https://www.fueleconomy.gov/ws/rest`
- **Authentication**: None required
- **Formats**: JSON and XML
- **Cost**: Free

### Key Endpoints

| Endpoint | Description |
|---|---|
| `/vehicle/menu/year` | Available model years |
| `/vehicle/menu/make?year=YYYY` | Manufacturers for a given year |
| `/vehicle/menu/model?year=YYYY&make=NAME` | Models for a year and make |
| `/vehicle/menu/options?year=YYYY&make=NAME&model=NAME` | Trim levels with vehicle IDs |
| `/vehicle/{id}` | Full vehicle record (MPG, specs, energy cost) |
| `/vehicle/emissions/{id}` | CO2 and emissions records for a vehicle |
| `/fuelprices` | Current fuel prices used by the service |
| `/ympg/shared/ympgVehicle/{id}` | Community MPG summary for a vehicle |
| `/ympg/shared/ympgDriverVehicle/{id}` | Individual user MPG submissions |

### Bulk Data Downloads

CSV, XML, and Excel files for all model years (1974-present) are available at:
`https://www.fueleconomy.gov/feg/download.shtml`

Data is updated weekly.

## Resources

- **Website**: https://www.fueleconomy.gov/
- **API Documentation**: https://www.fueleconomy.gov/feg/ws/index.shtml
- **Data Downloads**: https://www.fueleconomy.gov/feg/download.shtml
- **Widgets**: https://www.fueleconomy.gov/widgets/
- **Contact**: fueleconomy@ornl.gov
- **Mailing List**: FuelEconomyNews-join@elist.ornl.gov

## APIs.json

This repository contains an [APIs.json](apis.yml) index conforming to the APIs.json 0.19 specification, along with supporting profiles:

- [`plans/fueleconomy-plans-pricing.yml`](plans/fueleconomy-plans-pricing.yml) — API Commons Plans 0.1
- [`rate-limits/fueleconomy-rate-limits.yml`](rate-limits/fueleconomy-rate-limits.yml) — API Commons Rate Limits 0.1
- [`finops/fueleconomy-finops.yml`](finops/fueleconomy-finops.yml) — FinOps Framework 1.0 FOCUS-aligned

## Maintainer

Kin Lane — kin@apievangelist.com
