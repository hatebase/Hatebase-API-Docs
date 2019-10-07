# API v4.3

## Overview

<img src="diagram.png">

## Endpoints

### Authentication

- [authenticate](authenticate.md)

### Read Queries

- [/get_vocabulary](get_vocabulary.md)
- [/get_vocabulary_details](get_vocabulary_details.md)
- [/get_sightings](get_sightings.md)
- [/get_analysis](get_analysis.md)

### Write Queries

- [/analyze](analyze.md)

## Changelog

- Due to the increasing volume of sightings, a mandatory "year" input parameter has been added to [/get_sightings](get_sightings.md) ensure optimal query performance
- [/get_sightings](get_sightings.md) will now provide nongeolocated sightings
- Additional vocabulary attributes in [/get_sightings](get_sightings.md)
- Minor updates to the JSON data structure returned by the API which do not impact the structure of results (e.g. input parameters are now demarcated by the parent "query")
