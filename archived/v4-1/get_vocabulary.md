# Get Vocabulary

~~~
https://api.hatebase.org/4-1/get_vocabulary
~~~

## Description

The /get_vocabulary endpoint allows users to download Hatebase's lexicon of multilingual hate speech. Note that resultsets are paginated and that vocabulary is frequently updated based on usage, particularly sightings.

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
    <td>keywords</td>
    <td></td>
    <td>Searches in terms and meanings</td>
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
    <td>nationality</td>
    <td>CA</td>
    <td>2-character ISO 3166-2 code</td>
  </tr>
  <tr>
    <td>is_about_ethnicity</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>ethnicity</td>
    <td>Luo</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_religion</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>religion</td>
    <td>Islam</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_gender</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>gender</td>
    <td>female</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_sexual_orientation</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>sexual_orientation</td>
    <td>homosexual</td>
    <td></td>
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
    <td>created_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>created_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>updated_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>updated_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>GMT</td>
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
    <td>vocabulary_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>term</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>hateful_meaning</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>nonhateful_meaning</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>average_offensiveness</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>language</td>
    <td>ENG</td>
    <td>3-character ISO 639-3 code</td>
  </tr>
  <tr>
    <td>plural_of</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>variant_of</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>transliteration_of</td>
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
    <td>number_of_sightings</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>number_of_sightings_this_year</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>number_of_sightings_this_month</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>created_on</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>updated_on</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
</table>
