# Get Sightings

~~~
https://api.hatebase.org/4-4/get_sightings
~~~

## Description

The /get_sightings endpoint allows users to download sightings of Hatebase's vocabulary. Note that resultsets are paginated and do not contain the text from which the sighting was obtained if prohibited by third party terms of service.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>year</td>
    <td>2019</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>sighted_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>sighted_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>page</td>
    <td>1</td>
    <td>Defaults to 1 if not specified. Trial plans are limited to page 1 only.</td>
  </tr>
  <tr>
    <td>vocabulary_id</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td>2-character ISO 3166-2 code, ignored if latitude and longitude present</td>
  </tr>
  <tr>
    <td>city</td>
    <td>New York</td>
    <td>Requires country, ignored if latitude and longitude present</td>
  </tr>
  <tr>
    <td>latitude</td>
    <td>40.7483800</td>
    <td>Decimal format, must be accompanied by longitude and radial distance</td>
  </tr>
  <tr>
    <td>longitude</td>
    <td>-73.9967050</td>
    <td>Decimal format, must be accompanied by latitude and radial distance</td>
  </tr>
  <tr>
    <td>radius</td>
    <td>25</td>
    <td>If used with latitude and longitude, defines outer radial boundary measured in km (max 100 km)</td>
  </tr>
  <tr>
    <td>language</td>
    <td>ENG</td>
    <td>3-character ISO 639-3 code</td>
  </tr>
  <tr>
    <td>is_about_nationality</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_ethnicity</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_religion</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_gender</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_sexual_orientation</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_disability</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_class</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
</table>

## Resultset

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>sighting_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>vocabulary_id</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>term</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>probability</td>
    <td>79</td>
    <td>percentage</td>
  </tr>
  <tr>
    <td>country_id</td>
    <td>CA</td>
    <td>2-character ISO 3166-2 code</td>
  </tr>
  <tr>
    <td>city</td>
    <td>New York</td>
    <td></td>
  </tr>
  <tr>
    <td>latitude</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>longitude</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_nationality</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_ethnicity</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_religion</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_gender</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_sexual_orientation</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_disability</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_about_class</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>type</td>
    <td>recipient</td>
    <td>"recipient", "overheard" or "used"</td>
  </tr>
  <tr>
    <td>source</td>
    <td>Twitter</td>
    <td></td>
  </tr>
  <tr>
    <td>sighted_on</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
</table>
