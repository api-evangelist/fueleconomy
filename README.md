# FuelEconomy.gov

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
