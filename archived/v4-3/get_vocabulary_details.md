# Get Vocabulary Details

~~~
https://api.hatebase.org/4-3/get_vocabulary_details
~~~

## Description

The /get_vocabulary endpoint allows users to download more detail on a specific term in Hatebase's lexicon of multilingual hate speech.

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
    <td>vocabulary_id</td>
    <td>aBc123</td>
    <td></td>
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
    <td>is_unambiguous</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>is_unambiguous_in</td>
    <td>CA</td>
    <td>2-character ISO 3166-2 code</td>
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
    <td>nationalities</td>
    <td>['CA', 'US']</td>
    <td>2-character ISO 3166-2 codes</td>
  </tr>
  <tr>
    <td>is_about_ethnicity</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>ethnicities</td>
    <td>['Anuak', 'Apache']</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_religion</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>religions</td>
    <td>['Judaism', 'Islam']</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_gender</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>genders</td>
    <td>['male', 'female']</td>
    <td></td>
  </tr>
  <tr>
    <td>is_about_sexual_orientation</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>sexual_orientations</td>
    <td>['heterosexual', 'homosexual']</td>
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
    <td>is_archaic</td>
    <td>true</td>
    <td>"true" or "false"</td>
  </tr>
  <tr>
    <td>number_of_sightings</td>
    <td>100</td>
    <td></td>
  </tr>
  <tr>
    <td>number_of_sightings_this_year</td>
    <td>10</td>
    <td></td>
  </tr>
  <tr>
    <td>number_of_sightings_this_month</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
    <td>countries_sighted</td>
    <td>['CA' : 50, 'US' : 50]</td>
    <td></td>
  </tr>
  <tr>
    <td>countries_sighted_this_year</td>
    <td>['CA' : 5, 'US' : 5]</td>
    <td></td>
  </tr>
  <tr>
    <td>countries_sighted_this_month</td>
    <td>['CA' : 1, 'US' : 1]</td>
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
