# data

 Synthetic GeoJSON API with select pre-computed queries. 

## Usage

The programmatic entry point for each dataset is a `metadata.json` file. Given the datasets `slug`, its metadata file can be found at the following location:

    https://github.com/gbosystems/data/raw/main/{slug}/metadata.json

This file contains a single JSON object which conforms to the following schema:

* `source`: `string` - Original data source (if applicable)
* `credit`: `string` - Attribution credits
* `updated`: `number` - Timestamp of most recent data update (milliseconds since January 1, 1970 00:00:00)
* `total`: `number` - Total features in complete dataset
* `endpoints`: `object` - Describes available endpoints
  * `all`: `object` - Complete dataset endpoint
    * `url`: `string` - URL of endpoint
  * `query`: `object` - Query endpoint
    * `url`: `string` - URL format of endpoint
    * `properties`: `object` - Object describing properties available for query
      * `{property-name}`: `array` - Array of primitive values which can be used to build the endpoint URL

## Datasets

### Airports

World wide airport dataset maintained by [OurAirports](https://ourairports.com/).

Slug: `airports`

### Hospitals

US-only hospital dataset built with data maintained by [U.S Centers for Medicare & Medicaid Services](https://www.cms.gov/), geocoded using [HERE Technologies](https://www.here.com/) services.

Slug: `hospitals`

### Ports

World wide port dataset maintained by the [US National Geospatial-Intelligence Agency](https://www.nga.mil/).

Slug: `ports`
